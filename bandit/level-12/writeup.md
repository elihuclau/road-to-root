# Bandit Level 12 → Level 13

## Goal
Tujuan challenge: 
Menemukan password yang tersimpan pada file "data.txt" yang terkompres berkali kali atau yang biasa disebut hexdump

## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Password yang berada di file data.txt terkompres berulang kali dan kita harus menggunakan directory didalam /temp

## Approach
Cara berpikir untuk menyelesaikan challenge.
Dikarenakan file ini terkompres berulangkali jadi kita juga harus melihat jenis file ini terus setelah kita mengesktrak nya
pada level ini kita menggunakan 2 type extract yaitu:
- gzip
- bzip2

## Commands
ssh bandit12@bandit.labs.overthewire.org -p 2220
ls
cat data.txt
mktemp -d
cd /tmp/temp.SPuL8Ac6y9
cp ~/data.txt .
xxd -r data.txt > file1
file file1
mv file1 file1.gz
gunzip file1.gz
file file1
tar -xvf file1
file data5.bin
tar -xvf data5.bin
file data6.bin
mv data6.bin data6.bz2
bunzip2 data6.bz2
file data6
tar -xvf data6
file data8.bin
mv data8.bin data8.gz
gunzip data8.gz
file data8
cat data8

## Solution Steps

1. Login ke server bandit

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```

2. Lihat isi directory

```bash
ls
```

3. Bikin directory di dalam /tmp

```bash
mktemp -d
```

4. Masuk ke dalam directory nya

```bash
cd /tmp/tmp.SPuL8Ac6y9
```

5. Copy file "data.txt" ke dalam /tmp nya

```bash
cp ~/data.txt .
```

6. Reverse hexdump ke file asli

```bash
xxd -r data.txt > file1
```

6. Extract file nya berulang kali sampai jadi file yang asli

```bash
file file1
mv file1 file1.gz
gunzip file1.gz
file file1
tar -xvf file1
file data5.bin
tar -xvf data5.bin
file data6.bin
mv data6.bin data6.bz2
bunzip2 data6.bz2
file data6
tar -xvf data6
file data8.bin
mv data8.bin data8.gz
gunzip data8.gz
file data8
```

6. Print file asli

```bash
cat data8
```

Output menunjukkan hasil decode dari file yang terencode:

```
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```


## Password
```
password-next-level
```
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- Menggunakan tools gzip & bzip2 untuk mengesktrak file yang terkompres berulang kali, tar untuk menggabungkan banyak folder jadi 1 file

## New Commands Learned
Command baru yang dipelajari:

-tar (menggabungkan folder jadi 1 file)
-bzip2 gzip (mengesktrak file)
-cp (mengcopy file)
