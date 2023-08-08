## Soal 6

Terdapat 2 kotak tertutup yang masing-masing berisi 40 buah. Sebanyak 7 dari 80
buah tersebut dalam keadaan busuk, dan sisanya segar. Diketahui beberapa
pernyataan berikut:

1. setiap kotak berisi setidaknya 36 buah segar
2. salah satu kotak berisi lebih dari 3 buah busuk
3. salah satu kotak berisi setidaknya 37 buah segar
4. tepat satu kotak berisi setidaknya 33 buah segar

Manakah pernyataan di atas yang pasti benar.

- 2 dan 3
- 1 dan 2
- 1 dan 3
- 1, 2, dan 3
- 1, 2, 3, dan 4

<details><summary>Solusi</summary>

Pada prinsip _Pegeon hole_, apabila ada $n+1$ merpati dan hanya tersedia $n$ buah sarang, maka setidaknya ada satu sarang yang berisi $2$ merpati

Diketahui ada 2 kotak, berisi masing-masing 40 buah, dan terdapat 7 buah busuk

sesuai prinsip _Pegeon hole_, karna ada 2 kotak dan 7 buah busuk, maka salah satu kotak berisi setidaknya 4 buah busuk.

Sehingga kotak lainnya berisi 3 buah busuk atau kurang, dengan kata lain berisi 37 atau lebih buah segar

Dengan prinsip _Pegeon hole_ ini, pernyataan yang pasti benar adalah pernyataan 2 dan 3

Akan dicek pernyataan 1 dan 4

- Pada pernyataan 1

jika semua (7) buah busuk berada pada satu kotak, maka kotak ini hanya berisi 33 buah segar. Mengakibatkan pernyataan 1 tidak selalu benar

(tidak setiap kotak berisi setidaknya 36 buah segar)

- Pada peryataan 4

jika satu kotak berisi 4 buah busuk dan kotak lain berisi 3 buah busuk, maka buah segar pada kedua kotak berisi 33 dan 34 buah segar. Mengakibatkan pernyataan 4 tidak selalu benar.

(tidak tepat satu kotak yang berisi setidaknya 33 buah segar)

Pernyataan yang pasti benar hanyalah pernyataan 2 dan 3

</details>

## Soal 7

Sebuah situs undian gratis berniat mengundi sebuah string berisi huruf dengan
panjang 3. Mereka membuka slot tak terbatas untuk menebaknya. Tebakan benar
akan mendapat hadiah 10 miliar. Pak Dengklek mengajak 17.576 bebeknya untuk ikut
menebak dari AAA hingga ZZZ urut secara leksikografis (bebek ke-1 menebak AAA,
bebek ke-2 menebak AAB, bebek ke-17.576 menebak ZZZ) agar dipastikan
memenangkan hadiah. Maka bebek yang ke 1532 akan menebak string $\dots$

- CGX
- BFX
- BGX
- CGY
- AFX

<details><summary>Solusi</summary>

Jelas bahwa huruf-huruf A$-$Z terdiri dari 26 huruf.

jadi, AAA$-$AAZ terdiri dari 26 string

untuk setiap string $abc$, dengan $a,b,c \in {A-Z}$. Banyaknya kemungkinan pasangan $bc$ adalah $26\times 26 = 676$

Jadi, AAA$-$AZZ terdiri dari 676 string, begitu juga dengan BAA$-$BZZ terdiri dari 676 string

Perhatikan bahwa

$$
1532 = 676\times 2 + 180 = 676\times 2 + 26\times 6 +24
$$

jelas bahwa string CFZ merupakan string ke-$676\times 2 + 26\times 6$.

jadi string ke-1532 adalah string ke-24 setelah CFZ atau string ke-2 sebelum CGZ. sehingga, string dimaksud adalah `CGX`

</details>

## Soal 8

Sebuah situs undian gratis berniat mengundi sebuah string berisi huruf dengan
panjang 3. Mereka membuka slot tak terbatas untuk menebaknya. Tebakan benar
akan mendapat hadiah 10 miliar. Pak Dengklek mengajak 17.576 bebeknya untuk ikut
menebak dari AAA hingga ZZZ urut secara leksikografis (bebek ke-1 menebak AAA,
bebek ke-2 menebak AAB, bebek ke-17.576 menebak ZZZ) agar dipastikan
memenangkan hadiah. Jika string yang keluar adalah `OSN` maka bebek keberapa
yang berhasil menebak dengan benar?

- 3528
- 3990
- 9945
- 9946
- 10648

<details><summary>Solusi</summary>

Dengan logika yang sama dengan nomor sebelumnya (7).

- huruf $O$ menempati urutan ke-15 diantara $A-Z$
- huruf $S$ menempati urutan ke-19 diantara $A-Z$
- huruf $N$ menempati urutan ke-14 diantara $A-Z$

Bebek yang menebak NZZ adalah bebek ke-$676\times 14 = 9464$.

Bebek yang menebak ORZ adalah bebek ke-$26\times 18 = 468$ setelah bebek yang menebak NZZ.

Bebek yang menebak OSN adalah bebek ke-14 setelah bebek yang menebak ORZ.

jadi, bebek yang menebak string `OSN` adalah bebek ke-$676\times 14 + 26\times 18 + 14 = 9946$

</details>

## Soal 9

Dalam sebuah program pembelajaran, akan diberikan 50 mata pelajaran yang diberi
nomor dari 1 sampai 50. Untuk setiap $k$, diketahui bahwa kelas untuk mata pelajaran
bernomor $k$ hanya diadakan pada semua hari yang bernomor kelipatan $k$. Jika hari
dimulai dari nomor 1, hari dengan nomor berapakah yang merupakan hari ke-11 yang
hanya ada tepat satu kelas?

- 89
- 91
- 97
- 29
- 23

<details><summary>Solusi</summary>

Sebuah bilanga $p$ dikatakan prima jika dan hanya jika tidak ada bilangan bulat $k$ dengan $1<k<p$ sehingga $p$ merupakan kelipatan dari $k$.

Jelas bahwa semua bilangan bulat positif $k$ merupakan kelipatan dari 1. Jadi pelajaran 1 selalu diadakan setiap hari.

Jadi, untuk hari ke-2 sampai hari ke-50 setidaknya ada 2 mata pelajaran yang diadakan, pelajaran 1 dan pelajaran ke hari itu sendiri.

Karna pada hari ke-$p$ dengan $p$ prima dan $p>50$ hanya ada tepat satu kelas (pelajaran 1) maka persoalan setara dengan mencari bilangan prima ke-10 setelah 50.

`note`: hari ke-1 hanya satu mata pelajaran yang diadakan yaitu pelajaran 1.

Daftar 10 bilangan prima setelah 50: 53, 59, 61, 67, 71, 73, 79, 83, 89, dan `97`

Jadi, hari ke-11 yang hanya ada tepat satu kelas adalah hari ke-97

</details>

## Soal 10

Andi menuliskan dua buah bilangan bulat positif yang berbeda di papan. Kemudian,
pada setiap langkah, ia menghapus bilangan yang lebih kecil dan menggantinya
dengan bilangan yang lebih besar, sedangkan bilangan yang lebih besar ia ganti
nilainya dengan dua kali nilai bilangan besar dikurangi nilai yang bilangan yang kecil
sebelum diganti (sebagai contoh, apabila di papan tertulis bilangan 1 dan 3, maka ia
akan mengganti 1 dengan 3 dan 3 dengan 5). Setelah beberapa kali langkah, ia
mendapatkan nilai 101 dan 104. Bilangan berapa saja yang pada mulanya Andi
tuliskan di papan?

- 1 dan 4
- 2 dan 5
- 3 dan 6
- 2 dan 6
- 3 dan 7

<details><summary>Solusi</summary>

## Alternatif 1

Misalkan dua bilangan pertama yang ditulis Andi adalah $a$ dan $b$, dengan $a<b$ maka

| langkah | bilangan terkecil | bilangan terbesar |
| ------- | ----------------- | ----------------- |
| 0       | $a$               | $b$               |
| 1       | $b$               | $2b-a$            |
| 2       | $2b-a$            | $3b-2a$           |
| 3       | $3b-2a$           | $4b-3a$           |
| 4       | $4b-3a$           | $5b-4a$           |
| .       | .                 | .                 |
| $k$     | $kb-(k-1)a$       | $(k+1)b-ka$       |

Jadi, $101 = kb-(k-1)a$ dan $104= (k+1)b-ka$

$$
kb-ka+b=104
kb-ka+a=101\\
$$

dengan mengurangkan kedua persamaan diatas diperoleh $b-a=3$

dengan menjumlahkan kedua persamaan diatas diperoleh $k(b-a)+(a+b)=205$

setelah meyederhanakan hasil kedua diperoleh $3k+(a+b)=205$

karna 205 dibagi 3 bersisa 1 dan $3k$ habis dibagi 3, maka $(a+b)$ haruslah bersisa 1 jika dibagi 3.

Dari pilihan yang ada dan memenuhi $b-a=3$ dan sisa $a+b$ dibagi 3 = 1 adalah 2 dan 5

## Alternatif 2

Misalkan Andi memperoleh bilangan 104 dan 101 setelah $n$ langkah. Maka pada langkah sebelumnya, bilangan terbesar merupakan 101 dan $104=2\times 101 -$ bilangan terkecil, atau bilangan terkecil $=2\times 101-104$

| langkah | bilangan terkecil | bilangan terbesar |
| ------- | ----------------- | ----------------- |
| $n$     | 101               | 104               |
| $n-1$   | $202-104=98$      | 101               |
| $n-2$   | $196-101=95$      | 98                |
| $n-3$   | $190-98=92$       | 95                |

Dapat dilihat, bahwa pada tiap langkah, bilingan terkecil dan terbesar merupakan bilangan sebelumnya ditambah 3.

Persoalan ini setara dengan mencari suku pertama dan kedua dari deret aritmatika dengan beda $b=3$, dan $U_k=101$ dan $U_{k+1}=104$ untuk suatu $k$.

$$
U_k=a+(k-1)b\\
101=a+(k-1)3\\
2+33\times 3=a+(k-1)3\\
$$

Kemungkinan $a=U_1=2$ atau $a=2+3n$, dan $U_2=a+3$ untuk suatu bilangan bulat positif $n$.

Dari pilihan yang tersedia, hanya 2 dan 5 yang memenuhi, untuk 2 dan 6, 6 tidak memenuhi nilai $U_2$.

</details>
