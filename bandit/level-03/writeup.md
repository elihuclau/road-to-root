# Bandit Level 3 → Level 4

## Goal
Tujuan challenge: 
Mencari file tersembunyi yang berada di direktori (inhere)

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Mencari file yang di sembunyikan dalam direktori (inhere) yang tidak muncul
jika hanya menggunakan command (ls) biasa

## Approach
Cara berpikir untuk menyelesaikan challenge.
Jika "ls" biasa tidak bisa memunculkan file tersembunyinya maka kita harus 
menambahkan option / flag pada command, contohnya di level ini kita akan
menggunakan -la

## Commands
ssh bandit3@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls-la
cat ...Hiding-From-You


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Masuk ke directory `inhere`

```bash
cd inhere
```

4. Tampilkan file tersembunyi

```bash
ls -la
```

Output menunjukkan file:

```
...Hiding-From-You
```

5. Baca isi file untuk mendapatkan password

```bash
cat ...Hiding-From-You
```



## Password
```
password-next-level
```
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan Flag / Option -la pada command "ls" untuk memunculkan file
tersembunyi

## New Commands Learned
Command baru yang dipelajari:

-"ls -la" (untuk memunculkan hidden file