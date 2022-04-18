# Video Online Course:
- Recursive Function: https://www.youtube.com/watch?v=KgUidUhp8XQ
- Go Konkurensi 101 - Mengenal Primitif Konkurensi di Golang: https://www.youtube.com/watch?v=sqZRLHw3ihk&t=11s
- Go Konkurensi 101 - Belajar Konkurensi Sambil Bermain Ping-Pong: https://www.youtube.com/watch?v=hdAUI3-3OEM

# Quizz Golang

## Online Course Complexity Analysis:

1. Algoritma mana yang paling cepat dalam mencari element di array?
    - [X] A. Binary search
    - [ ] B. Linear search
    - [ ] C. Brute force
    - [ ] D. Sequential search

2. Time complexity mana yang paling lambat (n < 10)?
    - [ ] A. O(2^n)
    - [ ] B. O(e^n)
    - [ ] C. O(n^3logn)
    - [X] D. O(n^4)

3. Time complexity mana yang paling lambat (n > 1,000)?
    - [ ] A. O(2^n)
    - [X] B. O(e^n)
    - [ ] C. O(n^3logn)
    - [ ] D. O(n^4)

4. Kode mana yang memiliki kompleksitas waktu O(n^3)?
    - [ ] A.
        ```go
        for (i:=1; i < N; i++) {
            for (j:=0; j < 3; j++) {   
                for (k:=0; k < N; k++) {
                    // do something
            } } }
        ```
    - [ ] B. 
        ```go
        for (i:=1; i < 3; i++) {
            for (j:=0; j < 10; j++) {   
                for (k:=0; k < N; k++) {
                    // do something
                } } }
        ```
    - [X] C.
        ```go
        for (i:=1; i < N; i++) {
            for (j:=0; j < N; j++) {   
                for (k:=0; k < N; k++) {
                    // do something
                } } }
        ```
    - [ ] D. 
        ```go
        for (i:=1; i < N; i++) {
            for (j:=0; j < N; j++) { 
                // do something
            }
        }
        ```
5. Perhatikan data dibawah ini:
    ```
    {
        "key1": "data1",
        "key2": "data2",
        ...
        "key1M": "data1M",
    }
    ```

    Berapa time complexity dan space complexity untuk mengakses data dari hashMap ?
    - [ ] A. O(1) dan O(1)
    - [X] B. O(1) dan O(n)
    - [ ] C. O(n) dan O(1)
    - [ ] D. O(n) dan O(n)

6. Algoritma manakah yang memiliki O(n log n)
    - [ ] A. Bubble Sort
    - [ ] B. Bellman ford
    - [X] C. Merge sort
    - [ ] D. Melakukan cek palindrom

7. Perhatikan code dibawah ini
    ```go
    func search(nums []int, target int) int {
        var i, j = 0, len(nums) - 1
        for i <= j {
            var mid = i + (j - i) / 2
            if nums[mid] == target {
                return mid
            }
            if target > nums[mid] {
                i = mid + 1
            } else {
                j = mid - 1
            }
        }    
        return -1
    }
    ```
    Kompleksitas apa yang dimiliki oleh algoritma ini?
    - [ ] A. O(n)
    - [X] B. O(log n)
    - [ ] C. O(n log n)
    - [ ] D. O(1)

## Online Course Recursion:

1. Apa itu Recursion?
    - [ ] A. Suatu urutan atau lebih dari langkah algoritmik dilakukan di loop program
    - [X] B. Ketika suatu fungsi yang memanggil dirinya sendiri
    - [ ] C. unit dasar dari pemanfaatan CPU
    - [ ] D. Struktur tata bahasa yang umum digunakan untuk menggambarkan konsekuensi dari suatu kondisi atau situasi

2. Kapan menggunakan Recursion?
    - [ ] A. Input data ke database
    - [ ] B. Mengkonversi sebuah type data string menjadi type data number
    - [ ] C. Menyelesaikan masalah dengan time complexity yang rendah
    - [X] D. Menyelesaikan permasalahan yang memiliki keteraturan pola dalam prosesnya

3. Syntax mana yang menggambarkan Recursion?
    - [ ] A.
        ```go
        var recursion = [length]datatype{values}
        ```
    - [ ] B.
        ```go
        if condition {
            // code recursion in here
        }
        ```
    - [ ] C.
        ```go
        for statement1; statement2; statement3 {
            // code recursion in here
        }
        ```
    - [X] D.
        ```go
        func recurse() {
            … …
            … …
            recurse()
        }
        ```

4. Manakah yang bukan merupakan jenis Recursion?
    - [X] A. Boom Recursion
    - [ ] B. Tail Recursion
    - [ ] C. Indirect Recursion
    - [ ] D. Direct Recursion

5. Recursion tidak cocok digunakan jika dalam kondisi?
    - [X] A. Jika time complexity adalah titik fokus
    - [ ] B. Jika time complexity bukan masalah
    - [ ] C. Jika permasalahan yang memiliki keteraturan pola dalam prosesnya
    - [ ] D. Jika ingin mempersingkat kode


## Online Concurency:

1. Apa itu Goroutin?
    - [X] A. Lightweight thread yang dikelola oleh runtime Go.
    - [ ] B. Sebuah kanal yang digunakan oleh konkuren goroutine untuk berkomunikasi.
    - [ ] C. Instance dari program yang sedang berjalan
    - [ ] D. Entitas dalam process yang dapat dieksekusi secara independen

2. Perhatikan code dibawah ini:
    ```go
    func say(s string) {
        for i := 0; i < 5; i++ {
            time.Sleep(100 * time.Millisecond)
            fmt.Println(s)
        }
    }

    func main() {
        go say("world")
        say("hello")
    }
    ```
    Kenapa "hello" dan "world" tidak muncul dalam urutan yang sama dengan kode?
    - [ ] A. Goroutin dieksekusi dengan waktu yang sudah ditentukan
    - [ ] B. Goroutin selalu menjalankan fungsi sebelum main function
    - [X] C. Goroutin dieksekusi dengan waktu yang tidak bisa ditentukan
    - [ ] D. Goroutin tidak selalu menjalankan fungsi sebelum main function

3. Perhatikan code dibawah ini:
    ```go
    func say(s string) {
        for i := 0; i < 5; i++ {
            time.Sleep(100 * time.Millisecond)
            fmt.Println(s)
        }
    }

    func main() {
        go say("world")
    }
    ```
    Ada berapa "world" yang muncul dengan program ini?
    - [ ] A. 5
    - [ ] B. 6
    - [ ] C. 4 
    - [X] D. Program exited.

4. Apa itu Channel?
    - [ ] A. Lightweight thread yang dikelola oleh runtime Go.
    - [X] B. Sebuah kanal yang digunakan oleh konkuren goroutine untuk berkomunikasi.
    - [ ] C. Instance dari program yang sedang berjalan
    - [ ] D. Entitas dalam process yang dapat dieksekusi secara independen

5. Perhatikan code dibawah ini menggunakan channel untuk mengirim dan menerima data:
    ```go
    func sum(s []int, c chan int) {
        sum := 0
        for _, v := range s {
            sum += v
        }
        c <- sum // send sum to c
    }

    func main() {
        s := []int{7, 2, 8, -9, 4, 0}

        c := make(chan int)
        go sum(s[:len(s)/2], c)
        go sum(s[len(s)/2:], c)
        x, y := <-c, <-c // receive from c

        fmt.Println(x, y, x+y)
    }
    ```
    Apa output dari program diatas?
    - [ ] A. -2 34 20 
    - [ ] B. -5 18 12
    - [X] C. -5 17 12
    - [ ] D. -6 17 13

6. Perhatikan code dibawah ini:
    ```go
    package main

    import "fmt"

    func main() {
        c := make(chan bool)
        c <- true

        fmt.Println("this line will never be printed")
    }
    ```
    Code diatas akan menghasilkan `fatal error: all goroutines are asleep - deadlock!`. Mengapa demikian?
    - [ ] A. Pengiriman dan penerimaan channel akan terbuka hingga sisi yang lain siap untuk menerima atau mengirimkan data.
    - [X] B. Pengiriman dan penerimaan channel akan terkunci hingga sisi yang lain siap untuk menerima atau mengirimkan data.
    - [ ] C. Pengiriman channel selalu terjadi error saat digunakan
    - [ ] D. Pengiriman channel akan dibuka saat data bernilai string

7. Disebut apakah Channel dengan jumlah buffer 0?
    - [ ] A. Range Channel
    - [ ] B. Close Channel
    - [X] C. Rendezvous Channel
    - [ ] D. Anonymous Channel

8. Pengirim (sender) bisa menutup (close) channel untuk mengindikasikan tidak ada lagi value untuk dikirimkan. Penerima (receiver) dapat mengecek apakah sebuah channel sudah ditutup dengan cara? 
    - [X] A. `v, ok := <-ch` ok bernilai false jika channel sudah ditutup
    - [ ] B. `v, ok := <-ch` v bernilai false jika channel sudah ditutup
    - [ ] C. `v, ok := <-ch` ok bernilai true jika channel sudah ditutup
    - [ ] D. `v := <-ch` v bernilai true jika channel sudah dibuka