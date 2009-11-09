---
layout: post
title: Pierwsze koty za płoty
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

## Ostra jazda z Rails!

Co dzisiaj będziemy robić? Nie, nie, tym razem nie będziemy podbijać świata. Mamy ciekawsze zajęcia - zaczynamy bowiem zabawę z Railsami.

Startujemy od wygenerowania nowego projektu komendą
{% highlight html %}
rails kontakty
{% endhighlight %}

Linie tekstu śmigają nam przed oczami, dobrze! Pełna automatyzacja, to mi się podoba. Chcielibyśmy widzieć efekty naszej pracy więc startujemy serwer komendą 
{% highlight html %}
./script/server -d
{% endhighlight %}
Nasza pierwsza aplikacja to lista kontaktów, zatem przydałoby wygenerować jakiś szkielet obiektów, które będziemy przetrzymywać. Z odsieczą przychodzi nam
{% highlight html %}
./script/generate scaffold osoba imie:string nazwisko:string telefon:string
{% endhighlight %}
Pola dla imienia, nazwiska i telefonu powinny wystarczyć :) Musimy wykonać jeszcze migrację, więc z katalogu db wklepujemy 
{% highlight html %}
rake db:migration
{% endhighlight %}
Wpisując adres http://localhost:3000 możemy podziwiać efekt naszych trzyminutowych wypocin. Co prawda lista nie jest zbytnio funkcjonalna (zapewnia odczyt rekordów, dodawanie nowych, edytowanie istniejących i usuwanie niepotrzebnych), nie zachwyca również oprawą graficzną, ale zostawiamy sobie to na później :)
   
Naturalnie, na koniec pozwolę zagrać głos YSlow - A i 96 pointsów nie jest oceną złą. Tradycyjnie skarcono mnie za brak kompresji i expire headers. Pal to licho, nie jest źle jak na 5 minut roboty. W najbliższym czasie postaram się zainstalować jakiś layout, a na razie chillout (dobry rym!).