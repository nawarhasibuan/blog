## Soal 31

Perhatikan potongan program berikut:

```cpp
int a = 0, b = 0, c = 0, d = 0;
int ans = 0;
void kebersamaan(int x)
{
  ans += a;
  a = b;
  b = c;
  c = d;
  d = x;
}
int main()
{
  a += 4;
  b += 3;
  c += 7;
  d += 2;
  kebersamaan(5);
  kebersamaan(2);
  a += 2;
  c += 3;
  kebersamaan(3);
  d += 4;
  c += 4;
  kebersamaan(0);
  a += 5;
  b += 6;
  kebersamaan(1);
  c += 9;
  a += 7;
  c += 2;
}
```

Berapa nilai akhir `ans` setelah potongan program di atas dijalankan?

## Soal 32

Perhatikan fungsi-fungsi berikut:

```cpp
int a, b, c, d;
int kiri()
{
  d--;
  return c - a / b;
}
int kanan()
{
  d--;
  return a + b - c;
}
void atas()
{
  c = c / 3;
  a -= 5;
}
int bawah(int x, int y, int z)
{
  a = x;
  b = y;
  c = z;
  d = 0;
  while (kiri() > kanan())
  {
    d = a + b + c + d;
    atas();
    b = b + 3;
  }
  d += b * c;
  d += x / y;
  return d - 2 * a;
}
```

Berapa nilai yang dikembalikan dari pemanggilan `bawah(42, 17, 265)`?

## Soal 33

Perhatikan fungsi berikut:

```cpp
int bersih(int x, int y)
{
  return x + y;
}
int hijau(int x, int y)
{
  return x - y;
}
int berhiber(int x, int y)
{
  if (y == 0)
  {
    return 0;
  }
  else
  {
    return bersih(x, y) + hijau(x, y) + berhiber(x - 1, y - 1);
  }
}
```

Berapa nilai yang dikembalikan dari pemanggilan `berhiber(20, 15)`?

## Soal 34

Diketahui dua buah fungsi `merah()` dan `putih()` sebagai berikut:

```cpp
int info(int x)
{
  if (x == 0)
  {
    return 1;
  }
  else
  {
    return info(x - 1) + format(x - 1);
  }
}
int format(int x)
{
  if (x == 0)
  {
    return 1;
  }
  else
  {
    return info(x - 1) + matika(x - 1);
  }
}
int matika(int x)
{
  if (x == 0)
  {
    return 1;
  }
  else
  {
    return format(x - 1) + matika(x - 1);
  }
}
```

Berapa nilai yang dikembalikan dari pemanggilan `info(9)`?

## Soal 35

Didefinisikan fungsi-fungsi sebagai berikut:

```cpp
int hijau(int x, int y)
{
  if (x < y)
  {
    x = x + y;
    y = x - y;
    x = x - y;
  }
  if (y == 0)
  {
    return x;
  }

  return hijau(x - y, y);
}
int merah(int q, int w, int e, int r)
{
  if (q < w)
  {
    return 0;
  }
  return hijau(q, e) + merah(q - r, w, e, r);
}
int biru(int n)
{
  int ans = 0;
  ans += merah(n, 1, n, 1);
  ans -= merah(2 * n, 2, n, 2);
  return ans * 3;
}
```

Berapa nilai yang dikembalikan dari pemanggilan `biru(69)`!
