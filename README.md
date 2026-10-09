<h1 align="center">Selamat Datang di Tema DeNatra!</h1>

<p align="center">
  <img style="max-width: 100%;" width="500" alt="Tema DeNatra" src="https://user-images.githubusercontent.com/46939846/147866426-d50e1d2b-1ead-43de-b562-6f83fa85a1e1.png">
</p>

## Tentang Tema DeNatra
Tema DeNatra adalah salah satu tema yang digunakan untuk halaman website OpenSID (Sistem Informasi Desa).

Tema ini dibuat oleh Ariandi Ryan Kahfi, S.Pd. dengan mengangkat nama Desa Natai Raya yang disingkat menjadi DeNatra.

Sebelumnya ada Tema Natra (https://github.com/OpenSID/tema-natra) kependekan dari Natai Raya yang merupakan pemenang Sayembara Tema Web OpenSID 2019.

## Panduan Penggunaan
Untuk mengkonfigurasi berbagai pengaturan pada tema, Anda dapat melakukan langkah berikut:

### Salin dan Tempel Konfigurasi (tidak wajib)
Salin dan tempel beberapa baris kode konfigurasi di bawah ini sesuai dengan kebutuhan Anda ke dalam file `desa/config/config.php`. 

	$config['chats'] = true; // Munculkan icon chat di halaman website. Jika ingin sesuaikan jam tampil, edit file: partials/home/chats.php dibaris 45 sampai 51

	$config['kode_kota'] = '2207'; // Kode Kota Jadwal Sholat di https://www.ariandi.net/kode
   
	$config['random_doa'] = true; // Tampilkan Random Do'a pada halaman website

	$config['color'] = 'primary'; //Pilih salah satu untuk ubah warna tampilan: primary, success, warning, danger, atau secondary

	$config['fluid'] = true; //Tampilkan Halaman Penuh

	$config['menu'] = true; //Tampilkan Menu di Header
	
	$config['hide_banner_layanan'] = true; // Sembunyikan Info Layanan Surat Pengantar di halaman website

	$config['hide_banner_laporan'] = true; // Sembunyikan Info Perkembangan Penduduk di halaman website

	$config['berita_duka'] = 'Turut Berduka Cita'; // Sesuaikan kalimat berita duka di tabel Kematian pada Tabel Perkambangan Penduduk.

	$config['ip_address'] = 'ketik_ip_address'; // Tampilkan Halaman Anjungan Tema (URL Utama)

Cara mendapatkan ID Profil Akun Facebook bisa lihat di https://www.natairaya.desa.id/artikel/2019/1/30/memasang-komentar-facebook-di-sistem-informasi-desa

## Fitur Lapak (Manual)
Untuk menambahkan fitur Lapak secara manual, ikuti langkah-langkah berikut:

### Edit File `lapak.json`
1. Buka file `lapak.json` di direktori `denatra/partials/lapak/`.

2. Temukan dan edit bagian berikut sesuai petunjuk:
   - `"aktif": false` (ubah `false` menjadi `true` untuk menampilkan Lapak Desa bawaan tema)
   - `"id": "1"` (pastikan id bersifat unik dan urut jika Anda menambahkan produk baru)
   - `"gambar": "akar_pinang.jpg"` (nama gambar, mp4, video YouTube atau file wave/wom yang ada di folder `denatra/assets/lapak`)
   - `"hp": "628115222660"` (nomor HP Penjual)
   - `"lat": "-2.665093"` (Titik koordinat Latitude)
   - `"lng": "111.709899"` (Titik koordinat Langitude)

### Tampilan Produk
Tampilan produk bisa berupa gambar, mp4, atau bahkan embed dari YouTube. Misalnya, jika Anda ingin menampilkan produk dengan gambar, Anda cukup menyertakan nama gambar dalam file `lapak.json`.

Jika Anda ingin menampilkan produk menggunakan video YouTube, cukup tambahkan Link video YouTube ke dalam file `lapak.json`.

## Fitur Galeri Video (Manual) Berlaku untuk versi sebelum rilis Premium bulan April 2024 atau sebelum rilis Umum November 2024
Untuk menambahkan fitur Galeri Video secara manual, ikuti langkah-langkah berikut:

### Edit File `video.json`
1. Buka file `video.json` di direktori `desa/themes/denatra/partials/video/`.

2. Temukan dan edit bagian berikut sesuai petunjuk:
   - `"aktif": false` (ubah `false` menjadi `true` untuk menampilkan Galeri Video)
   - `"id": "1"` (pastikan id bersifat unik dan urut jika Anda menambahkan video baru)
   - `"youtube": "https://www.youtube.com/watch?v=8H3wmfaS7Lc"` (link video YouTube yang ingin Anda tampilkan)

## Keterangan Tambahan
Berikut adalah langkah-langkah untuk melakukan perubahan pada Tema DeNatra:

### Ubah Background Header
Untuk mengubah latar belakang header, ikuti langkah berikut:
- Sesuaikan tampilan header, edit file: `denatra/commons/header.php`.
- Atau, ganti file "header.jpg" di direktori `denatra/assets/img`.

### Sesuaikan Tampilan Widget di halaman utama website
Jika Anda ingin menyesuaikan tampilan widget di halaman utama bagian bawah, lakukan hal berikut:
- Edit file `desa/themes/denatra/partials/module_home.php` (baris 18, 24, 54, 60).
- ganti file php yang ada di $data["isi"] sesuai dengan nama file widget yang ingin ditampilkan. (baris 78, 83, 88, dan 93).

(secara default ada 4 widget, statistik.php, peta_wilayah_desa.php, peta_lokasi_kantor.php dan komentar.php)

### Tambahkan Script pada Bagian Meta Web
Jika Anda ingin menambahkan script pada bagian meta web (sebelum tag `</head>`), ikuti langkah berikut:
- Sisipkan pada file `denatra/partials/module_top.php`.

### Tambahkan Script pada Bagian Footer Web
Untuk menambahkan script pada bagian footer web (sebelum tag `</body>`), lakukan hal berikut:
- Sisipkan pada file `denatra/partials/module_bottom.php`.

### Sesuaikan Sidebar
Jika Anda perlu menyesuaikan sidebar (tombol bagian atas), ikuti langkah ini:
- Edit file `denatra/commons/sidebar.php` sesuai kebutuhan.

### Sesuaikan Sidebar
Untuk menyesuaikan tinggi slider, lakukan hal berikut:
- Edit file `denatra/commons/slider.php`.
- Pada baris 25 (max-height: 350px dan 450px) sesuaikan angka yg diinginkan.

### Sesuaikan Banner di Halaman Utama
Untuk mengubah link tujuan dan link gambar pada banner di halaman utama, lakukan hal berikut:
- Edit file `denatra/partials/home/banner.php` sesuai kebutuhan.

### Munculkan Icon Statistik Pengunjung
Untuk memunculkan icon statistik pengunjung di header Mobile View, lakukan hal berikut:
- Edit file `denatra/commons/header.php`.
- Sesuaikan di baris 19 (hapus text-hide-xs didalam class nya).

### Munculkan Loading di Halaman Utama
Untuk memunculkan loading di halaman utama, lakukan hal berikut:
- Edit file `denatra/commons/loader.php` sesuai kebutuhan.

### Sesuaikan Hitung Mundur Manual
Jika Anda ingin mengatur  hitung mundur manual, ikuti instruksi ini:
- Edit file `denatra/partials/event/event.json`.
- Ubah `"hitungmundur"` menjadi `true` untuk menampilkan countdown manual.

### Ubah Waktu pada Countdown Otomatis
Jika Anda perlu merubah jam pada countdown otomatis, lakukan langkah berikut:
- Edit file `denatra/partials/event/index.php`.
- Sesuaikan waktu pada variabel `$customTime` di baris 5 sesuai kebutuhan.

### Sesuaikan Kata pada Status Kehadiran di Halaman Website
Jika Anda ingin menyesuaikan kata pada status kehadiran di halaman website, lakukan hal berikut:
- Edit file `desa/themes/denatra/commons/sidebar.php` (baris 162 dan 168).
- Edit file `desa/themes/denatra/partials/pemerintah/index.php` (baris 97 dan 103).
- Edit file `desa/themes/denatra/widgets/aparatur_desa.php` (baris 53 dan 59).

Pastikan untuk menyimpan perubahan yang Anda buat setelah mengedit file-file tersebut. Semoga panduan ini membantu!
