# Bandit Level 2 → Level 3

## Goal
Tujuan challenge: 
Membuka isi file yang terdapat karakter (-) dan (spasi) di nama file nya


## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Kasusnya sama seperti bandit 1, dimana kita harus mencari password yang 
tersembunyi pada file bernama (--spaces in this filename--)

Untuk membuka file tersebut, kita perlu menggunakan karakter tambahan 
karena nama file mengandung karakter khusus dan spasi

Karakter yang digunakan

< : digunakan untuk memproses pada karakter (-)
' ': digunakan supaya spasi di dalam nama file dapat di baca sebagai 
satu kesatuan nama file

## Approach
Cara berpikir untuk menyelesaikan challenge.
menggunakan karakter tambahan (<) untuk memproses karakter (-) yang terdapat
pada nama file, lalu menggunakan karakter (' ') supaya spasi di bisa terbaca
sebagai nama file


## Commands
```bash
command1 ssh bandit1@bandit.labs.overthewire.org -p 2220
command2 ls
command3 cat <'--spaces in this filename--'
```



## Solution Steps

1.
```bash
command
```

2.
```bash
command
```

3.
```bash
command
```



## Password
```
password-next-level
```
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- beberapa karakter khusus memerlukan karakter tambahan 
(escape character) agar dapat diproses atau ditampilkan dengan benar



## New Commands Learned
Command baru yang dipelajari:

- < : untuk membaca karakter (-)
- ' ' : untuk membaca spasi pada filename
- 
