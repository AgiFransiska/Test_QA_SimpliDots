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
| TC001        | Verifikasi bahwa pengguna dapat mengubah bahasa ke Bahasa Indonesia    | Pengguna sudah login (opsional) | 1. Arahkan untuk membuka web https://www.themoviedb.org/ pada browser <br> 2. Cari menu pemilihan bahasa dan klik (terletak di navbar antara icon "+" dan "masuk"). <br> 3. Klik pada menu pemilihan bahasa <br> 4. Pilih "Bahasa Indonesia" dari daftar bahasa yang tersedia | Bahasa website berubah menjadi Bahasa Indonesia. Semua label, menu, dan konten kini harus ditampilkan dalam Bahasa Indonesia. | Pass/Fail | [Catatan tambahan] |
| TC002        | Memastikan bahasa tetap tersetting pada bahasa indonesia setelah di refresh  | Bahasa tetap tersetting ke bahasa Indonesia | 1. Refresh halaman website <br> 2. Arahkan ke untuk membuka berbagai bagian situs web (misalnya, Beranda, Film, Acara TV) | [Hasil yang diharapkan] | Pass/Fail | [Catatan tambahan] |
| ...          | ...                    | ...            | ...        | ...             | ...    | ...     |

- **Test Data:**  
  Deskripsi singkat mengenai test data yang akan digunakan.

- **Execution Date:**  
  03 September 2024 sampai 05 September 2024
  
- **Tested By:**  
  Agi Fransiska

- **Overall Status:**  
  Hasil testing secara keseluruhan (Pass/Fail).

---

## Test Summary
Deskripsi singkat mengenai hasil testing, termasuk jumlah test case yang berhasil, gagal, dan catatan penting lainnya.

---

## References
- [Dokumen referensi 1](#)
- [Dokumen referensi 2](#)
