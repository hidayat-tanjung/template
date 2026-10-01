
Klik ☰ → drawer buka dari kiri.

---

## Mobile Drawer

Berisi 4 section:

| Section | Isi |
|---------|-----|
| **NAVIGASI** | 14 tab (auto-generate dari `nav.tabs-nav`) |
| **TOOLS** | API Keys, History, Theme, Export JSON/CSV, Rating |
| **COMMUNITY** | Link sosmed (GitHub, Twitter, Discord, dll) |
| **LANGUAGE** | Pilihan bahasa (10 bahasa) |

**Cara tutup:**
- Klik tombol ✕
- Klik overlay gelap
- Tekan **Escape**
- Resize ke desktop (>900px) → auto-close

---

## API Key Manager

Multi-provider AI yang bisa lo input sendiri:

| Provider | Default Model | Test Endpoint |
|----------|---------------|---------------|
| OpenAI | gpt-4o-mini | `api.openai.com` |
| Google Gemini | gemini-2.0-flash | `generativelanguage.googleapis.com` |
| Anthropic Claude | claude-3-5-haiku | `api.anthropic.com` |
| Groq | llama-3.1-8b-instant | `api.groq.com` |
| OpenRouter | openai/gpt-4o-mini | `openrouter.ai` |
| Mistral AI | mistral-small-latest | `api.mistral.ai` |
| Cohere | command-r7b | `api.cohere.com` |
| **Custom** | (bebas) | (Base URL sendiri) |

**Cara pakai:**
1. Buka **⚙️ API Keys & AI**
2. Pilih provider dari dropdown
3. Input API Key
4. Klik **💾 Simpan**
5. Klik **🧪 Test** buat cek valid atau gak
6. Klik **🗑️** buat hapus

**Storage:** localStorage (`linuxploiter_api_keys`)

**Keamanan:**
- ⚠️ Tidak dienkripsi
- ⚠️ Jangan pakai di perangkat bersama
- ⚠️ Jangan share export settings yang berisi API keys

---

## Donasi

LinuxPloiter gratis & open. Kalau tool ini membantu, lo bisa dukung developer:

### PayPal
- Tombol "Donasi via PayPal"
- QR Code PayPal (scan pake HP)
- Link: `https://www.paypal.com/donate`

### Bitcoin
- Tombol "Copy Bitcoin Address"
- QR Code Bitcoin (scan pake wallet app)
- Address: `bc1qlinuxploiterxxxxxxxxxxxxxxxxxxxxxx`

**QR Code:**
- Library: **QRCode.js** (client-side, offline-ready)
- Privacy: gak ada request ke server pihak ketiga
- Ukuran: 144x144px

**Lokasi:**
- Profile Modal (`#profileModal`) — QR + tombol
- Settings Modal (`#settingsModal`) — tombol + link

---

## Notifikasi & Validasi

Semua form punya validasi otomatis dengan notifikasi toast:

| Skenario | Notifikasi |
|----------|-----------|
| Field kosong | ⚠️ "[Label] wajib diisi" |
| Terlalu pendek | ⚠️ "[Label] minimal X karakter" |
| Format salah | ⚠️ "[Label] format tidak valid" |
| API Key 401 | ❌ "API Key tidak valid atau expired (401)" |
| API Key 403 | ❌ "Akses ditolak (403)" |
| Rate limit 429 | ❌ "Rate limit tercapai (429)" |
| Network error | ❌ "Network error / CORS" |
| Server error 500 | ❌ "Server error (500)" |
| Global error | ❌ "Error: [message]" |

**Bonus:** Border input jadi **merah selama 3 detik** kalau invalid (`highlightError()`).

---

## Tab Navigasi

14 tab yang bisa diakses dari dropdown:

| No | Tab | Fungsi |
|----|-----|--------|
| 1 | 📊 Recon Dashboard | Stats + chart |
| 2 | 🎯 Dork Generator | Buat Google dork |
| 3 | 🔍 Google API | Google Custom Search |
| 4 | 🛡️ security.txt | Batch scanner |
| 5 | 🌐 Shodan | Host intelligence |
| 6 | 🔎 Censys | Search hosts + TLS |
| 7 | 📋 H1 Scope | HackerOne scope extractor |
| 8 | ⌨️ Command Builder | Generate CLI commands |
| 9 | 🛠️ Recon Tools | 45+ recon tools |
| 10 | 🕵️ OSINT Tools | 30+ OSINT tools |
| 11 | 🏆 Bounty Tracker | Track submissions |
| 12 | 📝 Report Generator | Generate vulnerability report |
| 13 | ⚠️ Error Analyzer | Pattern DB + AI |
| 14 | 📖 Guide | Panduan lengkap |

---

## Recon Tools

45+ tool recon bug bounty, dibagi per kategori:

| Kategori | Tools |
|----------|-------|
| **Subdomain** | Subfinder, Amass, Assetfinder, PureDNS, ShuffleDNS, Sublist3r, Alterx, DNSDumpster, CRT.sh |
| **DNS** | DNSX, DNSRecon |
| **Probing** | HTTPX, TLSX |
| **Port Scan** | Naabu, Nmap, Masscan, RustScan |
| **Crawling** | Katana, Gospider, Hakrawler, Photon, Crawlergo |
| **Archive** | GAU, Waybackurls, URLScan, GitHub Subdomains, Gotator |
| **Dir Fuzz** | FFUF, Feroxbuster, Dirsearch, Gobuster, ParamSpider |
| **Params** | Arjun, X8 |
| **Vuln Scan** | Nuclei, Dalfox, SQLMap, Smap |
| **Secrets** | TruffleHog, Gitleaks |
| **Cloud** | S3Scanner, Cloud_enum, CloudBrute, S3crets, GrayHatWarfare, Bucket Finder |

**Cara pakai:**
- Klik **Run** → command template disalin ke clipboard
- Paste di terminal
- Ganti `TARGET` / `USERNAME`

---

## OSINT Tools

30+ tool intelligence:

| Kategori | Tools |
|----------|-------|
| **People** | Sherlock, Maigret, Blackbird, Social-Searcher |
| **Breach** | theHarvester, Hunter.io, HIBP, H8Mail, Intelligence X, DeHashed |
| **Infra** | Shodan, Censys, FOFA, ZoomEye, Hunter.how, FullHunt |
| **Network** | IPInfo, AbuseIPDB, GreyNoise, ViewDNS, Whois |
| **Leaks** | Pastebin, NerdyData, GitHub Code Search |
| **Dorks** | GHDB, Google Advanced Search |
| **Social** | Twitter/X Advanced, LinkedIn, Telegram Web |
| **Automasi** | SpiderFoot |

---

## Command Builder

55+ command siap pakai + 15 pipeline otomatis:

| Kategori | Contoh |
|----------|--------|
| **Host Setup** | IP resolve, DNS baseline |
| **Cloud Recon** | Cloud_enum, S3Scanner, CloudBrute |
| **Takeover** | Subzy, Nuclei takeover |
| **JS Recon** | SubJS, LinkFinder |
| **Subdomain Recon** | Subfinder, Amass, ShuffleDNS |
| **HTTP Probing** | HTTPX, DNSX, Naabu, Nmap |
| **Crawling** | Katana, Gospider |
| **Archive** | GAU, Waybackurls |
| **Content Discovery** | FFUF, Feroxbuster, Dirsearch, Arjun |
| **Vuln Scanning** | Nuclei, Dalfox, SQLMap, Nikto |
| **Source Code** | TruffleHog, Gitleaks |
| **Header Injection** | CRLFuzz, CORS scan |
| **Full Pipeline** | 15 pipeline otomatis |

**Fitur:**
- **Download .sh script** — pipeline recon 10 fase
- **Copy All Pipelines** — semua command sekaligus
- **Filter Kategori** — saring per kategori

---

## Changelog

### v8.0
- ✅ Header desktop **2 baris** dengan brand, community, Rating, bahasa, tab dropdown, dan tombol aksi
- ✅ Menambahkan **tab dropdown desktop**; nav utama tetap menjadi sumber data
- ✅ Menambahkan **mobile drawer** dengan daftar tab yang dibuat otomatis
- ✅ Menghapus form input nama/email dan HackerOne Profile
- ✅ Tombol **PayPal/Bitcoin** dan **QR code donasi** ditampilkan di profil
- ✅ Menambahkan **API Key Manager** multi-provider: OpenAI, Gemini, Claude, Groq, OpenRouter, Mistral, Cohere, dan Custom
- ✅ AI API keys disimpan di localStorage dan dapat diuji/dihapus
- ✅ Menambahkan **validasi input** + notifikasi error di semua form
- ✅ Menambahkan **safeFetch()** untuk error handling HTTP
- ✅ Menambahkan **global error handler**
- ✅ Menambahkan **highlightError()** (border merah 3 detik)
- ✅ Update **tab Panduan** dengan dokumentasi UI baru
- ✅ Tambah **changelog v8.0** di tab Panduan

---

## Legal Notice

> ⚠️ **Gunakan hanya untuk target yang kamu punya izin:**
> - Scope program bug bounty
> - Lab sendiri
> - Domain milikmu
>
> Segala penyalahgunaan adalah **tanggung jawab pengguna sepenuhnya**.

---

## Lisensi

MIT License — bebas dipakai, dimodifikasi, dan didistribusikan.

---

## Kontribusi

Pull request & issue welcome! Buat:
- 🐛 Bug report
- 💡 Feature request
- 📝 Dokumentasi
- 🌐 Terjemahan

---

## Kontak

- 🐙 GitHub: [github.com](https://github.com)
- 🐦 Twitter/X: [x.com](https://x.com)
- 💬 Discord: [discord.com](https://discord.com)

---

**Dibuat dengan ❤️ untuk komunitas bug bounty Indonesia.**

*Weekend update — atau saat ada waktu luang.*
