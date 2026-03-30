# Bandit Level 7 → Level 8

## Goal
Tujuan challenge: 
Mencari password pada file .txt yang memiliki banyak data di dalam nya

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Mencari password pada file .txt yang berada di sebelah kata "millionth"

## Approach
Cara berpikir untuk menyelesaikan challenge.
Dikarenakan file ini memiliki ribuan data di dalam nya, kita bisa menggunakan
command grep untuk mencari kata spesifik yang kita inginkan pada file 
tertentu

## Commands
ssh bandit7@bandit.labs.overthewire.org -p 2220
ls
grep "millionth" data.txt


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Cari password meggunakan kata kunci yang telah di berikan

```bash
grep "millionth" data.txt
```

Output menunjukkan kata kunci dan password yang berada tepat di sebelah nya:

```
millionth	dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```


## Password
```
password-next-level
```
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan command "grep" untuk mencari kata tertentu yang kita inginkan

## New Commands Learned
Command baru yang dipelajari:

-grep (mencari kata pada file yang kita inginkan)