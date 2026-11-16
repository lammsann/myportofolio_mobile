# MyPortfolio Mobile

- **Nama**: Ghulam Muhammad Ihsan
- **NPM**: 2506656766
- **Kelas**: PBP B

## Cara Menjalankan Proyek

1. Pastikan Flutter SDK sudah terpasang (flutter doctor).
2. Masuk ke direktori proyek dan unduh dependensi:
   ```bash
   flutter pub get
   ```
3. Jalankan aplikasi di Google Chrome atau emulator:
   ```bash
   flutter run -d chrome
   ```

---

### Tugas 7

1. Widget tree itu struktur hierarki yang bentuknya tree, yang merepresentasikan seluruh elemen user interface di aplikasi. Hampir segala sesautu di flutter itu widget. Parent widget gunanya sebagai container yang mengatur posisi, constraint, dll dari widget di dalamnya, bisa punya satu anak atau lebih. Child widget yang menerima constraint atau context dari parentnya lalu nentuin sendiri ukuran dan render di posisi yang ditentuin parent.
2. - **MaterialApp:** Widget utama yang membungkus aplikasi. Berfungsi untuk mengatur konfigurasi global seperti judul aplikasi (title), tema warna (theme), dan halaman awal (home).
   - **Scaffold:** Menyediakan kerangka struktur visual dasar halaman standar Material Design yang mencakup bagian atas (appBar) dan konten utama (body).
   - **AppBar:** Menampilkan bilah navigasi di bagian atas layar aplikasi yang memuat judul teks 'MyPortfolio' dengan latar belakang warna utama.
   - **Text:** Digunakan untuk merender dan menampilkan teks ke layar (seperti judul aplikasi, teks sambutan, label NPM, nama, kelas, hingga nama tombol menu).
   - **Padding:** Memberikan jarak atau ruang kosong (padding) di sekeliling widget anaknya agar tampilan tidak terlalu menepi.
   - **Column:** Menyusun sekumpulan widget anak secara vertikal (dari atas ke bawah).
   - **Row:** Menyusun sekumpulan widget anak secara horizontal (dari kiri ke kanan)—digunakan untuk menampilkan tiga kartu informasi (InfoCard) secara sejajar.
   - **SizedBox:** Memberikan jarak kosong dengan tinggi atau lebar yang spesifik (misalnya untuk memberi jarak antar elemen secara vertikal).
   - **Center:** Mengatur posisi widget anaknya agar berada tepat di tengah (center alignment) secara horizontal maupun vertikal.
   - **GridView (melalui GridView.count):** Menampilkan daftar item dalam bentuk tata letak kisi-kisi (grid) 3 kolom dengan pengaturan jarak antar elemen yang teratur.
   - **Card:** Wadah bergaya Material Design yang memberikan efek elevasi atau bayangan tipis di sekelilingnya.
   - **Container:** Komponen kotak serbaguna yang digunakan untuk mengatur ukuran (lebar/tinggi), dekorasi, dan padding dari widget di dalamnya.
   - **Material:** Menyediakan fondasi visual Material Design, memungkinkan pengaturan warna latar belakang kustom (color) dan sudut melengkung (borderRadius).
   - **InkWell:** Menambahkan area interaktif sentuhan dengan efek visual ripple ketika ditekan (onTap), yang diimplementasikan untuk memicu aksi seperti menampilkan SnackBar.
   - **Icon:** Menampilkan simbol ikon grafis (seperti ikon sekolah, tombol tambah, dan tombol logout).
   - **MyApp:** Kelas utama turunan StatelessWidget yang berfungsi sebagai akar aplikasi untuk menginisialisasi MaterialApp.
   - **MyHomePage:** Kelas turunan StatelessWidget yang merepresentasikan halaman utama aplikasi, memuat struktur informasi profil (InfoCard) serta grid tombol menu (ItemCard).
   - **InfoCard:** Widget kustom berupa kartu terstruktur yang berfungsi menampilkan label informasi beserta isinya (seperti data NPM, Nama, dan Kelas) secara berdampingan.
   - **ItemCard:** Widget kustom yang merepresentasikan kartu menu interaktif di dalam grid (misalnya tombol "Lihat Education", "Tambah Education", dan "Logout") lengkap dengan ikon, warna latar belakang, dan aksi ketika diklik.
3. Material app fungsinya sebagai widget container di tingkat aplikasi berbagai core service yang standarnya material design, umumnya digunakan sebagai root widget karena komponen material dibawahnya bergantung pada konteks dan inheritedwidget yang disediakan oleh materialapp. jika tidak jadi root widget maka child widgetnya tidak bisa mengakses.
4. StatelessWidget sifatnya immutable, atributnya final, tidak dapat mengubah datanya sendiri secara dinamis setelah ditampilin. Kalo StatefulWidget sifatnya mutable, punya objek yang tipenya state yang dapat meniympan data yang berubah rubah selama apps nya berjalan, serta bisa rebuild. StatelessWidget dipakai ketika komponen hanya akan menampilkan informasi yang tetap dan tidak perlu mengubah state lokalnya secara dinamis, Sedangkan StatefulWidget dipakai ketika komponen harus diperbarui secara dinamis akibat user atau perubahan data lokal.
5. BuildContext adalah objek yang merepresentasikan lokasi atau posisi widget di struktur widget tree, ini penting karena widget perlu referensi posisinya di tree agar bisa menulusuri widget di atasnya untuk mengambil data (inheritedwidget). Kegunaannya untuk ambil warna primer dari tema MaterialApp untuk Appbar. Lalu read width layar device saat ini agar InfoCard proporsional, cari ScaffoldMessenger terdekat di atas tree untuk hide dan show SnackBar saat ItemCard ditekan.
6. Hot Reload gampangnya langsung apply perubahan kode dart terbaru dengan hanya menjalankan method build()) tanpa menghapus current statenya, sedangkan Hot Restart dia reset seluruh state dan jalanin ulang aplikasi dari function main() dan initState() tanpa compile ulang codenya. Kalo full restart dia full shutdown appsnya dan compile ulang projeknya termasuk native codenya dari awal. Alasan hot reload saja tidak cukup karena ketika mau mengubah variabel global/static, atau ubah kode di main/initstate, atau ngubah nilai atribut yang sudah terinisialisasi di page atau ubah suatu class dari statelesswidget jadi statefulwidget vice versa maka harus melakukan hot restart, sedangkan semisal mau nambah dependensi baru, aset baru, atau mau ubah native code maka harus pakai full restart.

---

## AI Disclosure: [share.gemini.google/WZt0T35GLFdh](https://share.gemini.google/WZt0T35GLFdh)
