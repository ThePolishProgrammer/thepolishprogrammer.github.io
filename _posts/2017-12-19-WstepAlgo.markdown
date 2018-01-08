---
layout: post
title:  "Wstęp do algorytmiki. #1 Pojęcie algorytmu"
date:   2017-12-19
categories: algo
---

## Do kogo kierowany jest ten kurs?

Kurs kieruje głównie do osób początkujących jeśli chodzi o algorytmikę,
co oczywiście można wydedukować już po tytule. Oczękuję chociaż bardzo podstawowej
znajomości jakiegoś języka programowania. Chcę tu wspomnieć również
iż nie będę tu uczył żadnego konkretnego języka. Przykłady
będą przedstawione najczęściej w pseudokodzie lub w postaci blokowej.
Do każdego algorytmu będzie dołączona jego implementacja w jednym lub
kilku językach takich jak C, C++ czy Lua.

## Czym jest algorytm?

Algorytm - to zestaw instrukcji przeznaczony do rozwiązania danego problemu, zadania.
Przykładem z życia wziętym może być chociażby przepis kulinarny:

##### Przepis na naleśniki

* Przygotuj dużą miskę
...
* Dodaj mleko
...

(...)

Oczywiście przepis jest algorytmem zrozumiałym dla człowieka, a komputer
nie wiedziałby jak ma te dane interpretować.
Przedstawiony powyżej sposób reprezentacji nazywany jest listą kroków.
Mamy również sposoby przedstawiania algorytmów takie jak: 
pseudokod, schemat blokowy, kod źródłowy w danym języku programowania
(szerzej omówione w dalszej części).

Po co nam właściwie algorytmy? Głównie po to aby rozwiązywać skompilkowane problemy
z użyciem komputera, np. chcemy  posortować rosnąco dowolny zbiór liczb całkowitych. W tym przypadku nie możemy po prostu „powiedzieć” naszemu procesorowi w komputerze: „posortuj mi te liczby”. 
Musimy mu „wyjaśnić” jak ma to wykonywać, używając przy tym prostych, podstawowych poleceń zrozumiałych dla komputera. I tu z pomocą przychodzi algorytmika. 


## Sposoby reprezentacji

### Lista kroków

Z tym sposobem najczęściej spotykamy się najczęściej, znajduje on zastosowanie w wielu instrukcjach
obsługi, przepisach kulinarnych i nie tylko. Przykład algorytmu mnożącego dwie liczby a i b:

1. Wczytaj A i B
2. Zapisz do C wynik A*B
3. Wypisz C

### Schemat blokowy

Schematy blokowe są jedną z najlepszych metod obrazowania działania algorytmów.
Składają się one (jak sama nazwa mówi) z bloków. Na początku mamy tzw. blok start,
który mówi, od którego miejsca zacząć wykonywanie algorytmu, następnie mamy bloki
instrukcji połączone strzałkami, które wskazują kierunek wykonywania. Na końcu znajduje
się blok końca, oznaczający oczywiście koniecy wykonywania. Przykład schematu blokowego
(algorytm sprawdzający czy liczba jest parzysta):

![przykład schematu blokowego]({{ "/assets/algo_example.png" | absolute_url }})

### Pseudokod

Pseudokod to uogólnione przedstawienie algorytmu, które zachowując strukturę charakterystyczną dla kodu zapisanego w języku programowania, rezygnuje ze ścisłych reguł składniowych na rzecz prostoty i czytelności (nie zawiera szczegółów implementacyjnych). Przykładowy pseudokod:

{% highlight plain-text %}
jeżeli a | 2   to
wypisz "Parzysta liczba!"
jeżeli nie to
wypisz "Nieparzysta liczba!"
koniec warunku
{% endhighlight %}

### Kod źródłowy w danym języku programowania

Jeśli miałeś/aś już styczność z programowaniem w jakimś języku (a powinieneś/aś) to nie będzie to dla ciebie żadna magia. Kilka przykładów algorytmów w różnych językach:

C/C++:
{% highlight cpp %}

bool isEven(int x){
	if(x%2==0) return true;
	return false;
}

{% endhighlight %}

Lua:
{% highlight lua %}
function isEven(number)
	return number % 2 == 0
end
{% endhighlight %}

Java:
{% highlight java %}
public static boolean isEven(int number){
	return (number%2==0);
}
{% endhighlight %}

## Zakończenie

Zapraszam do następnej części kursu.
