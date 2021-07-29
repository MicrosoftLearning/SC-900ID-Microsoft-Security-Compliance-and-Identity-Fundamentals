---
lab:
    title: 'Menjelajahi Azure Security Center'
    module: 'Modul 3 Pelajaran 2: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan manajemen keamanan Azure'
---


# Lab: Menjelajahi Azure Security Center 

## Skenario lab
Di lab ini, Anda akan menjelajahi Azure Security Center dan mempelajari cara Skor Aman Azure dapat digunakan untuk meningkatkan kondisi keamanan organsisasi Anda.

  

**Perkiraan Waktu**: 10-15 menit

#### Tugas 1: Dalam tugas ini, Anda akan mengenal secara singkat mengenai Azure Security Center.
1.	Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Pada pojok kiri atas layar, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger), lalu klik **All Services**.  
1. Di kotak layanan filter, masukkan **Security Center**, lalu dari daftar pertama, pilih **Security Center**.
1. Perhatikan informasi yang tersedia pada halaman gambaran umum Pusat keamanan.  
1. Anda mungkin melihat kotak informasi warna biru pada bagian atas halaman yang menunjukkan bahwa Anda mungkin sedang melihat informasi yang dirahasiakan.  Klik **click here**.
    1. Untuk memastikan bahwa Anda mendapatkan visibilitas yang luas tentang penyewa, tetapkan diri Anda sebagai pemegang peran penting.  Pilih **Security Admin** lalu pilih **Get access** di bagian bawah halaman.
   
     1. Anda mungkin akan melihat pesan berikut: Grup manajemen akar tidak ada.  Sesuai deskripsi, sistem akan membuat grup untuk Anda.  Perlu waktu 15 menit untuk selesai (tetapi biasanya lebih cepat), setelah Anda dapat mengulang proses untuk mendapatkan akses.  Setelah mendapat akses, klik **Security Center** di ujung kiri atas halaman, di atas yang bertuliskan Dapatkan izin, lalu segarkan halaman gambaran umum Pusat keamanan.
1. Informasi di bagian atas halaman mencatumkan jumlah langganan Azure, jumlah Sumber daya yang dinilai, jumlah rekomendasi yang aktif, serta peringatan keamanan.  Di bagian isi halaman ada kartu yang mewakili Skor aman, Kepatuhan terhadap peraturan, Wawasan, Azure Defender, dan banyak lainnya.  
1. Dari bagian atas halaman, pilih **Assessed resources**.  Upaya ini akan membawa Anda ke halaman inventaris yang menunjukkan Anda langganan kartu Azure.  Pilih **Azure Pass – Sponsorship**.
1. Halaman Kesehatan sumber daya menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih **There should be more than one owner assigned to your subscription**. 
1. Pilih panah tarik-turun di samping Langkah-langkah perbaikan. Perhatikan bagaimana langkah-langkah perbaikan rinci disediakan bersama dengan opsi mengambil tindakan.  
1. Pilih **Security Center** dari sudut kiri atas layar untuk kembali ke halaman ikhtisar Pusat Keamanan.
1. Dari bagian atas halaman, pilih **Active recommendations**.  
1. Halaman rekomendasi menunjukkan tindakan khusus yang dapat diambil pada potensi peningkatan skor aman.  Keluar dari halaman rekomendasi dengan mengklik **X** di ujung kanan atas layar.
1. Dari halaman utama, pilih **Regulatory compliance**.
1. Halaman kepatuhan terhadap peraturan menyediakan daftar kontrol kepatuhan.  Pada tiap kontrol adalah seperangkat penilaian yang didasarkan pada Tolok Ukur Keamanan Azure yang menyediakan rekomendasi tentang cara Anda dapat mengamankan solusi cloud Anda di Azure.
1. Klik **IM. Identity Management**, kemudian pilih **IM.4 Use strong authentication controls for all Azure Active Directory based access**.  Daftar ini menunjukkan tindakan tanggung jawab pelanggan yang dapat diambil untuk meningkatkan kondisi keamanan organisasi Anda.
1. Klik **X** di ujung kanan atas layar untuk menutup halaman dan kembali ke halaman Gambaran Umum Pusat Keamanan. 
1. Biarkan halaman gambaran umum Pusat keamanan terbuka, Anda akan menggunakannya di tugas berikutnya.


#### Tugas 2: Dalam tugas ini, Anda akan melewati Skor Aman Azure dan menjelajahi rekomendasi yang dapat meningkatkan skor keamanan Anda. 

1. Dari halaman gambaran umum Pusat keamanan, klik kartu **Secure Score**.

2. Pilih **Azure Pass – Sponsorship**.  Catat skor aman Anda.
3. Di halaman rekomendasi, klik **Manage access and permissions**. Perhatikan bahwa ada satu item di grup itu yang berwarna merah.
4. Klik item **There should be more than one owner assigned to your subscription**, yang menunjukkan status kesehatan sumber daya berwarna merah. Jika memilih item ini tidak berfungsi.
    1. Dari pojok kiri atas halaman, klik **Security Center**, di atas yang bertuliskan Rekomendasi.
    
    1. Di panel navigasi sebelah kiri, klik **Recommendations**.
    1. Di halaman rekomendasi, klik **Manage access and permissions**. Perhatikan bahwa ada satu item di grup itu yang berwarna merah.
    1. Klik item **There should be more than one owner assigned to your subscription**, yang menunjukkan status kesehatan sumber daya berwarna merah. 
5. Klik **Azure subscription**.
6. Di bagian atas halaman Kontrol akses (IAM), klik **+ Add**, lalu dari menu tarik-turun klik **Add role assignment**.
7. Di Bidang peran, klik **Owner**, lalu klik **Owner** pada daftar di bawah.
8. Di daftar pengguna, klik **Alex Wilber**, lalu klik **Save** di bagian bawah halaman.
9. Perlu waktu hingga 24 jam agar status diperbarui, dan setelah skor keamanan Anda juga diperbarui serta semua item di Kelola grup izin dan akses dipenuhi.
10. Di pojok kiri atas halaman, di atas yang bertuliskan Azure Pass, klik **Security Center**, lalu klik **Overview** untuk kembali ke halaman gambaran umum pusat keamanan.
11. Biarkan halaman ini terbuka untuk tugas berikutnya.


#### Tugas 3:  Ingat bahwa Pusat keamanan ditawarkan dalam dua mode: Azure Defender NONAKTIF (gratis) dan Azure Defender AKTIF. Dalam tugas ini, Anda menemukan cara mengaktifkan dan menonaktifkan Azure Defender.

1.	Di halaman gambaran umum Pusat keamanan, klik **Enable Azure Defender** dari kartu Azure Defender.

2.	Klik kotak **Azure Defender on**.  Perhatikan bahwa semua status perubahan paket defender Menyala dan perhatikan harga untuk tiap item, lalu klik **Save** di pojok atas kiri halaman.
3.	Kembali ke halaman Pusat keamanan, dengan memilih **Security Center** di pojok kiri atas halaman.   Perlu waktu beberapa menit agar kartu Azure Defender melakukan perubahan.  Segarkan halaman, jika perlu.
4.	Untuk menonaktifkan Azure Defender, klik **Pricing & settings** di panel navigasi kiri halaman pusat keamanan, klik **AAzure Pass – Sponsorship subscription**.
5.	Di halaman paket Azure Defender, klik kotak **Azure Defender off**, lalu klik **Save** di halaman pojok kiri atas halaman.
6.	Sebuah jendela akan muncul meminta konfirmasi penurunan peringkat.  Hapus centang kotak Microsoft untuk menghubungi Anda dan klik **Confirm**.
7.	Sekarang Anda dapat menghapus tab browser untuk keluar portal Azure.


#### Tinjauan
Dalam lab ini, Anda sudah menjelajahi Azure Security Center dan mempelajari bagaimana Skor Aman Azure dapat digunakan untuk meningkatkan kondisi keamanan organsisasi Anda.
