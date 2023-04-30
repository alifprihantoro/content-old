Anda dapat menggunakan **codeceptjs-resemblehelper** untuk membandingkan screenshot pada codeceptjs⁴⁵⁶. Helper ini dapat digunakan untuk membandingkan screenshot dan membuat tes gagal / lulus berdasarkan toleransi yang diizinkan. Jika dua perbandingan tangkapan layar memiliki perbedaan yang lebih besar dari toleransi yang diberikan, tes akan gagal. Semoga membantu!

Source: Conversation with Bing, 3/30/2023(1) codeceptjs-resemblehelper - npm. https://www.npmjs.com/package/codeceptjs-resemblehelper Accessed 3/30/2023.
(2) GitHub - codeceptjs/codeceptjs-resemblehelper. https://github.com/codeceptjs/codeceptjs-resemblehelper Accessed 3/30/2023.
(3) codeceptjs-resemblehelper - npm. https://www.npmjs.com/package/codeceptjs-resemblehelper/v/1.3.0 Accessed 3/30/2023.
(4) Getting Started | CodeceptJS. https://codecept.io/basics/ Accessed 3/30/2023.
(5) Screenshot comparison is not working · Issue #115 · codeceptjs .... https://github.com/codeceptjs/codeceptjs-resemblehelper/issues/115 Accessed 3/30/2023.
(6) GitHub - newbielity/Codeceptjs-copied--w-screenshot. https://github.com/newbielity/Codeceptjs-copied--w-screenshot Accessed 3/30/2023.

## contoh configs

Berikut adalah contoh konfigurasi **codeceptjs-resemblehelper** untuk membandingkan screenshot pada berbagai layar/responsive :

```json
{
  "helpers": {
    "ResembleHelper": {
      "require": "codeceptjs-resemblehelper",
      "screenshotFolder": "./tests/screenshots/",
      "baseFolder": "./tests/screenshots/base/",
      "diffFolder": "./tests/screenshots/diff/",
      "prepareBaseImage": true,
      "tolerance": 5,
      "singleWindow": false,
      "createDiffFolders": true,
      "formatImageName": "{tag}-{logName}-{width}x{height}",
      "resizeDimensions": false,
      "autoSaveBaseline": true,
      "blockOutStatusBar": true,
      "blockOutToolBar": true
    }
  },
  // Konfigurasi untuk desktop
  "desktop": {
    "windowSize": "1920x1080",
    // Konfigurasi untuk screenshot pada desktop
    "screenshots": {
      // Konfigurasi untuk screenshot pada halaman utama
      "homePage": {
        // Nama tag untuk screenshot
        "fullPage": true,
        // Mengambil screenshot seluruh halaman
        "disableCSSAnimation": true,
        // Menonaktifkan animasi CSS
        "selectorExpansion": true,
        // Mengambil screenshot seluruh halaman
        "selector": "#app",
        // Selector untuk mengambil screenshot
        "fileName": "{tag}-homepage-{browserName}-{width}x{height}.png"
        // Format nama file screenshot
      },
      // Konfigurasi untuk screenshot pada halaman produk
      "productPage": {
        // Nama tag untuk screenshot
        "fullPage": true,
        // Mengambil screenshot seluruh halaman
        "disableCSSAnimation": true,
        // Menonaktifkan animasi CSS
        "selectorExpansion": true,
        // Mengambil screenshot seluruh halaman
        "selector": "#app",
        // Selector untuk mengambil screenshot
        "fileName": "{tag}-productpage-{browserName}-{width}x{height}.png"
        // Format nama file screenshot
      }
    }
  },
  // Konfigurasi untuk tablet
  "tablet": {
    "windowSize": ["768x1024"],
    // Konfigurasi untuk screenshot pada tablet
    "screenshots": {
      // Konfigurasi untuk screenshot pada halaman utama
      "homePageTablet": {
        // Nama tag untuk screenshot
        "fullPage": true,
        // Mengambil screenshot seluruh halaman
        "disableCSSAnimation": true,
        // Menonaktifkan animasi CSS
        "selectorExpansion": true,
        // Mengambil screenshot seluruh halaman
        "selector": "#app",
        // Selector untuk mengambil screenshot
        "fileName": "{tag}-homepage-tablet-{browserName}-{width}x{height}.png"
        // Format nama file screenshot
      },
      // Konfigurasi untuk screenshot pada halaman produk
      "productPageTablet": {
        // Nama tag untuk screenshot
        "fullPage": true,
        // Mengambil screenshot seluruh halaman
        "disableCSSAnimation": true,
        // Menonaktifkan animasi CSS
        "selectorExpansion": true,
        // Mengambil screenshot seluruh halaman
        "selector": "#app",
         // Selector untuk mengambil screenshot
         "fileName":"{tag}-productpage-tablet-{browserName}-{width}x{height}.png"
         // Format nama file screenshot
       }
     }
   },
   // Konfigurasi untuk mobile
   “mobile”: {
     “windowSize”: [“375x667”],
     “screenshots”: {
       “homePageMobile”: {
         “fullPage”: true,
         “disableCSSAnimation”: true,
         “selectorExpansion”: true,
         “selector”: “#app”,
         “fileName”: “{tag}-homepage-mobile-{browserName}-{width}x{height}.png”
       },
       “productPageMobile”: {
         “full
```

penjelasan :
Berikut adalah penjelasan masing-masing konfigurasi pada contoh konfigurasi **codeceptjs-resemblehelper** yang telah saya berikan sebelumnya:
- `"screenshotFolder": "./tests/screenshots/"`: folder tempat menyimpan screenshot
- `"baseFolder": "./tests/screenshots/base/"`: folder tempat menyimpan screenshot dasar
- `"diffFolder": "./tests/screenshots/diff/"`: folder tempat menyimpan screenshot perbedaan
- `"prepareBaseImage": true`: menyiapkan gambar dasar sebelum membandingkan
- `"tolerance": 5`: toleransi perbedaan antara gambar
- `"singleWindow": false`: mengambil screenshot pada semua jendela
- `"createDiffFolders": true`: membuat folder untuk setiap perbedaan
- `"formatImageName": "{tag}-{logName}-{width}x{height}"`: format nama file screenshot
- `"resizeDimensions": false`: tidak mengubah ukuran dimensi gambar
- `"autoSaveBaseline": true`: otomatis menyimpan gambar dasar
- `"blockOutStatusBar": true`: memblokir status bar pada gambar
- `"blockOutToolBar": true`: memblokir toolbar pada gambar

Semoga membantu!

## contoh lanjut
Maaf atas ketidaknyamanannya. Berikut adalah contoh konfigurasi **codeceptjs-resemblehelper** yang lebih lengkap:
```json
{
  "helpers": {
    "ResembleHelper": {
      "require": "codeceptjs-resemblehelper",
      "screenshotFolder": "./tests/screenshots/",
      "baseFolder": "./tests/screenshots/base/",
      "diffFolder": "./tests/screenshots/diff/",
      "prepareBaseImage": true,
      "tolerance": 5,
      "singleWindow": false,
      "createDiffFolders": true,
      "formatImageName": "{tag}-{logName}-{width}x{height}",
      "resizeDimensions": false,
      "autoSaveBaseline": true,
      "blockOutStatusBar": true,
      "blockOutToolBar": true
    }
  },
  "plugins": {
    "screenshotOnFail": {
      "enabled": true
    }
  },
  "multiple": {
    "desktop": {
      "windowSize": "1920x1080",
      "screenshots": {
        "homePage": {
          "fullPage": true,
          "disableCSSAnimation": true,
          "selectorExpansion": true,
          "selector": "#app",
          "fileName":"{tag}-homepage-{browserName}-{width}x{height}.png"
        },
        "productPage":{
          "fullPage": true,
          "disableCSSAnimation": true,
          "selectorExpansion": true,
          "selector":"#app",
          "fileName":"{tag}-productpage-{browserName}-{width}x{height}.png"
        }
      }
    },
    "tablet":{
      "windowSize":["768x1024"],
      "screenshots":{
        "homePageTablet":{
          "fullPage":true,
          "disableCSSAnimation":true,
          "selectorExpansion":true,
          "selector":"#app",
          "fileName":"{tag}-homepage-tablet-{browserName}-{width}x{height}.png"
        },
        "productPageTablet":{
          "fullPage":true,
          "disableCSSAnimation":true,
          "selectorExpansion":true,
          "selector":"#app",
          "fileName":"{tag}-productpage-tablet-{browserName}-{width}x{height}.png"
        }
      }
    },
    “mobile”: { 
      “windowSize”: [“375x667”], 
      “screenshots”: { 
        “homePageMobile”: { 
          “fullPage”: true, 
          “disableCSSAnimation”: true, 
          “selectorExpansion”: true, 
          “selector”: “#app”, 
          “fileName”: “{tag}-homepage-mobile-{browserName}-{width}x{height}.png” 
        } 
      } 
    }
  }
}
```
Semoga membantu!
