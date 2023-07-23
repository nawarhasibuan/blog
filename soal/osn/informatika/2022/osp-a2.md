---
type: exercise
title: penerjemah diplomat
tags:
  - kombinasi
  - logika
score: 7
author:
  id: 64b910655d86d8eaf2d6c045
  name: panawar hasibuan
date: Sun Jul 23 2023
---

Kwak, Kwik, Kwuk, Kwek, Kwok ditugasi sebagai seorang diplomat. Kwak hanya dapat berbicara bahasa
Inggris dan Jerman. Kwik hanya berbicara dalam bahasa Perancis, Jepang, dan Cina. Kwuk hanya dapat
berbicara bahasa Jerman. Kwek hanya berbicara dalam bahasa Inggris, Jepang, dan Cina. Kwok hanya
dapat berbicara dalam bahasa Perancis dan Jerman. Ada berapa banyak pasangan diplomat yang harus
menggunakan penterjemah dalam berkomunikasi?

<details>

<summary>Jawaban</summary>

| Diplomat | Inggris    | Jerman     | Prancis    | Jepang     | China      |
| -------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Kwak     | $\bigcirc$ | $\bigcirc$ |            |            |            |
| Kwik     |            |            | $\bigcirc$ | $\bigcirc$ | $\bigcirc$ |
| Kwuk     |            | $\bigcirc$ |            |            |            |
| Kwek     | $\bigcirc$ |            |            | $\bigcirc$ | $\bigcirc$ |
| Kwok     |            | $\bigcirc$ | $\bigcirc$ |            |            |

Dari tabel diatas dapat dilihat bahwa:

- Kwak mempunyai bahasa yang saling dipahami dengan Kwek, Kwuk, Kwok. Butuh 1 penerjemah Kwak dan Kwik
- Kwik mempunyai bahasa yang saling dipahami dengan Kwek, Kwok. Butuh 1 penerjemah antara Kwik dan Kwuk
- Kwuk mempunyai bahasa yang saling dipahami dengan Kwok. Butuh 1 penerjemah antara Kwuk dan Kwek
- Kwek dan Kwok butuh 1 penerjemah

Jadi, dibutuhkan 4 penerjemah.
</details>
