# Lab7web

# Nama : Taufik Eka Albani
# Nim  : 312210347
# Kelas: TI.22.A3

## Instruksi Praktikum
1. Persiapkan text editor misalnya VSCode.
2. Buat folder baru dengan nama lab7_php_dasar pada docroot webserver (htdocs)
3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.
* Langkah-langkah Praktikum
### Persiapan
#### Untuk memulai membuat kode php, perlu disiapkan web server dan interpreter PHP terlebih dahulu. Web servar yang kita gunakan adalah Apache 2 dan interpreter PHP 7. Untuk memudahkan proses praktikum, kita gunakan aplikasi bundle web server yaitu ```XAMPP.```
```Install XAMPP```
#### Unduh XAMPP dari ```https://www.apachefriends.org/download.html``` dan pilih versi portable untuk memudahkan proses installasi. Kemudian extract file tersebut, seusikan direktorinya ```(misal: c:\xampp).```
![Screenshot 2024-01-15 111138](https://github.com/taufikalbani13/Lab1web/assets/115517181/3b3ed1f4-d7bf-45fb-8d08-e93d224693db)

### Persiapan
#### Untuk memulai membuat kode php, perlu disiapkan web server dan interpreter PHP terlebih dahulu. Web servar yang kita gunakan adalah Apache 2 dan interpreter PHP 7. Untuk memudahkan proses praktikum, kita gunakan aplikasi bundle web server yaitu ```XAMPP.```
```Install XAMPP```
#### Unduh XAMPP dari ```https://www.apachefriends.org/download.html``` dan pilih versi portable untuk memudahkan proses installasi. Kemudian extract file tersebut, seusikan direktorinya ```(misal: c:\xampp).```
![Screenshot 2024-01-15 111108](https://github.com/taufikalbani13/Lab1web/assets/115517181/e084d790-60fd-43be-a15b-d64578c6df55)

• Uji coba apakah server sudah berkerja dengan baik
##### ```vhttp://127.0.0.1``` atau ```http://localhost```
##### Tampil halaman utama XAMPP jika server sudah berkerja dengan baik.
• Dokumen Website
##### Semua file website tempatkan di direktori: ```\xampp\htdocs\```
• Database MySQL
##### Direktori: ```\xampp\mysql\```
##### Manajemen database: ```http://localhost/phpmyadmin```
##### Memulai PHP
##### Buat folder lab7_php_dasar pada root directory web server ```(c:\xampp\htdocs)```
![Screenshot 2024-01-15 111138](https://github.com/taufikalbani13/Lab1web/assets/115517181/d08ebcd3-a6b9-4b85-81a7-7677c9c63d95)

##### Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL: ```http://localhost/lab7_php_dasar/```
![Screenshot 2024-01-15 111213](https://github.com/taufikalbani13/Lab1web/assets/115517181/1216971e-9f46-4b92-a0b5-06378d17b695)



##### PHP Dasar
##### Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut.
```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
```
##### Hasil Output
![Screenshot 2024-01-15 105553](https://github.com/taufikalbani13/Lab1web/assets/115517181/c8c536a6-858c-46a2-b35e-525ccd7071f3)

##### Kemudian untuk mengakses hasilnya melalui URL: ```http://localhost/lab7_php_dasar/php_dasar.php```
##### Variable PHP
##### Menambahkan variable pada program.
```python
<h1>Menggunakan Variable</h1>
    <?php
    $nim = "312210689";
    $nama = 'Hendra parsaulian';
    echo "NIM : " . $nim . "<br>";
    echo "Nama : $nama";
    ?>
```
##### Hasil Output
![Screenshot 2024-01-15 105612](https://github.com/taufikalbani13/Lab1web/assets/115517181/404193f2-5894-40e5-bf69-39d3d32a2178)

##### Predefine Variable $_GET
```pyhton
 <h1>Predefine Variable</h1>
    <?php
    echo "Selamat Datang " . $_GET ["nama"];
    ?>
</body>
</html>
```
##### Hasil Output
![Screenshot 2024-01-15 105621](https://github.com/taufikalbani13/Lab1web/assets/115517181/2670722c-d7c8-49da-aa5c-9969a060b232)

##### Untuk mengaksesnya gunakan URL: ```http://localhost/lab7_php_dasar/php_dasar.php```
##### Membuat Form Input
```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
    <label>Nama: </label>
    <input type="text" name="nama">
    <input type="submit" value="Kirim">
</form>
<?php
  echo "Selamat Datang " . $_GET ["nama"];
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105638](https://github.com/taufikalbani13/Lab1web/assets/115517181/da83a15e-09a6-47b8-b4de-02b60ea06cb1)

##### Operator
```python
<h2>Operator</h2>
<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji*$pajak);
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105653](https://github.com/taufikalbani13/Lab1web/assets/115517181/5bfb177b-43d1-4f62-acd3-fcc78d735a6c)

##### Kondisi IF
```python
<h2>Kondisi IF</h2>
<?php
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
    echo "Minggu";
} elseif ($nama_hari == "Monday") {
    echo "Senin";
} else {
    echo "Selasa";
}
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105700](https://github.com/taufikalbani13/Lab1web/assets/115517181/25983a5e-636b-41a2-ac5b-6cfe3659c997)


##### Kondisi Switch
```python
<h2>Kondisi Switch</h2>
<?php
$nama_hari = date("l");
switch ($nama_hari) {
    case "Sunday":
        echo "Minggu";
        break;
    case "Monday":
        echo "Senin";
        break;
    case "Tuesday":
        echo "Selasa";
        break;
    default:
        echo "Sabtu";
    }
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105705](https://github.com/taufikalbani13/Lab1web/assets/115517181/6ffed46b-e55c-4c52-85a4-2dab2dec1f16)


##### Perulangan for
```python
<h2>Perulangan for</h2>
<?php
echo "Perulangan 1 sampai 10 <br />";
for ($i=1; $i<=10; $i++) {
    echo "Perulangan ke: " . $i . '<br />';
}
echo "Perulangan Menurun dari 10 ke 1 <br />";
for ($i=10; $i>=1; $i--) {
    echo "Perulangan ke: " . $i . '<br />';
}
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105714](https://github.com/taufikalbani13/Lab1web/assets/115517181/2675d9f4-02f1-4cc9-a13c-13d2900c853d)


##### Perulangan while
```python
<h2>Perulangan while</h2>
<?php
echo "Perulangan 1 sampai 10 <br />";
$i=1;
while ($i<=10) {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
}
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105720](https://github.com/taufikalbani13/Lab1web/assets/115517181/bdd165eb-6bb9-4907-a835-1891da340738)


##### Perulangan dowhile
```python
<h2>Perulangan dowhile</h2>
<?php
echo "Perulangan 1 sampai 10 <br />";
$i=1;
do {
echo "Perulangan ke: " . $i . '<br />';
$i++;
} while ($i<=10);
?>
```
##### Hasil Output
![Screenshot 2024-01-15 105727](https://github.com/taufikalbani13/Lab1web/assets/115517181/97bb8127-2d39-4534-87bf-ef05baee42a4)


</body>
</html>



## Pertanyaan dan Tugas
##### Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.
##### Input
```python
<!DOCTYPE html>
<html lang="en">

    <head>
        <title>Form Input</title>
        <meta charset="utf-8">

        <!-- CSS -->
        <style>
        body {
            width: 100%;
            height: 100vh;
            margin: 0;
            font-family: tahoma;
            font-size: 16px;
        }
        h1, p {
            margin: 1em auto;
            text-align: center;
        }
        form {
            width: 60vw;
            max-width: 500px;
            min-width: 300px;
            margin: 0 auto;
            padding-bottom: 2em;
            }
        label {
            display: block;
            margin: 0.5rem 0;
        }
        button[type="submit"] {
            display: block;
            width: 60%;
            margin: 1em auto;
            height: 2em;
            font-size: 1.1rem;
            background-color: #e0daca;
            border-color: white;
            min-width: 300px;
        }
        </style>
    </head>

    <body>
        <h1 id="title">Survey Formulir Pekerjaan dan Gaji</h1>
        <p id="description"><i>Melansir dari situs <a href="https://id.indeed.com/career/php-developer/salaries"> indeed.com</a></i></p>

        <form id="survey-form" action="" method="POST">
            <fieldset>
                <label>Nama: 
                    <input type="text" name="nama" required/>
                </label>
                <label>Tanggal lahir: 
                    <input type="date" name="date">
                </label>
                <label>Pekerjaan: 
                    <label>
                    <input type="radio" name="job" value="0"/>Database Administrator
                    </label>
                    <label>
                    <input type="radio" name="job" value="1"/>Software Developer
                    </label>
                    <label>
                    <input type="radio" name="job" value="2"/>Web Developer
                    </label>
                </label>
                <button type="submit" name="submit">Kirim</button>
            </fieldset>
            <fieldset>
                <?php
                if( isset($_POST['submit']))
                {
                    $nama = $_POST['nama'];
                    $date = $_POST['date'];
                    $job = $_POST['job'];


                    $date_user = new DateTime($date);
                    $today =  new DateTime('today');
                    $usia = $today->diff($date_user)->y;

                    $job_array = ["Database Administrator","Software Developer","Web Developer"];
                    $salary_array = ["Rp. 5.300.000","Rp. 5.400.000","Rp. 4.800.000"];


                    echo "Halo, ".$nama."<br>Kamu lahir pada tanggal ".$date.", Usia mu ".$usia." tahun";
                    echo "<br>Pekerjaan yang kamu pilih adalah ".$job_array[(int)$job].", dengan penghasilan kurang lebih ".$salary_array[(int)$job];
                }
                ?>
            </fieldset>
        </form>
    </body>
</html>
```
##### Hasil Output
![Screenshot 2024-01-15 105749](https://github.com/taufikalbani13/Lab1web/assets/115517181/210144d8-7347-41a0-a00d-d9baa8344cda)
### Laporan Praktikum
1. Buatlah repository baru dengan nama Lab7Web.
2. Kerjakan semua latihan yang diberikan sesuai urutannya.
3. Screenshot setiap perubahannya.
4. Buatlah file README.md dan tuliskan penjelasan dari setiap langkah praktikum beserta screenshotnya.
5. Commit hasilnya pada repository masing-masing.
6. Kirim URL repository pada e-learning ecampus
