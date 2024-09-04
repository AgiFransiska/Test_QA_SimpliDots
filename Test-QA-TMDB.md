# Test Case Documentation

## Project: [The Movie Database]
## Date: [03 September 2024 - 05 September 2024]
## Author: [Agi Fransiska]

---

## Table of Contents
1. [Introduction](#introduction)
2. [Test Scope](#test-scope)
3. [Test Environment](#test-environment)
4. [Test Cases](#test-cases)
5. [Test Execution](#test-execution)
6. [Test Summary](#test-summary)
7. [References](#references)

---

## Introduction
Tujuan dari testing ini adalah untuk melihat function "mark as favorite" pada website (The Movie Database) sudah berfungsi dengan semestinya dan sesuai dengan requirement yang dibuat. Beberapa fungsi wajib yang akan diujiakan adalah:
- Ubah bahasa menjadi bahasa indonesia
- User hanya bisa melakukan ”mark as favorite” ketika dia sudah login
- Ketika user melakukan “mark as favorite” dari suatu film, maka film tersebut akan tersimpan di bagian favorite movies di profil pengguna
- User bisa memfavorite lebih dari 1 movie dan validasi hasilnya
- User bisa meremove movie dari daftar favorite movies di favorite list
- User bisa mengurutkan / ordering daftar favorite movies dia
- Ubah kembali ke bahasa Inggris lalu lakukan regresi test kembali



---

## Test Scope
- **Functionalities to be tested:**  
  Fitur utama yang akan diujikan adalah fitur "Mark as favorite", dan ada beberapa fitur lainnya seperti mengubah ke bahasa indonesia dan yang berkaitan dengan fitur tersebut.
  
- **Out of Scope:**  
  Fungsi yang tidak disebutkan dan tidak berkaitan dengan futur utama pengujian yaitu "Mark as favorite"

---

## Test Environment
- **Operating System:**  
  OS yang saya gunakan untuk melakukan pengujian adalah "Windows"
  
- **Browsers:**  
  Browser yang saya gunakan untuk melakukan pengujian adalah "Google Chrome"
  
---

## Test Case: Change Language to Bahasa Indonesia

| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC001        | Verifikasi bahwa pengguna dapat mengubah bahasa ke Bahasa Indonesia    | Pengguna sudah login (opsional) | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari menu pemilihan bahasa dan klik (terletak di navbar antara icon "+" dan "masuk"). <br> 3. Klik pada menu pemilihan bahasa <br> 4. Pilih "Bahasa Indonesia" dari daftar bahasa yang tersedia | Bahasa website berubah menjadi Bahasa Indonesia. Semua label, menu, dan konten kini harus ditampilkan dalam Bahasa Indonesia. | Pass | [Catatan tambahan] |
| TC002        | Memastikan bahasa tetap tersetting pada bahasa indonesia setelah di refresh  | Bahasa tetap tersetting ke bahasa Indonesia | 1. Refresh halaman website <br> 2. Arahkan ke untuk membuka berbagai bagian situs web (misalnya, Beranda, Film, Acara TV) | [Hasil yang diharapkan] | Pass | [Catatan tambahan] |
| TC003        | Verifikasi bahwa perubahan bahasa tidak memengaruhi pengaturan akun pengguna  | Pengguna sudah login dan bahasanya diatur ke Bahasa Indonesia | 1. Pergi kehalaman setting account pada website <br> 2. Periksa detail akun | [Hasil yang diharapkan] | Pass | [Catatan tambahan] |
| TC004        | Verifikasi bahwa bahasa kembali ke default (Bahasa Inggris) saat diubah kembali  | Bahasa disetel ke Bahasa Indonesia | 1. Buka menu pemilihan bahasa <br> 2. Ubah bahasa kembali ke "Bahasa Inggris" | [Hasil yang diharapkan] | Pass | [Catatan tambahan] |


- **Test Data:**  
  User Data
  - Email: user@example.com
  - Password: password123
  Valid Language Options
  - Indonesia
  - English

- **Execution Date:**  
  03 September 2024 sampai 05 September 2024
  
- **Tested By:**  
  Agi Fransiska

  **Tujuan Test Case**
  - Memastikan bahwa pengaturan bahasa pada website TMDb berfungsi dengan baik.
  - Memvalidasi bahwa perubahan bahasa akan bertahan di seluruh halaman situs, meskipun halaman di-refresh atau user berpindah halaman.
  - Mengonfirmasi bahwa perubahan bahasa tidak mempengaruhi informasi penting lainnya seperti pengaturan akun.

- **Overall Status:**  
  Untuk hasil dari ke 4 test case yang diujikan, semua test case berjalan dengan baik dan memberikan output sesuai dengan expected result.

  ---

  ## Test Case: Mark as Favorite

| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC001        | Verifikasi bahwa tombol "Mark as Favorite" tidak dapat diklik atau nonaktif saat pengguna tidak login | Pengguna tidak atau belum login | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari film (misalnya, "Inception"). <br> 3. Coba tandai film tersebut sebagai favorit | Tombol "Tandai sebagai Favorit" seharusnya meminta pengguna untuk masuk atau dinonaktifkan, mencegah pengguna menambahkan film ke favorit. | Pass | [Catatan tambahan] |
| TC002        | Verifikasi bahwa pengguna dapat menandai film sebagai favorit setelah masuk | Pengguna berhasil dan sudah login | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari film (misalnya, "Inception"). <br> 3. Coba tandai film tersebut sebagai favorit | Film tersebut akan berhasil ditambahkan ke daftar favorit pengguna dan tombolnya akan berubah untuk menunjukkan bahwa film tersebut telah ditandai sebagai favorit. | Pass | [Catatan tambahan] |
| TC003        | Verifikasi bahwa film yang ditandai sebagai favorit muncul di daftar film favorit pengguna | Pengguna telah menandai film sebagai favorit | 1. Buka halaman profil pengguna <br> 2. Navigasi ke bagian "Favorit". <br> 3. Verifikasi bahwa film yang ditandai muncul di daftar favorit Film yang ditandai sebagai favorit akan muncul di daftar favorit pengguna. | Film yang ditandai sebagai favorit akan muncul dalam daftar favorit pengguna. | Pass | [Catatan tambahan] |

- **Test Data:**  
  1. User Data
  - Email: user@example.com
  - Password: password123
  2. Valid Language Options**
  - Indonesia
  - English

- **Execution Date:**  
  03 September 2024 sampai 05 September 2024
  
- **Tested By:**  
  Agi Fransiska

  **Tujuan Test Case**
  - Memastikan bahwa pengaturan bahasa pada website TMDb berfungsi dengan baik.
  - Memvalidasi bahwa perubahan bahasa akan bertahan di seluruh halaman situs, meskipun halaman di-refresh atau user berpindah halaman.
  - Mengonfirmasi bahwa perubahan bahasa tidak mempengaruhi informasi penting lainnya seperti pengaturan akun.

- **Overall Status:**  
  Untuk hasil dari ke 4 test case yang diujikan, semua test case berjalan dengan baik dan memberikan output sesuai dengan expected result.

---

## Test Summary
Deskripsi singkat mengenai hasil testing, termasuk jumlah test case yang berhasil, gagal, dan catatan penting lainnya.

---

## References
- [Dokumen referensi 1](#)
- [Dokumen referensi 2](#)
