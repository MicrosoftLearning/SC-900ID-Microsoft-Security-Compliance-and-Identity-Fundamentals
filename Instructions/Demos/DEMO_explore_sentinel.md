---
Demo:
    title: 'Azure Sentinel'
    module: 'Modul 3 Pelajaran 3: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan keamanan Azure Sentinel'
---


# Demo: Azure Sentinel 

### Skenario demo
Dalam demo ini, Anda akan menelusuri proses pembuatan instans Azure Sentinel.  Anda juga akan mengatur izin untuk memastikan akses ke sumber daya yang akan disebarkan guna mendukung Azure Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan mengikuti langkah-langkah menghubungkan Sentinel ke sumber data, menggunakan analitik bawaan untuk mendapatkan pemberitahuan tentang sesuatu yang mencurigakan, dan terakhir Anda akan menjelajahi kemampuan otomatisasi.  

#### Demo Bagian 1:  Membuat instans Azure Sentinel

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, di bilah biru bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **sentinel**, lalu pilih **Azure Sentinel** dari hasil pencarian.

1. Dari halaman Azure Sentinel, pilih **Create Azure Sentinel**.

1. Dari halaman Tambahkan Sentinel Azure ke halaman ruang kerja, pilih **Create a new workspace**.

1. Dari tab dasar-dasar ruang kerja Buat Analisis Log, masukkan berikut ini:
    1. Langganan:  **Azure Pass – Sponsorship**
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:: **East US** (biarkan default)
    1. Pilih **Next: Tingkat harga >**

1. Untuk Tingkat Harga, biarkan pengaturan default: **Pay-as-you-go (per GB 2018)**, lalu pilih **Next: Tag >**.

1. Untuk Tag, Anda dapat mengosongkannya, lalu pilih **Review + Create**.

1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.

1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, halaman berita & panduan | Azure Sentinel akan ditampilkan.  Perhatikan tiga langkah yang tercantum di halaman Mulai.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

#### Demo Bagian 2:  Dengan instans Azure Sentinel yang dibuat, Anda harus memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebarkan untuk mendukung Azure Sentinel.  Dalam tugas ini, Anda akan masuk ke halaman kontrol akses (IAM) untuk grup sumber daya yang Anda buat dengan instans Azure Sentinel, melihat peran yang tersedia, dan menetapkan diri Anda sendiri (administrator MOD) peran yang diperlukan. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Azure Sentinel.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **resource groups**, lalu pilih **Resource groups** dari hasil pencarian.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Azure Sentinel, **SC900-Sentinel-RG**.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Ingat bahwa peran saat ini adalah Administrator layanan.  Tutup jendela tugas Administrator MOD dengan memilih **X** di sudut kanan atas jendela.

1. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

1. Jendela Tambahkan penetapan peran akan terbuka.  Pilih panah menu tarik-turun di bidang Pilih peran untuk menampilkan peran yang tersedia. Di kotak pilih pencarian peran, masukkan **sentinel** untuk melihat 4 peran yang terkait dengan Sentinel. Sebagai praktik terbaik, Anda harus menetapkan hak istimewa paling sedikit yang diperlukan untuk peran tersebut.  Untuk kenyamanan lab ini, masukkan **Owner** di kotak pencarian dan pilih **Owner** dari hasil tersebut.  Sebagai referensi, tinjau izin di Azure Sentinel:  https://docs.microsoft.com/id-id/azure/sentinel/roles

1. Dari daftar pengguna yang ditampilkan, pilih **MOD Administrator**.

1. Pilih **Save** di bagian bawah halaman.

1. Dari halaman kontrol akses, pilih **View my access** untuk mengonfirmasi peran telah ditambahkan, lalu tutup jendela dengan memilih **X** di sudut kanan atas jendela.

#### Demo Bagian 3:  Di bagian demo ini, Anda akan menjalani proses menghubungkan Azure Sentinel ke sumber data Anda untuk mulai mengumpulkan data.  Catatan: perlu sedikit waktu untuk menampilkan status konektor yang terhubung (~30 menit, tergantung penyewa).

1. Di kotak pencarian, di bilah biru bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **sentinel**, lalu pilih **Azure Sentinel** dari hasil pencarian.

1. Dari halaman Azure Sentinel, pilih ruang kerja yang Anda buat dengan contoh Azure Sentinel, **SC900-LogAnalytics-workspace**.

1. Langkah pertama dengan Azure Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

1. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Azure**, lalu dari daftar pilih **Azure Active Directory**.

1. Jendela konektor Azure Active Directory terbuka.  Pilih **Open connector page**.

1. Dari halaman konektor Azure Active Directory, tinjau deskripsi dan catat konten terkait yang menyertakan buku kerja, kueri, dan templat aturan analitik.  

1. Tab instruksi di jendela utama, menyediakan fasilitas tambahan untuk Azure Sentinel untuk diintegrasikan dengan Azure Active Directory.   Di bawah konfigurasi, pilih **Sign-in logs**, lalu pilih Terapkan Perubahan (beberapa konektor dapat dipilih).  Catatan: perlu beberapa saat sebelum Anda melihat status konektor terhubung (~30 menit atau lebih).  Sebagai acuan:
    1. Tinjau izin di Azure Sentinel:  https://docs.microsoft.com/id-id/azure/sentinel/roles
    1. Sambungkan ke Azure Active Directory:  https://docs.microsoft.com/id-id/azure/sentinel/connect-azure-active-directory

1. Dari tab Langkah berikutnya, catat daftar buku kerja yang direkomendasikan.   Di bawah buku kerja yang direkomendasikan, pilih **Azure Sign-in logs** (buku kerja tambahan dapat dipilih).

1. Dari halaman buku kerja dan dengan tab templat yang dipilih (digarisbawahi), pilih **Azure Sign-in logs**.

1. Dari jendela log masuk Azure AD yang terbuka, tinjau deskripsi, dan pilih **View template**.  Keluar dari templat, dengan memilih **X** di pojok kanan atas layar.  Pilih **Save** dari bagian bawah halaman, lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.

1. Dari sudut kiri atas halaman Buku Kerja, di atas tempat tertulis Buku Kerja, pilih **Azure Sentinel**. Ini mengembalikan Anda ke halaman Konektor Data Azure Sentinel.

1. Bagian atas halaman Konektor data akan menampilkan 1 terhubung, untuk menunjukkan bahwa Anda sekarang terhubung ke Azure Active Directory.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**.

1. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru saja Anda simpan terdaftar dan tersedia bagi Anda untuk melihat dan memantau data Anda.  Masuk berikutnya akan tercatat dalam buku kerja, jadi Anda dapat memilih untuk menampilkannya.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

#### Demo Bagian 4 (Opsional):  Di bagian demo ini, Anda akan menjalani proses penggunaan templat aturan analitik bawaan untuk membuat aturan agar mendapat pemberitahuan saat terjadi sesuatu yang mencurigakan.

1. Dari panel navigasi sebelah kiri, pilih **Analytics**.

1. Halaman Analitik akan menampilkan aturan aktif (Deteksi serangan banyak tahap lanjutan diaktifkan secara default) dan juga akan menyediakan akses ke templat Aturan.  Pilih tab **Rule templates**.  Perhatikan daftar templat yang tersedia dan berbagai cara untuk memfilter daftar.  Menggunakan peringatan analitik bawaan di dalam ruang kerja Azure Sentinel, Anda akan diberi tahu saat terjadi sesuatu yang mencurigakan.

1. Di bilah Pencarian, masukkan **Azure Portal**.  Pilih **Failed login attempts to Azure Portal**.  

1. Dari jendela yang terbuka, baca deskripsi dan tinjau informasi yang terkait dengan templat.  Pilih **Create rule** di bagian bawah halaman.
    1. Dari wizard Aturan analitik, tinjau informasinya, lalu pilih **Next: Set rule logic >**.
    1. Halaman Setel logika aturan, adalah tempat Anda menentukan logika untuk aturan analitik baru. Templat sudah menyediakan beberapa logika dan pengaturan yang telah ditentukan sebelumnya.  Gulir halaman untuk melihat pengaturan yang tersedia.  Biarkan default. Pilih **Next: Incident settings (preview)>**.
    1. Dengan pengaturan Insiden, peringatan Azure Sentinel dapat dikelompokkan bersama menjadi Insiden yang harus diperhatikan. Anda dapat menyetel apakah peringatan yang dipicu oleh aturan analitik ini harus menghasilkan insiden.  Biarkan pengaturan default dan pilih **Next: Automated response >**.
    1. Di tab Respons otomatis, perhatikan bagaimana Anda dapat menambahkan buku pedoman untuk mengotomatisasi respons.  Demikian pula, Anda dapat membuat aturan otomatisasi insiden.  Pilih **+ Add** baru di bawah otomatisasi insiden.  Jendela untuk membuat aturan otomatisasi baru akan terbuka.  Aturan otomatisasi apa pun yang Anda buat di halaman ini dipicu oleh aturan analitik Anda c Perhatikan bahwa Anda dapat menambahkan ketentuan dan menetapkan tindakan untuk aturan tersebut.   Pilih **Cancel** untuk keluar dari jendela.
    1. Pilih **Next: Tinjau>** untuk meninjau semua detail yang terkait dengan aturan dan berdasarkan templat yang dipilih. Pada titik ini, Anda dapat memilih untuk membuat aturan, dengan memilih **Create** atau keluar tanpa membuat aturan dengan memilih **X** di pojok kanan atas halaman.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

#### Demo Langkah 5 (Opsional):  Pada langkah sebelumnya, Anda telah membuat aturan analitik untuk diberi tahu tentang aktivitas yang mencurigakan.  Tersemat dalam wizard opsi untuk mengotomatisasi respons terhadap insiden berdasarkan aturan tertentu.  Namun, Anda juga dapat membuat aturan otomatisasi dengan langsung membuka opsi konfigurasi otomatisasi.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  

1. Pilih **+ Create**. Dari menu tarik-turun, perhatikan bagaimana Anda dapat memilih untuk menambahkan buku pedoman baru atau menambahkan aturan baru.  Pilih **Add new rule**.  
    1. Jendela untuk membuat aturan otomatisasi baru akan terbuka.  Perhatikan bahwa Anda dapat menambahkan ketentuan dan menetapkan tindakan untuk aturan tersebut.  Satu-satunya perbedaan adalah bahwa kondisi pertama mengaitkan aturan analitik yang ingin Anda terapkan aturan otomatisasi ini.  Ini berwarna abu-abu di tugas sebelumnya karena otomatisasi sedang dikonfigurasi untuk aturan tertentu.  Pilih **Cancel** untuk keluar dari jendela Buat aturan otomatisasi baru.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

#### Langkah 6: PENGHAPUSAN - Instruktur melakukan langkah ini setelah kelas. Hapus grup Sumber Daya Azure Sentinel.  Azure Sentinel ditagih berdasarkan volume data yang diserap untuk analisis di Azure Sentinel. Meskipun jumlah data yang diserap sebagai hasil dari lab ini minimal, Anda disarankan untuk menghapus grup sumber daya Azure Sentinel saat Anda selesai menjelajahi fitur kemampuan Azure Sentinel.

1. Dari halaman Azure Sentinel, di sudut kiri atas halaman, di atas tempat tertulis Azure Sentinel, pilih **All Services**.

1. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan pilih **Resource groups**.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Azure Sentinel, **SC900-Sentinel-RG**.

1. Dari bagian tengah atas halaman, pilih **Delete resource group**.  Tinjau peringatannya.  Masukkan nama grup sumber daya, **SC900-Sentinel-RG**, lalu pilih **Delete** dari bagian bawah halaman.  Diperlukan beberapa menit untuk menghapus grup sumber daya.

1. Setelah Anda memverifikasi grup sumber daya telah dihapus, tutup halaman browser. 

#### Tinjauan

Dalam demo ini, Anda telah menunjukkan proses pembuatan instans Azure Sentinel.  Anda telah menunjukkan cara mengatur izin untuk memastikan akses ke sumber daya yang terkait dengan instans Azure Sentinel.  Dengan instans Azure Sentinel yang dibuat, Anda telah mengikuti langkah-langkah untuk menghubungkan Sentinel ke sumber data, cara menggunakan aturan analitik bawaan untuk mendapatkan pemberitahuan tentang sesuatu yang mencurigakan, dan terakhir Anda telah menjelajahi kemampuan otomatisasi. Anda telah mengakhiri demo dengan menghapus grup sumber daya yang terkait dengan instans Azure Sentinel yang Anda buat.
