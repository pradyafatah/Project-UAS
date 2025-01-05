# Pengelolaan Data Mahasiswa Menggunakan Konsep Modular dan Pemrograman Berorientasi Objek
Membuat project OOP untuk UAS
### Nama : PRADYA MUHAMAD FATAH
### NIM  : 312410408

# 1. Membuat class untuk menangani data 
![Cuplikan layar 2025-01-04 211357](https://github.com/user-attachments/assets/4aff6f4b-f104-45f2-8291-f337cbcd0e32)
### Class ini bertanggung jawab untuk menyimpan data yang diinput oleh pengguna. Data disimpan dalam bentuk list of dictionaries.
![Cuplikan layar 2025-01-04 211409](https://github.com/user-attachments/assets/24539be8-3c21-4775-9ee0-0d2686e2bbfc)
### Metode ini digunakan untuk menambahkan data baru ke dalam list records. Data tersebut berupa dictionary dengan kunci 'Name', 'Age', dan 'Score'.

# 2. Membuat Class untuk proses validasi dan manipulasi data
![Cuplikan layar 2025-01-04 211423](https://github.com/user-attachments/assets/81cec629-b470-4594-afbc-ae2f20f8ffb4)
### Class Process digunakan untuk memproses dan memvalidasi data input dari pengguna. Kelas ini menggunakan metode statis (@staticmethod) untuk memeriksa setiap input tanpa perlu membuat instance dari kelas ini. Class ini digunakan untuk melakukan validasi terhadap input pengguna seperti nama, usia, dan nilai.
Kode ini mendefinisikan sebuah kelas bernama Process yang berisi metode-metode statis untuk validasi data, seperti nama, umur, dan nilai. Berikut penjelasan setiap bagian kode dalam bentuk paragraf.

Kelas Process bertujuan untuk memvalidasi dan memanipulasi data yang diterima. Metode pertama adalah validate_name(name), yang digunakan untuk memvalidasi nama. Metode ini memeriksa apakah parameter name tidak kosong atau hanya berisi spasi. Jika tidak valid, fungsi akan menghasilkan error dengan pesan "Name cannot be empty." Sebaliknya, jika valid, nama akan dikembalikan apa adanya. Metode kedua, validate_age(age), memvalidasi umur. Fungsi ini memeriksa apakah parameter age berupa angka (dengan isdigit()) dan bernilai positif. Jika tidak memenuhi kriteria, error dengan pesan "Age must be a positive integer." akan dilempar. Nilai yang valid akan dikembalikan dalam bentuk integer. Metode terakhir adalah validate_score(score), yang digunakan untuk memvalidasi nilai. Metode ini memastikan parameter score adalah angka dan berada dalam rentang 0 hingga 100. Jika nilai tidak memenuhi kriteria, error dengan pesan "Score must be an integer between 0 and 100." akan dilempar. Nilai yang valid akan dikembalikan dalam bentuk integer. Kelas ini memastikan bahwa data yang diterima valid sebelum diproses lebih lanjut.

# 3. Membuat class untuk menampilkan data
![Cuplikan layar 2025-01-04 211437](https://github.com/user-attachments/assets/85589044-e6a5-454b-8682-c0eeccb8030f)
### Class ini bertugas menampilkan data yang telah disimpan dalam bentuk tabel menggunakan pustaka
Kode di atas mendefinisikan sebuah kelas bernama View, yang digunakan untuk menampilkan data dalam bentuk tabel. Kelas ini memiliki sebuah metode statis bernama display_table(data), yang dapat dipanggil tanpa harus membuat instance dari kelas View. Metode ini menerima sebuah parameter data, yang berisi data yang akan ditampilkan. Jika data yang diberikan kosong, metode ini akan mencetak pesan "No records to display." ke konsol. Sebaliknya, jika data tersedia, metode ini akan mengonversi data tersebut ke dalam bentuk tabel menggunakan DataFrame dari pustaka pandas dan menampilkannya di konsol. Dengan pendekatan ini, kode menjadi lebih rapi dan terstruktur, terutama untuk keperluan pengelolaan tampilan data.


# 4. Fungsi utama untuk menjalankan program
![Cuplikan layar 2025-01-04 211451](https://github.com/user-attachments/assets/bdf73606-af3e-4173-96e0-7d86a8f9bc6d)
### Penjelasan
Kode Python yang ditampilkan adalah bagian dari sebuah program untuk mengelola data siswa. Program ini memiliki tiga komponen utama: Data, Process, dan View, yang masing-masing bertanggung jawab atas pengelolaan data, validasi input, dan tampilan data. Berikut penjelasan tiap bagian kode:

Fungsi main(): Fungsi utama ini berfungsi untuk menjalankan keseluruhan program. Di dalamnya, dibuat tiga objek, yaitu data, process, dan view, yang mewakili tiga komponen utama. Objek data digunakan untuk menyimpan data siswa, process digunakan untuk memvalidasi input, dan view digunakan untuk menampilkan data dalam format tabel.

Loop while True: Loop ini digunakan untuk meminta input pengguna secara berulang untuk menambahkan data siswa. Program akan terus meminta input hingga pengguna memutuskan untuk berhenti dengan mengetikkan sesuatu selain "yes" pada prompt terakhir.

Blok try: Di dalam blok try, input pengguna divalidasi melalui metode validate_name, validate_age, dan validate_score dari objek process. Metode ini memastikan nama, umur, dan nilai siswa valid sebelum data disimpan. Jika input valid, data siswa ditambahkan ke dalam objek data melalui metode add_record.

Blok except: Jika terjadi kesalahan input (misalnya pengguna memasukkan data yang tidak valid), blok except menangkap kesalahan ValueError dan mencetak pesan error yang menjelaskan masalah.

Prompt untuk menambahkan data lagi: Setelah setiap data berhasil ditambahkan atau terjadi kesalahan, pengguna ditanya apakah mereka ingin menambahkan data siswa lain. Input pengguna diproses dengan fungsi strip() untuk menghapus spasi tambahan dan lower() untuk mengonversi ke huruf kecil. Jika pengguna menjawab selain "yes", loop dihentikan dengan perintah break.

Menampilkan tabel data akhir: Setelah pengguna memutuskan untuk tidak menambahkan data lagi, program menampilkan tabel data siswa menggunakan metode display_table dari objek view. Data diambil melalui metode get_records dari objek data.

Blok if __name__ == "__main__":: Blok ini memastikan bahwa fungsi main() hanya akan dieksekusi jika file Python dijalankan langsung, bukan diimpor sebagai modul oleh file lain.

Secara keseluruhan, program ini mencakup proses validasi input, penyimpanan data, dan tampilan data dalam format tabel dengan penanganan error yang baik. Program ini cocok untuk pengelolaan data siswa dalam skala kecil.
# 5. hasil
![image](https://github.com/user-attachments/assets/6b2ab3ce-0c5e-4466-a031-d99cf6140a3d)
## Penjelasan
Program meminta pengguna untuk menginputkan data berupa nama mahasiswa, umur, dan nilai (dalam rentang 0-100). Setelah data dimasukkan, program menampilkan pesan bahwa data berhasil ditambahkan, lalu memberikan opsi kepada pengguna untuk menambahkan data baru dengan mengetik "yes" atau menghentikan program dengan mengetik "no". Jika pengguna memilih "yes", program akan mengulangi proses input data. Program ini kemungkinan menggunakan struktur perulangan seperti while untuk memungkinkan pengulangan proses input hingga pengguna memutuskan berhenti. Data yang dimasukkan kemungkinan disimpan dalam struktur data seperti list atau dictionary untuk diolah lebih lanjut. Program ini cocok digunakan untuk sistem manajemen data sederhana dalam konteks tugas atau ujian pemrograman.

