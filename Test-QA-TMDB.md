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
5. [Test Summary](#test-summary)

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
## Test Case

**Test Case: Mengubah Bahasa Menjadi Bahasa Indonesia**

| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC001        | Verifikasi pengguna dapat mengubah bahasa ke Bahasa Indonesia. | Pengguna sudah login (opsional) | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari menu pemilihan bahasa (terletak di navbar antara icon "+" dan "masuk"). <br> 3. Klik pada menu pemilihan bahasa <br> 4. Pilih "Bahasa Indonesia" dari daftar bahasa yang tersedia | Bahasa pada website terubah menjadi Bahasa Indonesia. Semua label, menu, dan konten kini harus ditampilkan dalam Bahasa Indonesia. | Pass | Fitur ini berfungsi sesuai dengan expected result |

---

  **Test Case: Mark as Favorite Functionality**

| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC002        | Verifikasi bahwa tombol "Mark as Favorite" tidak dapat diklik atau nonaktif saat pengguna tidak login | Pengguna tidak atau belum login | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari film (misalnya, "Inside Out"). <br> 3. Coba tandai film tersebut sebagai favorit | Tombol "Tandai sebagai Favorit" seharusnya meminta pengguna untuk login dahulu atau tombolnya dinonaktifkan untuk mencegah pengguna menambahkan film ke favorit. | Pass | Fitur ini berfungsi sesuai dengan expected result |
| TC003        | Verifikasi bahwa pengguna dapat menandai film sebagai favorit setelah login. | 1. Cari film yang ingin ditembahkan sebagai favorite. <br> 2. Klik button “Tandai sebagai Favorit” | Film seharusnya berhasil ditambahkan ke daftar favorit pengguna, dan tombol akan berubah untuk menunjukkan bahwa film tersebut ditandai sebagai favorit. | Pass | Fitur ini berfungsi sesuai dengan expected result |
| TC004        | Verifikasi bahwa film yang ditandai muncul di bagian “Daftar Tontonan” pada profil pengguna | Pengguna telah menandai film sebagai favorit | 1. Buka profil dan pengaturan pengguna <br> Arahkan ke bagian “Daftar Tontonan” | Film yang ditandai akan muncul di daftar favorit pengguna. | Pass | Fitur ini berfungsi sesuai dengan expected result |
| TC005        | Verifikasi bahwa pengguna dapat menandai beberapa film sebagai favorit	 | Pengguna telah login dan telah menandai beberapa film | 1. Menandai beberapa film sebagai favorit (misalnya, “Inside Out”, “Deadpool and Wolverin”). <br> 2. Buka bagian menu "Daftar Tontonan" | Semua film yang ditandai sebagai favorit akan muncul di daftar “Daftar Tontonan”. | Pass | Fitur ini berfungsi sesuai dengan expected result |
| TC006        | Verifikasi bahwa pengguna dapat menghapus film dari daftar favorit mereka | Pengguna masuk dan memiliki film dalam daftar favorit | 1. Navigasikan ke bagian menu “Daftar Tontonan”. <br> Klik “Hapus dari Favorit” untuk film yang dipilih | Film harus dihapus dari daftar dan tombol akan kembali ke “Tandai sebagai Favorit”. | Pass | Fitur ini berfungsi sesuai dengan expected result |
| TC007        | Verifikasi pengguna dapat mengurutkan film favorit mereka dengan kriteria yang berbeda | Pengguna masuk dan memiliki beberapa film dalam daftar favorit | 1. Navigasikan ke bagian menu “Daftar Tontonan”. <br> 2. Gunakan fitur pengurutan untuk mengurutkan berdasarkan kriteria (misalnya, judul, tanggal ditambahkan, tanggal rilis) | Daftar favorit harus disusun ulang dengan benar berdasarkan kriteria yang dipilih. | Pass | Fitur ini berfungsi sesuai dengan expected result |

---

**Test Case: Mengubah Bahasa Kembali ke Bahasa Inggris**

| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC008        | Verifikasi pengguna dapat mengubah bahasa kembali ke bahasa Inggris | Bahasa diatur ke Bahasa Indonesia | 1. Cari menu pilihan bahasa. <br> 2. Pilih “Bahasa Inggris” dari daftar bahasa | Situs web mengubah bahasa kembali ke bahasa Inggris. Semua teks dan label ditampilkan dalam bahasa Inggris. | Pass | Fitur ini berfungsi sesuai dengan expected result |

---

**Test Case: Verifikasi Semua Fitur Berfungsi Setelah Mengubah Kembali ke Bahasa Inggris**

**Mark as Favorite**
| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC009        | Verifikasi pengguna masih dapat menandai film sebagai favorit setelah mengubahnya kembali ke bahasa Inggris | Bahasa diatur ke Bahasa Inggris, dan pengguna telah login | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari film (misalnya, "Inside Out"). <br> 3. Coba tandai film tersebut sebagai favorit | Film harus berhasil ditambahkan ke daftar favorit. | Pass | Fitur ini berfungsi sesuai dengan expected result |

**Remove From Favorite**
| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC0010       | Verifikasi pengguna dapat menghapus film dari favorit setelah mengubahnya kembali ke bahasa Inggris | Bahasa diatur ke Bahasa Inggris, dan sudah menambahkan beberapa film dalam daftar favorit | 1. Navigasikan ke bagian “Daftar Tontonan”. <br> 2. Klik “Hapus dari Favorit” untuk film yang dipilih | Film tersebut harus dihapus dari daftar favorit dan tombolnya harus dikembalikan ke “Tandai sebagai Favorit”. | Pass   | Fitur ini berfungsi sesuai dengan expected result |

**Sorting the list Favorite movie**
| Test Case ID | Test Case Description | Pre-conditions | Test Steps | Expected Result | Status | Remarks |
|--------------|-----------------------|----------------|------------|-----------------|--------|---------|
| TC0011       | Verifikasi pengguna masih dapat memesan film favorit mereka setelah mengubah kembali ke bahasa Inggris | Bahasa diatur ke Bahasa Inggris, dan telah menambahkan beberapa film di favorit	| 1. Navigasikan ke bagian “Daftar Tontonan”. <br> 2. Gunakan fitur pengurutan untuk mengurutkan berdasarkan kriteria yang berbeda | Daftar favorit harus disusun ulang berdasarkan kriteria yang dipilih (misalnya, tanggal ditambahkan, judul, peringkat). | Pass   | Fitur ini berfungsi sesuai dengan expected result |

---

- **Test Data:**  
  User Data
  - Email: user@example.com
  - Password: password123

  Valid Language Options
  - Indonesia
  - English

  Movie Selected
  - Inside Out 2
  - Deadpool and Wolverin


- **Execution Date:**  
  03 September 2024 sampai 05 September 2024
  
- **Tested By:**  
  Agi Fransiska

  **Tujuan Test Case**
  - Memastikan bahwa pengaturan bahasa bisa diubah dan berfungsi dengan baik, baik saat diubah ke Bahasa Indonesia maupun kembali ke Bahasa Inggris.
  - Memverifikasi bahwa fitur "Mark as Favorite" dan "Remove from Favorite" hanya berfungsi setelah pengguna login, dan tetap bekerja dengan benar setelah regresi testing.
  - Mengonfirmasi bahwa pengguna dapat memanipulasi dan mengurutkan daftar film favorit mereka.

- **Overall Status:**  
  Untuk hasil dari ke 11 test case yang diujikan adalah positif, dimana semua test case berfungsi dengan baik dan memberikan output sesuai dengan expected result.

  ---

## Test Summary
**1. Ubah Bahasa ke Bahasa Indonesia**
- Pengguna dapat mengubah bahasa situs web ke Bahasa Indonesia. Semua menu, label, dan konten ditampilkan dengan benar dalam Bahasa Indonesia.
- Hasil **Passed**

**2. Tandai sebagai Fungsionalitas Favorit (Wajib Login)**
- Sistem dengan benar meminta pengguna untuk login sebelum mengizinkan mereka menandai film sebagai favorit. Setelah masuk, pengguna berhasil menandai film sebagai favorit.
- Hasil : **Passed**

**3. Film Favorit di Profil Pengguna**
- Film yang ditandai sebagai favorit muncul di bagian “Daftar Tontonan” pengguna di halaman profil mereka. Semua film yang ditambahkan ke favorit ditampilkan dengan benar.
- Hasil : **Passed**

**4. Menandai beberapa Film sebagai Favorit dan Memvalidasi**
- Pengguna dapat menandai beberapa film sebagai favorit. Setiap film muncul di daftar “Daftar Tontonan”, dan fungsinya bekerja secara konsisten di beberapa film.
- Hasil : **Passed**

**5. Menghapus Film dari Daftar Favorit**
- Pengguna berhasil menghapus film dari daftar favorit mereka. Film dihapus seperti yang diharapkan, dan tombol “Tandai sebagai Favorit” kembali ke kondisi default.
- Hasil : **Passed**

**6. mengurutkan Film Favorit**
- Pengguna dapat mengurutkan film favorit mereka berdasarkan kriteria yang berbeda, seperti judul, tanggal ditambahkan, dan rating. Fitur pengurutan berfungsi dengan benar, dan daftar favorit diperbarui berdasarkan kriteria yang dipilih.
- Hasil : **Passed**

**7. Ubah Bahasa Kembali ke Bahasa Inggris dan Lakukan Uji Regresi**
- Setelah mengubah bahasa kembali ke bahasa Inggris, semua fungsi (Tandai sebagai Favorit, Hapus dari Favorit, dan Mengurutkan Film Favorit) terus bekerja tanpa masalah. Tidak ada bug atau masalah fungsionalitas yang ditemukan selama pengujian regresi.
- Hasil : **Passed**

**Semua kasus pengujian untuk fitur “Ubah Bahasa”, “Tandai sebagai Favorit”, “Hapus dari Favorit”, dan “Mengurutkan Film Favorit” telah berhasil dijalankan. Sistem bekerja seperti yang diharapkan, dan tidak ada cacat yang ditemukan selama fase pengujian.**

---

