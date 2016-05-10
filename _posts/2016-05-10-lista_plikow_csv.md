---
layout: post
title: "Lista plików w folderze"
date: 2016-05-10
---

Aby sprawdzić ile jest plików danego typu (np. csv) w konkretnym folderze można użyć funkcji _list.files_. Atrybut _pattern_ pozwala przy pomocy wyrażeń regularnych wybrać pliki z konkretnym rozszerzeniem. W tym przypadku jest to __.csv__.

```
> pliki<-list.files(pattern = "\\.(csv|CSV)$")
> pliki
[1] "tekstowy_1.csv" "tekstowy_2.csv"
> read.csv2(pliki[1])
   kolumna_1 kolumna_2 kolumna_3 kolumna_4 kolumna_5
1          1        23         a        39       101
2          2        25         b        44       121
3          3        27         c        49       141
4          4        29         a        54       161
5          5        31         b        59       181
6          6        33         c        64       201
7          7        35         a        69       221
8          8        37         b        74       241
9          9        39         c        79       261
10        10        41         a        84       281
11        11        43         b        89       301
12        12        45         c        94       321
13        13        47         a        99       341
14        14        49         b       104       361
```
