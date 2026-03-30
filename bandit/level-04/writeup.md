# Bandit Level 4 → Level 5

## Goal
Tujuan challenge: 
Mencari file yang "human-readable" yang berada di directory (inhere)

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Mencari file yang human-readable di antara file file lain yang berisi tulisan
random/bahasa bahasa lain

## Approach
Cara berpikir untuk menyelesaikan challenge.
Menggunakan command file untuk mencari type file yang mau kita cari,
pada level ini kita mencari file dengan type ASCII text(human-readable)

## Commands
ssh bandit4@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls -la
file ./*
cat ./-file07


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
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

5. Cari file dengan type file (ASCII text)

```bash
file ./*
```

Output menunjukkan file:

```
./-file00: data
./-file01: OpenPGP Public Key
./-file02: OpenPGP Public Key
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data

```

6. Buka file dengan type file (ASCII text)

```bash
cat ./-file07
```


## Password
```
password-next-level
```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan command "file" supaya bisa mencari type file secara langsung,
tanpa harus kita cari 1 per 1

## New Commands Learned
Command baru yang dipelajari:

-file (untuk mencari type file dan kondisi file)