# Bandit Level 7 → Level 8

## Goal
Tujuan challenge: 
Mencari password pada file data.txt

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Pada file data.txt terdapat banyak password acak yang berulang, tetapi
password yang benar hanya 1x pengulangan

## Approach
Cara berpikir untuk menyelesaikan challenge.
Untuk menselesaikan challenge ini kita menggunakan 2 command,
yaitu sort & uniq
sort = digunakan untuk mengurutan text yang ada di file tersebut
uniq = untuk menyaring, menghapus baris-baris yang berdekatan dan duplikat

dengan tambahan flag / option pada command uniq
-u = untuk menampilkan baris yang tidak memiliki duplikat

## Commands
ssh bandit8@bandit.labs.overthewire.org -p 2220
ls
sort data.txt | uniq -u


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Cari password meggunakan command sort & uniq

```bash
sort data.txt | uniq -u
```

Output menunjukkan password yang tidak memiliki duplikat:

```
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```


## Password
```
password-next-level
```
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- menggunakan command sort & uniq untuk mengurutkan text lali menyaring nya

## New Commands Learned
Command baru yang dipelajari:

-sort (mengurutkan baris)
-uniq (menyaring, menghapus baris)