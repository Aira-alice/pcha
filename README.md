# Pchat

**Chatting and game** — aplikasi untuk berkomunikasi dan bermain bersama.

> 🚧 Masih dalam pengembangan (work in progress).

Dibuat bersama **[@im_da](https://github.com/im_da) (Mr. A)** dan **Mr. Claude**.

---

## Tentang

Pchat adalah aplikasi chat sekaligus game, dibangun sebagai single-page web app (HTML/JS) yang dibungkus jadi aplikasi Android lewat [Capacitor](https://capacitorjs.com/). Bisa dipakai offline, online, maupun mode local online, lengkap dengan kontak, grup, broadcast, dan katalog game bawaan.

## Fitur

- 💬 Chat personal, grup, dan broadcast list
- 🎮 Katalog game bawaan untuk dimainkan bareng kontak
- 🌐 Tiga mode koneksi: offline / online / local online
- 🔐 Login dengan **Google Sign-In** (native, satu klik pilih akun) — satu email Google hanya untuk satu akun Pchat
- 📎 Attachment (dokumen, foto/video) di-staging dulu sebelum dikirim
- 📝 Draft pesan tersimpan otomatis per kontak

## Teknologi

| Bagian | Teknologi |
|---|---|
| App | HTML/CSS/JS single-file (`www/index.html`) |
| Login & data | Firebase Authentication + Realtime Database |
| Login provider | Google Sign-In lewat [`@capacitor-firebase/authentication`](https://github.com/capawesome-team/capacitor-firebase) |
| Wrapper Android | [Capacitor](https://capacitorjs.com/) |
| Build APK | GitHub Actions (otomatis tiap push) |

## Struktur repo

```
.
├── .github/workflows/build.yml   # build APK otomatis
├── www/
│   └── index.html                 # seluruh aplikasi
├── capacitor.config.json
├── package.json
└── README.md
```

## Build

APK debug dibuild otomatis lewat GitHub Actions setiap kali ada push, dan bisa diunduh dari tab **Actions** → pilih run terbaru → artifact `app-debug`.

Build manual (lokal):

```bash
npm install
npx cap add android      # sekali saja kalau folder android/ belum ada
npx cap sync android
cd android && ./gradlew assembleDebug
```

## Status

Proyek masih aktif dikembangkan — fitur, tampilan, dan struktur bisa berubah sewaktu-waktu.

---

Dibuat dengan 🤍 oleh **@im_da (Mr. A)** & **Mr. Claude**.
