---
layout: post
title: Blueprint-CSS
---

<blockquote>
<img src="../../../../images/alan-perlis.gif" alt="[Alan Perlis]" />
<p>
  Dealing with failure is easy: Work hard to improve. Success is also
  easy to handle: You've solved the wrong problem. Work hard to improve.
</p>
<p class="author">— Alan Perlis</p>
</blockquote>

# {{ page.title }}

## Blueprint-CSS!

Druge laboratoria obfitowały w kolejne emocje. Pomimo usilnych prób, Prowadzącemu nie udało się uruchomić strony domowej - musieliśmy zadowolić się wersją odpalaną z portu 8006.
    
Tym razem do czynienia mieliśmy z Blueprint-CSS, który jak można się domyśleć, jest frameworkiem do CSS-ów. Rozpoczeliśmy od pobrania repozytorium z Githuba. Krótka czytanka pliku Readme i Tutoriala w połaczeniu z pięcioma minutami zaowocowała postaniem [strony testowej](http://sigma.inf.ug.edu.pl/~mmackows/rails3/maq.html).
   
Warto wiedzieć, że Blueprint bazuje na podstawie siatki standardowo na 24 części, po 30 pikseli każda + odstepów między nimi, po 10 pikseli. Całość daje 950 pikseli szerokości. Bazując na domyślnych ustawieniach, można z nudów zapisać swoje imię - [jak tutaj](http://sigma.inf.ug.edu.pl/~mmackows/rails3/maq2.html). Kolejne litery są wpisane w bloki o tej samej szerokości, lecz owe są przesunięte (za pomocą klasy prepend o wzrastające wartości 1..5).
   
Następnie zainteresowaliśmy się narzędziem compress.rb. Pozwala ono spersonalizować ustawienia dotyczące szerokości bloków i odstępów, o których wspomniałem wyżej. Wyeksportowałem nowe pliki css, wybierając następujące wartości 40/25/15, kolejno szerość bloków/marginesy/ilość bloków (szerokośc 950 pikseli została bez zmian). Po aktualizacji ta sama strona wygląda [trochę inaczej](http://sigma.inf.ug.edu.pl/~mmackows/rails3/maq3.html). Widać, że bloki są zbyt szerokie by cały napis się zmieścił - ale to nie nasz problem, przynajmniej nauczyliśmy się modyfikować css-y narzędziem compress.rb :) Przy okazji [cukierek dla leniuchów](http://kematzy.com/blueprint-generator/)
   
Jedziemy dalej. Przy pomocy wtyczki Dust-Me Selectors dowiaduję się, że moja pierwsza strona testowa zawiera jedynie 427 nieużywanych selektorów. To chyba dużo przy 17 używanych. Sprzątamy...

<img src="http://sigma.inf.univ.gda.pl/~mmackows/rails3/dms.jpg" alt="[Dust-Me Selectors]"
   
Wow, jesteśmy przy trzecim punkcie - walidacja HTML i CSS. Walidowaliśmy od początku, więc mamy z głowy ;)
   
Ostatnia misja - YSlow. To wtyczka do Firefoxa, która potrafi oceniać poprawnośc/przejrzystośc/wydajność witryn internetowych. Bułka z masłem. Szybka instalacja i biorę pod lupę stronę testową z uśmiechniętym Murzynkiem ;) Dostajemy A z notą 90 pointsów. Całkiem całkiem ]:> Z ciekawości robię kilka testów - 

<table><tr><td>URL</td><td>Ocena/Punkty</td><td></td></tr>
<tr><td>www.google.pl</td><td>A i nota 97</td><td>z nimi przegrać to zaszczyt</td></tr>
<tr><td>www.onet.pl</td><td>C i 65 pktów</td><td>niszczymy ich!</td></tr>
<tr><td>www.inf.ug.edu.pl</td><td>C i 72 punkty</td><td>to było do przewidzenia :P</td></tr>
</table>.

Tyle roboty na dzisiaj - jutro też jest dzień ;-)