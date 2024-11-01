
# Materi Pelatihan Dasar Pemrograman Python

## 1. Setup Environment
- **Instalasi Python**: 
  - Download dan instal Python dari [python.org](https://www.python.org/downloads/). Pastikan untuk mencentang opsi "Add Python to PATH" saat instalasi.
- **IDE**: 
  - **VS Code**: Cukup populer dan mudah digunakan. Instal VS Code dan Python Extension.
  - **Jupyter Notebook**: Cocok untuk interaktif coding. Instal dengan `pip install jupyter` dan jalankan dengan perintah `jupyter notebook`.
- **Cek Instalasi**:
  - Buka terminal atau command prompt, ketik `python --version` atau `python3 --version` untuk memastikan Python terinstal dengan benar.
  - Coba jalankan kode berikut untuk mengetes apakah Python sudah siap:
    ```python
    print("Hello, Python!")
    ```

## 2. Variabel dan Tipe Data
- **Variabel**: Tempat untuk menyimpan nilai. Dalam Python, variabel didefinisikan langsung tanpa perlu deklarasi tipe.
  ```python
  nama = "Andi"
  umur = 25
  ```
- **Tipe Data Dasar**:
  - **Integer**: Angka bulat, contoh: `x = 10`
  - **Float**: Angka desimal, contoh: `y = 3.14`
  - **String**: Teks, contoh: `nama = "Python"`
  - **Boolean**: Nilai benar/salah, contoh: `is_active = True`
- **Fungsi `type()`**:
  - Untuk mengetahui tipe data dari variabel:
    ```python
    print(type(nama))   # Output: <class 'str'>
    print(type(umur))   # Output: <class 'int'>
    ```

## 3. Operator
- **Operator Aritmatika**:
  - `+` (tambah), `-` (kurang), `*` (kali), `/` (bagi), `**` (pangkat), `%` (modulus)
    ```python
    a = 10
    b = 3
    print(a + b)  # Output: 13
    print(a ** b) # Output: 1000
    ```
- **Operator Perbandingan**:
  - `==`, `!=`, `>`, `<`, `>=`, `<=`
    ```python
    print(a > b)  # Output: True
    print(a == b) # Output: False
    ```
- **Operator Logika**:
  - `and`, `or`, `not`
    ```python
    is_student = True
    has_id = False
    print(is_student and has_id)  # Output: False
    print(is_student or has_id)   # Output: True
    ```

## 4. Struktur Kontrol
- **Kondisi (if, elif, else)**:
  - Struktur dasar untuk pengambilan keputusan.
    ```python
    age = 20
    if age >= 18:
        print("Dewasa")
    elif age >= 13:
        print("Remaja")
    else:
        print("Anak-anak")
    ```
- **Perulangan (for dan while)**:
  - **for loop** untuk iterasi yang terdefinisi:
    ```python
    for i in range(5):
        print(i)
    ```
  - **while loop** untuk iterasi berdasarkan kondisi:
    ```python
    count = 0
    while count < 5:
        print(count)
        count += 1
    ```

## 5. Fungsi
- **Definisi Fungsi**:
  - Fungsi dibuat dengan keyword `def`, diikuti dengan nama fungsi dan parameter opsional.
    ```python
    def sapa(nama):
        print(f"Halo, {nama}!")
    ```
- **Memanggil Fungsi**:
    ```python
    sapa("Budi")  # Output: Halo, Budi!
    ```
- **Fungsi dengan Nilai Kembali (`return`)**:
    ```python
    def tambah(a, b):
        return a + b

    hasil = tambah(10, 5)
    print(hasil)  # Output: 15
    ```

## 6. List
- **Pengenalan List**:
  - List adalah kumpulan data terurut yang dapat diubah dan bisa menampung berbagai tipe data.
    ```python
    angka = [1, 2, 3, 4, 5]
    nama = ["Andi", "Budi", "Cici"]
    ```
- **Akses Elemen List**:
    ```python
    print(nama[0])   # Output: Andi
    print(angka[-1]) # Output: 5
    ```
- **Operasi pada List**:
  - Menambah elemen: `list.append()`
  - Menghapus elemen: `list.remove()`, `list.pop()`
    ```python
    angka.append(6)  # Menambahkan angka 6
    print(angka)     # Output: [1, 2, 3, 4, 5, 6]
    angka.pop()      # Menghapus elemen terakhir
    print(angka)     # Output: [1, 2, 3, 4, 5]
    ```

## 7. Praktikum
- **Latihan Praktik**:
  1. **Kalkulator Sederhana**:
     - Buat program kalkulator sederhana yang bisa menerima dua angka dari pengguna dan melakukan operasi tambah, kurang, kali, atau bagi berdasarkan input.
     ```python
     def kalkulator():
         angka1 = float(input("Masukkan angka pertama: "))
         operasi = input("Masukkan operasi (+, -, *, /): ")
         angka2 = float(input("Masukkan angka kedua: "))

         if operasi == '+':
             hasil = angka1 + angka2
         elif operasi == '-':
             hasil = angka1 - angka2
         elif operasi == '*':
             hasil = angka1 * angka2
         elif operasi == '/':
             hasil = angka1 / angka2
         else:
             print("Operasi tidak valid")
             return

         print("Hasil:", hasil)

     kalkulator()
     ```
  2. **Program Mengelola Data Siswa**:
     - Buat list kosong untuk menyimpan data nama siswa. Buat fungsi untuk menambah siswa baru ke dalam list, menghapus siswa, dan menampilkan semua siswa.
     ```python
     siswa = []

     def tambah_siswa(nama):
         siswa.append(nama)
         print(f"{nama} telah ditambahkan.")

     def hapus_siswa(nama):
         if nama in siswa:
             siswa.remove(nama)
             print(f"{nama} telah dihapus.")
         else:
             print(f"{nama} tidak ditemukan.")

     def tampilkan_siswa():
         print("Daftar Siswa:")
         for nama in siswa:
             print(f"- {nama}")

     # Contoh pemakaian
     tambah_siswa("Andi")
     tambah_siswa("Budi")
     tampilkan_siswa()
     hapus_siswa("Andi")
     tampilkan_siswa()
     ```

Selamat mengajar! Semoga sukses dengan materi ini!
