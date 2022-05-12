# Web
- TUTORIAL POINT:  https://www.tutorialspoint.com/sqlite/index.htm

# Video Source:
- Membuat Database SQLITE (Create - Read - Update - Delete): https://www.youtube.com/watch?v=F5Bhu84fJwo
- Using A SQLite Database For Local Data In A Golang Application: https://www.youtube.com/watch?v=YpDVQC8hfik

# Quizz Database SQLite

1. Ketika kita memiliki subquery di dalam main query, query mana yang dieksekusi lebih dulu?

    - [ ] A. Subquery tidak pernah dieksekusi. main query yang dieksekusi.
    - [ ] B. Mereka dieksekusi pada saat yang sama   
    - [ ] C. main query
    - [X] D. subquery

2. Kita harus memastikan keakuratan dan keandalan data dalam database. Kita menetapkan beberapa batasan untuk membatasi tipe data yang bisa masuk ke dalam tabel. Jenis batasan apa yang kita tetapkan?
   - [ ] A. row level
   - [ ] B. database level
   - [X] C. column level
   - [ ] D. function level

3. Management telah meminta kita membangun employee database. Kita mulai dengan employee table. Mana sintaks yang benar?
   - [ ] A. 
        ```sql
        CREATE TABLE employee (
            employeeID integer,
            firstName varchar(50),
            lastName varchar(50),
            phone varchar(20),
            address varchar(50),
            PRIMARY KEY employeeID
        );
        ```
   - [ ] B. 
        ```sql
           CREATE TABLE employee (
            employeeID integer,
            firstName varchar(50),
            lastName varchar(50),
            phone varchar(20),
            address varchar(50),
            PRIMARY KEY ON employeeID
        );
        ```
   - [ ] C. 
        ```sql
        CREATE TABLE IF EXISTS employee (
            employeeID integer,
            firstName varchar(50),
            lastName varchar(50),
            phone varchar(20),
            address varchar(50),
            PRIMARY KEY (employeeID)
        );
        ```
   - [X] D. 
        ```sql
        CREATE TABLE IF NOT EXISTS employee (
            employeeID integer,
            firstName varchar(50),
            lastName varchar(50),
            phone varchar(20),
            address varchar(50),
            PRIMARY KEY (employeeID)
        );
        ```

4. Jika kita membuat skema tabel untuk menyimpan nilai id sebagai nomor (1, 2, 3, 4, atau 5) jenis kolom mana yang menjadi pilihan terbaik?
   - [X] A. INTEGER
   - [ ] B. OTEXT
   - [ ] C. VARCHAR
   - [ ] D. LONGTEXT

5. Perintah command line mana yang menunjukkan struktur tabel SQLite?
   - [ ] A. .column
   - [X] B. .schema
   - [ ] C. .header on
   - [ ] D. .mode column

6. Pilih command SQLite untuk memodifikasi data yang sudah ter-records pada table?
   - [X] A. UPDATE
   - [ ] B. MODIFY
   - [ ] C. CHANGE
   - [ ] D. ALTER

7. Bagaimana kita menghapus data yang telah ter-record menggunakan SQLite?
   - [ ] A. DELETE
   - [X] B. DELETE FROM
   - [ ] C. REMOVE
   - [ ] D. REMOVE FROM

8. Pilih mana yang BUKAN statement yang kita gunakan untuk mem-filter data?
   - [ ] A. LIKE
   - [ ] B. LIMIT
   - [ ] C. WHERE
   - [X] D. GROUP BY

9. Apa yang dikembalikan oleh statement SQL berikut? `SELECT * FROM Employees WHERE EmployeeName LIKE 'a%'`
   - [ ] A. Ini me-records dalam tabel Employees di mana nilai dalam kolom EmployeeName tidak memiliki "a".
   - [X] B. Ini me-records dalam tabel Employees di mana nilai dalam kolom EmployeeName dimulai dengan "a".
   - [ ] C. Ini me-records dalam tabel Employees di mana nilai dalam kolom EmployeeName memiliki "a".
   - [ ] D.  Ini me-records dalam tabel Employees di mana nilai dalam kolom EmployeeName diakhiri dengan "a".

10.  Dalam **SELECT * FROM clients;** apa yang menjadi representasi dari clients?
     - [ ] A. a SQL query
     - [ ] B. a SQL statement
     - [ ] C. a database
     - [X] D. a table

11.  Jika kita butuh order pada tabel movies berdasarkan name, kueri mana yang akan berfungsi?
        - [ ] A. SELECT * FROM movies GROUP BY name
        - [X] B. SELECT * FROM movies ORDER BY name
        - [ ] C. SELECT * FROM movies ORDER TABLE by name
        - [ ] D. SELECT * FROM movies FILTER BY name

12.  Jika bekerja dengan tabel yang sangat besar di database. SQL mana yang digunakan untuk mencegah hasil kueri yang terlalu besar?
UNIK
        - [ ] A. UNIQUE
        - [X] B. LIMIT
        - [ ] C. DISTINCT
        - [ ] D. CONSTRAINT

13.  Bagaimana kita mem-filter data duplicate saat mengambil data pada table?
        - [X] A. DISTINCT
        - [ ] B. WHERE
        - [ ] C. LIMIT
        - [ ] D. AS

14.  Bagaimana Anda memilih setiap baris dalam tabel yang diberi nama "inventory"?
        - [ ] A. SELECT all FROM inventory;
        - [ ] B. FROM inventory SELECT all;
        - [ ] C. FROM inventory SELECT *;
        - [X] D. SELECT * FROM inventory;

15. Relasional harus dirancang secara efisien pada database, apa yang  harus dimiliki oleh setiap tabel?
    - [ ] A. set of triggers
    - [ ] B. sequential id field
    - [ ] C. minimum of three columns
    - [X] D. primary key

16.  Manakah sintaks yang benar dari untuk insert statement?
        - [ ] A. insert into cars (make, model, year) values ('Ford', 'Mustang', 2002) ('Mercedes', 'C', 2003);
        - [ ] B. insert into cars (make, model, year) values ('Ford', 'Mustang', 2002) values ('Mercedes', 'C', 2003);
        - [ ] C. insert into cars (make, model, year) extended ('Ford', 'Mustang', 2002), ('Mercedes', 'C', 2003);
        - [X] D. insert into cars (make, model, year) values ('Ford', 'Mustang', 2002), ('Mercedes', 'C', 2003);