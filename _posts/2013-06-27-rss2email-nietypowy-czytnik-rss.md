---
layout: post
title: "rss2email - nietypowy czytnik rss"
date: 2013-06-27 17:50:00
category: theory
tags: [rss2email, rss, atom, linux, windows, mac os]

description: "Google już w marcu zapowiedziało, że z dniem 1. lipca zamyka usługę Google Reader. Nie trzeba go nikomu przedstawiać - znany i bardzo wygodny czytnik rss był wykorzystywany przez ogrom osób. Co może go zastąpić? Nie wiem, pokażę Wam za to pewną ciekawą alternatywę."
excerpt: "/assets/images/2013/8-reader.jpg"

---

{% include JB/setup %}

Google już w marcu zapowiedziało, że [z dniem 1. lipca zamyka usługę Google Reader](http://googleblog.blogspot.com/2013/03/a-second-spring-of-cleaning.html). Nie trzeba go nikomu przedstawiać - znany i bardzo wygodny czytnik rss był wykorzystywany przez ogrom osób. Co może go zastąpić? Nie wiem, pokażę Wam za to pewną ciekawą alternatywę.

<img src="/assets/images/2013/8-reader.jpg" alt="staromodny czytnik rss" />

1) Na czym mi zależało? (i nadal zależy)
----------------------------------------

Podstawą przy szukaniu jakiegokolwiek rozwiązania czy oprogramowania jest zdefiniowanie co tak naprawdę chcemy mieć. Bardzo lubiłem Google Readera i szukałem czegoś podobnego. Wziąłem się za testy różnych aplikacji i... żadna mi nie podpasowała. Niektóre nie umożliwiały swobodnego przeglądania newsów (skróty klawiszowe!), niektóre nie działały poprawnie, niektóre mocno psociły. W końcu wybór padł na feedly, jednak z uwagi na powtarzające się błędy miałem w końcu ich dość. Zacząłem szukać czegoś ciekawszego.

2) Lubisz swoją pocztę?
-----------------------

Nie wiem jak Wy, ale ja na poczcie (tej internetowej, nie tradycyjnej) spędzam ogromną ilość czasu. Ba, lubię interfejs i uważam go za bardzo wygodny. Co powiecie na to, że wiadomości z rssów będą lądowały prosto do Waszej skrzynki? Mi się ten pomysł spodobał i właśnie jego postanowiłem wdrożyć. Wyszło z tego jeszcze trochę dobrego, bo zamiast przeskakiwać między pocztą a czytnikiem rss i fejsem, została sama poczta i fejs.

3) rss2email, czyli mój mały sekret
-----------------------------------

Moim wymogom sprostała aplikacja [rss2email](http://www.allthingsrss.com/rss2email/), która, zgodnie z nazwą, wysyła wiadomości z rssów na maila. Napisana jest w Pythonie i należy postawić ją na własnym komputerze. Dzięki tym cechom i mojej znajomości pythona mogę zmieniać w niej co chcę, będzie działać jeśli tylko będę chciał (w końcu jest na moim serwerze), a w dodatku mam wygodny interfejs w postaci swojego maila.

Nie będę psuć wpisu nudną instrukcją instalacji i konfiguracji, bo cały proces jest dokładnie opisany na stronie autora. Ostrzegę Was jedynie, aby nie brać wersji z repozytorium, ale od razu pobierać najnowszą edycję ze strony internetowej (inaczej będziecie mieli problem z konfiguracją, która się trochę zmienia zależnie od wersji). Przy pobraniu programu zajmuje on jedynie 1 katalog i dokładnie wiecie gdzie wszystko jest.

4) Ale zaraz, i tak mam dużo maili!
-----------------------------------

Ja też. Powiem jedno - segreguj je. Mam w mailu dużo etykiet i filtrów, a program umożliwia wysłanie wiadomości z każdego kanału na inny adres. Ja podzieliłem wiadomości podobnie jak w czytniku. Jak? Każdy serwer poczty powinien uznawać, że między loginem i małpką może być plus i dowolny ciąg znaków dozwolonych przez RFC, więc mail+costam@example.com jest to dokładnie to samo co mail@example.com. W rss2email ustawiłem odpowiednie adresy dla rssów, a w poczcie filtruję wiadomości po adresie odbiorcy i wrzucam do odpowiedniej szufladki. Wszystko jest piękne i działa bardzo dobrze.

5) Podsumowanie.
----------------

Rss2email jest moim zdaniem najciekawszą alternatywą dla google readera. Mogę dowolnie zmieniać co chcę i kiedy chcę oraz nie ma kogoś, kto może zamknąć czytnik. Śmiało mogę powiedzieć, że ilością funkcjonalności przerosło to stary czytnik i moje oczekiwania (na plus!). Jeśli nie umiecie / nie macie jak postawić rss2email to są 2 opcje - albo się nauczyć (to proste, instrukcja jest na stronie projektu), albo skorzystać z komercyjnych projektów, które oferują to samo. Nie używałem, więc żadnego nie polecę.

foto: [flickr](http://www.flickr.com/photos/8579740@N02/3820957485/)

