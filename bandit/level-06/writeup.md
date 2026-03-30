# Bandit Level 6 → Level 7

## Goal
Tujuan challenge: 
Mencari file yang tersembunyi pada server

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Mencari file dengan ketentuan yang sudah di berikan

## Approach
Cara berpikir untuk menyelesaikan challenge.
Ketentuan yang diberikan adalah
1. Owned by user bandit7
2. Owned by group bandit6
3. 33bytes in size

Dengan ciri ciri file di atas maka kita bisa menemukan nya menggunakan
command find dengan option/flag tambahan
/ = mulai mencari dari directory root
-user bandit7 = mencari file milik user "bandit7"
-group bandit6 = mencari file milik group "bandit6"
-size 33c = mencari file dengan ukuran 33bytes

tambahan flag yang saya gunakan untuk menghilangkan output yang tidak
dibutuhkan seperti permission denied yang bisa mengganggu
 2>/dev/null

## Commands
ssh bandit6@bandit.labs.overthewire.org -p 2220
ls
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password


## Solution Steps

1. Login ke server bandit

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Cari file yang memiliki password menggunakan ketentuan yang sudah
diberikan

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

Output menunjukkan file yang sesuai:

```
/var/lib/dpkg/info/bandit7.password
```

4. Buka file

```bash
cat /var/lib/dpkg/info/bandit7.password
```


## Password
```
password-next-level
```
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan command "find" untuk mencari file dengan ketentuan yang kita 
inginkan

## New Commands Learned
Command baru yang dipelajari:

-find (mencari file dengan ketentuan yang kita inginkan dengan menambahkan
flag / option tertentu)