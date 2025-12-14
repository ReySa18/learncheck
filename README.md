# 🎓 LearnCheck

> **AI-Powered Formative Assessment for Smarter Learning**

<div align="center">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Web%20App-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI-Generative%20AI-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Integration-iFrame-yellow?style=for-the-badge" />
</div>

---

## 📌 Deskripsi Proyek

**LearnCheck** adalah aplikasi web berbasis AI yang dirancang untuk mendukung *formative assessment* dalam pembelajaran digital. Aplikasi ini menghasilkan soal dan umpan balik secara otomatis dari materi pembelajaran, sehingga siswa dapat mengecek pemahaman secara mandiri dan real-time.
LearnCheck dapat di-*embed* ke dalam platform pembelajaran atau LMS menggunakan **iframe**, sehingga terintegrasi secara seamless tanpa mengganggu sistem utama.

---

## 🛠️ Fitur Utama

* **Generate Soal Otomatis**
  Soal dihasilkan langsung dari materi pembelajaran menggunakan AI.

* **Feedback Instan Berbasis AI**
  Umpan balik diberikan secara otomatis berdasarkan jawaban pengguna.

* **Dukungan Multiple Choice & Multiple Answer**
  Mendukung variasi tipe soal untuk evaluasi yang lebih fleksibel.

* **Integrasi via iFrame**
  LearnCheck dapat digunakan langsung di LMS atau website lain tanpa berpindah halaman.

* **Penyimpanan Progress Lokal**
  Progress pengerjaan disimpan menggunakan *local storage* di browser.

* **Fallback Model AI**
  Sistem secara otomatis menggunakan model AI cadangan ketika model utama mencapai batas limit.

---

## 🎯 Visi & Dampak

### Visi

Meningkatkan efektivitas pembelajaran digital melalui *formative assessment* yang cerdas, cepat, dan terintegrasi.

### Dampak

* **Bagi Siswa**: Membantu memahami materi sebelum melanjutkan ke topik berikutnya.
* **Bagi Instruktur**: Mengurangi beban pembuatan soal dan evaluasi manual.
* **Bagi Platform Pembelajaran**: Menambah fitur evaluasi berbasis AI tanpa kompleksitas integrasi.

---

## 🔄 Cara Kerja Sistem

1. LearnCheck di-*embed* ke platform pembelajaran menggunakan **iframe**
2. Frontend menerima `userId` dan `tutorialId`
3. Backend mengambil materi dari platform induk
4. AI melakukan *summary* materi untuk efisiensi token
5. Sistem menghasilkan soal berdasarkan hasil *summary*
6. Pengguna menjawab soal
7. AI menghasilkan feedback
8. Hasil ditampilkan secara real-time di frontend

---

## 🧠 Dokumentasi AI & Prompt Engineering

### Pendekatan AI

* *Chunking* materi pembelajaran
* *Summarization* untuk menghemat token
* Prompt terpisah untuk:

  * Generate soal
  * Generate feedback

### Optimasi & Keandalan

* Pengendalian penggunaan token
* Penanganan latency
* Fallback ke model AI sekunder
* Validasi output agar sesuai konteks materi

---

## 🖥️ Frontend Overview

* Dibangun sebagai **web app yang di-embed via iframe**
* Fokus pada UI/UX sederhana dan intuitif
* Menampilkan soal, navigasi, dan feedback secara bertahap
* Mengelola state soal, jawaban, dan hasil evaluasi

---

## ⚙️ Backend Overview

* Menyediakan REST API untuk frontend
* Endpoint utama:

  * `/generate` → menghasilkan soal
  * `/submit` → menghasilkan feedback
* Validasi input pengguna
* Logging proses AI
* Pengelolaan error dan fallback model

---

## 💻 Tech Stack

<div align="center">

### Frontend
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=for-the-badge" />
<img src="https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black&style=for-the-badge" />
<img src="https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/TailwindCSS-38B2AC?logo=tailwindcss&logoColor=white&style=for-the-badge" />

<br/>

### Backend
<img src="https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/Express.js-000000?logo=express&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/REST%20API-005571?style=for-the-badge" />

<br/>

### AI & LLM
<img src="https://img.shields.io/badge/Generative%20AI-FF6F00?style=for-the-badge" />
<img src="https://img.shields.io/badge/Prompt%20Engineering-8A2BE2?style=for-the-badge" />
<img src="https://img.shields.io/badge/Fallback%20Model-FF4500?style=for-the-badge" />

<br/>

### Tools & Deployment
<img src="https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/Railway-0B0D0E?logo=railway&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/Postman-FF6C37?logo=postman&logoColor=white&style=for-the-badge" />

</div>

---

## 🎨 Design & Prototype

Desain antarmuka **LearnCheck** dirancang dengan fokus pada kemudahan penggunaan (*usability*) dan pengalaman belajar yang sederhana serta intuitif. Seluruh proses perancangan dilakukan menggunakan **Figma** untuk memastikan konsistensi desain antara kebutuhan pengguna, frontend, dan sistem secara keseluruhan.

🔗 **Figma Design & Prototype:**  
👉 [Klik di sini untuk melihat desain dan prototype LearnCheck](https://www.figma.com/design/tCBAiz3Gp1QKTq0b0keLGx/Design-Project?node-id=0-1&p=f&t=fUmiSsWM8ew7IUte-0)
)

---

## 📁 Struktur Repository (Monorepo)

```text
learncheck/
├── frontend/
│   └── source code frontend LearnCheck
├── backend/
│   └── source code backend & AI service
└── README.md
```

---

## 🚀 Cara Menjalankan Proyek (Local)

Ikuti langkah-langkah berikut untuk menjalankan aplikasi **LearnCheck** di lingkungan lokal.

---

### 1️⃣ Prasyarat

Pastikan perangkat Anda telah terpasang:
- **Node.js** (disarankan versi LTS)
- **npm**
- **Git**
- Code Editor (disarankan **Visual Studio Code**)
- Browser (Chrome / Edge / Firefox)

---

### 2️⃣ Clone Repository

```bash
git clone https://github.com/USERNAME/learncheck.git
cd learncheck
````

---

### 3️⃣ Setup Backend

#### a. Masuk ke folder backend

```bash
cd backend
```

#### b. Install dependency backend

```bash
npm install
```

#### c. Konfigurasi Environment Variable

Salin file `.env.example` menjadi `.env`:

```bash
cp .env.example .env
```

> **Catatan:**
> Sesuaikan nilai variabel di dalam file `.env` (seperti API key AI, base URL, dan konfigurasi lainnya) sesuai dengan environment yang digunakan.

#### d. Jalankan backend

```bash
npm run start
```

Backend akan berjalan secara default di port yang telah ditentukan pada konfigurasi.

---

### 4️⃣ Setup Frontend

#### a. Buka terminal baru dan masuk ke folder frontend

```bash
cd frontend
```

#### b. Install dependency frontend

```bash
npm install
```

#### c. Konfigurasi Environment Variable

Salin file `.env.example` menjadi `.env`:

```bash
cp .env.example .env
```

Contoh konfigurasi:

```env
VITE_BASE_URL=http://localhost:3000
```

Sesuaikan `VITE_BASE_URL` dengan alamat backend Anda.

#### d. Jalankan frontend

```bash
npm run dev
```

Frontend akan berjalan secara default di:

```
http://localhost:5173
```

---

### 5️⃣ Integrasi Menggunakan iFrame

LearnCheck dirancang untuk digunakan sebagai aplikasi ter-*embed*.

Contoh penggunaan iframe:

```html
<iframe
  src="http://localhost:5173?userId=1&tutorialId=123"
  width="100%"
  height="700"
  frameborder="0">
</iframe>
```

Parameter `userId` dan `tutorialId` digunakan untuk:

* Identifikasi pengguna
* Pengambilan materi pembelajaran

---

### 6️⃣ Aplikasi Siap Digunakan 🎉

* Frontend: berjalan di browser
* Backend: melayani API dan proses AI
* AI: menghasilkan soal dan feedback secara otomatis

---

### ⚠️ Catatan Tambahan

* Pastikan backend **berjalan lebih dulu** sebelum frontend
* Gunakan API key AI yang valid
* Untuk production, deployment dilakukan terpisah (frontend di **Vercel**, backend di **Railway**)

---

## 🎬 Demo 

Berikut adalah dokumentasi pendukung dari proyek **LearnCheck**:

### 🎥 Video Demonstrasi (YouTube)
👉 [Tonton Video Demo LearnCheck](https://youtu.be/asHTLhFTamo)

---

## 👥 Tim Pengembang

**Capstone Project – LearnCheck**

| Nama                          | Student ID    | Learning Path                  | GitHub |
|-------------------------------|---------------|--------------------------------|--------|
| Reymondo Saputra Simbolon     | R891D5Y1688   | React & Backend with AI        | [GitHub](https://github.com/ReySa18) |
| Enrique G B D                 | R891D5Y0534   | React & Backend with AI        | [GitHub](https://github.com/enriquegiovanni) |
| Faris Maulana Saputra         | R891D5Y0603   | React & Backend with AI        | [GitHub](https://github.com/farismns) |
| Muhammad Daffa Umam           | R891D5Y1234   | React & Backend with AI        | [GitHub](https://github.com/DaffaU) |
| Hafidz Ramadhan Ghiffari      | R318D5Y0713   | React & Backend with AI        | [GitHub](https://github.com/ramadhafidz) |

---

## 🙏 Ucapan Terima Kasih

Terima kasih kepada:

* Advisor dan mentor capstone
* Tim pengembang LearnCheck
* Penguji dan reviewer proyek

---

## 🌐 Live Website

Aplikasi **LearnCheck** dapat diakses melalui tautan berikut:

<div align="center">
  <a href="https://learncheck-fe.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/🚀%20Open%20LearnCheck%20Web-Visit%20Now-success?style=for-the-badge" />
  </a>
</div>

---
