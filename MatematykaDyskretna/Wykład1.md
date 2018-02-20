# Zasady i prawa przeliczania //Wykład #1
## 1. Prawo dodawania

Jeśli $A_1, A_2, \ldots, A_n$ są skończonymi zbiorani parami rozłącznymi (tj. $A_i \cap A_j = \emptyset$ dla $i,j=1,2,\ldots,n$ oraz $i \neq j$), to:

$$\bigg| \displaystyle\bigcup_{i=1}^n A_i \bigg| = \displaystyle\sum_{i=1}^n |A_i|$$

## 2. Prawo mnożenia

Niech $A_1, A_2, \ldots, A_n$ bęą zadanymi zbiorami skończonymi. Wówwczas liczba ciągów $(a_1, a_2, \ldots, a_n)$ gdzie $a_i \in A_i, i = 1,2,\ldots, n$, jest równa:

$$\big| A_1 \times A_2 \times \ldots \times A_n \big| = \big\{ (a_1, a_2, \ldots, a_n) \ \text{gdzie} a_i \in A_i, \forall i \in \{ 0, 1 \} \big\}$$


$$\big| A_1 \times A_2 \times \ldots \times A_n \big| = \big| A_1\big| \cdot \big| A_2\big| \cdot \ldots \cdot \big| A_n\big|$$

## 3. Ciąg binarny

\\TODO:

## P1. Przykład:
Ile jest $4$-cyfrowych liczb zbudowanych z cyft $\{1,2,3,4,5,6,7,8,9\}$ zawierających cyfrę $5$ dokładnie raz?

___

Mamy cztery szufladki, oznaczmy je w symboliczny sposób: $\_ \ \_ \ \_ \ \_$.

Z założenia zadania wiemy, że w jednej z nich musi być cyfra $5$ ale nie wiemy konkretnie której, czyli musimy rozpatrzyć $4$ przypadki:

(1) $5 \ \_ \ \_ \ \_$:

Na pierwszym miejscu ustawiamy cyfrę $5$ więc na pozostałych miejscach pozostaje nam tylko i wyłącznie wybór spośród $\{1,2,3,4,6,7,8,9\}$. Możliwości jest wyłącznie $8$. Co zapisujemy $1 \cdot 8 \cdot 8 \cdot 8 = 8^3$.

(2) $\_ \ 5 \ \_ \ \_$:

Sytuacja symetryczna do pierwszej jedynym odstępstwem jest to że nasze możliwości wyglądają $8 \cdot 1 \cdot 8 \cdot 8 = 8^3$. Aczkolwiek to jest dalej inny przypadek!

(3) i (4) dają identyczne wyniki

Sumując wyniki (1) (2) (3) i (4) otrzymujemy wynik $8^3 \cdot 4$

## 4. Zasada szufladkowa Dirichleta

### Wersja szczególna

Mamy $N$ przedmiotów i $k$ szufladek. Jeżeli $N>k$ to istnieje szufladka zawierająca co najmniej $2$ przedmioty.

### Wersja ogólna

Mamy $N$ przedmiotów i $k$ szufladek. Jeżeli $N > k \cdot M$ to istnieje szufladka zawierająca $M+1$ przedmiotów.

### Dowód wersji ogólnej

$M_i$ - ilość przedmiotów w $i$-tej szufladce $( i \in \{ 1, \ldots, k \} )$

$$ N = n_1 + n_2 + \ldots + n_k $$

Zakładamy w tym momencie, że twierdzenie te nie jest prawdziwe:

$$ n_i \leq M, \ \text{gdzie} \ \forall i \in \{ 1, \ldots, k \} $$

$$ N = n_1 + \ldots + n_k \leq \underbrace{M + \ldots + M}_{k \ \text{razy} } = M \cdot k$$ 

$$ N \leq M \cdot k \ \text{- sprzeczność}$$ 

## 5. Zasada bijekcji

Mamy dwa skończonone zbiory $A$ i $B$. Istnieje dla nich bijekcja $f: A \rightarrow B$, wtedy i tylko wtedy, gdy  $|A| = |B|$ (gdy ma taką samą ilość elementów).

$$ [n] = \{ 1, 2, \ldots, n\} $$

## T1. Twierdzenie (o zależności między rodziną podzbiorów a zbiorem ciągów binarnych)

### Założenie

Istnieje bijekcja pomiędzy rodziną wszystkich podzbiorów zbioru $n$-elementowego, a zbiorem ciągów binarnych długości $n$.

### Idea dowodu

$$ n = 5 \implies [5] = \{ 1, 2, 3, 4, 5 \}$$

$$ \{ 1, 3, 5 \} \subset [n] \rightarrow \{ 1, 0, 1, 0, 1 \} $$

$$ \{ \emptyset \} \subset [n] \rightarrow \{ 0, 0, 0, 0, 0 \} $$

$$ \{ 1, 2, 3, 4, 5 \} \subset [n] \rightarrow \{ 1, 1, 1, 1, 1 \} $$

### Formalny dowód

$$ X \subset [n] $$

$$ f(x) = (a_1, \ldots, a_n) \text{- ciąg binarny} $$

$$ \ $$

$$ 1 \in X \rightarrow a_1 = 1; 1 \not\in X \rightarrow a_1 = 0 $$

$$ 2 \in X \rightarrow a_2 = 1; 2 \not\in X \rightarrow a_2 = 0 $$

$$ \vdots $$

$$ i \in X \rightarrow a_i = 1; i \not\in X \rightarrow a_i = 0 $$

Odwzorowanie jest wzajemnie różnowartościowe gdy $X \not= Y$ to istnieje $i \in X \setminus Y$

$$ X \rightarrow (\ldots \frac{1}{i} \ldots ) $$

$$ Y \rightarrow (\ldots \frac{0}{i} \ldots ) $$

$$ f(X) \not= f(Y) $$

Odwzorowanie $f$ jest odwzorowaniem "na", ponieważ każdy ciag binarny długości $n$ określa pewny podzbiór.

### Wniosek

Zbiór $n$-elementowy zawiera dokładnie $2^2$ podzbiorów

### Przykład

Rozmieszczenie kul w szufladkach: 6 kul, 4 szufladki


![00001](https://i.imgur.com/0beKVPx.png)

Co można zapisać jako binarny ciąg $6$ zer i $3$ jedynek ($1$ - "ścianka półki"; $0$ - kula): $0011010000$

### Podsumowanie

Każde rozmieszczenie $k$ kul i $N$ szuflad można zapisać jako ciąg binarny długości $k+N-1$ zawierający $k$ zer i $N-1$ jedynek.

# Koniec Wykładu #1
