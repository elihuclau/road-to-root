# Bandit Level 11 → Level 12

## Goal
Tujuan challenge: 
Mencari password yang teks nya telah di ubah menggunkan cipher type ROT13

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Pada file data.txt terdapat password yang teks ya diacak menggunakan subtitution cipher

## Approach
Cara berpikir untuk menyelesaikan challenge.
Dengan menggunakan command tr untuk memecahkan cipher dengan jenis ROT13
dengan analogi :
diapply 1x menjadi terenkripsi
diapply lagi balik ke normal

## Commands
ssh bandit10@bandit.labs.overthewire.org -p 2220
ls
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

## Solution Steps

1. Login ke server bandit

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Balikan enkripsi nya ke normal

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

Output menunjukkan hasil decode dari file yang terencode:

```
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```


## Password
```
password-next-level
```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan tr untuk menyelesaikan masalah ROT13

## New Commands Learned
Command baru yang dipelajari:

-tr (untuk translate teks yang diubah)
