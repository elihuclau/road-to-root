# Bandit Level 7 → Level 8

## Goal
Tujuan challenge: 
Mencari password tersembunyi pada file data.txt

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Pada file data.txt ada banyak tulisan acak yang tidak human-readable, tugas 
kita mencari password yang diawali dengan karakter "="

## Approach
Cara berpikir untuk menyelesaikan challenge.
Untuk menyelesaikan level ini kita menggunakan 2 command yaitu strings & grep
strings = digunakan untuk mengekstrak urutan karakter yang bisa di cetak
grep = digunakan untuk mencari baris yang memiliki unsur karakter yang kita
minta


## Commands
ssh bandit9@bandit.labs.overthewire.org -p 2220
ls
strings data.txt | grep ===


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Cari password meggunakan command strings & grep

```bash
strings data.txt | grep ===
```

Output menunjukkan baris yang memiliki 3 karakter "=" pada baris tersebut:

```
========== the
========== password
f\Z'========== is
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```


## Password
```
password-next-level
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- mengekstrak urutan baris pada file data.txt menggunakan straing lalu
 menyaring nya menggunakan command grep

## New Commands Learned
Command baru yang dipelajari:

-strings (digunakan mengekstrak urutan baris yang dapat dicetak