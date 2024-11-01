
# Workflow Kerja Kelompok Menggunakan Git dan GitHub

## 1. Setup
- **Instalasi Git**:
  - Download dan instal Git dari [git-scm.com](https://git-scm.com/downloads). Setelah instalasi, buka terminal atau command prompt dan ketik `git --version` untuk memastikan Git telah terinstal.
- **Konfigurasi Git**:
  - Konfigurasikan nama dan email yang akan digunakan dalam setiap commit:
    ```bash
    git config --global user.name "Nama Anda"
    git config --global user.email "email@domain.com"
    ```
- **Membuat Repository di GitHub**:
  - Login ke akun GitHub, klik tombol "New Repository", beri nama repository, deskripsi, pilih visibilitas (public atau private), dan klik "Create Repository".

## 2. Invite Collaborator
- **Menambahkan Kolaborator**:
  - Di GitHub, buka repository yang telah dibuat.
  - Masuk ke **Settings** > **Collaborators**.
  - Ketik username atau email anggota tim, lalu klik "Add collaborator".
- **Penerimaan Undangan**:
  - Kolaborator akan menerima email undangan dan perlu menyetujuinya agar mendapatkan akses kontribusi ke repository.

## 3. Forking Repository
- **Fork Repository**:
  - Fork adalah menyalin repository orang lain ke akun kita untuk pengembangan yang terpisah.
  - Pada halaman repository GitHub, klik tombol **Fork** di bagian kanan atas.
  - Setelah fork, repository akan tersalin ke akun GitHub pribadi kolaborator dengan semua data dan commit yang sama.

## 4. Clone Repository
- **Meng-clone Repository**:
  - Clone adalah mengunduh repository dari GitHub ke komputer lokal agar bisa dikerjakan secara offline.
  - Buka terminal dan masukkan perintah berikut dengan URL repository yang ingin di-clone:
    ```bash
    git clone https://github.com/username/reponame.git
    ```
  - Setelah clone selesai, masuk ke folder repository tersebut:
    ```bash
    cd reponame
    ```

## 5. Branching
- **Membuat Branch Baru**:
  - Branching digunakan untuk membuat cabang pengembangan yang terpisah dari branch utama (biasanya `main` atau `master`).
  - Untuk membuat dan berpindah ke branch baru:
    ```bash
    git checkout -b nama-branch
    ```
- **Daftar Branch**:
  - Melihat daftar branch yang ada di repository:
    ```bash
    git branch
    ```
- **Berpindah Branch**:
  - Untuk berpindah ke branch lain:
    ```bash
    git checkout nama-branch
    ```

## 6. Push ke Repository
- **Push Perubahan ke Repository Remote**:
  - Setelah melakukan perubahan, gunakan perintah berikut untuk menyimpan perubahan lokal ke GitHub:
    ```bash
    git add .
    git commit -m "Pesan commit"
    git push origin nama-branch
    ```
- **Penjelasan Singkat**:
  - `git add .` untuk menambah semua perubahan.
  - `git commit -m "Pesan"` untuk menyimpan perubahan dengan deskripsi singkat.
  - `git push origin nama-branch` untuk mengunggah perubahan ke GitHub pada branch tertentu.

## 7. Pull Request
- **Apa itu Pull Request (PR)**:
  - Pull request digunakan untuk mengajukan penggabungan branch kita dengan branch utama di repository.
  - Pada GitHub, buka repository Anda, pilih branch yang ingin di-pull request, lalu klik **New Pull Request**.
  - Beri deskripsi singkat tentang perubahan yang dilakukan, lalu klik **Create Pull Request**.

## 8. Merge Pull Request
- **Menggabungkan (Merge) Pull Request**:
  - Pemilik atau kolaborator repository akan mengecek PR yang diajukan.
  - Jika sudah diperiksa dan siap digabungkan, klik **Merge Pull Request** pada halaman PR.
  - Klik **Confirm Merge** untuk menggabungkan branch ke branch utama.
- **Menghapus Branch Setelah Merge** (Opsional):
  - Setelah PR berhasil di-merge, Anda bisa menghapus branch lama dengan klik **Delete Branch**.

## 9. Resolve Conflict
- **Apa itu Conflict**:
  - Conflict terjadi ketika dua perubahan pada branch yang berbeda berbenturan di file atau baris yang sama.
- **Mengatasi Conflict**:
  - Saat melakukan merge, Git akan menunjukkan file mana yang memiliki konflik.
  - Buka file yang mengalami konflik, biasanya akan ditandai dengan tanda:
    ```
    <<<<<<< HEAD
    (kode pada branch saat ini)
    =======
    (kode pada branch lain)
    >>>>>>> nama-branch
    ```
  - Edit dan tentukan kode mana yang ingin disimpan, lalu hapus tanda-tanda tersebut.
  - Setelah selesai, simpan perubahan, tambahkan, dan commit:
    ```bash
    git add .
    git commit -m "Menyelesaikan konflik"
    ```

## 10. Fetch dan Pull Update
- **Fetch**:
  - `fetch` digunakan untuk mengambil informasi terbaru dari repository remote tanpa menggabungkan ke branch lokal. Ini berguna untuk melihat perubahan apa yang terjadi di branch remote sebelum menggabungkannya.
    ```bash
    git fetch origin
    ```
- **Pull**:
  - `pull` digunakan untuk mengambil perubahan terbaru dari branch remote dan menggabungkannya ke branch lokal.
    ```bash
    git pull origin nama-branch
    ```

---
