---
layout: post
title: "jak stary jest Twój linux?"
date: 2014-04-21 21:00:00
category: code
tags: [linux, wiek, debian]

description: "W życiu każdego użytkownika, kiedy serwer w pracy nie działa, skończył się ostatni poziom w ulubionej grze i brzuszek jest już bardzo zadowolony pojawia się pewne pytanie - ile lat ma mój linux. Okazuje się, że uzyskanie odpowiedzi na to pytanie nie jest trywialne, ale wymaga podejścia trochę naokoło."
excerpt: ""

---

{% include JB/setup %}

W życiu każdego użytkownika, kiedy serwer w pracy nie działa, skończył się ostatni poziom w ulubionej grze i brzuszek jest już bardzo zadowolony pojawia się pewne pytanie - ile lat ma mój linux. Okazuje się, że uzyskanie odpowiedzi na to pytanie nie jest trywialne, ale wymaga podejścia trochę naokoło.

Niestety system nie przechowuje informacji o dacie instalacji, więc możemy spróbować zrobić to wykorzystując następujące sposoby:

1) Logi z instalacji.
---------------------

Jeśli ktoś ma szczęście i uchowały się logi z instalacji - może w nich być data ich utworzenia i zapisu.

2) Wiek katalogu.
-----------------

Drugim pomysłem jest sprawdzenie daty utworzenia bądź ostatniej modyfikacji jednego z katalogów systemowych. Wykonujemy to poleceniem **stat**. Przykład:

<pre><code class="bash">tosia:~# stat /root/
  Plik: „/root/”
  rozmiar: 4096         bloków: 8          bloki I/O: 4096   katalog
Urządzenie: 801h/2049d  inody: 914030      dowiązań: 32
Dostęp: (0700/drwx------)  Uid: (    0/    root)   Gid: (    0/    root)
Dostęp:      2013-06-02 18:08:28.505365611 +0200
Modyfikacja: 2014-04-21 03:12:37.297245049 +0200
Zmiana:      2014-04-21 03:12:37.297245049 +0200
Utworzenie:  -</code></pre>

3) Wiek systemu plików.
-----------------------

Może jednak okazać się, tak samo jak powyżej, że system plików nie zapisuje informacji o dacie utworzenia. Wtedy musimy sięgnąć do ustawień dysku, a dokładnie jednej z naszych partycji. Warto jednak pamiętać, że jeśli nadpisaliśmy system na poprzedni bez ruszania układy partycji - ten sposób także zawiedzie.

Najpierw warto sprawdzić poleceniem **df -h** jakie mamy obecne partycje. Opcji -h użyjemy, aby przedstawione wartości miały bardziej ludzką postać.

<pre><code class="bash">tosia:~# df -h   
System plików  rozm. użyte dost. %uż. zamont. na
/dev/sda1        22G   15G  5,5G  74% /
udev             10M     0   10M   0% /dev
tmpfs           357M  576K  356M   1% /run
tmpfs           5,0M     0  5,0M   0% /run/lock
tmpfs           713M  3,2M  710M   1% /run/shm
none            1,8G  296K  1,8G   1% /tmp</code></pre>

Powyżej widzimy, że partycji głównej (**/**) odpowiada **/dev/sda1**. Teraz sprawdzamy kiedy utworzyliśmy partycję korzystając z **tune2fs**:

<pre><code class="bash">tosia:~# tune2fs -l /dev/sda1 | grep created
Filesystem created:       Thu Feb 28 00:45:07 2013</code></pre>

Dzięki grepowi wyświetla nam się jedynie data utworzenia partycji, a nie wszystkie informacje o niej.

3) Jeśli wszystko zawiedzie...
------------------------------

Jeśli wiemy, że data utworzenia partycji nie będzie zgadzać się z datą instalacji to... pozostaje nam uruchomić własną wyobraźnię. Mimo wszystko powyższe dwa sposoby powinny dać radę w znacznej części przypadków, szczególnie 2. :-)

