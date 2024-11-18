# **Pemrograman Mobile Pertemuan Minggu 10**

| Nama  :   | Haidar Aly |
| :--------: | :-------: |

| Kelas :  | TI-3F    |
| :--------: | :-------: |

| Absen : |  09  |
| :--------: | :-------: |

| NIM   :  | 2241720258   |
| :--------: | :-------: |

## **Praktikum 1**

### Hasil Praktikum 1
<![alt](assets/01.gif)>

### Tugas Praktikum 1

1. Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian?
> 1. Modularisasi: Dengan mengekspor beberapa file dari satu file, Anda dapat mengelompokkan dan mengorganisir kode Anda dengan lebih baik. Ini membantu dalam menjaga kode tetap modular dan mudah dikelola.
> 2. Kemudahan Akses: File yang mengimpor file ini hanya perlu melakukan satu kali impor untuk mendapatkan akses ke semua deklarasi yang diekspor.
> 3. Pengurangan Duplikasi: Mengurangi kebutuhan untuk mengimpor banyak file secara individual di berbagai tempat dalam proyek Anda. Ini membuat kode lebih bersih dan lebih mudah untuk dipelihara.

2. Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta?
> - Variabel plan diperlukan dalam kode tersebut untuk menyimpan instance dari kelas Plan, yang mungkin berisi data atau logika yang diperlukan untuk menampilkan dan mengelola rencana dalam aplikasi. Variabel plan dibuat sebagai konstanta (const Plan()) karena: 
> 1. Immutability: Dengan menjadikannya konstanta, kita memastikan bahwa instance Plan tersebut tidak akan berubah setelah diinisialisasi. Ini membantu mencegah perubahan yang tidak disengaja dan meningkatkan keandalan kode.
> 2. Optimisasi: Konstanta memungkinkan compiler untuk melakukan optimisasi yang lebih baik, karena compiler tahu bahwa nilai tersebut tidak akan berubah selama runtime.

3. Lakukan capture hasil dari Langkah 9 berupa GIF, kemudian jelaskan apa yang telah Anda buat!
> <![alt](assets/02.gif)>

4. Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state ?
> - Method pada Langkah 11 dan 13 digunakan untuk mengelola perubahan state aplikasi. Method ini biasanya digunakan untuk:
> 1. Menginisialisasi state aplikasi ketika aplikasi pertama kali dibuka
> 2. Mengupdate state aplikasi ketika pengguna melakukan aksi tertentu
> 3. Menghentikan aplikasi ketika pengguna keluar dari aplikasi
> 4. Menghandle perubahan state aplikasi ketika aplikasi berada di background
> - Dengan menggunakan method ini, kita dapat mengelola state aplikasi dengan lebih baik dan meningkatkan kinerja aplikasi.

## **Praktikum 2**

### Hasil Praktikum 2
<![alt](assets/03.gif)>

### Tugas Praktikum 2

1. Jelaskan mana yang dimaksud InheritedWidget pada langkah 1 tersebut! Mengapa yang digunakan InheritedNotifier?
> ```dart
> static ValueNotifier<Plan> of(BuildContext context) {
>   return context.
>   dependOnInheritedWidgetOfExactType<PlanProvider>()!.notifier!;
> }
> ```
> InheritedWidget adalah widget yang dapat diakses oleh widget-childnya. Dalam kasus ini, InheritedNotifier digunakan untuk mengakses Notifier yang telah diinisialisasi sebelumnya. InheritedNotifier digunakan karena:
> 1. Mengurangi duplikasi kode: Dengan menggunakan InheritedNotifier, kita tidak perlu membuat instance Notifier di setiap widget-child.
> 2. Meningkatkan keandalan: InheritedNotifier memastikan bahwa Notifier hanya diinisialisasi sekali, sehingga mengurangi kemungkinan kesalahan
> 3. Meningkatkan kinerja: InheritedNotifier memungkinkan kita untuk mengakses Notifier tanpa perlu membuat instance baru.

2. Jelaskan maksud dari method di langkah 3 pada praktikum tersebut! Mengapa dilakukan demikian?
> - Keterbacaan: Menggunakan getter membuat kode lebih bersih dan mudah dibaca. Sehingga dapat mengakses completedCount dan completenessMessage seperti properti biasa tanpa perlu memanggil metode.
> - Pemeliharaan: Getter memisahkan logika perhitungan dari tempat di mana nilai tersebut digunakan, sehingga lebih mudah untuk memelihara dan memperbarui logika jika diperlukan.
> - Efisiensi: Getter hanya dihitung saat diakses, sehingga tidak ada overhead memori tambahan untuk menyimpan nilai yang mungkin tidak selalu diperlukan.

3. Lakukan capture hasil dari Langkah 9 berupa GIF, kemudian jelaskan apa yang telah Anda buat!
> <![alt](assets/03.gif)>

## **Praktikum 3**

### Hasil Praktikum 3
<![alt](assets/04.gif)>

### Tugas Praktikum 3

1. Berdasarkan Praktikum 3 yang telah Anda lakukan, jelaskan maksud dari gambar diagram berikut ini!
> Pada diagram sebelah kiri, kita memiliki struktur komponen yang dimulai dari MaterialApp, diikuti oleh PlanProvider, dan PlanCreatorScreen. Di dalam PlanCreatorScreen, kita menggunakan Column sebagai kontainer utama yang berisi TextField dan Expanded yang menampung sebuah ListView. Struktur ini mungkin digunakan untuk menampilkan input dari pengguna (di dalam TextField) dan daftar elemen (di dalam ListView).
> Kemudian, diagram ini menunjukkan bahwa ketika Navigator.push digunakan, layar akan berpindah ke struktur layout di sebelah kanan. Pada tampilan ini, kita memiliki MaterialApp yang sekarang terhubung ke PlanScreen yang di dalamnya menggunakan Scaffold sebagai struktur dasar. Di dalam Scaffold, terdapat Column yang memuat dua elemen utama, yaitu Expanded dan SafeArea. Expanded berisi ListView yang memungkinkan tampilan daftar item, sedangkan SafeArea digunakan untuk memastikan teks (atau elemen UI lainnya) tidak terpotong oleh area layar yang kritis (seperti notch atau status bar).
> Perbedaan utama antara dua tampilan ini adalah pada struktur layout dan komponen-komponen yang digunakan untuk membangun tampilan yang lebih aman dan terorganisir pada layar setelah Navigator.push.

2. Lakukan capture hasil dari Langkah 14 berupa GIF, kemudian jelaskan apa yang telah Anda buat!
> <![alt](assets/04.gif)>