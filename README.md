<p align="center">
  <img src="https://api.cloudsky.biz.id/file?key=kurumi-bot/1766640592653.jpg" alt="Joy Bot Logo" width="600"/>
</p>

<h1 align="center">Joy Bot</h1>

<p align="center">
  <a href="https://github.com/Futaroukun/Joy"><img src="https://img.shields.io/badge/Node.js-v20+-339933?logo=node.js&style=for-the-badge" alt="Node.js"></a>
  <a href="https://github.com/Futaroukun/Joy"><img src="https://img.shields.io/badge/Baileys-Latest-25D366?logo=whatsapp&style=for-the-badge" alt="Baileys"></a>
  <a href="https://github.com/Futaroukun/Joy"><img src="https://img.shields.io/badge/Type-ESM-00d4ff?style=for-the-badge" alt="Type"></a>
</p>

<p align="center">
  <strong>Joy</strong> adalah bot WhatsApp berarsitektur modern yang dirancang untuk performa tinggi dan efisiensi sumber daya. Dibangun sepenuhnya menggunakan <strong>Node.js ESM</strong>, bot ini menawarkan struktur modular yang mudah dipahami, dimodifikasi, dan didistribusikan secara <strong>Gratis ($0)</strong>.
</p>

---

## Features

- [x] Pairing Code
- [x] NodeJs ESM Sytem
- [x] Simpel Menu
- [x] Auto Reconnect
- [x] Plugins Sytem

> [!NOTE]
> Bot ini menggunakan ECMAScript Modules (ESM), bukan CommonJS. Pastikan menggunakan `import/export` bukan `require()`.

---

## Installation

Anda perlu mengkloning repositori ini. Pastikan [Node.js v20+](https://nodejs.org) sudah terinstal di komputer Anda.

### 1. Clone repositori:
```bash
git clone https://github.com/Futaroukun/Joy
```

### 2. Atur nomor bot Anda:
Edit file `settings.js` di bagian `global.info`. Kemudian ubah nomor owner dan bot.

```javascript
global.owner = ["628xxxxx"]

global.info = {
    nomorbot: "628xxxxx",
    namabot: "Joy",
    nomorowner: "628xxxxx", 
    namaowner: "Rafli"
}
```

### 3. Install modules:
Untuk menginstal modul, Anda dapat langsung menjalankan perintah:

```bash
npm install
```

### 4. Jalankan bot:
Jalankan file utama dengan:

```bash
npm start
# or
node main.js
```

### 5. Masukkan nomor
Masukkan nomor telpon yang akan dijadikan bot di terminal anda lalu enter

### 6. Masukkan kode
Masukan kode yang muncul di terminal ke fitur tautkan perangkat di WhatsApp, caranya begini:

```
1. Klik titik 3 di pojok kanan atas di WhatsApp anda
2. Lalu pilih perangkat tertaut atau tautkan perangkat
3. Klik tombol tautkan perangkat yang berada dibawah
4. Jika muncul popup pilih "Gunakan data seluler"
5. Disini kalian diminta untuk scan (abaikan saja itu) pilih saja "Tautkan dengan nomor telepon saja"
6. Masukan kode yang muncul di terminal tadi lalu tunggu 
```

Selesai! Bot Anda siap digunakan!

---

## Creating a Plugins
Joy dibangun dengan sistem modular yang fleksibel. Anda hanya perlu membuat file .js baru di folder plugins, dan perintah tersebut akan langsung aktif. Berikut adalah contoh struktur plugin standar (ping/speed):

```javascript
import { performance } from 'perf_hooks';

let handler = async (m, { conn }) => {
    let start = performance.now();
    await m.reply('Testing speed...');
    let end = performance.now();
    
    let speed = (end - start).toFixed(2);
    m.reply(`🚀 Latency: ${speed}ms`);
}

handler.help = ['ping'];
handler.tags = ['info'];
handler.command = /^(ping|speed)$/i;

export default handler;

```

---

## Plugin System

Joy dirancang dengan arsitektur *Plug-and-Play* yang sangat efisien. Setiap perintah (command) bersifat modular, artinya lu bisa menambah atau menghapus fitur tanpa mengganggu stabilitas sistem inti.

*Kelebihan sistem plugin Joy:*
- *Hot-Reloading:* Lu cuma perlu edit atau tambah file `.js` di folder `plugins/`, pencet Save, dan Joy bakal otomatis nge-load fiturnya *tanpa perlu restart bot*.
- *ESM Native:* Menggunakan standar modul terbaru (ESM) untuk performa yang lebih enteng.
- *Easy Maintenance:* Kode lebih rapi dan gampang dicari kalau ada error.

---

## License & Contributing

Skrip ini didistribusikan di bawah [MIT license](./LICENSE). Bebas untuk digunakan, dimodifikasi, atau didistribusikan ulang dengan biaya **$0**. Saya akan sangat menghargai jika Anda dapat membantu saya mengembangkannya!

---

<div align="center">

**Made with ❤️ by [Rafli](https://github.com/Futaroukun)**

[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/Futaroukun)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Contact-25D366?logo=whatsapp)](https://wa.me/6283854551575)

</div>
