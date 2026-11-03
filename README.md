# zadatci_app

## Osnovni podaci
- **Ime i prezime:** Petar Vladić
- **Kolegij:** Napredni razvoj aplikacija za mobilne uređaje
- **Vježba:** Vježba 3 Forma, validacija i navigacija
- **Operacijski sustav:** Windows 
- **Flutter verzija:** Flutter 3.47.7 
- **Dart verzija:** Dart SDK version: 3.13.5
- **Korišteni uređaj:** Android emulator 

## Odgovori na pitanja za provjeru razumijevanja

1. Zašto je bolje zadati boju u temi nego na svakom widgetu?
Zato što kada definiramo u temi odmah postavljamo to boju za sve ostale widgete.
2. Objasnite što radi validate() i zašto validator vraća null za ispravan
uno
Validate provjera ispravnost polja u formi. U naše slučaju je to je li polje prazno ili ima manje od 3 znaka. 
kada validator vraca null to znači da nije otkrio niti jednu pogrešku
3. Objasnite zašto se nakon await Navigator.push provjerava
mounted..
sprjecava rušenje aplikacije i provjera je li widget akitvan prije nego li mijenjamo njegov sadržaj. 

## Izmjena iz M1
1. Dodano ograničenje naslovana 40 znakova
2. Dodan zahjtev da naslov počinje velikim slovom
3. Spiječen unos naslova koji već postoji





