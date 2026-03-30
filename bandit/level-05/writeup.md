# Bandit Level 5 → Level 6

## Goal
Tujuan challenge: 
Mencari file berisi password tersembunyi yang tersimpan di directory yang
terdapat banyak file palsu/pancingan untuk mengecoh

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Mencari file dengan ketentuan yang sudah di berikan

## Approach
Cara berpikir untuk menyelesaikan challenge.
Ketentuan yang diberikan adalah
1. Human-readable
2. 1033 bytes in size
3. not executable

Dengan ciri ciri file di atas maka kita bisa menemukan nya menggunakan
command find dengan option/flag tambahan
-type f = digunakan untuk menampilkan reguler file
-readable = digunakan untuk mencari file yang dapat dibaca
-size 1033c = digunakan untuk menentukan suatu ukuran file yang kita cari
! -executable = digunakan untuk mencari file yang tidak bisa di eksekusi oleh
pengguna (jika tidak ada tanda "!" maka fungsi nya akan berkebalikan)

## Commands
ssh bandit5@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls 
find -type f -readable -size 1033c ! -executable
cat ./maybehere07/.file2


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Masuk ke directory `inhere`

```bash
cd inhere
```

4. Lihat semua isi directory

```bash
ls 
```

5. Cari file dengan ketentuan yang di minta

```bash
find -type f -readable -size 1033c ! -executable
```

Output menunjukkan file yang sesuai:

```
./maybehere07/.file2

```

6. Buka file

```bash
cat ./maybehere07/.file2
```


## Password
```
password-next-level
```
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan command "find" untuk mencari file dengan ketentuan yang kita 
inginkan

## New Commands Learned
Command baru yang dipelajari:

-find (mencari file dengan ketentuan yang kita inginkan dengan menambahkan
flag / option tertentu)