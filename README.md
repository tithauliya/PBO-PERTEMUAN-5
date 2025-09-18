# Implementasi Database PostgreSQL pada Toko Roti dengan Java NetBeans  

Dosen Pengampu : Bayu Adhi Nugroho, Ph.D.  

## Identitas  
- **Nama** : Titha Auliya Khotim  
- **NIM** : 09010624017  
- **Kelas** : H7B.3  
- **Program Studi** : Sistem Informasi  
- **Fakultas** : Sains dan Teknologi  
- **Universitas** : UIN Sunan Ampel Surabaya  
- **Tahun** : 2025  

Pada praktikum ini dipelajari cara menghubungkan **PostgreSQL** dengan **Java NetBeans** dan mengembangkan sistem sederhana untuk **Toko Roti**.  
Fokus utamanya adalah membuat **antarmuka grafis (Java GUI)** yang dapat melakukan operasi **CRUD** (Create, Read, Update, Delete) terhadap data roti.  

Dengan adanya GUI, pengguna dapat:  
- Menambah data roti baru.  
- Menampilkan data dalam bentuk tabel.  
- Memperbarui informasi stok atau harga.  
- Menghapus data berdasarkan id roti.  

Selain itu, diterapkan juga **exception handling** agar sistem lebih aman dan konsisten, misalnya validasi input kosong atau pengecekan stok roti.  

## Implementasi  

### 1. Struktur Database  
Tabel utama bernama `tokoroti` dengan kolom:  
- **id_kue** → Primary Key (serial)  
- **nama_kue** → Nama roti  
- **harga** → Harga roti  
- **stok** → Jumlah stok  

### 2. Operasi CRUD  
- **Create (Tambah Data)** → menambahkan data baru dengan query `INSERT`.  
- **Read (Tampil Data)** → menampilkan seluruh data dengan query `SELECT` ke JTable.  
- **Update (Perbarui Data)** → memperbarui stok atau harga dengan query `UPDATE`.  
- **Delete (Hapus Data)** → menghapus data berdasarkan `id_kue` dengan query `DELETE`.  

### 3. Exception Handling  
- Validasi input: field tidak boleh kosong.  
- Pengecekan stok: jika stok yang diminta lebih besar dari stok tersedia, program menampilkan pesan error melalui **StokTidakCukupException**.  
