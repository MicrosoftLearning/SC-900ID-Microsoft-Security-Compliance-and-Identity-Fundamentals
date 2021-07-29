﻿---
lab:
    title: 'Mempelajari Microsoft Cloud App Security'
    module: 'Modul 3 Pelajaran 4: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan perlindungan terhadap ancaman dengan Pertahanan Microsoft 365'
---


# Lab: Mempelajari Microsoft Cloud App Security

## Skenario lab
Di lab ini, Anda akan mempelajari kemampuan Microsoft Cloud App Security.  Anda akan mempelajari informasi yang tersedia di dasbor Cloud Discovery serta kemampuan yang tersedia untuk menyelidiki temuan dan mengontrol dampak terhadap organisasi Anda melalui kebijakan.  Catatan:  Organisasi harus memiliki lisensi untuk menggunakan Microsoft Cloud App Security yang merupakan layanan berlangganan berbasis pengguna. 

**Perkiraan Waktu**: 15-20 menit

#### Tugas 1: Mempelajari Cloud Discovery.

1.	Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Anda akan diarahkan ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri di pusat admin Microsoft 365, pilih **Show all**.

1. Di bawah Pusat admin, pilih **Security**.  Halaman browser baru terbuka ke halaman selamat datang di portal Pertahanan Microsoft 365.  

1. Dari bagian bawah panel navigasi kiri halaman Pertahanan Microsoft 365, pilih **More resources**.

1. Di kartu **Microsoft Cloud App Security**, plih **Open**.  Halaman browser baru terbuka ke Dasbor Cloud App Security.  Perhatikan kartu informasi yang tersedia.  Anda mungkin tidak melihat informasi apa pun pada kartu, karena lingkungan penyewa lab ini telah dikonfigurasi sebelumnya serta belum digunakan secara aktif.  

1. Dari panel navigasi sebelah kiri, pilih **Discover**, lalu dari menu tarik-turun, pilih **Cloud Discovery dashboard**.  Dasbor mencakup dan menampilkan ringkasan aplikasi yang ditemukan, kategori aplikasi, tingkat risiko, dan banyak lagi.  
    1. Dari bagian atas halaman Cloud Discovery, pilih tab **Discovered apps**.  Jendela aplikasi yang ditemukan memberikan tampilan yang lebih mendetail tentang aplikasi yang ditemukan, termasuk skor risiko, lalu lintas, jumlah pengguna, dan lainnya.
        1. Dari semua item dalam daftar, pilih **ellipses** di kolom tindakan tabel.  Perhatikan berbagai opsi yang tersedia, termasuk kemampuan untuk menandai aplikasi sebagai disetujui atau tidak.  Pilih elipsis sekali lagi, untuk menutup kotak tindakan.
        1. Memilih item baris tertentu akan membuka halaman detail untuk aplikasi tertentu.  Pilih item dari daftar.  Untuk item yang dipilih, buka setiap tab di bagian atas halaman detail:  **Usage**, **Info, IP**, **Addresses**, **Users**, dan **Alerts**. Setelah selesai menjelajahi halaman detail, kembali ke aplikasi yang ditemukan, dengan memilih **Discovered apps** dari panel navigasi sebelah kiri.
    1. Dari bagian atas halaman, pilih tab **IP addresses** (serupa dengan memilih alamat IP dari panel navigasi sebelah kiri).  Di sini, Anda akan menemukan data termasuk jumlah transaksi, jumlah lalu lintas, dan jumlah unggahan berdasarkan alamat IP.  Perhatikan bahwa Anda juga dapat memfilter menurut alamat IP tertentu atau mengekspor data untuk analisis lebih lanjut.
    1. Dari bagian atas halaman (atau panel navigasi sebelah kiri), pilih **Users**.  Ini adalah jenis informasi yang sama yang diberikan saat Anda memilih alamat IP, tetapi ini terdaftar untuk pengguna individu.  Di sini, sekali lagi, Anda memfilter menurut pengguna tertentu dan mengekspor data untuk analisis lebih lanjut.

1. Informasi yang diberikan di tab ini didasarkan pada laporan cuplikan dari log lalu lintas yang Anda unggah secara manual dari firewall dan proksi atau dari laporan berkelanjutan yang menganalisis semua log yang diteruskan dari jaringan Anda menggunakan Cloud App Security.  Untuk melihat tempat informasi ini diatur, pilih **ellipses** di pojok kanan atas halaman.
    1. Pilih opsi pertama, **Create Cloud Discovery snapshot report**. Di sini, Anda akan mengisi detail yang diminta dan mengunggah log lalu lintas untuk menghasilkan dan mengunggah laporan.  Pilih **Cancel**.  Data yang Anda lihat untuk penyewa lab berasal dari Laporan cuplikan, Anda dapat melihat informasi ini di sudut kanan atas layar.
    1. Untuk melihat opsi laporan berkelanjutan, pilih **ellipses** di sudut kanan atas halaman dan dari menu tarik-turun pilih **Configure automatic upload**.  Tidak ada sumber data yang terhubung, tetapi di sinilah Anda akan menambahkan sumber data. Pilih panah menu tarik-turun, **Select Appliance** untuk melihat jenis peralatan yang dapat Anda hubungkan sebagai sumber data.  Pilih **Cancel** untuk keluar.

1. Poin lain yang perlu diperhatikan adalah Anda dapat terhubung ke aplikasi secara langsung dengan menyiapkan konektor aplikasi yang akan memberi Anda visibilitas dan kontrol yang lebih besar atas aplikasi cloud Anda. Dari sudut kiri atas layar, pilih **Settings cog icon** dan dari daftar tarik-turun, pilih **App connectors**.  
    1. Pada halaman Aplikasi yang terhubung, Anda akan melihat Office 365 pada daftar dengan status terhubung.  Jika Office 365 menunjukkan kesalahan koneksi, kemungkinan besar karena Audit tidak diaktifkan.
    1. Pilih **+Connect an app** dan dari daftar tarik-turun pilih **Microsoft Azure**.  Dari jendela pop-up Microsoft Azure, pilih **Connect Microsoft Azure**.  Anda akan melihat status terhubung dan informasi terkait pemindaian, data, dan aktivitas pengguna.  Pilih **tutup Close**.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

#### Tugas 2: Menjelajahi cara-cara untuk menyelidiki aktivitas yang direkam.

1. Dari panel navigasi sebelah kiri, di bagian Selidiki, pilih **Activity Log**.  Di sini, Anda mendapatkan visibilitas ke semua aktivitas dari aplikasi yang terhubung.   Karena konektor Office 365 sudah terhubung, Anda seharusnya dapat melihat beberapa data. Setelah menghubungkan Cloud App Security ke aplikasi menggunakan konektor Aplikasi, Cloud App Security akan memindai semua aktivitas yang terjadi - periode waktu pemindaian retroaktif berbeda per aplikasi - dan kemudian diperbarui terus-menerus dengan aktivitas baru.  

1. Pilih item untuk menampilkan informasi selengkapnya. Perhatikan di bagian atas halaman, terdapat opsi untuk menambahkan kebijakan baru dari pencarian atau mengekspor data untuk analisis lebih lanjut.  Pilih **+New policy from search**.  Perhatikan bagaimana Anda dapat membuat kebijakan berdasarkan templat, memilih tingkat keparahan & kategori kebijakan, membuat filter untuk kebijakan, membuat peringatan, dan bahkan mengirim peringatan ke Power Automate.  Pilih **Cancel** untuk keluar dari jendela pembuatan kebijakan.

1. Dari panel navigasi kiri, pilih dan jelajahi opsi **Files**, serta perhatikan opsi untuk memfilter data, membuat kebijakan file, dan mengekspor data.  Pilih dan jelajahi opsi **user and accounts**.  Perhatikan opsi memfilter data dan mengekspor data.

1. Dari panel navigasi kiri, pilih Konfigurasi keamanan. Halaman ini memberi Anda penilaian konfigurasi keamanan untuk akun Azure, Amazon Web Services (AWS), dan Google Cloud Platform (GCP) Anda.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.


#### Tugas 3: Dalam tugas ini, Anda akan menjelajahi halaman kebijakan dan peringatan di keamanan aplikasi Microsoft Cloud.

1. Dari panel navigasi sebelah kiri, di bawah teks Kontrol, pilih **Policies**.  Kebijakan yang tercantum memberikan informasi tentang jumlah peringatan yang dihasilkan oleh kebijakan, tingkat keparahan, dll. Memilih item baris mana pun memberikan informasi selengkapnya tentang kebijakan tersebut. Pilih item dari daftar, mis., **Risky sign-in**.  

1. Dari panel navigasi sebelah kiri, pilih **Alerts**.  Jika Anda memiliki peringatan yang terdaftar, pilih item dari daftar peringatan. Tinjau informasi yang diberikan.  Dari sisi kanan atas jendela, pilih **Close alert**, guna melihat opsi untuk menutup peringatan.  

1. Tutup jendela browser.

#### Tinjauan
Di lab ini, Anda telah mempelajari kemampuan Microsoft Cloud App Security.  Anda telah mempelajari informasi yang tersedia di dasbor Cloud Discovery dan kemampuan yang tersedia serta menyelidiki temuan dan mengontrol dampaknya terhadap organisasi Anda melalui kebijakan.