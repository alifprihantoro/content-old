# Markdown dan MDX di Astro

Astro adalah sebuah framework web yang memungkinkan Anda membuat situs web statis dengan menggunakan komponen modern. Salah satu fitur Astro yang menarik adalah kemampuannya untuk mendukung Markdown dan MDX sebagai format konten. Dengan Markdown dan MDX, Anda dapat menulis konten dengan mudah dan fleksibel, serta memanfaatkan kekuatan komponen React atau Vue di dalamnya.

## Halaman Markdown dan MDX

Untuk membuat halaman dengan menggunakan Markdown atau MDX, Anda cukup membuat file dengan ekstensi `.md` atau `.mdx` di dalam folder `src/pages`. File tersebut akan diubah menjadi halaman HTML oleh Astro secara otomatis. Anda juga dapat menambahkan frontmatter di awal file untuk menentukan judul, deskripsi, layout, atau data lainnya yang ingin Anda gunakan di halaman tersebut.

Contoh file Markdown:

```markdown
---
title: Halaman Contoh
description: Ini adalah halaman contoh dengan Markdown
layout: ../layouts/default.astro
---
# Halaman Contoh

Ini adalah konten Markdown.

- Ini adalah daftar
- Dengan beberapa item
- Dan juga bisa menggunakan *italic* atau **bold**
```

Contoh file MDX:

```mdx
---
title: Halaman Contoh
description: Ini adalah halaman contoh dengan MDX
layout: ../layouts/default.astro
---
import MyComponent from '../components/MyComponent.jsx';

# Halaman Contoh

Ini adalah konten MDX.

- Ini adalah daftar
- Dengan beberapa item
- Dan juga bisa menggunakan komponen React atau Vue seperti <MyComponent />
```

## Koleksi Konten

Selain membuat halaman secara langsung, Anda juga dapat membuat koleksi konten dengan menggunakan Markdown atau MDX. Koleksi konten adalah sekumpulan file Markdown atau MDX yang memiliki struktur dan schema yang sama, dan dapat diakses melalui Astro API. Koleksi konten berguna untuk membuat situs web yang memiliki banyak konten, seperti blog, portofolio, dokumentasi, dll.

Untuk membuat koleksi konten, Anda perlu membuat folder khusus dengan nama `.astro` di dalam folder `src`. Di dalam folder `.astro`, Anda dapat membuat file dengan ekstensi `.astro` yang berfungsi sebagai template untuk koleksi konten tersebut. File tersebut harus mengimpor fungsi `createCollection` dari `astro/collections` dan mengekspor hasilnya sebagai `default`.

Contoh file `.astro/blog.astro`:

```astro
---
import { createCollection } from 'astro/collections';
import type { AstroCollectionResult } from 'astro';

export interface Post {
  title: string;
  slug: string;
  date: string;
  author: string;
  summary: string;
}

export default createCollection<Post>({
  route: '/blog/:slug',
  paths({ collection }) {
    return collection.data.map((post) => ({ params: { slug: post.slug } }));
  },
  async data({ params }) {
    const post = collection.data.find((post) => post.slug === params.slug);
    return post;
  },
});
---

<Layout>
  <h1>{data.title}</h1>
  <p>By {data.author} on {data.date}</p>
  <Content />
</Layout>
```

File template tersebut akan menghasilkan halaman untuk setiap file Markdown atau MDX yang ada di dalam folder `src/content/blog`. File Markdown atau MDX tersebut harus memiliki frontmatter yang sesuai dengan schema yang ditentukan di template (dalam hal ini, `Post`). File tersebut juga harus memiliki properti `slug` yang unik untuk menentukan URL halamannya.

Contoh file `src/content/blog/hello-world.md`:

```markdown
---
title: Hello World
slug: hello-world
date: 2021-10-30
author: John Doe
summary: This is my first blog post with Astro.
---
# Hello World

This is my first blog post with Astro.

I hope you enjoy it!
```

File tersebut akan menghasilkan halaman dengan URL `/blog/hello-world`, yang menggunakan template dari file `.astro/blog.astro`.

## Fitur Markdown

Markdown adalah sebuah bahasa markup yang sederhana dan mudah digunakan untuk menulis konten web. Markdown memiliki beberapa fitur standar yang didukung oleh Astro, seperti:

- Frontmatter: bagian awal file yang berisi metadata dalam format YAML atau TOML.
- layout: properti frontmatter yang menentukan layout Astro mana yang digunakan untuk halaman tersebut.
- Heading IDs: setiap heading (`#`, `##`, `###`, dll) akan mendapatkan ID otomatis berdasarkan teksnya, yang dapat digunakan untuk anchor link.
- Escaping karakter khusus: jika Anda ingin menampilkan karakter khusus seperti `#`, `*`, atau `_` tanpa mempengaruhi format Markdown, Anda dapat menambahkan tanda backslash (`\`) sebelumnya.

## Fitur MDX

MDX adalah sebuah ekstensi dari Markdown yang memungkinkan Anda untuk menggunakan komponen React atau Vue di dalam konten Anda. MDX memiliki beberapa fitur tambahan yang tidak dimiliki oleh Markdown biasa, seperti:

- Menggunakan variabel yang diekspor di MDX: Anda dapat mengekspor variabel dari file MDX dan menggunakannya di dalam konten Anda.
- Menggunakan variabel frontmatter di MDX: Anda dapat mengakses variabel frontmatter dari file MDX dengan menggunakan properti `frontmatter`.
- Menggunakan komponen di MDX: Anda dapat mengimpor komponen React atau Vue dari file lain dan menggunakannya di dalam konten Anda.
- Mengimpor properti yang diekspor dari Markdown: Anda dapat mengimpor properti seperti `title`, `description`, atau `Content` dari file Markdown lain dan menggunakannya di dalam konten Anda.
- Komponen `<Content>`: sebuah komponen khusus yang mengembalikan konten HTML dari file tersebut. Hanya berlaku untuk file Markdown.
- Ekspor khusus MDX: beberapa properti khusus yang dapat diekspor dari file MDX, seperti `layout`, `hydrate`, atau `collection`.

## Mengkonfigurasi Markdown dan MDX

Astro menggunakan [Unified](https://unifiedjs.com/) sebagai mesin untuk memproses Markdown dan MDX. Unified memiliki banyak plugin yang dapat digunakan untuk memperluas kemampuan Markdown dan MDX, seperti menambahkan sintaks baru, memodifikasi frontmatter, atau menambahkan highlight kode.

Untuk mengkonfigurasi plugin Unified, Anda dapat membuat file dengan nama `markdown.config.js` atau `markdown.config.mjs` di root proyek Anda. File tersebut harus mengekspor sebuah fungsi async yang menerima objek config sebagai parameter dan mengembalikan objek config yang dimodifikasi.

Contoh file `markdown.config.js`:

```js
import remarkGfm from 'remark-gfm';
import remarkFootnotes from 'remark-footnotes';
import remarkMath from 'remark-math';
import rehypeKatex from 'rehype-katex';

export default async function (config) {
  // Menambahkan plugin remark untuk mendukung fitur GitHub Flavored Markdown
  config.remarkPlugins.push(remarkGfm);

  // Menambahkan plugin remark untuk mendukung fitur catatan kaki
  config.remarkPlugins.push(remarkFootnotes);

  // Menambahkan plugin remark dan rehype untuk mendukung fitur matematika dengan LaTeX
  config.remarkPlugins.push(remarkMath);
  config.rehypePlugins.push(rehypeKatex);

  return config;
}
```

## Syntax Highlighting

Astro menggunakan [Prism](https://prismjs.com/) sebagai library untuk melakukan syntax highlighting pada kode di dalam konten Markdown atau MDX. Prism mendukung banyak bahasa pemrograman dan tema warna yang dapat dipilih sesuai keinginan.

Untuk mengubah tema Prism, Anda dapat membuat file CSS khusus di dalam folder `public` dan mengimpornya di dalam layout Astro Anda. File CSS tersebut harus mengandung aturan CSS untuk selector `.astro pre[class*=\"language-\"] > code`.

Contoh file `public/prism-theme.css`:

```css
/* Tema Prism Dark */
/* https://github.com/PrismJS/prism-themes/blob/master/themes/prism-dark.css */

/* PrismJS 1.23.0
https://prismjs.com/download.html#themes=prism-dark&languages=markup+css+clike+javascript */

/**
 * prism.js dark theme for JavaScript, CSS and HTML
 * Based on the slides of the talk “/Reg(exp){2}lained/” by Lea Verou http://lea.verou.me/talks/regexp/#slide1
 */
code[class*="language-"],
pre[class*="language-"] {
	color: white;
	background: none;
	text-shadow: 0 -.1em .2em black;
	font-family: Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace;
	font-size: 1em;
	text-align: left;
	white-space: pre;
	word-spacing: normal;
	word-break: normal;
	word-wrap: normal;
	line-height: 1.5;

	-moz-tab-size: 4;
	-o-tab-size: 4;
	tab-size: 4;

	-webkit-hyphens: none;
	-moz-hyphens: none;
	-ms-hyphens: none;
	hyphens: none;

}

/* Code blocks */
pre[class*="language-"] {
	padding: 1em;
	margin: .5em 0;
	overflow: auto;
	border-radius: 0.3em;
}

:not(pre) > code[class*="language-"],
pre[class*="language-"] {
	background: hsl(30, 20%, 25%);
}

/* Inline code */
:not(pre) > code[class*="language-"] {
	padding: .1em;
	border-radius: .3em;
	white-space: normal;
}

.token.comment,
.token.prolog,
.token.doctype,
.token.cdata {
	color: hsl(30, 20%, 50%);
}

.token.punctuation {
	color: #c5c8c6;
}

.namespace {
	opacity: .7;
}

.token.property,
.token.tag,
.token.constant,
.token.symbol,
.token.deleted {
	color: #f92672;
}

.token.boolean,
.token.number {
	color: #ae81ff;
}

.token.selector,
.token.attr-name,
.token.string,
.token.char,
.token.builtin,
.token.inserted {
	color: #a6e22e;
}

.token.operator,
.token.entity,
.token.url,
.language-css .token.string,
.style .token.string {
	color: #f8f8f2;
}

.token.atrule,
.token.attr-value,
.token.keyword {
	color: #e6db74;
}

.token.function,
.token.class-name {
	color: #fd971f;
}

.token.regex,
.token.important,
.token.variable {
	color: #fd971f;
}

.token.important,
.token.bold {
	font-weight: bold;
}
.token.italic {
	font-style: italic;
}

.token.entity {
	cursor: help;
}
```

## Mengambil Markdown dari Sumber Eksternal

Selain membuat file Markdown atau MDX secara lokal, Anda juga dapat mengambil konten Markdown dari sumber eksternal, seperti API, CMS, atau file remote. Untuk melakukan hal ini, Anda dapat menggunakan fungsi `fetchContent` dari `astro/content` di dalam file `.astro` Anda.

Contoh file `.astro/remote.astro`:

```astro
---
import { fetchContent } from 'astro/content';

// Mengambil konten Markdown dari URL
const content = await fetchContent('https://example.com/some-markdown-file.md');

// Mengambil konten Markdown dari CMS
// const content = await fetchContent('https://my-cms.com/api/posts/123');
---

<Layout>
  <h1>{content.title}</h1>
  <p>By {content.author} on {content.date}</p>
  <Content />
</Layout>
```

Fungsi `fetchContent` akan mengembalikan sebuah objek yang memiliki properti `title`, `description`, `Content`, dan properti lainnya yang berasal dari frontmatter file Markdown tersebut. Properti `Content` adalah sebuah komponen Astro yang dapat digunakan untuk menampilkan konten HTML dari file Markdown tersebut.

## Kesimpulan

Markdown dan MDX adalah format konten yang sangat cocok untuk digunakan dengan Astro. Dengan Markdown dan MDX, Anda dapat menulis konten dengan mudah dan fleksibel, serta memanfaatkan kekuatan komponen React atau Vue di dalamnya. Astro juga memberikan banyak fitur dan konfigurasi untuk memperluas kemampuan Markdown dan MDX, seperti koleksi konten, syntax highlighting, plugin Unified, dan pengambilan konten dari sumber eksternal.

Semoga artikel ini bermanfaat untuk Anda yang ingin belajar lebih lanjut tentang Markdown dan MDX di Astro. Jika Anda memiliki pertanyaan atau saran, silakan tinggalkan komentar di bawah ini. Terima kasih telah membaca!

Source:
- How to use content collection in Astro. - DEV Community. https://dev.to/obinnaspeaks/how-to-use-content-collection-in-astro-43j2.
- Markdown & MDX 🚀 Astro Documentation. https://docs.astro.build/en/guides/markdown-content/.
- Content Collections 🚀 Astro Documentation. https://docs.astro.build/en/guides/content-collections/.
- Astro - markdown content. https://www.readonlychild.com/blog/astro-md-content/.
