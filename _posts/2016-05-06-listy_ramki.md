---
layout: post
title: "Zamiana obiektu typu data.frame na obiekt typu list"
date: 2016-05-06
---

To jest jedna z ciekawszych sztuczek w R. Otóż okazuje się, że przy pomocy fumkcji _attr_ można każdy obiekt typu _data.frame_ przerobić na obiekt typu _list_. 

Zaczynam od stworzenie obiektu tyou _data.frame_ o nazwie _ramka.danych_

```
> ramka.danych<-data.frame(cyfry=0:9, litery=letters[1:10] )
> ramka.danych
   cyfry litery
1      0      a
2      1      b
3      2      c
4      3      d
5      4      e
6      5      f
7      6      g
8      7      h
9      8      i
10     9      j
```

Teraz w 2. etapach zamieniam _data.frame_ w _list_

## ETAP 1. Zmiana atrybutu "class" z "data.frame" na "list"

```
> attr(ramka.danych, "class")
[1] "data.frame"
> attr(ramka.danych, "class")<-c("list")
> attr(ramka.danych, "class")
[1] "list"
```

## ETAP 2. Kasowanie numerów wierszy

```
attr(ramka.danych, "row.names")<-c("")
```

W ten sposób otrzymujemy listę

```
ramka.danych
$cyfry
 [1] 0 1 2 3 4 5 6 7 8 9

$litery
 [1] a b c d e f g h i j
Levels: a b c d e f g h i j

attr(,"row.names")
[1] ""
attr(,"class")
[1] "list"
```

