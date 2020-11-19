# Tugas 12 MySQL
#### Sebagai tabel sample, silahkan buat tabel nilai_mahasiswa:
```
DROP TABLE IF EXISTS nilai_mahasiswa;

CREATE TABLE nilai_mahasiswa (
nim CHAR(8) PRIMARY KEY,
nama VARCHAR(50),
semester_1 DECIMAL(4,2),
semester_2 DECIMAL(4,2),
semester_3 DECIMAL(4,2)
) ENGINE = InnoDB;

INSERT INTO nilai_mahasiswa VALUES
('17090113', 'Riana Putria', 3.12, 2.98, 3.45),
('17140143', 'Rudi Permana', 2.56, 3.14, 3.22),
('17080305', 'Rina Kumala Sari', 3.45, 2.56, 3.67),
('17140119', 'Sandri Fatmala', 2.12, 2.78, 2.56),
('17090308', 'Christine Wijaya', 3.78, 3.23, 3.11);
```

#### #### 1. Buat view nilai_ipk yang diambil dari tabel nilai_mahasiswa. View ini terdiri dari kolom nim, nama, dan IPK. Tampilan akhir view adalah sebagai berikut:
![Tugas 12,1](https://github.com/troy213/tugas_12_mysql/blob/main/Tugas%2012.1%20MySQL.jpg)

(Note: Kolom IPK dalam kasus ini merupakan kolom komputasi, dimana nilainya akan dihitung dari kolom-kolom yang sudah ada. Kolom seperti ini sebaiknya tidak ikut disimpan ke dalam database, tapi cukup dihitung pada saat akan ditampilkan, atau disimpan ke dalam view).


#### 2. Buat view kedua dengan nama nilai_ipk_format. Isi view ini diambil dari view nilai_ipk. Tampilan akhir view adalah sebagai berikut:
![Tugas 12,2](https://github.com/troy213/tugas_12_mysql/blob/main/Tugas%2012.2%20MySQL.jpg)

Hasil diatas harus terurut dari IPK tertinggi ke terendah. (Tips: gunakan fungsi CONCAT() untuk menggabungkan string, serta query ORDER BY untuk pengurutan).


#### 3. Input 1 baris baru ke dalam tabel nilai_mahasiswa, kemudian periksa isi view nilai_ipk dan nilai_ipk_format. Data baru yang diinput boleh sembarang. Pastikan isi view juga langsung terupdate dengan penambahan data ini.


#### 4. Tampilkan mahasiswa yang namanya diawali dengan huruf R. Data ini diambil dari view nilai_ipk_format. Berikut tampilan akhir yang diiginkan:
![Tugas 12,4](https://github.com/troy213/tugas_12_mysql/blob/main/Tugas%2012.4%20MySQL.jpg)

(Tips: Gunakan query SELECT...LIKE untuk proses seleksi.)


#### 5. Hapus view nilai_ipk dan nilai_ipk_format.

