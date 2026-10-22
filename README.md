# zadatci_app

## Osnovni podaci
- **Ime i prezime:** Petar Vladić
- **Kolegij:** Napredni razvoj aplikacija za mobilne uređaje
- **Vježba:** Vježba 2 Asinkroni dohvat podataka Model, stanja učitavanja i prvi popis 
- **Operacijski sustav:** Windows 
- **Flutter verzija:** Flutter 3.47.7 
- **Dart verzija:** Dart SDK version: 3.13.5
- **Korišteni uređaj:** Android emulator 

## Odgovori na pitanja za provjeru razumijevanja

1. Objasnite zašto polja modela nisu promjenjiva i što bi se dogodilo da u JSON-u polje naslov nedostaje (as String na vrijednosti null).
Ako naslov bude nedostajao on će biti null,a to će uzrokvati pogrešku kod pretvaranja u String.
2. ojasnite što se događa kad iznimku iz Futurea ne uhvatimo ni na jednom mjestu.
Ako ne uhvatimo izniku sa try catchom onda će ona nastavi dalje obrađivati i može uzrokovati neobrađenu pogrešku, te prekinuti rad programa.
3. Objasnite zašto se Future stvara u polju, a ne u metodi build, i navedite tri stanja koja svaki zaslon s podacima mora prikazati.
Stvara se u polju kako se ne bi pokretao svaki put kad napravimo neki novi build. Tri osnovna stanje su: učitavanje podataka, prikaz dohvaćenih podatak, javljanje pogreške ako se podaci ne mogu dohvatiti.

## Samostalne izmjene
Tijekom vježbe provedene su sljedeće izmjene:
1. dodan opis tipa String? i prilagođene sve metode i konstruktor
2. u model_provjera dodan opis za samo jedan zadtak i ispsi za test
3. repozitorij filea dodan dhovat Future.wait dvaput istovremeno i izmjerno trajanj preko Stopwatch
4. dohvatu omotan s .timeout
5. u main.dart dodan normaln ispis kod pogreške
6. dodan ispis odrađenih zadataka
7. dodan refresh indicator




