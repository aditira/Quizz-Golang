# Quizz Golang

## Online Course I/O

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



