# Šolska zadruga SERŠ Market

Skupinski projekt RPS, skupina 1, 2. d, SERŠ Maribor, 2026/27. Mentor: Sergej Lah.

[Predstavitev DN1](https://rene-brodnjak.github.io/SERS-Market-RPS/) · [Izpolnjeni delovni list](projektna-listina.docx) · [Predogled listine](https://rene-brodnjak.github.io/SERS-Market-RPS/projektna-listina.html) · [GitHub Projects Kanban](https://github.com/users/rene-brodnjak/projects/1)

## Ekipa in odgovornosti

| Član | GitHub | Vloge |
| --- | --- | --- |
| Rene Brodnjak | [@rene-brodnjak](https://github.com/rene-brodnjak) | Vodja, PHP zaledje, MariaDB in cPanel |
| Gašper Kramberger | [@gasperkramberger-ctrl](https://github.com/gasperkramberger-ctrl) | HTML5/Pico.css, testiranje, README in Kanban |

Gašperju je poslano povabilo za sodelovanje. Dostop za pisanje začne veljati, ko ga sprejme.

Predhodni nalogi DN1: [Rene](https://github.com/rene-brodnjak/Solska-Zadruga-SERS-Market) in [Gašper](https://github.com/gasperkramberger-ctrl/moja-prva-RPS-web).

## Problem in cilj

Dijak pri naročanju šolskih majic, kap in laboratorijskih halj težko preveri velikost, zalogo in prevzem. MVP bo omogočal pregled ponudbe in oddajo naročila z dijaškim e-naslovom ter potrditev prevzema v šoli.

Persona je Luka Novak, 17 let, dijak 2. letnika računalništva. Izpolnjeni učiteljev delovni list vsebuje profil, štiri kvadrante empatije, razdelitev vlog in SCAMPER omejitev obsega. Referenčni primer v predlogi je ohranjen.

## Natanko dve jedrni funkciji MVP

1. Vnos naročila: HTML obrazec → PHP validacija → INSERT v `narocila`. Ena različica izdelka in količina, e-naslov `dijaki.sers.si`, preverjanje zaloge in transakcijsko zmanjšanje zaloge.
2. Prikaz ponudbe: SELECT iz `izdelki` → kartice Pico.css s fotografijo, opisom, velikostjo, ceno in zalogo. Po oddaji se prikažeta številka naročila in povzetek. Osebni podatki niso javno izpisani.

Izven obsega so kartična plačila in dostava, samostojna mobilna aplikacija/SMS/push ter košarica, uporabniški računi in administrativni portal. Nadomestijo jih prevzem v šoli, odzivna spletna stran in eno naročilo za eno različico izdelka.

## Orodja in potek dela

github.dev, Git/GitHub, PHP 8.x, MariaDB na šolskem cPanelu, Pico.css prek CDN in GitHub Projects. Dodatni stroški licenc so 0 € ob uporabi šolske infrastrukture.

Kanban: Backlog → Ready → In progress → In review → Done. Kartico prestavimo v Done po pregledu drugega člana in preverjenih merilih. Imeni v naslovih kartic določata odgovorno osebo.

Merila za prihodnji MVP: veljavno naročilo se shrani enkrat; napačen e-naslov, neveljavna količina in presežena zaloga se zavrnejo; katalog prikaže podatke iz baze; prikaz deluje na telefonu in tipkovnici; SQL uporablja pripravljene stavke in izpis je zaščiten pred XSS.

Ta repozitorij trenutno vsebuje predstavitev DN1 in projektno dokumentacijo. Razvoj PHP/MariaDB aplikacije in namestitev na cPanel sta prihodnji nalogi MVP. GitHub Pages gosti statično predstavitev in ne izvaja PHP.

## Datoteke in objava

- `index.html` in `dn1.html`: predstavitev projekta na podlagi DN1.
- `projektna-listina.docx`: izpolnjena izvirna učiteljeva predloga.
- `projektna-listina.pdf`: predogled istega delovnega lista.
- `projektna-listina.html`: spletni dostop do listine.

GitHub Pages se objavlja iz veje `main`, mape `/ (root)`. Dokumenta v Classroomu vsak član priloži sam; gumb Oddaj potrdi šele po lastnem pregledu.
