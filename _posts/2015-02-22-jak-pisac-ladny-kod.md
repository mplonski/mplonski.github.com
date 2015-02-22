---
layout: post
title: "jak pisać ładny kod?"
date: 2015-02-22 20:00:00
category: code
tags: [teoria, code, self-documented code, rupy, ruby, python]

description: "Początkujący programista cieszy się gdy jego kod działa. Średniozaawansowany programista cieszy się gdy jego kod jest udokumentowany. Zaawansowany programista cieszy się gdy jego kod ładnie wygląda. Jak pisać ładny kod?"
excerpt: ""

---

{% include JB/setup %}

Początkujący programista cieszy się gdy jego kod działa. Średniozaawansowany programista cieszy się gdy jego kod jest udokumentowany. Zaawansowany programista cieszy się gdy jego kod ładnie wygląda.

W ciągu ostatnich dwóch miesięcy moje podejście do programowania uległo znacznej zmianie. Zaczęło się od prezentacji wygłoszonej na dosyć słynnych spotkaniach RuPy:

<iframe width="560" height="315" src="https://www.youtube.com/embed/h2g8BhQhuTM" frameborder="0" allowfullscreen="allowfullscreen"> </iframe>

Większość programistów zamiast pomyśleć jak uczynić kod czytelniejszym czy ładniejszym po prostu… dodaje komentarze, bo słyszeli, że trzeba komentować. Mniej osób zauważa, że zamiast tworzyć dodatkowe linijki komentarzy opisujące co tak naprawdę robimy możemy po prostu przez sam kod powiedzieć co się dzieje. Pomaga w tym kilka rzeczy:

1) Dzielenie kodu na małe kawałki.
==================================

To spodobało mi się w rubym, który jest dosyć rygorystyczny jeśli chodzi o długość kodu. Niektóre walidatory sugerują ograniczenie długości metody nawet do 10 linii, co mi osobiście bardzo się spodobało, ale dopiero po chwili stosowania nowej konwencji. Początkowo było mocno irytujące.

Największe uproszczenie i sens dzielenia jest taki, że metodę, która ma maksymalnie 10-15 linijek łatwo ogarnąć na raz wzrokiem i wiemy co się w niej dzieje. Przy dłuższych - trzeba już chwilę pomyśleć.

Podoba sytuacja jest przy dzieleniu klas / modułów - ogarnięcie co się dzieje w pliku mającym 100 linijek jest proste, przy tych dłuższych już zaczynamy kręcić głową i szykować od razu dwa kubki kawy. :)

2) Tworzenie samodokumentującego się kodu.
==========================================

W sumie to tutaj mogę odesłać do wideo powyżej. W największym skrócie chodzi o to, aby stosować dobre nazwy zmiennych i odpowiednią składkę języka, która sama zasugeruje co się dzieje. Moim ulubionym przykładem jest:

{% highlight python %}
if not c in b:
	pass

if city not in available_city_set:
	pass
{% endhighlight %}

Niby obie instrukcje zrobią to samo, ale druga jest znacznie czytelniejsza. Odpowiednia kolejność instrukcji w kodzie, jak widać, także ma spore znaczenie dla czytelności. Nie mniej niż dobre nazwanie zmiennych, które mówią od razu kim są.

3) Refactoring jako etap programowania.
=======================================

Większość osób uznaje, że od razu po napisaniu kodu i testach można go wdrażać. Ja do programowania dodałem na stałe dodatkowy etap - refactoring tego, co przed chwilą napisałem. Normą jest, że ten kilkuminutowy kod jest już dla mnie brzydki i warto go zmienić.

Dodatkowo często w trakcie pisania kodu tak naprawdę wyjdzie coś dodatkowo, co jednak zajmie znacznie więcej niż się spodziewaliśmy, albo zmienne muszą być trochę inaczej wykorzystane niż było planowane, albo w ogóle zmieni się jakieś założenie… klasyka.

Wynikiem tych wszystkich zmian i naszych błędów jest to, że po napisaniu kodu należy go dokładnie obejrzeć i już od razu przeprowadzić refactoring. Poprawić nazwy zmiennych, może zmienić kolejność, dodać gdzieś enter, podzielić kod na mniejsze kawałki.

4) Code review jako część developmentu.
=======================================

Nie rozumiem dlaczego, ale etap code review przy grupowych pracach jest uznawany często za coś, co jest gdzieś tam na końcu, bo musi być. Moim zdaniem code review powinien być realizowany z całkiem innym założeniem i celem. On nie ma być umieszczony na końcu developmentu, ale w środku, aby spokojnie mieć czas na poprawki, których sami musimy chcieć.

Zmiana podejścia prowadzi do tego, że oddawany do code review kod nie jest tak wypieszczony jak zazwyczaj, bo i tak często mogą być spore zmiany z uwagi na to, że coś przegapiliśmy albo zrobiliśmy nieoptymalnie. Albo, po prostu, coś mocno popsuliśmy :-)

Oczywiście można zamiast tego omawiać dokładnie koncepcję każdego kawałka kodu, ale tak czy tak code review zawsze wychwyci jakiś głupi błąd czy konstrukcję, którą można zastąpić inną. Albo w ogóle skreśli rozwiązanie i zasugeruje lepsze.

5) Jak wygląda u mnie development?
==================================

Po kolei:
- analiza rozwiązań
- testy możliwych rozwiązań, wybór jednego
- przemyślenie implementacji
- implementacja
- napisanie testów, testy, poprawki
- refactoring
- skierowanie do code review
- poprawki po code review
- skierowanie na produkcję

Myślicie, że jak wygląda podział czasu? Implementacja zajmuje dużo? Nie, najwięcej zajmuje refactoring własnego kodu i poprawki po code review. Bo nasz kod ma nie tylko działać, ale też ładnie wyglądać, aby patrząc na niego za pół od razu od razu było wiadomo o co chodzi.

6) Czy umiem pisać ładny kod?
=============================

Nie, nie umiem. Wiem za to kiedy będzie dobrze - w znajomej firmie gdzie roi się od senior developerów ostatnio jedyna dyskusja nad kawałkiem kodu czekającym na code review była czy zmienna powinna zaczynać się od `unlisted` czy `not_listed` i tak cały dzień… chciałbym same takie problemy :-)

No i na koniec chyba najważniejsze, nie bójmy się zmian własnych zwyczajów. Czasem coś, co wydaje się gorsze, tak naprawdę z perspektywy czasu zaprowadzi nas na lepszą drogę.
