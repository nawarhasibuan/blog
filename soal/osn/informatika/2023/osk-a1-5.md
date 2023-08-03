---
type: exercise
title: osk-a1-5
tags:
  - osk
  - "2023"
  - bagian A
score: 5
author:
  id: 64b910655d86d8eaf2d6c045
  name: panawar hasibuan
date: Tue Aug 01 2023
---

## Soal 1

Kwik mempunyai tiga variabel boolean `P`, `Q`, dan `R`. Kwik ingin membuat sebuah
operasi logika yang mengembalikan nilai `TRUE` jika dan hanya jika minimal dua
variabel dari `P`, `Q`, atau `R` mempunyai nilai `TRUE`. Operasi logika mana yang
memenuhi kriteria Kwik tersebut?

- `(P or Q or R) and (not P or not Q or not R)`
- `(not (P or Q)) or (not (Q or R)) or (not (R or P))`
- `(not (P and Q)) and (not (Q and R)) and (not (R and P))`
- `(P and Q) or (Q and R) or (R and P)`
- `(P or Q) and (Q or R) and (R or P)`

<details><summary>Solusi</summary>

Ingat bahwa `p or q or r` bernilai `TRUE` jika satu atau lebih dari `p`, `q`, `r` bernilai `TRUE`, dan `p and q and r` bernilai `TRUE` jika semua dari `p`, `q`, `r` bernilai `TRUE`

Jika minimal dua dari `P`, `Q`, dan `R` bernilai `TRUE`

maka, jelas bahwa semua `P or Q`, `Q or R` dan `R or P` bernilai `TRUE`. Dan salah satu dari `P and Q`, `Q and R` dan `R and P` bernilai `TRUE`.

Misalkan,

```
A = P or Q, B = Q or R, C = P or R
D = P and Q, E = Q and R, F = P and R
```

maka `A = B = C = TRUE`, dan salah satu dari `D, E, F` bernilai `TRUE`

Akan dicek kelima pernyataan satu-persatu:

- jika ketiganya bernilai `TRUE` maka `not P or not Q or not R` bernilai `FALSE` sehingga penyataaN bernilai `FALSE` untuk kasus ini
- Pernyataan 2 ekuivalen dengan

```
not A or not B or not C = FALSE or FALSE or FALSE
```

Sehingga penyataan kedua pasti bernilai `FALSE`

- Pernyataan 3 ekuivalen dengan

```
not D and not E and not F
```

Salah satu dari `not D, not E, not F` bernilai `FALSE`. Sehingga penyataan ketiga pasti bernilai `FALSE`

- Pernyataan 4 ekuivalen dengan

```
D or E or F = TRUE
```

Sehingga penyataan keempat pasti bernilai `TRUE`

- Pernyataan 5 ekuivalen dengan

```
A and B and C
```

Sehingga penyataan kelima pasti bernilai `TRUE`

pernyataan yang pasti bernilai `TRUE` adalah pernyataan $4$ dan $5$ jika dan hanya jika minimal 2 dari `P`, `Q`, atau `R` mempunyai nilai `TRUE`.

</details>

## Soal 2

Pak Dengklek menemukan sebuah kotak mainan di dalam gudang rumahnya.
Ternyata, kotak tersebut milik lima bebek Pak Dengklek: Kwak, Kwik, Kwuk, Kwek,
dan Kwok. Terdapat lima buah bebek karet berwarna merah, biru, hijau, kuning, dan
ungu. Diketahui bahwa setiap bebek karet dimiliki oleh tepat satu bebek. Diketahui
juga bahwa setiap bebek pasti memiliki bebek karet dengan warna yang sesuai
dengan salah satu warna kesukaannya. Jika diberikan informasi sebagai berikut:

- Kwok hanya menyukai warna oranye, hijau dan kuning.
- Kwuk menyukai semua warna selain oranye, ungu, kuning, dan biru.
- Kwak hanya menyukai warna hijau, oranye, dan biru.
- Kwek hanya menyukai warna merah dan ungu.
- Kwik menyukai semua warna selain biru, ungu, hijau, dan merah.

Siapa pemilik bebek karet berwarna hijau?

- Kwok
- Kwuk
- Kwek
- Kwik
- Kwak

<details><summary>Solusi</summary>

Perhatikan tabel warna kesukaan dari pernyataan-pernyataan diatas dibawah ini

| warna/bebek | oranye     | hijau      | kuning     | ungu       | biru       | merah      |
| ----------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Kwok        | $\bigcirc$ | $\bigcirc$ | $\bigcirc$ |            |            |            |
| Kwuk        |            | $\bigcirc$ |            |            |            | $\bigcirc$ |
| Kwak        | $\bigcirc$ | $\bigcirc$ |            |            | $\bigcirc$ |            |
| Kwek        |            |            |            | $\bigcirc$ |            | $\bigcirc$ |
| Kwik        | $\bigcirc$ |            | $\bigcirc$ |            |            |            |

Dapat dilihat yang menyukai warna hijau adalah Kwok, Kwuk, dan Kwak. Bebek karet yang ditemukan Pak Dengklek adalah `merah`, `biru`, `hijau`, `kuning`, dan `ungu`. Jadi bebek karet warna `kuning` harus dimiliki oleh Kwik. Sehingga warna `hijau` harus dimiliki oleh Kwok

Pemilik bebek karet berwarna hijau adalah Kwok

`note`: warna oranye hanya sebagai pengecoh soal

</details>

## Soal 3

Karena merasa bebeknya sudah terlalu banyak, Pak Dengklek ingin mengurangi
jumlah bebeknya dengan cara menjual semua bebek yang tidak `unggul`. Pak
Dengklek menyiapkan 10 soal dari nomor 1 sampai 10 untuk dikerjakan semua
bebeknya (benar bernilai 1, salah bernilai 0). Bebek dikatakan `unggul` jika mendapat
nilai paling sedikit 8. Kwak adalah bebek yang sangat cerdas dan telah mengetahui
jawaban yang benar dalam menjawab soal apapun. Namun, Kwak tidak selalu ingin
memberikan jawaban yang benar. Agar Kwak tidak dijual, berapa banyaknya cara
Kwak memilih soal yang akan dijawab dengan benar jika Kwak menjawab soal nomor
1, 3, dan 5 dengan benar?

- 29
- 21
- 8
- 3
- 1

<details><summary>Solusi</summary>

Kwak sudah menjawab soal nomor 1, 3, dan 5 dengan benar, tersisa 7 pilihan soal.

Supaya Kwak tidak dijuan (`unggul`) dan tidak selalu ingin menjawab semua soal dengan benar, Kwak memiliki tiga pilihan:

- Menjawab benar 8 soal, 2 salah

Banyak cara memilih 2 soal salah dari 7 soal adalah $\binom{7}{2}=21$

- Menjawab benar 9 soal, 1 salah

Banyak cara memilih 1 soal salah dari 7 soal adalah $\binom{7}{1}=7$

- Menjawab benar semua soal, ada 1 cara

Total cara Kwak supaya tidak dijual ada $21+7+1=29$ cara

</details>

## Soal 4

Kwek mengikuti kegiatan maraton bebek dengan panjang lintasan tak terhingga.
Pertama-tama Kwek dapat berlari $100$ km sebelum lelah. Setelah istirahat, Kwek akan
lelah lagi setelah menempuh $3/5$ jarak yang telah ditempuh sejak lelah yang
sebelumnya, dan begitu seterusnya. Berapakah total jarak lintasan yang ditempuh
Kwek?

- $160$ km
- $196$ km
- $222$ km
- $250$ km
- $300$ km

<details><summary>Solution</summary>

Setiap selesai istirahat, Kwek akan berlari menempuh $3/5$ jarak sebelumnya. Persoalan ekuivalen dengan menghitung jumlah deret tak hingga dengan rasion, $r=3/5$ dan suku awal $U_1=a=100$.

dapat dihitung dengan rumus:

$$
S=\frac{a}{1-r}
$$

dengan $S$ jumlah deret tak hingga, $a$ suku pertama, dan $r$ rasio dari deret. Untuk $-1<r<1$

$$
100+100\times 3/5+100(\times 3/5)^2+100(\times 3/5)^3+ \dots\\
= \frac{100}{1-3/5}\\
= \frac{100\times 5}{2}=250
$$

Total jarak lintasan yang ditempuh adalah $250$ km

</details>

## Soal 5

Pak Dengklek memiliki bebek yang jumlahnya tak terhingga. Dalam 30 hari ke depan,
Pak Dengklek ingin memandikan bebek-bebeknya. Karena bebek-bebeknya malas
mandi, Pak Dengklek menunjuk 5 bebek paling setianya yaitu Kwak, Kwik, Kwuk,
Kwek, dan Kwok untuk mandi di hari pertama sekaligus sebagai inspirasi bagi bebek-bebek yang lain agar mau mandi. Setiap hari setelah hari pertama, bebek yang mau
mandi ada sebanyak bebek yang mandi di hari sebelumnya ditambah 3. Tidak ada bebek
yang mandi 2 kali. Setelah 30 hari berlalu, berapa banyak bebek yang sudah mandi?

- $150$
- $237$
- $1455$
- $1458$
- $2910$

<details><summary>Solusi</summary>

Persoalan setara dengan menghitung jumlah 30 suku pertama barisan aritmatika dengan suku pertama $U_1=a=5$, beda barisan $b=3$

Jumlah $n$ suku pertama barisan aritmatika dapat dihitung dengan

$$
S_n=n\times\frac{a+U_n}{2}=n\times\frac{2a+(n-1)b}{2}
$$

Setelah 30 hari berlalu, banyak bebek yang sudah mandi adalah $S_{30}$.

$$
S_{n}=n\times\frac{2a+(n-1)b}{2}\\
S_{30}=30\times\frac{2\times 5+(30-1)\times 3}{2}\\
S_{30}=30\times\frac{10+87}{2}=1455
$$

Bebek yang sudah mandi pada hari ke-30 ada $1.455$ bebek

</details>
