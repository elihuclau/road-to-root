# Bandit Level 1 → Level 2

## Goal
Tujuan challenge: 
Menemukan password tersembunyi yang tersimpan pada file bernama (-)


## Problem
Deskripsi singkat challenge / masalah yang harus diselesaikan.
Dikarenakan file tempat password nya berada adalah (-) yang tidak bisa
secara langsung di baca menggunakan command "cat" maka kita harus mencari
karakter tambahan yaitu (<)


## Approach
Cara berpikir untuk menyelesaikan challenge.
menambahkan karakter (<) sebelum (-) pada command "cat -"




## Commands
```bash
command1 ssh bandit1@bandit.labs.overthewire.org -p 2220
command2 ls
command3 cat <-
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
263JGJPfgU6LtdEvgfWU1XP5yac29mFx


## Key Takeaway
Hal penting yang dipelajari dari level ini:

- beberapa karakter khusus memerlukan karakter tambahan 
(escape character) agar dapat diproses atau ditampilkan dengan benar



## New Commands Learned
Command baru yang dipelajari:

- ssh
- cat
- ls
