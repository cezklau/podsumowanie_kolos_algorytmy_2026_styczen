# Algorytmy i struktury danych

# Wprowadzenie do algorytmów

1. Co to algorytm?

2. Co to oznacza, że algorytm jest poprawny?

3. Co to oznacza, że algorytm jest efektywny?

4. Co to pseudokod?

5. W jakim celu stosuje się pseudokod i jakie ma cechy?

# Struktury danych

1. Co to struktura danych?

2. Jakie są podstawowe struktury danych?
- Stosy
- Kolejki
- Tablice
- Listy

3. Co to jest FIFO i LIFO? (Dosłownie jak się nauczycie nazw rozwiniętych to wszystko wiecie)

4. Jak działa stos i czy to FIFO, czy LIFO?

LIFO, bo jak coś wejdzie ostatnie to ostatnie wyjdzie. Fajny przykład był z talerzami. Jak wsadzisz talerz do zlewu to wyciągniesz ten z góry (ostatni włożony), a nie ten z dołu.

5. Jakie operacje mamy dla stosów?

- PUSH
- POP

```javascript
const arr = [1,2,3]

// Wrzuci nam 5 na koniec
arr.push(5) // [1,2,3,5]

// Usunie nam z końca 5
arr.pop() // [1,2,3]
```

6. Jak indeksujemy w informatyce?

No indeksowanie, czyli dajemy jakiś numer jakiemuś elementowi w zależności od jego kolejności. Np. pierwszy element list.
W większości języków programowania (bo istnieje jeszcze R) ideksujemy nie od 1 a od 0. Czyli pierwszy element nie ma indeksu 1, tylko 0.
To się nazywało systemem amerykańskim, czy jakoś tak.

7. Co to jest kolejka i czy to FIFO, czy LIFO?

Kolejka to taka struktura danych, gdzie jak element pierwszy wejdzie to i pierwszy wyjdzie. Można to porównać do kolejki do kasy. Łatwe skojarzenie.

FIFO - First in, first out

8. Jak się nazywa początek i koniec kolejki?

Początek - Head
Koniec - Tail

9. Jakie są operacje w kolejce i jak działają?

- DEQUEUE - usuwanie z kolejki

Zabieramy element z pierwszego indeksu i dla reszty elementów zmniejszamy indeks indeks o 1. Czyli na początku mamy:
0 - a
1 - b
2 - c

Wykonujemy operacje DEQUEUE i a nam znika.

0 - b
c - 1

- ENQUEUE - dodanie do kolejki

Bierzemy jakiś element i na chama na koniec go wrzucamy. Cyk cyk pyk wszystko działa pięknie. Ma on indeks o jeden większy niż poprzednio ostatni element w kolejce.

0 - a
1 - b

Dodajemy c

0 - a
1 - b
2 - c

10. Co to tablica?

No to już w tym dokumencie była tablica (z and. array). To jest podstawowy, choć złożony typ danych. Porównamy ją do szafy z pułkami. Na każdej półce może być inny element.
półka 0 - "a"
półka 1 - "b"
półka 2 - "c"

Zapis w javascript

```javascript
const arr = ['a', 'b', 'c']

arr[0] // a
arr[1] // b
arr[2] // c
```

11. Co to jest lista i czym się różni od tablicy?

Jest to prawie to samo jak tablica, ale różni się metodą odszukania elementów. Przy tablicy dany indeks wskazuje na dany punkt w pamięci. Jednak w liście dany indeks nie wskazuje na dany punkt w pamięci gdzie można znaleźć daną informację. Zamiast tego jeden element wskazuje na drugi który jest po nim. 

Czyli chcemy znaleźć element o indeksie 2. Najpierw sprawdzamy element o indeksie 0 który wskazuje na element o indeksie 1. Po sprawdzeniu elementu o indeksie 1 on wskazuje na element o indeksie 2 i dopiero mamy element o indeksie 2.

Do tego lista jest dynamiczna.

12. Co to jest struktura dynamiczna?

To taka struktura danych która może zmieniać ulokowane w pamięci miejsce dla siebie.
Np. w c++ jak tworzysz tablicę to musisz sprecyzować jej typ (np. int czyli liczby całkowitę), oraz rozmiar (maksymalnie 20 elementów).
Wtedy w pamięci rezerwujemy miejsce na tą tablicę. Nie da się jej ani zmniejszyć, ani zwiększyć.

Lista za to dynamicznie zwiększa ilosć miejsca w pamięci. Nie ma tak, że maksymalnie ma xxx Kb miejsca ulokowanego i więcej nie wykorzysta.

13. Wymień operacje na strukturach dynamicznych i do czego służą. ( No wątpie by to było, ale warto znać )

- SEARCH - wyszukiwanie
- INSERT - dodawanie nowego elementu
- DELETE - usunięcie elementu
- MINIMUM - wyszukanie najmniejszego klucza
- MAXIMUM - wyszukanie największego klucza
(Tu skubany nawet nie opisał tych poniżej)
- SUCCESSOR - sprawdza następny element (w np. liście, ale nie tylko)
- PREDECESSOR - sprawdza poprzedni element (w np. liście, ale nie tylko)

14. Co to lista z dowiązaniem (linked list)

To jest lista która posida przechowywaną wartość i dowiązanie do następnej wartości ( czyli gdzie w pamięci szukać następnej wartości ).

15. Co to lista dwukierunkowa?

To taka lista z dowiązaniem która posiada dowiązanie do następnej wartości, **ORAZ** poprzedniej wartości.

16. Czy listy i tablicy w python to co o czym tu mówimy?

No nie. Bo python to język praktyczny który ma działać i ma się przy nim budować oprogramowanie. Tutaj mówimy o czymś, czego w pracy nie użyjecie nigdy. Ale jak potrafisz zrobić klasę LinkedList i jeszcze na jej podstawie zrobić jakiś algorytm to w pracy będzie Ci łatwiej. Mniej więcej tak to działa xd

## Rzędy wielkości funkcji

Dodał tu taki zapis:

```
Zagadnienia poruszane w prezentacji są złożone, a ich zrozumienie będzie weryfikowane
na zaliczeniu.
```

1. Co to rząd wielkości funkcji?
Jest to opis czsu działania algorytmu.

2. Jakie są notacje asymptotyczne i czym się różnią?
- Θ ( i weź powiedz mi co to jest? )
Opisuje z góry i z dołu czas działania funkcji.
- O
Opisuje czas działania z góry pewnej funkcji. Tzw. **Pesymistyczne** oszacowanie czasu działania.
- Ω
Opisuje czas działania z dołu pewnej funkcji. Tzw. **Optymistyczne** oszacowanie czasu działania.

3. Co to asymptotyczie niedokładne ograniczenie górne, jakim symbolem opisujemy?

To taka górna granica, ale ma margines błędu.

o(g(n))

4. Co to asymptotyczie niedokładne ograniczenie dolne, jakim symbolem opisujemy?

To taka dolna granica, ale ma margines błędu.

ω(g(n))

5. Jakie są standardowe rzędy wielkości funkcji. ( ciężko zapamiętać ładnie wszystko )

O(0) nie ma operacji
O(1) stała
O(log n) logarytmiczna
O((log n)^c) polilogarytmiczna
O(n) liniowa
O(n log n) log-liniowa
O(n^2) kwadratowa
O(n^c) wielomianowa
O(c^n) wykładnicza
O(n!) silnia
O(n^n) super wykładnicza

## Rekurencja

1. Co to rekurencja?

Wywołanie funkcji przez samą siebie.

```javascript
function test(i){
    console.log(i)
    test(i+1);
}

test(0)
// 0
// 1
// 2
// 3
// ...
```

2. Na czym polega metoda dziel i zwyciężaj?

Metoda ta polega na dzieleniu problemów na mniejsze podproblemy, a następnie rozwiązywania ich.

Gdzie code to jest zaszyfrowana część wiadomości, a next to kolejny obiekt posiadający kod i kolejny obiekt w sobie.
Jest to struktura Linked List. Chcemy połączyć roszyfrować wszystkie kody i je połączyć, aby otrzymać logiczny ciąg znaków, a przez technike szyfrowania nie da się połączyć kodów i je odszyfrować, bo odszyfrowana wartość będzie błedna.

```javascript
const obj = [
    {
        code: 'Fefg43'
    },
    {...},
    ...
]

function decodeList(list) {
    // decode to funkcja fikcyjna która odszyfrowuje kod
    if (list.length === 1) return decode(list[0].code);

    const mid = Math.floor(list.length / 2);
    // dzielimy liste na dwie mniejsze listy
    const left = decodeList(list.slice(0, mid));
    const right = decodeList(list.slice(mid));

    return left + right;
}

decodeLinkedList(obj)

// Przy poniższej tablicy
// [1,2,3,4,5]
// Ta funkcja zadziała tak:
// left [1,2] right [3,4,5]
// potem left na:
// left_left [1] i left_right [2]
// right na:
// right_left [3] i right_right [4,5]
// i
// right_right_left [4] i right_right_right [5]
```

To jest przykład użycia dziel i zwyciężaj. Na koniec rozwiązania wracają do pierwszego wywołania które zwraca wynik.

## Grafy i drzewa

1. Co to graf skierowany i nieskierowany? Czym się różnią?

Graf skierowany to graf który ma punkty połączone sobą strzałkami. Czyli od punktu a do punktu b. Również można zrobić pętle od punktu a do punktu a.

Graf nieskierowany łączy punkty liniami bez grota (czyli nie strzałkami). Nie można zrobić pętli.

2. Co to krawędzie w grafach i jakie mają typy?

Krawędź to strzałka, bądź linia łącząca dwa punkty grafu.

Dla grafów skierowanych mamy:
- krawędzie wychodzące
- krawędzie wchodzące

Zazwyczaj dana krawędź jest i wychodząca i wchodząca. Tutaj zależy z jakiego odniesienia. A -> B jest wychodząca z A i wchodząca do B.

Dla grafów nieskierowanych mamy krawędzie **incydenta** z wierzchołkami A i B. A - B

3. Co to stopnie wierzchołka i jakie są?

Typy:
- Stopień wyjściowy - ile krawędzi wychodzi z wierzchołka
- Stopień wejściowy - ile krawędzie wchodzi do wierzchołka
- stopień - suma powyższych

4. Co to jest ścieżka?

Ścieżka opisuje ile krawędzi trzeba pokonać, aby przejść z danego wierzchołka do danego wierzchołka.

A -> B -> C -> D

Tutaj z A do D mamy 3 krawędzie.

5. Co to jest cykl?
Cykl to ścieżka która zaczyna i kończy się w tym samym miejscu.

6. Co to jest pętla?
Pętla to cykl o długości 1.

Czyli z wierzchołka A do wierzchołka A.

7. Co to jest spójność, graf spójny i spójna składowa?

Spójność grafu występuje, gdy kazdy wierzchołek jest osiągalny z każdego wierzchołka
```
    B
    |
A - C - D
    |
    E
```
W powyższym przypadku C jest spójną składową która łączy ze sobą wszystkie wierzchołki.

8. Co to jest drzewo wolne?

Jest to acykliczny graf nieskierowany. Czyli krawędzie nie są wychodzące ani wchodzące, tylko incydentyczne (nie wiem czy można tak to napisać), oraz nie nie wraca znów do tego samego wierzchołka. Do tego drzewo musi być spójne, czyli z każdego wierzchołka dojdziesz krawędziami do każdego innego wierzchołka.

9. Co to jest Las?

Las to zbiór drzew. Las sam w sobie ie musi być spójny. Las graf nieskierowany i acykliczny.

10. Co to drzewo ukorzenione?

To takie drzewo którego jeden wierzchołek jest wyróżniony. Zazwyczaj jest to poczatek grafu. Nie ma poprzedników, ale ma następców.

11. Co to liść drzewa?

To taki wierzchołek który nie posiada następców, ale posiada poprzedników.

12. Jak się liczy wysokość drzewa?

Wysokość drzewa liczy się maksymalną ilością krawędzi od korzenia do któregoś z liści. 

13. Co to drzewo uporządkowane?

To drzewo ukorzenione którego dzieci każdego z węzłów są uporządkowane. Czyli musi być w kolejności.
Jako przykład zostało wymienione **drzewo binarne**. Ogólnie chodzi o to, że któryś z wierzchołków powinien być odczytany przed innym wierzchołkiem.

14. Co to drzewo binarne?

To jest takie drzewo którego węzeł ma zawsze dwoje albo zero dzieci (następców)

```
      1
      |
  2-------3
  |       |
4---5   6---7
```


## Drzewa wyszukiwań binarnych

1. Co to drzewo wyszukiwań binarnych (BST)?

Jest to dynamiczna struktura danych (czyli taka która może zmieniać swoją wielkość). Można ją opisać jako słownik jak i kolejkę priorytetową, oraz jest drzewem binarnym.
Każdy z węzłów zawiera informację o lewym i prawym potomku, oraz rodzicu. Jak nie ma poprzednika, lub poprzednika to ten atrybut ma wartość NIL

2. Co to jest własność drzewa BST?

Każdy węzeł zawiera atrybut key (klucz), który jest przechowywany w taki sposób, aby była spełniona własność drzewa BST.

Klucz danego elementu musi być większy od klucza elementu w lewym podrzewie tego elementu i mniejszy, bądź równy co klucz w prawym podrzewie tego elementu.

Dla drzewa:
```
      1
      |
  2-------3
  |       |
4---5   6---7
```
Wartości
```
1.key = 10
2.key = 9
```

Są dobre, ale
```

1.key = 10
2.key = 10
```
są złe.

Dodatkowo 
```
1.key = 10
3.key = 11
3.key = 10
```
Jest dobrze, ale 3.key nie może być mniejsze od 10.

3. Od czego zależy złożoność operacji w drzewie BST?

Zacznijmy od tego, że złożoność operacji to ile kroków trzeba zrobić, aby osiągnąć dany wynik. Np. zsumować wartości wierzchołków drzewa BST.
I złożoność operacji zależy od wysokości drzewa.

4. Jak można opisać złożoność operacji drzewa używając notacji Θ?

W większości przypadków Θ(log n), ale jak napiszesz algorytm jak przedszkolak to Θ(n). Więc ucz się lepiej ok?

5. Gdzie znaleźć najmniejszy klucz drzewa?

Zawsze w ostatnim **NODE** ( wierzchołku ) lewej strony drzewa.
Jest to związane z 

6. Gdzie znaleźć największy klucz drzewa?

Zawsze w ostatnim **NODE ** prawej strony drzewa.

7. Co jest trudniejsze, usuwanie, czy dodawanie węzłów do drzewa?

Usuwanie, bo może zmienić dużo w drzewie.

8. Jak działa wstawianie węzłów w drzewie?

Dobra ja tu omówie ten algorytm co dał, bo większość nic nie zrozumie z tego pseudokodu. Nie wiem czemu nie dodał krótkiego opisu.

```
1: function TREE‐INSERT(T, z)
2:    y ← NIL               // y ustawiamy na NIL, czyli jest puste. To będzie nasz "ogon" (przyszły rodzic).
3:    x ← T.root            // x ustawiamy na początek (korzeń drzewa T). T to nasz obiekt drzewa.
4:    while x != NIL        // Pętla trwa, dopóki x nie spadnie poniżej liści (nie będzie NIL).
5:        y ← x             // Ustawiamy y na x, żeby zapamiętać ostatni nie-pusty węzeł.
6:        if z.key < x.key then // Sprawdzamy, czy klucz nowego node jest mniejszy od klucza x.
7:            x ← x.left    // Jak mniejszy, to idziemy w lewo.
8:        else
9:            x ← x.right   // Jak nie (większy lub równy), to idziemy w prawo.
                            // W pewnym momencie x będzie NIL, a y stanie się ostatnim elementem drzewa.
10:   z.p ← y               // Mamy ostatni element (y), więc ustawiamy go jako rodzica nowego węzła z.
11:   if y = NIL then       // Sprawdzamy, czy y jest NIL.
12:       T.root ← z        // Jeśli tak, drzewo było puste i z zostaje nowym korzeniem.
13:   else if z.key < y.key then // W innym wypadku sprawdzamy, czy z powinno być po lewej...
14:       y.left ← z
15:   else                  // ...czy po prawej stronie rodzica y.
16:       y.right ← z       // Wstawiamy node w odpowiednią stronę. Koniec.
```

**DŁUŻSZY OPIS**

To tak T to jest nasze drzewo. Obiekt drzewa. Ma ono informacje o korzeniu a korzeń o wszystkich jego następcach.

z to nowy node który chcemy dodać. Jego left i right są równe **NIL**, bo dodajemy go, więz musi być ostatnim węzłem drzewa. Za to ma klucz i to jest ważne, bo musimy go wstawić w miejscu, gdzie ten klucz nie popsuje własności BST.

y ustawiamy na NIL, czyli jest puste.
x ustawiamy na początek (korzeń drzewa)

W while będziemy tak długo robić pętle aż nasze x nie będzie NIL. Czyli szybciej czy później będziemy chcieli je ustawić na NIL, ale to później więcej się dowiecie.

Ustawiamy y na x.
Sprawdzamy, czy klucz nowego node jest mniejszy od klucza x. Jak tak to ustawiamy x na node po lewej stronie, jak nie to po prawej. Jest to po to, aby zachować własność.
W pewnym momencie x będzie NIL, bo już po którejś ze stron nie będzie kolejnego elementu, a y stanie się ostatnim elementem drzewa.

Super jak mamy ostatni element drzewa to możemy dodać nowy node.

Ustawiamy rodzica drzewa jako y `z.p <- y`.

Potem sprawdzamy, czy y jest NIL. Jest to po to, bo wtedy to by oznaczało, że nie ma żadnych węzłów w naszym drzewie i nasz nowy node jest korzeniem drzewa.

W innym wypadku sprawdzamy, czy nasz nowy node powinien być po lewej, czy po prawej stronie `y` i wstawiamy go w odpowiednią stronę. 

Koniec.

9. Jak można przechodzić po drzewie? Wymień trzy typy przechodzenia.

- inorder
Przechodzimy od najmniejszego klucza do największego.

-pre-order
Przechodzimy od korzenia drzewa zawsze w lewo. Jak już w lewo nie ma żadnych node cofamy się do rodzica i idziemy w jego prawe dziecko. Jak nie ma prawego dziecka to cofamy się znowu do rodzica.

Po prostu po całym drzewie idziesz i zawsze najpierw wybierasz lewą stronę.

-post-order

Idziesz od lewej strony do prawej. Najpierw sprawdzasz najbardziej wysunięty na lewo ostatni node. Potem prawe dziecko jego rodzica. Potem dopiero rodzica.
Potem przechodzisz na węzeł po prawo od wcześniejszego rodzica i sprawdzasz jego lewe dziecko...

Ogólnie Chcesz zawsze priorytezować lewą stronę, ale zaczynając od dzieci. Żeby przejść do rodzica musisz przejść przez jego wszystkie dzieci.

```python
def preorderTreeWalk(x):
    if x is not None:
        print(x.key)
        preorderTreeWalk(x.left)
        preorderTreeWalk(x.right)

def inorderTreeWalk(x):
    if x is not None:
        inorderTreeWalk(x.left)
        print(x.key)
        inorderTreeWalk(x.right)

def postorderTreeWalk(x):
    if x is not None:
        postorderTreeWalk(x.left)
        postorderTreeWalk(x.right)
        print(x.key)
```

10. Jak usuwać node'y w drzewie?

- Jak dany node nie ma potomków to po prostu go usuwasz.

- Jak ma potomka tylko z jednej strony to ten potomek wskakuje na jego miejsce.

- Jak mamy dwóch potomków i tej z prawej nie ma potomka po lewej stronie to ten potomek z prawej wskakuje w miejsce usuniętego node stając się ojcem potomka z lewej.

- Jak mamy dwóch potomków i tej z prawej ma potomka z lewej to jego potomek z lewej wskakuje na miejsce usuniętego node. Ale tylko jak ten potomek z lewej nie ma z lewej własnego potomka.


---
Ogólnie weźcie tutaj sprawdźcie te algorytmy bo nie skumacie inaczej
https://moodle.ue.poznan.pl/pluginfile.php/1402660/mod_resource/content/1/07_bst.pdf
---

## Sortowanie

1. Jak działa sortowanie przez wstawianie (ang. Insertion-sort)

Lecimy po wszystkich elementach tablicy, ale pierwszego nie analizujemy. Porównujemy, czy dany element jest mniejszy od elementu przed nim. Jeżeli tak to zamieniamy je miejscami.
Kilka razy iterujemy (czyli lecimy po elementach tabicy), aż tablica będzie posortowana.

```
[1, 5, 6, 3, 2]
```
Porównujemy 5 i 1. 1 jest mniejsze to nic nie zmieniamy
```
[1, 5, 6, 3, 2]
```
Porównujemy 6 i 5. 5 jest mniejsze nic nie zmieniamy
```
[1,5,6,3,2]
```
Porównujemy 3 i 6. 6 jest większe. Zamieniamy 3 i 6 miejscami
```
[1,5,3,6,2]
```
Porównujemy 2 i6.  6 jest większe. Zamieniamy 2 i 6 miejscami
```
[1,5,3,2,6]
```

No i znowu lecimy
1 i 5 nic nie zmianiamy
```
[1,5,3,2,6]
```
tutaj 3 i 5 podmieniamy
```
[1,3,5,2,6]
```
5 i 2 zamieniamy miejscami
```
[1,3,2,5,6]
```
Tu 5 i 6 nie zamieniamy bo 5 jest mniejsze od 6
```
[1,3,2,5,6]
```
1 jest mniejsze od 3 zostawiamy
```
[1,3,2,5,6]
```
3 jest większe od 2 zamieniamy miejscami
```
[1,2,3,5,6]
```
Potem reszte porównujemy, ale nie zmieniamy bo już posortowane


A poniżej macie przykładową funkcję w javascript:

```javascript
const arrTest = [1,5,2,4,3];

function sort(arr){
    let sorted = false
    
    while(!sorted){
        // to nam się przyda, aby sprawdzać, czy się coś zamieniło
        let changed = false
        for(let i = 1; i<arr.length; i++){
            // sprawdzamy, czy elementy powinny się zamienić
            if(arr[i] < arr[i-1]){
                let temp = arr[i-1]
                arr[i-1] = arr[i]
                arr[i] = temp
                
                changed = true
            }
        }
        // jak się nic nie zamieniło miejscami to ustawiamy sorted na true co przerywa petle while
        if(!changed)
            sorted = true
    }
    
    // ciekawosta nawet bez zwracania arr, tablica którą daliśmy jako parametr będzie posortowana
    // bo operujemy na elemencie w pamięci podręcznej. Czyli tablcia arrTest jest posortowana i arrTest2 to ta sama tablica
    // w pamięci podręcznej co arrTest
    return arr;
}

const arrTest2 = sort(arrTest)
```

2. Jak działa sortowanie przez scalanie i jakiej metody używa?

Używa metody dziel i zwyciężaj.

Dzielimy jedną tablice na dwie, te dwie na kolejne dwie aż zostaną nam tablice z jednym elementem. Potem lecimy po elementach jednej i drugiej tablicy i je porównujemy. Zawsze ten mniejszy dodajemy pierwszy do nowej posortowanej tablicy. Jak już dodamy element mniejszej tablicy to dodajemy porównujemy kolejny element tej mniejszej tablicy.

```
[5,1,6,3,2,4,8,7]
[5,1,6,3] [2,4,8,7]
[5,1] [6,3] [2,4] [8,7]
[5][1] [6][3] [2][4] [8][7]
```
Warto zaznaczyć, że przy dzieleniu tak naprawde dzielimy do pojedyńczych elementów

Teraz te mniejsze tablice porównujemy i zaczynamy sortować. Jak już mamy posortowaną tablicę to łączymy ją z kolejną.
```
[1,5] [3,6] [2,4] [7,8]
```
Teraz łączymy kolejne pary, ale to już opisze jako para. To samo co zaraz opisze stało się krok wcześniej, ale nie chciało mi się tego opisywać bo to za łatwy przykład.
```
// to jest pusta tablica do której trafiają posortowane liczby
[]
[1,5] [3,6]
// tutaj porównujemy 1 i 3. 1 jest mniejsze
[1]
[5] [3,6]

// Przechodzimy do 5 i porównujemy ją z 3. 3 jest mniejsze
[1,3]
[5] [6]

// Przechodzimy do 6 i porównujemy ją z 5. 5 jest mniejsze

[1,3,5]
[] [6]

// Wrzuciliśmy wszystkie elementy z pierwszej tablicy, więc dorzucamy na koniec resztę z drugiej
[1,3,5,6]
[] []
```

Analogiczne robimy z drugą tablicą aż otrzymamy:
```
[1,3,5,6] [2,4,7,8]
```

Tutaj robimy to samo, czyli porównujemy pierwszy element z pierwszej tablicy z pierwszym z drugiej. Jak dodamy do nowej tablicy element danej tablicy to przechodzimy do kolejnego elementu tej tablicy.

### Kod

```python

// funkcja pomocnicza która operuje na podzielonym elemencie
def merge(left, right):
    A = []
    i,j = 0,0
    
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            A.append(left[i])
            i += 1
        else:
            A.append(right[j])
            j += 1
    
    A += left[i:]
    A += right[j:]
    
    return A
    
def mergesort(A):
    if len(A) > 1:
        q = len(A) // 2
        left = mergesort(A[:q])
        right = mergesort(A[q:])
        return merge(left,right)
    return A

```

3. Jak działa QuickSort?

Bierzemy ostatni element i sprawdzamy ile jest po lewo od niego większych elementów. Przesuwamy ten element, aby po lewo miał element mniejszy a po prawo wszystkie elementy były większe.
Brawo utworzyłeś dwie tablice które oddziela pierwszy przesunięty element. Teraz robisz to samo z tymi mniejszymi tablicami kumasz?

```
[2, 1, 6, 5, 3]
```
Tutaj przesuwamy 3 między 1 a 6
```
[2, 1, 3, 6, 5]
```
Następnie przesuwamy 1 przed 2
```
[1,2,3,6,5]
```
2 nie ma żadnego mniejszego elementu po lewo.
Następnie przesuwamy 5 przed 6
```
[1,2,3,5,6]
```
6 nie ma mniejszego elementu po lewo

Posortowane!

4. Jak można opisać złożoność wykonania sortowania przez wstawianie, scalanie i quick sort?

- Sortowanie przez wstawianie - O(n^2)
- Sortowanie przez scalanie - O(n log n)
- QuickSort - O(n log n), ale może być w najgorszym przypadku O(n^2)

5. Daj algorytmy sortowania przez wstawianie, scalanie i quick sort w kolejności od najszybszego do najwolniejszego.

QuickSort, Scalanie, Wstawianie

Ale też może być

Scalanie, QuickSort = Wstawianie

Ze złymi danymi wejściowymi QuickSort jest tak szybki jak Wstawianie. Niby złożoność czasowa QuickSort jest taka jak scalania, ale jednak jest szybszy.

6. Co to znaczy, że algorytm jest niestabilny?

Chodzi o to, że jak mamy dwa elementy o wartości np. 5. To te elementy przy stabilnym algorytmie pierwszy element z wartością 5 będzie dalej pierwszy.
Przy niestabilnym, te elementy o tej samej wartośći mogą zmienić kolejność.

7. Podaj stabilność algorytmów sortowania przez wstawianie, scalanie i quick sort.

Wstawianie - stabilny
scalanie - stabilny
quick sort - niestabilny
