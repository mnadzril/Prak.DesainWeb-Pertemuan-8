# Event Registration Form - Tugas Individu
# Muhammad Nadzril Ilham Kusuma - 4525210084

## Deskripsi
Project ini merupakan aplikasi form registrasi event berbasis website yang dibuat menggunakan murni HTML5 dan CSS3. Form ini digunakan untuk mengumpulkan data peserta yang ingin mengikuti suatu event teknologi dengan menyediakan berbagai jenis input data serta validasi bawaan (client-side) agar data yang dimasukkan sesuai dengan ketentuan.

## Teknologi yang Digunakan
*   **HTML5**: Untuk membangun struktur form, elemen input (radio, checkbox, select, file, textarea), dan menerapkan validasi bawaan client-side.
*   **CSS3**: Untuk mengatur tata letak, warna latar (tema pastel), dan desain antarmuka agar rapi dan responsif.

## Fitur Form
1.  **Input Nama Lengkap** (Teks)
2.  **Input Nomor WhatsApp** (Angka/Pola tertentu)
3.  **Select Option** untuk memilih profesi/pekerjaan peserta
4.  **Radio Button** untuk memilih jenis kehadiran (Offline/Online)
5.  **Checkbox** untuk memilih sesi workshop yang diminati (boleh lebih dari satu)
6.  **Textarea** untuk menuliskan alasan atau motivasi mengikuti event
7.  **File Upload** untuk mengunggah dokumen (CV/Resume)

## Aturan Validasi
Berikut aturan validasi yang diterapkan pada form:
1.  Nama lengkap **wajib diisi** minimal 3 karakter dan maksimal 50 karakter.
2.  Nomor WhatsApp **wajib diisi** berupa angka dengan panjang 10-13 digit.
3.  Profesi atau pekerjaan **wajib dipilih**.
4.  Jenis kehadiran **wajib dipilih** salah satu.
5.  Motivasi mengikuti event **wajib diisi** dengan panjang minimal 20 karakter dan maksimal 300 karakter.
6.  Dokumen CV/Resume **wajib diunggah** dan dibatasi hanya menerima format **PDF**.

## Struktur Folder
```
tugas
├── index.html
├── css/
│   └── style.css
└── README.md
```

## Cara Menjalankan Project
1.  Download atau *clone* repository/folder project ini.
2.  Buka folder `projek` menggunakan Code Editor (misalnya Visual Studio Code).
3.  Buka file `index.html` menggunakan browser (klik dua kali pada file atau gunakan ekstensi *Live Server*).
4.  Isi seluruh data pada form registrasi sesuai dengan ketentuan.
5.  Klik tombol **Daftar Sekarang**.
6.  Perhatikan pesan validasi *tooltips* bawaan browser yang muncul apabila terdapat input yang tidak sesuai aturan.

## Pengujian Validasi (Test Case)
Pengujian dilakukan dengan mencoba beberapa skenario input yang tidak valid/salah:

| No | Field Uji | Skenario Input Salah | Hasil yang Diharapkan (Client-Side) |
| :--- | :--- | :--- | :--- |
| 1 | Nama Lengkap | Mengisi hanya dengan 2 huruf (Contoh: "Ed") | Ditolak. Muncul pesan untuk memperpanjang teks minimal 3 karakter. |
| 2 | Nomor WhatsApp | Mengisi dengan campuran huruf ("08123ABCD") | Ditolak. Muncul pesan format tidak sesuai pola yang diminta. |
| 3 | Profesi | Dibiarkan kosong / tidak memilih opsi | Ditolak. Muncul pesan wajib memilih salah satu item di daftar. |
| 4 | Motivasi (Textarea) | Menulis alasan kurang dari 20 karakter | Ditolak. Muncul pesan untuk memperpanjang teks minimal 20 karakter. |
| 5 | Upload CV | Memilih file gambar (.jpg / .png) | *File explorer* hanya menampilkan PDF. Jika dipaksa, form tetap menolak ekstensi yang salah. |

## Validasi Client-Side dan Server-Side
Proses validasi pada project ini dilakukan di browser (**Client-Side Validation**) menggunakan atribut HTML5 murni seperti `required`, `minlength`, `maxlength`, `pattern`, dan `accept`.

**Catatan Penting:** 
Meskipun validasi client-side sudah diterapkan, **validasi Server-Side tetap wajib dilakukan**. Pengguna tingkat lanjut dapat memanipulasi kode HTML (melalui *Inspect Element*) untuk menghapus atribut validasi. Pemeriksaan di server sangat penting untuk memastikan integritas tipe file (mencegah upload *malware* berkedok PDF), ukuran file, dan mencegah serangan seperti *SQL Injection* sebelum data benar-benar disimpan ke database.

## Tampilan Aplikasi
Aplikasi dirancang dengan tampilan bersih, simpel, dan rapi menggunakan latar belakang berwarna pastel muda (`#fce4ec`) dan kotak form putih dengan bayangan (*box-shadow*) agar terlihat modern.

### Output desktop
<img width="1307" height="1281" alt="screenshoot desktop" src="https://github.com/user-attachments/assets/be0fd5f0-cd58-4975-95bf-69d19042e203" />

### Output mobile
<img width="750" height="1780" alt="screenshoot mobile" src="https://github.com/user-attachments/assets/0229de0f-7806-4679-97bc-50d42d9f646c" />


---
**Informasi Project**
*   **Nama Project:** Form Registrasi Event Tech 2026
*   **Jenis Project:** Tugas Individu (Client-Side Validation)
*   **Kategori:** Front-End Development
*   **Bahasa:** HTML, CSS
