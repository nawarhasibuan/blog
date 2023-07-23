---
type: exercise
title: kombinasi pola bilangan
tags:
  - kombinasi
  - teori bilangan
score: 7
author:
  id: 64b910655d86d8eaf2d6c045
  name: panawar hasibuan
date: Sun Jul 23 2023
---

Pak Dengklek sangat suka mengutak-atik bilangan dan memberikan nama untuk sifat unik dari sebuahbilangan. Salah satu sifat unik bilangan yang dlsukal oleh Pak Dengklek adalah Bilangan Menanjak. Sebuah bilangan $X$ disebut Bilangan Menanjak apabila digit-digit dari $X$ menaik dari kiri ke kanan.

Contoh Bilangan Menanjak adalah 122349. Tiba-tiba Pak Dengklek penasaran, ada berapa Bilangan Menanjak yang nilainya yang kurang dari $(10^{10})$.

Bantulah Pak Dengklek supaya tidak berulah dengan pemikiran dan tingkah anehnya lagi

<details> 
<summary>Jawaban</summary>

Bilangan yang nilainya kurang dari $10^{10}$ adalah bilangan yang terdiri dari 10 digit atau kurang.

Misalkan $n$ adalah bilangan menanjak dan $x_i$ banyaknya digit $i$ untuk $0\le i \le 9$ adalah banyaknya digit $n$ yang bernilai $i$. Sebagai contoh, jika

$n = 122349 = 0.000.122.349$ maka

$x_0 = 4$, $x_1 = 1$, $x_2 = 2$, $x_3 = 1$, $x_4 = 1$, $x_5 = 0$, $x_6 = 0$, $x_7 = 0$, $x_8 = 0$, $x_9 = 1$.

Jadi persoalan diatas equivalen dengan banyaknya kombinasi

$(x_0, x_1, x_2, x_3, x_4, x_5, x_6, x_7, x_8, x_9)$

sehingga,

$$
x_0 + x_1+ x_2+ x_3 + x_4 + x_5 + x_6 + x_7 + x_8 + x_9 = 10 \\
0\le x_i \le 10
$$

Banyak bilangan menanjak: $\binom{19}{9} = 92378$

(note: ada 10 bola dibagi dalam 10 kelompok sehingga ditambah 9 bola sebagai pembatas, jadi ada 19 bola akan dipilih 9 bola)

</details>
