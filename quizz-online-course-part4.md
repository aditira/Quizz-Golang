# Quizz Golang

## Online Course I/O and JSON

1. Which ioutil function is used to read a file by name?
    - [ ] A. 
        ```go 
        func ReadAll(r io.Reader) ([]byte, error) {
            return io.ReadAll(r)
        }
        ```
    - [X] **B.**
        ```go 
        func ReadFile(filename string) ([]byte, error) {
            return os.ReadFile(filename)
        }
        ```
    - [ ] C.
        ```go 
        func WriteFile(filename string, data []byte, perm fs.FileMode) error {
            return os.WriteFile(filename, data, perm)
        }
        ```
    - [ ] D.
        ```go 
        func NopCloser(r io.Reader) io.ReadCloser {
            return io.NopCloser(r)
        }
        ```
2. Look at the code below:
    ```go
    f, err := os.OpenFile("namaFile.txt", os.O_APPEND|os.O_WRONLY, 0644)
    if err != nil {
        log.Printf("failed opening file: %s", err)
    }

    defer f.Close()
    ```
    What does the OpenFile function do?
    - [ ] A.  OpenFile returns the default directory to use for temporary files.
    - [ ] B. OpenFile returns the default root directory to use for user-specific
    - [ ] C. OpenFile returns the number of bytes written and an error, if any
    - [X] **D.**  OpenFile is the generalized open call, most users will use Open or Create instead

3. The code in question no 2. The OpenFile function has 3 parameters, namely?
    - [X] **A.** (name string, flag int, perm FileMode)
    - [ ] B. (oldpath string, newpath int, perm FileInfo)
    - [ ] C. (name string, mode FileMode, flag int)
    - [ ] D. (perm string, flag int, pages Getpagesize)

4. The code in question no 2, the os.O_APPEND and os.O_WRONLY flags function as?
    - [ ] A. open the file read-only and and open the file write-only
    - [ ] B. append data to the file when writing and open for synchronous I/O
    - [X] **C.** append data to the file when writing and open the file write-only
    - [ ] D. truncate regular writable file when opened and open the file write-only
5. The code in question no 2, the third parameter of the OpenFile function is 0644 for what purpose?
    - [ ] A. FileInfo describes a file and is returned by Stat and Lstat.
    - [X] **B.** FileMode represents a file's mode and permission bits.
    - [ ] C. File represents an open file descriptor.
    - [ ] D. Getpagesize returns the underlying system's memory page size.

6.  Look at the code below:
    ```go
       type student struct {
            Name  string `json:"nama"`
            Score int    `json:"nilai"`
            Class string `json:"kelas"`
        }

        func main() {
            fileName := "siswa"
            arif := student{Name: "arif", Score: 90, Class: "c"}
            andi := student{Name: "andi", Score: 85, Class: "c"}
            newData := []student{arif, andi}
            JSON(fileName, newData)
            reset(fileName)
        }

        func JSON(fileName string, data []student) error {
            path, err := filepath.Abs(fileName + ".json")
            if err != nil {
                return err
            }
            file, err := openFile(path)
            if err != nil {
                return err
            }
            defer file.Close()
            jsonData, _ := json.Marshal(data)
            ioutil.WriteFile(path, jsonData, 0644)
            return nil
        }

        func openFile(path string) (*os.File, error) {
            file, err := os.OpenFile(path, os.O_RDWR|os.O_CREATE, os.ModePerm)
            if err != nil {
                return nil, err
            }
            return file, nil
        }

        func reset(fileName string) {
            os.Remove(fileName + ".json")
        }

        func (s student) String() string {
            return fmt.Sprintf("name: %v\nscore: %v\nclass: %v\n", s.Name, s.Class, s.Score)
        }

    ```
    What is the main purpose of the code above?
    - [ ] A. To delete json file
    - [ ] B. To update json file
    - [ ] C. To read json file
    - [X] **D.** To write json file 

7. Look at the code below:
    ```go
    type Barang struct {
        Nama        string `json:"nama"`
        Harga       int    `json:"harga"`
        JenisBarang string `json:"jenis_barang"`
    }

    func main() {
        jsonString := `{"nama": "AAA", "harga": 78000, "jenis_barang": "Makanan"}`
        jsonData := []byte(jsonString)

        var Bar Barang

        err := json.Unmarshal(jsonData, &Bar)
        if err != nil {
            fmt.Println(err)
        }

        fmt.Println(Bar.Nama)
        fmt.Println(Bar.Harga)
        fmt.Println(Bar.JenisBarang)
    }
    ```
    What is the main purpose of the code above?
    - [ ] A. Encode Object to JSON  
    - [ ] B. Decode JSON to Interface
    - [ ] C. Decode JSON to MapStringInterface
    - [X] **D.** Decode JSON to Object


8. Look at the code below:
    ```go
    type Barang struct {
        Nama        string `json:"nama"`
        Harga       int    `json:"harga"`
        JenisBarang string `json:"jenis_barang"`
    }

    func main() {
        jsonString := `[
            {"nama": "AAA", "harga": 78000, "jenis_barang": "Makanan"},
            {"nama": "BBB", "harga": 88000, "jenis_barang": "Minuman"},
            {"nama": "CCC", "harga": 98000, "jenis_barang": "Makanan"},
            {"nama": "DDD", "harga": 108000, "jenis_barang": "Minuman"}
        ]`
        jsonData := []byte(jsonString)

        var Bar []Barang

        err := json.Unmarshal(jsonData, &Bar)
        if err != nil {
            fmt.Println(err)
        }

        for _, v := range Bar {
            fmt.Println("Nama barang", v.Nama)
            fmt.Println("Harga barang", v.Harga)
        }
    }
    ```
    What is the main purpose of the code above?
    - [ ] A. Decode JSON to Object
    - [X] **B.** Decode Array JSON to Object
    - [ ] C. Encode Object to JSON 
    - [ ] D. Decode JSON to MapStringInterface

9.  Look at the code below:
    ```go
        func main() {
            jsonString := `{"nama": "AAA", "harga": 78000, "jenis_barang": "Makanan"}`
            jsonData := []byte(jsonString)

            var Bar map[string]interface{}

            err := json.Unmarshal(jsonData, &Bar)
            if err != nil {
                fmt.Println(err)
            }

            fmt.Println(Bar["jenis_barang"])
            fmt.Println(Bar["harga"])
        }
    ```
    What is the main purpose of the code above?
    - [X] **A.** Decode JSON to MapStringInterface
    - [ ] B. Decode JSON to Objec
    - [ ] C. Decode JSON to Interface
    - [ ] D. Encode Object to JSON 

10. Look at the code below:
    ```go
        func main() {
            jsonString := `{"nama": "AAA", "harga": 78000, "jenis_barang": "Makanan"}`
            jsonData := []byte(jsonString)

            var Bar interface{}

            err := json.Unmarshal(jsonData, &Bar)
            if err != nil {
                fmt.Println(err)
            }

            decodeBar := Bar.(map[string]interface{})

            fmt.Println(decodeBar["nama"])
        }
    ```
    What is the main purpose of the code above?
    - [ ] A. Decode Array JSON to Object
    - [ ] B. Decode JSON to MapStringInterface
    - [X] **C.** Decode JSON to Interface
    - [ ] D. Decode JSON to Object
