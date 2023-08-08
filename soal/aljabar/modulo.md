Pak Blangkon mendapat kurang dari 500 bebek dari Bu Dengklek.

Jika Pak Blangkon membagi bebek dalam 4 kandang dengan banyak yang sama, tersisa tiga ekor bebek diluar kandang.

Jika Pak Blangkon membagi bebek dalam 5 kandang dengan banyak yang sama, tersisa empat ekor bebek diluar kandang.

Jika Pak Blangkon membagi bebek dalam 6 kandang dengan banyak yang sama, tersisa lima ekor bebek diluar kandang.

Tapi Pak Blangkon bisa membagi bebek tepat dalam 7 kandang. Berapa banyak bebek yang Pak Blangkon terima dari Bu Dengklek?

<details> 
<summary>Jawaban</summary>

Misalkan banyaknya bebek yang diterima Pak Blangkon sebanyak $n$, $0< n < 500$, maka

$$
n \equiv 3 \mod 4 \equiv -1 \mod 4 \\
n \equiv 4 \mod 5 \equiv -1 \mod 5 \\
n \equiv 5 \mod 6 \equiv -1 \mod 6 \\
n \equiv 0 \mod 7
$$

Jadi,

$$
n \equiv -1 \mod (4\cdot 5\cdot3) \\
n \equiv 59 \mod (60)
$$

atau $n$ dapat ditulis dalam bentuk $n = 60k+59$ untuk suatu bilangan bulat $k$.

Tetapi karena $n$ habis dibagi 7 maka $60k+59$ juga habis dibagi 7, jika $k = 7a +b$ untuk bilangan bulat $a$, $0\le b<7$

maka $n = 60(7a+b)+59= 420a + 60b+59 = 420a + 7(6b+8) + 4b+3$, jadi $4b+3$ harus juga harus kelipatan 7, diperoleh $b= 1$.

$n = 420a+60(1)+59 = 420a+119$, karna $n<500$, $n$ yang memenuhi hanyalah $n = 119$

Banyak bebek yang didapat Pak Blangkon dari Bu Dengklek adalah $119$ ekor.

</details>
