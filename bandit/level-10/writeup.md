# Bandit Level 10 → Level 11

## Goal
Tujuan challenge: 
Mencari password yang di encode pada file data.txt

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Pada file data.txt terdapat text acak yang terdapat karakter "=" di akhir kalimat nya, lalu kita harus mengdecode nya ke password asli nya 

## Approach
Cara berpikir untuk menyelesaikan challenge.
Dikarenakan password nya ter encode menjadi:
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
kita akan mengdecode ya menggunakan command dari linux yaitu "base64"

## Commands
ssh bandit10@bandit.labs.overthewire.org -p 2220
ls
cat data.txt | base64 -d


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Decode file tersebut

```bash
cat data.txt | base64 -d
```

Output menunjukkan hasil decode dari file yang terencode:

```
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```


## Password
```
password-next-level
```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- penggunaan base64 untuk encode maupun decode

## New Commands Learned
Command baru yang dipelajari:

-base64 (untuk mengdecode/encode file)
