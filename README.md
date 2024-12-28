Riwayat_Pemesanan adalah kelas Java berbasis Swing yang digunakan untuk menampilkan dan mengelola riwayat pemesanan dalam bentuk tabel. Kelas ini memiliki fitur untuk menambah, memperbarui, menghapus data, serta menyimpan data ke dalam file teks.

Deskripsi Kelas

//Atribut Utama
tableRiwayat: Sebuah komponen JTable untuk menampilkan data riwayat pemesanan.
tableModel: Model data untuk JTable yang berisi kolom-kolom ID, Nama, Nomor HP, Tanggal, Wisata, Jumlah Tiket, dan Total Biaya.
btnKembali: Tombol untuk kembali ke panel utama.
btnUpdate: Tombol untuk memperbarui data pada baris yang dipilih.
btnHapus: Tombol untuk menghapus data pada baris yang dipilih.
filePath: String yang menunjukkan lokasi file untuk menyimpan data (riwayat_pemesanan.txt).

//Fitur dan Fungsi
1. Tampilan dan Desain
- Panel utama menggunakan tata letak BorderLayout.
- Latar belakang panel utama diatur menjadi biru muda (173, 216, 230) untuk kesan estetis.
- Tabel memiliki header dengan warna latar biru muda dan teks hitam.
2. Fungsi Tambah Data
- Fungsi tambahRiwayat memungkinkan penambahan data baru ke tabel dengan parameter berikut:
- id: ID pemesanan.
- nama: Nama pelanggan.
- nomorHP: Nomor HP pelanggan.
- tanggal: Tanggal pemesanan.
- wisata: Tujuan wisata.
- jumlahTiket: Jumlah tiket yang dipesan.
- totalBiaya: Total biaya pemesanan.
- Setelah data ditambahkan, perubahan akan disimpan ke file teks menggunakan fungsi simpanKeFile.
3. Fungsi Update Data
- Menggunakan tombol btnUpdate, pengguna dapat memperbarui data pada baris yang dipilih di tabel.
  Proses:
    - Data diambil dari baris yang dipilih.
    - Dialog input muncul untuk setiap kolom, memungkinkan pengguna memperbarui nilainya.
    - Data yang dimasukkan divalidasi (khusus untuk jumlah tiket dan total biaya).
    - Tabel diperbarui, dan data disimpan ke file teks.
4. Fungsi Hapus Data
- Menggunakan tombol btnHapus, pengguna dapat menghapus data pada baris yang dipilih.
  Proses:
  -Memunculkan dialog konfirmasi sebelum penghapusan.
  -Jika disetujui, baris dihapus dari tabel, dan perubahan disimpan ke file teks.
5. Fungsi Simpan Data ke File
- Fungsi simpanKeFile digunakan untuk menyimpan data tabel ke file teks (riwayat_pemesanan.txt).
- Setiap baris pada tabel disimpan dalam format CSV.
- File akan diperbarui setiap kali data ditambahkan, dihapus, atau diubah.
6. Navigasi Antar Panel
- Tombol btnKembali menggunakan CardLayout untuk kembali ke panel utama (Utama).
  Cara Kerja
  Tampilan Awal: Panel dengan tabel kosong siap untuk menampilkan data riwayat.
  Tambah Data: Pengguna dapat menambahkan data melalui fungsi tambahRiwayat (biasanya dipanggil dari panel lain).
  Perbarui Data: Klik tombol Update, lalu masukkan data baru melalui dialog input.
  Hapus Data: Pilih baris yang dihapus, klik tombol Hapus, lalu konfirmasi penghapusan.
  Kembali: Klik tombol Kembali untuk kembali ke panel utama.
  Struktur Kolom Tabel
  ID: Nomor identifikasi unik untuk setiap pemesanan.
  Nama: Nama pelanggan.
  Nomor HP: Kontak pelanggan.
  Tanggal: Tanggal pemesanan dalam format string.
  Wisata: Destinasi wisata yang dipesan.
  Jumlah Tiket: Jumlah tiket yang dipesan (integer).
  Total Biaya: Total biaya pemesanan dalam format string dengan prefiks "Rp".