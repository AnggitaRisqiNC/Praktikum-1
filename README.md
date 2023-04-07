# Praktikum 1 
Nama : Anggita Risqi Nur Clarita

NIM : 312210450

Kelas : TI.22.A.4

Mata Kuliah : Basis Data

Dosen Pengampu : Agung Nugroho, S.Kom., M.Kom.

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Tugas Praktikum 1|[Click Here](#tugas-praktikum-1)|
|2|Penjelasan dan Output Praktikum 1|[Click Here](#penjelasan-dan-output-program)|
|3|Evaluasi dan Pertanyaan|[Click Here](#evaluasi-dan-pertanyaan)|

## Tugas Praktikum 1
[Link Soal Praktikum 1](https://drive.google.com/file/d/190J1_LjGoJSVxSZueOp47iOySnhA2eV-/view)

## Penjelasan dan Output Program
### 1. Buat sebuah database dengan nama *latihan2*!
Untuk membuat database gunakan perintah sebagai berikut :

```sql
CREATE DATABASE [nama_database]
```

```sql
CREATE DATABASE latihan2;
```

Lalu, setelah kita membuat database, Kita masuk ke dalam database tersebut dengan perintah sebagai berikut :

```sql
USE latihan2;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/1.png)

### 2. Buat sebuah tabel dengan nama *biodata* (nama, alamat) di dalam database *latihan2*!
Untuk membuat Tabel gunakan perintah sebagai berikut :

```sql
CREATE TABLE nama_tabel (nama_field1 tipe _data(ukuran), nama_field2 tipe_data(ukuran), ..., nama_fieldn tipe_data(ukuran));
```

```sql
create table biodata (nama varchar(15), alamat text);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/2.png)

### 3. Tambahkan sebuah kolom *keterangan* (varchar 15), sebagai kolom terakhir!
Untuk menambahkan kolom terakhir yaitu dengan sering digunakan kata **AFTER**:

```sql
ALTER TABLE [nama_tabel] ADD COLUMN nama_field tipe_data(ukuran) [AFTER|BEFORE|FIRST];
```

```sql
alter table biodata add column keterangan varchar(15) after alamat;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/3.png)

### 4. Tambahkan kolom *id(int 11)* di awal (sebagai kolom pertama)!
Untuk menambahkan kolom pertama yaitu dengan perintah sebagai berikut :

```sql
ALTER TABLE [nama_tabel] ADD COLUMN nama_field tipe_data(ukuran) [AFTER|BEFORE|FIRST];
```

```sql
alter table biodata add column id int(11) first;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/4.png)

### 5. Sisipkan sebuah kolom dengan nama *phone* (varchar 15) setelah kolom *alamat*!
Untuk menyisipkan kolom setelah kolom lain yaitu dengan perintah **AFTER**:

```sql
ALTER TABLE [nama_tabel] ADD COLUMN nama_field tipe_data(ukuran) [AFTER|BEFORE|FIRST];
```

```sql
alter table biodata add column phone varchar(15) after alamat;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/5.png)

### 6. Ubah tipe data kolom *id* menjadi char(11)!
Untuk mengubah tipe data yaitu dengan perintah sebagai berikut :

```sql
ALTER TABLE [nama_tabel] MODIFY COLUMN nama_field tipe_data_baru(ukuran);
```

```sql
alter table biodata modify column id CHAR(11);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/6.png)

### 7. Ubah nama kolom *phone* menjadi *hp* (varchar 20)!
Untuk mengubah kolom yaitu dengan perintah sebgai berikut :

```sql
ALTER TABLE [nama_tabel] CHANGE COLUMN nama_field_lama nama_field_baru tipe_data(ukuran);
```

```sql
alter table biodata change column phone hp varchar(20);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/7.png)

### 8. Tambahkan kolom *email* setelah kolom *hp*
Untuk menambahkan kolom setelah kolom hp yaitu dengan menggunakan kata **AFTER**:

```sql
ALTER TABLE [nama_tabel] ADD COLUMN nama_field tipe_data(ukuran) [AFTER|BEFORE|FIRST];
```

```sql
alter table biodata add column email varchar(20) after hp;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/8.png)

### 9. Hapus kolom *keterangan* dari tabel!
Untuk menghapus kolom dari tabel yaitu dengan perintah sebagai berikut :

```sql
ALTER TABLE [nama_tabel] DROP COLUMN nama_field;
```

```sql
alter table biodata drop keterangan;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/9.png)

### 10. Ganti nama tabel menjadi *data_mahasiswa*!
Untuk mengganti nama tabel yaitu dengan perintah sebagai berikut :

```sql
ALTER TABLE [nama_tabel] RENAME [nama_tabel_baru];
```

```sql
alter table biodata rename data_mahasiswa;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/10.png)

### 11. Ganti nama *field* id menjadi *nim*!
Untuk mengganti nama field yaitu dengan perintah sebagai berikut :

```sql
ALTER TABLE [nama_tabel] CHANGE nama_field_lama nama_field_baru tipe_data(ukuran);
```

```sql
alter table data_mahasiswa change id nim char(11);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/11.png)

### 12. Jadikan *nim* sebagai *PRIMARY KEY*!
Untuk menambahkan index atau key, gunakan perintah sebagai berikut :

```sql
ALTER TABLE [nama_tabel] ADD [INDEX|PRIMARY KEY] (nama_field);
```

```sql
alter table data_mahasiswa add primary key(nim);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/12.png)

### 13. Jadikan kolom *email* sebagai *UNIQUE KEY*!
Perintah yang digunakan sama seperti perintah pada nomer 12, hanya saja PRIMARY KEY diganti menjadi UNIQUE KEY

```sql
alter table data_mahasiswa add unique key(email);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/Praktikum1/13.png)

## Evaluasi dan Pertanyaan
### Tulis semua perintah-perintah SQL percobaan di pdf praktikum 1 beserta outputnya!

#### a) Membuat Database
```sql
CREATE DATABASE latihan1;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/a.png)

#### b) Membuat Tabel
```sql
CREATE TABLE siswa (nama VARCHAR(100), alamat TEXT);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/b.png)

#### c) Menambah Kolom
```sql
ALTER TABLE biodata ADD COLUMN keterangan TEXT AFTER alamat;
```

Di perintah yang terdapat pada PDF Praktikum 1 ada kesalahan yaitu di nama tabelnya, seharusnya **siswa** bukan biodata, seharusnya seperti ini :

```sql
alter table siswa add column keterangan text after alamat;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/c.png)

#### d) Menambah kolom diawal
```sql
ALTER TABLE siswa ADD COLUMN id INT FIRST;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/d.png)

#### e) Mengubah nama kolom
```sql
ALTER TABLE siswa CHANGE COLUMN keterangan TO kelas;
```

Diperintah ini ada kesalahan, seharusnya yang benar yaitu :

```sql
alter table siswa change column keterangan kelas text;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/e.png)

#### f) Mengubah tipe data
```sql
ALTER TABLE siswa MODIFY COLUMN kelas VARCHAR(10);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/f.png)

#### g) Menghapus kolom
```sql
ALTER TABLE siswa DROP COLUMN kelas;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/g.png)

#### h) Menambah PRIMARY KEY
```sql
ALTER TABLE siswa ADD PRIMARY KEY(id);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/h.png)

#### i) Menghapus PRIMARY KEY
```sql
ALTER TABLE siswa DROP PRIMARY KEY;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/i.png)

#### j) Menambah CONSTRAINT
```sql
ALTER TABLE siswa ADD CONSTRAINT pk_sisiwa PRIMARY KEY(id);
```

Di perintah yang terdapat pada PDF Praktikum 1 ada kesalahan yaitu **pk_sisiwa** seharusnya **siswa**, seharusnya seperti ini :

```sql
alter table siswa add constraint PK_siswa primary key(id);
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/j.png)

#### k) Menghapus CONSTRAINT
```sql
ALTER TABLE siswa DROP CONSTRAINT pk_siswa;
```

Pada bagian ini saya menggunakan :
```sql
alter table siswa drop primary key;
```

![image](https://github.com/AnggitaRisqiNC/Praktikum-1/blob/main/screenshot/SQL%20DDL/k.png)

### Apa maksud dari int (11)?
Yang dimaksud **int(11)** artinya suatu data yang dipakai atau digunakan dengan tipe data **int** atau **integer** dengan length atau panjang **karakter 11**.

### Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang berisi Yes dan No. Apa maksudnya?
Apabila **Null** berisi **no**, maka data tersebut nantinya akan dilakukan *pengisian atau penginputan*. Sedangkan apabila **Null** berisi **yes**, maka artinya data tersebut akan *dikosongkan atau tidak dilakukan penginputan*.

## Finish