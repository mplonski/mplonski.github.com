---
layout: post
title: "języki ezoteryczne - technologia przyszłości?"
date: 2013-12-11 21:00:00
category: code
tags: [język ezoteryczny, brainfuck, whitespace, asdf, dogescript, blub, ook, chef, lolcode, shakespeare, perl, one-liner, wtf, wtf-level]

description: "Wczoraj miałem przyjemność wygłosić krótką prezentację na temat języków ezoterycznych. Dla tych, którym ten termin jest obcy, już ślę zaproszenie do wikipedii. Najogólniej mówiąc są to takie języki programowania, na których widok pierwszą reakcją jest WTF."
excerpt: "/assets/images/bitstrip.png"

---

{% include JB/setup %}

Wczoraj miałem przyjemność wygłosić krótką prezentację na temat języków ezoterycznych. Dla tych, którym ten termin jest obcy, już ślę zaproszenie do [wikipedii](http://pl.wikipedia.org/wiki/Ezoteryczny_j%C4%99zyk_programowania). Najogólniej mówiąc są to takie języki programowania, na których widok pierwszą reakcją jest WTF.

1) Czym jest WTF-level.
-----------------------

W naszym codziennym życiu **wiele razy spotykamy się z sytuacjami, na które jedyną rozsądną reakcją jest WTF**. Pewni mądrzy ludzie wpadli na pomysł, aby można było jakoś mierzyć poziom tej reakcji, więc wymyślono WTF-level. Niestety **nie ma on żadnej jednostki**, a jedynym sposobem pomiaru jest porównanie do efektu uzyskanego przy innej sytuacji.

Warto wspomnieć, że **WTF-level jest dosyć wszechstronny**. Nie istnieje on tylko w świecie IT, ale także w każdej dziedzinie naszego życia. Można go używać zarówno do oceny naszej pracy (WTF?! co to za kod?!), naszego życia osobistego (WTF?! to jest na obiad?!), a także sytuacji codziennych (WTF?! co on tutaj robi?!).

**Największy poziom WTF-level zachowany jest przy sytuacjach niecodziennych, nietypowych.** Dlatego postanowiłem, że idealnie spisuje się przy ezoterycznych językach, przy których często jedyną reakcją jest właśnie WTF (i czasem śmiech).

2) Przykłady języków ezoterycznych.
-----------------------------------

**Uwaga:** Dla zwiększenia czytelności niektóre fragmenty kodu urywają się w pewnej części. Jeśli (nie wiadomo po co) chcecie skompilować kod, pobierzcie go ze strony autora języka.

(Chyba) **najbardziej popularnym językiem z tej rodziny jest [Brainfuck](http://pl.wikipedia.org/wiki/Brainfuck)**. Składa się on jedynie ze znaków większy / mniejszy, plusa, minusa, kropki, przecinka i nawiasów kwadratowych. Przykładowo, oto jest Hello World w Brainfucku:

	++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.

Przejdziemy teraz do kolejnej perełki, czyli **[Whitespace](http://compsoc.dur.ac.uk/whitespace/)**. Język ten jest jeszcze prostszy - **jedyną składnią są spacje, tabulatory i nowe linie**. Przykładowy kod? Tym razem oszczędzę tych atrakcji, poszukajcie w googlu.

Kolejnym językiem (albo i nie językiem?) jest **[dogescript](https://github.com/remixz/dogescript)**. Powstał on z powodu słynnego psa, wow psa. Przykładowy kod? Proszę:

	shh THIS IS DOGESCRIPT
	
	trained
	
	so dogeudle
	so boring as wow
	
	very dogescript is 'such messy; very doge-friendly'
	
Z psiego języka przechodzimy do **[asdf](http://esolangs.org/wiki/Asdf)**. Zasada działania podobna jest jak w Brainfucku, jednak tym razem zmniejszyliśmy ilość znaków: **mamy do dyspozycji jedynie 4 literki** z nazwy języka. Hello World:

	sasaaaasssasaaaasssasaasssasaasssasaasssasaasssasaaaasssasaasssasaaaasssasaaaaaasssas
	aasssasaaaaaaaasssasaaaasssasaasssasaasssasaaaasssasaaaaaaaasssasaasssasaaaaaaaaaaaas
	ssasaasssasaaaaaaaasssasaasssasaaaaaasssasaaaasssasaasssasaaaasssasaaaasssasaasssasaa
	sssasaaaaaasssasaaaasssasaaaasssasaasssasaaaaaaaasssasaasssasaaaaaaaasssasaa

Jeśli już nauczyliśmy się większej ilości znaków to możemy przejść do **[Blub](http://esolangs.org/wiki/Blub)**. Nawet najstarsi programiści wiedzą, że jakoś trzeba dogadywać się z rybami, a właśnie **Blub to jedyny język, który rozumiany jest także przez ryby**. Jeśli chcemy wyświetlić *Hello World!* to wystarczy skorzystać z takiego kodu:

	blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub! blub?
	blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub? blub! blub!
	blub? blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub. blub.
	blub. blub. blub. blub. blub. blub. blub? blub! blub! blub? blub! blub? blub. blub. blub.

Wiadomo jednak, że nie samymi rybami człowiek żyje i trzeba jakoś dogadać się z ludźmi. Jeśli nauczyliśmy się mówić Ok! to możemy skorzystać z języka **[Ook!](http://esolangs.org/wiki/Ook!)**. Składni domyślcie się sami po zeknięciu na kod:

	Ook. Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
	Ook. Ook. Ook. Ook. Ook! Ook? Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
	Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook? Ook! Ook! Ook? Ook! Ook? Ook.
	Ook! Ook. Ook. Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.

Tymczasem przejdziemy do czegoś bardziej zaawansowanego. **Jeśli nauczyliśmy się układać słowa to możemy skorzystać z języka [Chef](http://esolangs.org/wiki/Chef)**, który przypomina raczej przepis na pyszne danie (w tym przypadku znów Hello World!).

	Hello World Souffle.
	
	Ingredients.
	72 g haricot beans
	101 eggs
	33 potatoes
	
	Method.
	Put potatoes into the mixing bowl.
	Put dijon mustard into the mixing bowl.
	Pour contents of the mixing bowl into the baking dish.
	
	Serves 1.

Z kuchni przechodzimy do misek i rybek, czyli kotów. Tym razem chciałbym pokazać Wam słynny na świat cały **[LOLCODE](http://esolangs.org/wiki/LOLCODE)**, który, podobnie jak Blub, dedykowany jest zwierzętom, tym razem kotom. Witaj świecie!

	HAI
	CAN HAS STDIO?
	VISIBLE "HAI WORLD!"
	KTHXBYE

O kotach są różne poradniki, czyli czas na książki. Dla fanów dzieł wielkiego poety (tym razem nie Mickiewicza) mam propozycję języka **[Shakespeare](http://en.wikipedia.org/wiki/Shakespeare_%28programming_language%29)**. Chcecie się przywitać? Oto i kawałek kodu:

	Romeo, a young man with a remarkable patience.
	Juliet, a likewise young woman of remarkable grace.
	Ophelia, a remarkable woman much in dispute with Hamlet.
	Hamlet, the flatterer of Andersen Insulting A/S.
	
	                   Act I: Hamlet's insults and flattery.
	                   Scene I: The insulting of Romeo.
	[Enter Hamlet and Romeo]
	Hamlet:
	You lying stupid fatherless big smelly half-witted coward! You are as
	stupid as the difference between a handsome rich brave hero and thyself!
	Speak your mind!
	[Exit Romeo]

Wspomnę, że wyświetlenie "Hello World!" zajmuje jedynie dwa akty, z czego pierwszy składa się z trzech, a drugi z dwóch scen.

Po nasyceniu się egzotycznymi językami chciałbym przejść do tych bliższych rzeczywistości. **Uznawanym za najdziwniejszy język jest często Perl**, któremu bliżej jest do awk czy sed, a nie znanego nam modelu programowania.

Na koniec wspomnę o słynnych **one-linerach** (nie są językiem, ale są dziwne!), które są ulubionymi źródłami błędów i lansu programisto-administratorów. Czy jest w końcu coś piękniejszego od 10-linijkowego polecenia, które działa i robi pożądane zadanie? Nikt nie zna fenomenu tych rozwiązań, ale na ich widok niektórym od razu skacze poziom szczęścia ponad 60. piętro.

3) Gdzie sens? Gdzie logika?
----------------------------

Jeśli chwilę pomyślimy to **wyżej wymienione języki (oprócz Perla;) nie są używane w codziennej pracy**, a raczej jako rozrywka dla ludzi z IT. Niestety nie udało mi się znaleźć żadnej pracy naukowej na ten temat, a sam nie widzę w tych rozwiązaniach sensu oprócz zwykłej zabawy.

**Jedyną opcją, w których te języki miałyby jakiś sens, jest IT w filmach i serialach.** Ile to razy widzieliśmy hakowanie wielkich sieci poprzez wyświetlenie plików w katalogu czy odpalenia traceroute? Może gdyby zamiast tego stosować Brainfucka albo Blub to byłoby ciekawiej? Przynajmniej ludzie wiedzący coś o tej dziedzinie mieliby niezły ubaw.

4) Podsumowanie.
----------------

Języki tego typu nie mają żadnego sensu, oczywiście oprócz zabawy. A dla zainteresowanych zamieszczam moją prezentację (są obrazki):

<iframe
	src="http://www.slideshare.net/slideshow/embed_code/29053933"
	width="500px"
	height="330px"
	frameborder="0"
	marginwidth="0"
	marginheight="0"
	scrolling="no"
	style="border:1px solid #CCC;border-width:1px 1px 0;margin-bottom:5px"
	allowfullscreen="allowfullscreen"
> </iframe>

[Most Bizarre Programming Languages Ever Created](https://www.slideshare.net/mplonski/most-bizarre-programming-languages-ever-created) @ SlideShare

