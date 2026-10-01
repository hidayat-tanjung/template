<div align="center">

# 🐧 LinuxPloiter

### Bug Bounty Companion & Reconnaissance Workstation

Client-side OSINT dan reconnaissance toolkit untuk workflow bug bounty yang berizin. Aplikasi berjalan di browser tanpa backend milik LinuxPloiter; hasil, riwayat, preferensi, dan API key disimpan di `localStorage` browser.

[![Version](https://img.shields.io/badge/version-8.0-a020f0?style=for-the-badge)](#-changelog)
[![License](https://img.shields.io/badge/license-MIT-10b981?style=for-the-badge)](#-lisensi)
[![Platform](https://img.shields.io/badge/platform-Web%20Browser-00e5ff?style=for-the-badge)](#-persyaratan)
[![Made with](https://img.shields.io/badge/made%20with-HTML%20%2B%20CSS%20%2B%20JS-f59e0b?style=for-the-badge)](#-teknologi)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=for-the-badge)](#-kontribusi)
[![GitHub Stars](https://img.shields.io/github/stars/OWNER/REPOSITORY?style=for-the-badge&logo=github)](https://github.com/OWNER/REPOSITORY/stargazers)

[🚀 Quick Start](#-quick-start) · [📖 Dokumentasi](#-daftar-isi) · [🐛 Report Bug](https://github.com/OWNER/REPOSITORY/issues/new?template=bug_report.yml) · [💡 Request Feature](https://github.com/OWNER/REPOSITORY/issues/new?template=feature_request.yml)

</div>

> **Setup repository:** ganti `OWNER/REPOSITORY` pada badge dan tautan dengan alamat GitHub proyek yang sebenarnya. Hubungkan badge License ke file `LICENSE` saat file tersebut tersedia.

## 🧭 Daftar Isi

- [📸 Screenshots](#-screenshots)
- [🐧 Apa Itu LinuxPloiter?](#-apa-itu-linuxploiter)
- [✨ Fitur Utama](#-fitur-utama)
- [🚀 Quick Start](#-quick-start)
- [🧰 Persyaratan](#-persyaratan)
- [🧱 Teknologi](#-teknologi)
- [🖥️ Struktur Header](#️-struktur-header)
- [📱 Mobile Drawer](#-mobile-drawer)
- [🔑 API Key Manager](#-api-key-manager)
- [💖 Donasi](#-donasi)
- [🛡️ Notifikasi & Validasi](#️-notifikasi--validasi)
- [🧭 Tab Navigasi](#-tab-navigasi)
- [🛠️ Recon Tools](#️-recon-tools)
- [🕵️ OSINT Tools](#️-osint-tools)
- [⌨️ Command Builder](#️-command-builder)
- [📊 Dashboard](#-dashboard)
- [🏆 Bounty Tracker](#-bounty-tracker)
- [📝 Report Generator](#-report-generator)
- [⚠️ Error Analyzer](#️-error-analyzer)
- [📖 Guide](#-guide)
- [🗃️ Penyimpanan Data](#️-penyimpanan-data)
- [🔐 Privasi & Keamanan](#-privasi--keamanan)
- [🧾 Changelog](#-changelog)
- [⚖️ Legal Notice](#️-legal-notice)
- [📄 Lisensi](#-lisensi)
- [🤝 Kontribusi](#-kontribusi)
- [📬 Kontak](#-kontak)

## 🐧 Apa Itu LinuxPloiter?

LinuxPloiter adalah workstation reconnaissance client-side untuk bug bounty hunter, security researcher, dan pentester. UI dan sebagian besar pemrosesan berjalan di browser melalui satu file HTML.

Aplikasi menyediakan generator dork, pemeriksaan `security.txt`, pencarian berbasis API, parser scope, command templates, tracker, report generator, serta dokumentasi penggunaan.

LinuxPloiter bukan scanner backend dan tidak menjalankan command-line tools di browser. Tool CLI hanya menghasilkan template command untuk disalin dan dijalankan secara terpisah pada sistem pengguna.

Aplikasi tidak memiliki server LinuxPloiter yang menerima hasil scan. Namun, penggunaan Google, Shodan, Censys, provider AI, CDN, QRCode.js, atau CORS proxy dapat mengirim request ke layanan pihak ketiga.

| Kelebihan | Deskripsi |
|---|---|
| Client-side | Antarmuka berjalan di browser; tidak membutuhkan backend aplikasi. |
| Satu file | Implementasi utama berada di `index.html`. |
| Workflow praktis | Tab mengelompokkan discovery, pencarian, pelacakan, dan pelaporan. |
| Penyimpanan lokal | Preferensi, history, statistik, API keys, dan bounty disimpan pada browser. |
| Responsive | Header desktop dua baris dan drawer navigasi untuk layar kecil. |
| Ekspor data | Beberapa hasil dapat diekspor ke JSON, CSV, Markdown, TXT, atau shell script. |

## ✨ Fitur Utama

| Area | Ringkasan |
|---|---|
| Navigasi | Header dua baris pada desktop, dropdown 14 tab, dan drawer pada mobile. |
| Dorking | Susun query dari platform, path, keyword, target domain, dan file type. |
| API search | Google Custom Search, Shodan, dan Censys dengan kredensial pengguna. |
| Disclosure | Batch scanner untuk `security.txt` dan parser scope HackerOne. |
| Recon helpers | Katalog tool dan template CLI untuk aktivitas reconnaissance. |
| OSINT | Shortcut ke layanan people, breach, infra, network, leaks, dan social search. |
| Workflow | Command Builder, script 10 fase, Bounty Tracker, dan Report Generator. |
| Analisis error | Pattern database dengan opsi analisis provider AI yang dikonfigurasi. |
| Dashboard | Statistik lokal dan grafik Chart.js. |
| Donasi | Link PayPal, alamat Bitcoin, dan QR code di modal profil. |
| Input feedback | Validasi input, toast, highlight field, dan normalisasi error HTTP. |

## 🚀 Quick Start

### Buka langsung

1. Unduh atau clone repository setelah mengganti URL placeholder dengan URL proyek yang benar.
2. Buka `index.html` menggunakan browser modern.
3. Pilih tab dari dropdown header.
4. Tambahkan API key hanya untuk layanan yang akan digunakan.
5. Jalankan aktivitas hanya pada target yang termasuk scope izin.

### Jalankan melalui server lokal statis

Server lokal opsional dapat membantu clipboard, origin browser, dan integrasi API tertentu. Server ini hanya menyajikan file statis; ia bukan backend LinuxPloiter.

```bash
git clone https://github.com/OWNER/REPOSITORY.git
cd REPOSITORY
python3 -m http.server 8000
```

Buka URL berikut di browser:

```text
http://localhost:8000
```

Untuk menghentikan server, tekan `Ctrl+C` pada terminal yang menjalankannya.

### Cara menggunakan alur dasar

1. Baca scope program bug bounty dan pastikan aset target diizinkan.
2. Pilih tab dari dropdown header desktop atau dari drawer mobile.
3. Isi target, query, atau data yang diminta oleh tab.
4. Simpan kredensial layanan hanya jika fitur tersebut membutuhkannya.
5. Tinjau pesan validasi sebelum mengirim request.
6. Jalankan pencarian atau scan sesuai rate limit layanan dan program.
7. Simpan hasil yang relevan ke file ekspor atau report.
8. Hapus key yang tidak lagi dipakai dari API Key Manager.

### Tips penggunaan

- Gunakan target domain yang telah dinormalisasi dan termasuk scope.
- Mulai dari query dan concurrency rendah; ikuti batas rate layanan.
- Jika browser memblokir CORS, pahami bahwa proxy pihak ketiga dapat melihat request.
- Cek hasil secara manual; output tool bukan bukti final vulnerability.
- Jangan jalankan command recon ke sistem tanpa otorisasi eksplisit.
- Jangan mengunggah screenshot yang memperlihatkan token, target privat, atau data sensitif.
- Ekspor settings dapat berisi API key lama dan data profil; simpan seperti secret.

## 🧰 Persyaratan

| Komponen | Persyaratan |
|---|---|
| Browser | Chrome, Firefox, Edge, atau Safari versi modern. |
| JavaScript | Harus diaktifkan untuk seluruh fitur interaktif. |
| Internet | Dibutuhkan untuk CDN, API eksternal, dan link komunitas. |
| Backend aplikasi | Tidak dibutuhkan. |
| API key | Opsional; dibutuhkan hanya untuk provider/layanan berbayar atau terautentikasi. |
| OS untuk CLI | Linux/macOS/Windows sesuai tool yang akan dijalankan terpisah. |

## 🧱 Teknologi

| Teknologi | Pemakaian |
|---|---|
| HTML | Struktur aplikasi single-page. |
| CSS | Tema gelap/terang, layout responsive, drawer, toast, dan modal. |
| JavaScript vanilla | Validasi, navigasi, penyimpanan lokal, request, dan rendering. |
| Chart.js 4.4.1 | Grafik aktivitas dan penggunaan tools. |
| QRCode.js 1.0.0 | Membuat QR PayPal dan Bitcoin di browser. |
| localStorage | Menyimpan settings, AI keys, form state, history, statistik, dan bounty. |

## 🖥️ Struktur Header

### Desktop

```text
┌──────────────────────────────────────────────────────────────────────────────┐
│ 🐧 LinuxPloiter v8.0              🐙 🐦 💬 🤖 🏆 ⭐ Rating ⚙️ API Keys 🇮🇩 ID │
├──────────────────────────────────────────────────────────────────────────────┤
│ 📊 Recon Dashboard ▾   🕐 History   🌓 Theme   📄 JSON   📊 CSV               │
└──────────────────────────────────────────────────────────────────────────────┘
```

- Baris pertama mempertahankan brand di kiri dan kelompok community/settings di kanan.
- Baris kedua memulai navigasi dari kiri dan menyediakan aksi history, theme, serta ekspor.
- Tab dropdown dibangun dari `<nav class="tabs-nav">` yang disimpan sebagai sumber data tersembunyi.
- Nav sumber berisi 14 tombol `.tab-btn` dengan `data-tab` unik.
- Pada lebar di bawah 1240px, label tombol aksi disembunyikan agar kontrol tetap muat.
- Dropdown tetap menampilkan nama tab aktif pada ukuran desktop kompak.

### Mobile

```text
┌────────────────────────────────────────┐
│ 🐧 LinuxPloiter v8.0             ☰     │
└────────────────────────────────────────┘
```

- Di bawah 900px, row-1 controls dan row-2 disembunyikan.
- Brand tetap di kiri dan hamburger tetap di kanan.
- Nav sumber tidak dihapus; tabnya dipakai untuk mengisi dropdown dan drawer.

## 📱 Mobile Drawer

Drawer muncul dari sisi kiri setelah tombol hamburger ditekan.

| Bagian | Isi |
|---|---|
| NAVIGASI | Semua 14 tab yang dibuat dari `nav.tabs-nav`. |
| TOOLS | API Keys, History, Theme, ekspor JSON/CSV, dan Rating. |
| COMMUNITY | Link community yang ditampilkan oleh aplikasi. |
| LANGUAGE | Pilihan bahasa yang disinkronkan dengan selector desktop. |

Drawer ditutup dengan salah satu cara berikut:

- Tekan tombol `✕` di header drawer.
- Klik overlay gelap di luar drawer.
- Tekan tombol `Escape`.
- Ubah ukuran viewport menjadi lebih dari 900px.
- Pilih salah satu item navigasi; drawer menutup setelah tab berpindah.

`data-mobile-tab` dibuat dari setiap tombol `.tab-btn`. Ini mencegah daftar mobile berbeda dari dropdown desktop.

## 🔑 API Key Manager

API Key Manager mendukung provider berikut. Model default hanya dipakai saat field model dibiarkan kosong pada provider yang mendukung default tersebut.

| Provider | Model analisis default | Endpoint test yang digunakan |
|---|---|---|
| OpenAI | `gpt-4o-mini` | `https://api.openai.com/v1/models` |
| Google Gemini | `gemini-2.0-flash` | `https://generativelanguage.googleapis.com/v1/models` |
| Anthropic Claude | `claude-3-5-haiku-latest` | `https://api.anthropic.com/v1/models` |
| Groq | `llama-3.1-8b-instant` | `https://api.groq.com/openai/v1/models` |
| OpenRouter | `openai/gpt-4o-mini` | `https://openrouter.ai/api/v1/models` |
| Mistral | `mistral-small-latest` | `https://api.mistral.ai/v1/models` |
| Cohere | `command-r7b-12-2024` | `https://api.cohere.com/v1/models` |
| Custom | Diisi pengguna | `{BASE_URL}/models` |

Nama model/provider dan endpoint di atas menggambarkan konfigurasi yang tertulis di `index.html`; provider dapat mengubah API-nya sewaktu-waktu.

### Menambahkan dan memakai key

1. Buka `⚙️ API Keys` dari header atau drawer.
2. Pilih provider dari daftar.
3. Masukkan key pada field API Key.
4. Untuk Custom, masukkan Base URL `http://` atau `https://`; masukkan Model untuk analisis.
5. Tekan `Simpan` untuk menyimpan key di `localStorage`.
6. Tekan `Test` untuk menguji endpoint daftar model provider.
7. Gunakan ikon 🧪 pada baris key tersimpan untuk mengulang test.
8. Gunakan ikon 🗑️ untuk menghapus key tertentu.
9. Error Analyzer memakai key AI terakhir yang tersimpan; jika tidak ada, ia mencoba key Gemini/Groq lama pada settings.

### Keamanan API key

- Key disimpan di `localStorage`; browser tidak mengenkripsi nilai tersebut.
- Jangan memakai browser profile bersama untuk key produksi.
- Jangan membagikan ekspor settings yang berisi key.
- Request AI mengirim prompt langsung ke provider yang dipilih.
- Provider dapat mencatat request sesuai kebijakan privasinya.
- Request browser dapat gagal karena CORS walaupun key valid.
- CORS proxy pihak ketiga dapat membaca URL, header, dan body yang diteruskan.
- Jangan menaruh API key dalam screenshot, laporan bug publik, atau commit.
- Hapus key dari Manager dan cabut key di dashboard provider jika bocor.

## 💖 Donasi

### PayPal

- Link: [Donasi via PayPal](https://www.paypal.com/donate)
- QR code mengodekan URL donasi umum PayPal.
- Perbarui URL ke halaman donasi proyek yang tepat bila tersedia.

### Bitcoin

- Address yang tertulis pada source saat README ini dibuat: `bc1qlinuxploiterxxxxxxxxxxxxxxxxxxxxxx`.
- QR code mengodekan URI `bitcoin:` dengan address tersebut.
- **Address itu tampak sebagai placeholder, bukan wallet address yang dapat diverifikasi. Ganti dengan address Bitcoin valid sebelum menerima pembayaran.**
- Verifikasi hasil scan QR dan address secara independen sebelum publikasi.

QRCode.js membuat gambar QR di client-side saat modal profil dibuka. Kode PayPal dan Bitcoin berada di bagian donasi pada `profileModal`; link dan salin wallet tersedia di profile modal serta di bagian `Support LinuxPloiter` pada settings modal.

## 🛡️ Notifikasi & Validasi

| Skenario | Pemeriksaan | Feedback |
|---|---|---|
| Google API Key kosong/pendek | Wajib, minimal 20 karakter | Toast error dan field diberi border merah. |
| Google CX kosong/pendek | Wajib, minimal 10 karakter | Toast error dan field diberi border merah. |
| Query Google terlalu pendek | Minimal 3 karakter | Toast error dan field diberi border merah. |
| Shodan API key kosong | Wajib diisi | Toast error dan focus ke API key. |
| Query Shodan/Censys pendek | Wajib, minimal 3 karakter | Toast warning dan focus ke query. |
| Censys ID atau secret kosong | Wajib diisi | Toast error dan focus ke field terkait. |
| security.txt input kosong | Minimal satu domain | Toast warning dan textarea disorot. |
| security.txt domain malformed | Validasi domain per item | Toast warning menyebut domain invalid. |
| HackerOne handle invalid | Wajib, alfanumerik | Toast warning dan input disorot. |
| Error Analyzer kosong/pendek | Minimal 10 karakter | Toast warning dan textarea disorot. |
| Dork tanpa chip aktif | Minimal satu chip platform/path/keyword | Toast warning; query tidak dibuat. |
| Target dork malformed | Format domain | Toast warning dan input disorot. |
| Report title kosong | Wajib diisi | Toast error; generate/copy/download dibatalkan. |
| Report description kosong | Wajib diisi | Toast error; generate/copy/download dibatalkan. |
| Custom Base URL salah | Wajib URL HTTP/HTTPS | Toast error dan field disorot. |
| HTTP 401 | Kredensial invalid/expired | Pesan API key tidak valid. |
| HTTP 403 | Akses ditolak | Pesan cek API key atau IP. |
| HTTP 404 | Endpoint tidak ditemukan | Error endpoint 404. |
| HTTP 429 | Rate limit | Pesan coba lagi nanti. |
| HTTP 5xx | Kesalahan server | Pesan server error dan status. |
| Network/CORS | Fetch gagal | Pesan periksa koneksi atau CORS proxy. |

`highlightError()` menyorot border dan shadow field selama tiga detik, lalu mengembalikan style ke nilai default.

`safeFetch()` memeriksa status HTTP dan melempar pesan yang sesuai untuk 401, 403, 404, 429, dan 5xx. Error jaringan/CORS dinormalisasi sebelum ditampilkan lewat toast.

Handler global untuk `error` dan `unhandledrejection` mencatat error ke console serta menampilkan toast. Handler global adalah lapisan tambahan; alur form tetap menangani error yang diharapkan secara lokal.

## 🧭 Tab Navigasi

| No. | Tab | Fungsi |
|---:|---|---|
| 1 | 📊 Recon Dashboard | Ringkasan statistik, aktivitas, tool usage, dan distribusi hasil. |
| 2 | 🎯 Dork Generator | Membuat, menyalin, mengimpor, mencari, dan mengekspor query Google. |
| 3 | 🔍 Google API | Pencarian melalui Google Programmable Search / Custom Search API. |
| 4 | 🛡️ security.txt | Batch scan file security contact pada daftar domain. |
| 5 | 🌐 Shodan | Mencari host dan service melalui Shodan API. |
| 6 | 🔎 Censys | Mencari host dan service melalui Censys Hosts API v2. |
| 7 | 📋 H1 Scope | Mengambil, memuat sample, atau parse scope JSON HackerOne. |
| 8 | ⌨️ Command Builder | Menyusun command CLI dan pipeline recon. |
| 9 | 🛠️ Recon Tools | Katalog shortcut layanan dan template CLI reconnaissance. |
| 10 | 🕵️ OSINT Tools | Katalog layanan OSINT berdasarkan kategori. |
| 11 | 🏆 Bounty Tracker | Mencatat submission, severity, status, reward, dan tanggal. |
| 12 | 📝 Report Generator | Menghasilkan laporan Markdown dan JSON. |
| 13 | ⚠️ Error Analyzer | Mencocokkan pattern error dan meminta analisis AI opsional. |
| 14 | 📖 Guide | Dokumentasi fitur dengan pencarian dan tombol navigasi tab. |

## 🛠️ Recon Tools

Jumlah aktual pada array source: 46 tools.

| Kategori | Tools |
|---|---|
| Subdomain | Subfinder, Amass, Assetfinder, PureDNS, ShuffleDNS, Sublist3r, Alterx, DNSDumpster, CRT.sh |
| DNS | DNSX, DNSRecon |
| Probing | HTTPX, TLSX |
| Port Scan | Naabu, Nmap, Masscan, RustScan |
| Crawling | Katana, Gospider, Hakrawler, Photon, Crawlergo |
| Archive | GAU, Waybackurls, URLScan.io, GitHub Subdomains, Gotator |
| Directory fuzzing | FFUF, Feroxbuster, Dirsearch, Gobuster, ParamSpider |
| Parameter discovery | Arjun, X8 |
| Vulnerability scan | Nuclei, Dalfox, SQLMap, Smap |
| Secrets | TruffleHog, Gitleaks |
| Cloud | S3Scanner, Cloud_enum, CloudBrute, S3crets Scanner, GrayHatWarfare, Bucket Finder |

### Menjalankan shortcut

1. Buka `Recon Tools` dari tab dropdown atau mobile drawer.
2. Gunakan search box untuk memfilter nama, deskripsi, dan kategori.
3. Tekan `Run` pada tool yang diinginkan.
4. Shortcut berbasis browser membuka situs eksternal di tab baru.
5. Shortcut CLI menyalin template command ke clipboard.
6. Ganti placeholder seperti `TARGET`, `USERNAME`, atau `ORG` sebelum menjalankan command.
7. Pastikan tool terkait terinstal di lingkungan terminal.

Aplikasi hanya menyalin command; aplikasi tidak menjalankan tool sistem secara langsung.

## 🕵️ OSINT Tools

Jumlah aktual pada array source: 30 tools.

| Kategori | Tools |
|---|---|
| People | Sherlock, Maigret, Blackbird, Social-Searcher |
| Breach | theHarvester, Hunter.io, Have I Been Pwned, H8Mail, Intelligence X, DeHashed |
| Infra | Shodan, Censys, FOFA, ZoomEye, Hunter.how, FullHunt |
| Network | IPInfo.io, AbuseIPDB, GreyNoise, ViewDNS, Whois |
| Leaks | Pastebin Search, NerdyData, GitHub Code Search |
| Dorks | Google Hacking Database, Google Advanced Search |
| Social | Twitter/X Advanced, LinkedIn People, Telegram Web |
| Automasi | SpiderFoot |

Beberapa layanan membuka halaman eksternal; beberapa template CLI menyalin command. Login, API key, kuota, CORS, dan terms of service ditentukan oleh layanan masing-masing.

## ⌨️ Command Builder

Source saat ini berisi 58 command template, termasuk 15 item kategori Full Pipeline.

| Kategori | Contoh command |
|---|---|
| Host Setup | Clean Target, DNS Baseline, Curl Header Test |
| Cloud Recon | Cloud_enum, S3Scanner, GCP checks, bucket ACL, sensitive-file grep |
| Takeover | Subzy, Nuclei Takeover, HTTPX CNAME hints |
| JS Recon | SubJS, LinkFinder |
| Subdomain Recon | Subfinder, Assetfinder, Amass, ShuffleDNS |
| HTTP/DNS/Port | HTTPX, DNSX, Naabu, Nmap |
| Crawling/Archive | Katana, Gospider, GAU, Waybackurls |
| Content Discovery | FFUF, Feroxbuster, Dirsearch, Arjun |
| Vuln Scanning | Nuclei, Dalfox, SQLMap, Nikto, GF, QSReplace, Maquina |
| Source Code | TruffleHog, Gitleaks |
| Header Injection | CRLFuzz, security-header audit, CORS check |
| Full Pipeline | Subfinder→HTTPX, passive sweep, Wayback mining, Nuclei, takeover, XSS, JS secrets, 403, redirect, SSRF, VHOST, screenshot, ports, S3, Discord notification |

### Pipeline yang tersedia

| Pipeline | Ringkasan |
|---|---|
| `pipeline_subs_httpx` | Enumerasi subdomain pasif lalu HTTP probe. |
| `pipeline_full_sweep` | Subfinder dan Assetfinder diikuti sort dan HTTPX. |
| `pipeline_wayback_sensitive` | Mencari URL arsip dengan ekstensi file sensitif. |
| `pipeline_nuclei_auto` | Subfinder, HTTPX, lalu Nuclei. |
| `pipeline_takeover` | Kandidat takeover melalui DNSX, HTTPX, Subzy, Nuclei. |
| `pipeline_xss_hunt` | Katana, GF, QSReplace, dan Dalfox. |
| `pipeline_js_secrets` | SubJS dan Nuclei exposure templates. |
| `pipeline_403_bypass` | Mengumpulkan response 403 untuk pemeriksaan manual. |
| `pipeline_open_redirect` | Menyaring parameter redirect dan memeriksa lokasi response. |
| `pipeline_ssrf` | Mengumpulkan kandidat parameter SSRF untuk verifikasi manual. |
| `pipeline_vhost` | Alterx dan HTTPX untuk kandidat virtual host. |
| `pipeline_screenshot` | HTTPX dan Gowitness untuk screenshot host. |
| `pipeline_port_to_nuclei` | Naabu, HTTPX, lalu Nuclei pada service yang ditemukan. |
| `pipeline_s3_recon` | Cloud enum, identifikasi bucket, lalu S3Scanner. |
| `pipeline_notify_discord` | Nuclei dan pengiriman hasil melalui webhook Discord. |

### Menggunakan Command Builder

1. Masukkan Target, Input File, Output Dir, Threads, Wordlist, dan Custom Header.
2. Pilih kategori jika ingin menyaring command.
3. Tekan `Copy` untuk menyalin command tertentu.
4. Tekan `Copy All Pipelines` untuk menyalin seluruh template.
5. Tekan `Download .sh Script` untuk menghasilkan skrip pipeline reconnaissance 10 fase.
6. Periksa skrip sebelum menjalankan dan sesuaikan input, path, rate, serta tool yang terinstal.

Skrip hasil unduhan tidak dijalankan dari browser. Jalankan hanya setelah memeriksa bahwa seluruh target termasuk scope dan tiap langkah diizinkan.

## 📊 Dashboard

Dashboard membaca statistik lokal untuk menampilkan:

- Total scan dan findings.
- Jumlah dork yang tercatat.
- Jumlah tool yang pernah digunakan.
- Aktivitas scans dan findings per hari selama tujuh hari.
- Grafik tool usage.
- Grafik distribusi dork, scan, dan aktivitas lain.
- Statistik hari ini dan agregat tujuh hari.
- Tabel channel, scan, findings, dan success rate.

Grafik memakai Chart.js. Statistik disimpan pada `localStorage`; data dapat berbeda antar browser profile dan perangkat.

## 🏆 Bounty Tracker

Bounty Tracker mencatat hasil submission secara lokal.

| Field | Isi |
|---|---|
| Program | Nama program bug bounty. |
| Vulnerability | Judul vulnerability yang dilaporkan. |
| Severity | Tingkat severity. |
| Status | Status triage atau penyelesaian. |
| Reward | Nilai reward jika ada. |
| Date | Tanggal entri dicatat. |

Data tersimpan di `localStorage` dan dapat ikut disertakan dalam ekspor report agregat.

## 📝 Report Generator

Report Generator menyiapkan konten Markdown dan JSON dengan field berikut:

- Program.
- Title.
- Severity.
- Description.
- Steps to Reproduce.
- Impact.
- Remediation.

Title dan Description wajib diisi. Tombol Generate, Copy, Markdown, dan JSON menghentikan operasi serta menampilkan toast bila validasi gagal.

Selalu tinjau report sebelum dikirim. Hapus informasi pribadi, credential, data pengguna, dan detail yang tidak diperlukan.

## ⚠️ Error Analyzer

Error Analyzer mencocokkan teks terhadap pattern umum untuk:

- CORS.
- Kegagalan fetch/network.
- HTTP 401.
- HTTP 403.
- HTTP 404.
- HTTP 429/rate limit.
- HTTP 500.
- Timeout.
- SSL/TLS/certificate.
- DNS/NXDOMAIN/SERVFAIL.

Input minimal 10 karakter. Jika AI key tersedia, key AI terakhir yang disimpan digunakan; jika tidak, integrasi Gemini/Groq lama dapat dipakai. Request AI mengirim error yang ditempel ke provider terpilih.

## 📖 Guide

Guide berisi 13 topik untuk alur Dork Generator, Google API, security.txt, Shodan, Censys, H1 Scope, Command Builder, Recon Tools, OSINT, Bounty Tracker, Report Generator, Error Analyzer, dan fitur global.

- Gunakan search box untuk mencari topik.
- Tekan tombol `Buka ...` untuk berpindah ke tab terkait.
- Nav dropdown dan drawer dibangun dari sumber data tab yang sama.
- Baca batasan CORS, API key, dan legal notice sebelum melakukan request.

## 🗃️ Penyimpanan Data

| Key localStorage | Jenis data |
|---|---|
| `linuxploiter_api_keys` | API keys lama, konfigurasi provider, CORS proxy, dan AI provider keys. |
| `linuxploiter_history` | Maksimum 50 aktivitas terbaru. |
| `linuxploiter_theme` | Tema `dark` atau `light`. |
| `linuxploiter_stats` | Total dan statistik harian/channel/tool. |
| `linuxploiter_form_state` | Nilai form yang dipulihkan saat reload. |
| `linuxploiter_bounty_tracker` | Entri Bounty Tracker. |
| `linuxploiter_user_profile` | Data profil lokal yang dipertahankan aplikasi. |
| `linuxploiter_lang` | Preferensi bahasa. |

Hapus data melalui kontrol aplikasi atau browser settings. Menghapus browser storage akan menghapus data lokal yang belum diekspor.

## 🔐 Privasi & Keamanan

- LinuxPloiter tidak menyertakan backend aplikasi untuk menerima hasil scan.
- `localStorage` bukan penyimpanan terenkripsi; perangkat lokal dan browser profile harus diamankan.
- API calls mengirim kredensial ke endpoint provider terkait.
- Google, Shodan, Censys, AI providers, CDN, QRCode.js, dan CORS proxy adalah pihak ketiga.
- Jangan masukkan secret atau informasi sensitif pada query yang tidak dipercaya.
- Jangan gunakan fitur untuk melewati scope, autentikasi, atau kebijakan layanan.
- Hasil scanner adalah petunjuk; verifikasi manual sebelum melaporkan.
- Patuhi rate limit, acceptable use policy, dan aturan program bug bounty.

## 🧾 Changelog

### v8.0

- ✅ Header desktop dua baris dengan brand, community, Rating, API Keys, language, dropdown tab, dan aksi.
- ✅ Tab dropdown desktop dibangun dari `nav.tabs-nav` yang dipertahankan.
- ✅ Mobile drawer membangun 14 item navigasi otomatis dari sumber tab.
- ✅ Menghapus input profil nama/email/HackerOne dari panel profil.
- ✅ Menambahkan QR PayPal dan Bitcoin di modal profil.
- ✅ API Key Manager multi-provider untuk OpenAI, Gemini, Claude, Groq, OpenRouter, Mistral, Cohere, dan Custom.
- ✅ Key AI dapat dimask, diuji, dihapus, dan digunakan oleh Error Analyzer.
- ✅ Menambahkan validasi form dan highlight error tiga detik.
- ✅ Menambahkan `safeFetch()` untuk HTTP/network errors.
- ✅ Menambahkan notifikasi global untuk error dan promise rejection.
- ✅ Memperbarui Guide dan changelog di dalam aplikasi.

### 🔜 Roadmap v9.0 (ide, belum menjadi komitmen)

- 🔜 Konfigurasi endpoint dan model AI per key dengan kemampuan verifikasi yang lebih lengkap.
- 🔜 Import/export laporan per modul dengan redaksi secret.
- 🔜 Pengaturan concurrency dan rate limit yang lebih terperinci.
- 🔜 Pengujian browser otomatis untuk alur utama.
- 🔜 Terjemahan UI dan dokumentasi yang dikelola bersama.
- 🔜 Penyediaan screenshot aktual dan aset dokumentasi.
- 🔜 Pengelolaan konfigurasi donation yang dapat diverifikasi.

## ⚖️ Legal Notice

> **Gunakan LinuxPloiter hanya untuk target yang Anda miliki atau target yang secara eksplisit masuk dalam scope dan aturan program.** Pengguna bertanggung jawab atas izin, dampak request, dan kepatuhan hukum.

### Penggunaan yang diizinkan

- ✅ Aset milik sendiri atau lab lokal.
- ✅ Target program bug bounty yang tercantum in-scope.
- ✅ Aktivitas sesuai rate limit dan aturan tertulis program.
- ✅ Validasi temuan dengan dampak minimal dan tanpa mengambil data yang tidak diperlukan.

### Penggunaan yang dilarang

- ❌ Scan, fuzz, exploit, atau akses tanpa otorisasi.
- ❌ Menguji aset out-of-scope atau pihak ketiga tanpa izin.
- ❌ Mengganggu ketersediaan layanan atau menjalankan traffic berlebihan.
- ❌ Mengakses, menyimpan, atau menyebarkan data pribadi tanpa izin.
- ❌ Menggunakan tool untuk phishing, credential theft, malware, atau penyalahgunaan lain.

## 📄 Lisensi

README ini mendokumentasikan lisensi MIT sesuai spesifikasi proyek. Repository saat ini belum memiliki file `LICENSE`; tambahkan file lisensi resmi sebelum menyatakan lisensi tersebut berlaku secara hukum.

```text
MIT License

Copyright (c) 2026 LinuxPloiter contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Pastikan isi `LICENSE`, pemegang hak cipta, badge, dan tahun sesuai keputusan maintainer.

## 🤝 Kontribusi

Kontribusi dipersilakan untuk dokumentasi, perbaikan aksesibilitas, validasi, keamanan, dan kualitas UI.

- 🐛 Bug report: `https://github.com/OWNER/REPOSITORY/issues/new?template=bug_report.yml`
- 💡 Feature request: `https://github.com/OWNER/REPOSITORY/issues/new?template=feature_request.yml`
- 📖 Dokumentasi: perbaiki instruksi dan sertakan versi browser yang diuji.
- 🌐 Terjemahan: gunakan istilah keamanan yang konsisten dan hindari menerjemahkan nama API.

### Alur kontribusi

```bash
git clone https://github.com/OWNER/REPOSITORY.git
cd REPOSITORY
git checkout -b docs/readme-improvement
# Edit README.md atau index.html
# Jalankan pemeriksaan syntax dan uji manual di browser
git diff --check
git status --short
git add README.md
git commit -m "docs: improve project README"
git push origin docs/readme-improvement
```

Sebelum membuat pull request:

1. Pastikan perubahan hanya mencakup tujuan pull request.
2. Jangan commit API key, wallet seed, token, atau data target privat.
3. Uji desktop dan mobile pada browser modern.
4. Sertakan langkah reproduksi untuk bug UI atau fetch.
5. Jangan klaim hasil scan sebagai temuan terverifikasi tanpa bukti.
6. Jelaskan batasan CORS dan endpoint pihak ketiga bila relevan.
7. Perbarui screenshot hanya menggunakan data aman untuk publikasi.

## 📬 Kontak

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-OWNER%2FREPOSITORY-181717?style=for-the-badge&logo=github)](https://github.com/OWNER/REPOSITORY)
[![Twitter/X](https://img.shields.io/badge/Twitter%2FX-Profile-000000?style=for-the-badge&logo=x)](https://x.com/)
[![Discord](https://img.shields.io/badge/Discord-Community-5865F2?style=for-the-badge&logo=discord)](https://discord.com/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail)](mailto:YOUR_EMAIL@example.com)

