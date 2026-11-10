# zadatci_app

## Osnovni podaci
- **Ime i prezime:** Petar Vladić
- **Kolegij:** Napredni razvoj aplikacija za mobilne uređaje
- **Vježba:** Vježba 4 MVVM i ChangeNotifier Refaktoriranje aplikacije Zadatci
- **Operacijski sustav:** Windows 
- **Flutter verzija:** Flutter 3.47.7 
- **Dart verzija:** Dart SDK version: 3.13.5
- **Korišteni uređaj:** Android emulator 

## Odgovori na pitanja za provjeru razumijevanja

1. U README navedite tri stvari koje u vježbi 3 rade ekranu ne pripadaju
(po obrascu MVVM) i u koji bi sloj ih premjestili.

Generiranje ID i upravljanje podatcima se odvija preko _spremi i widget.postojeci. Premjestiti u ViewModel, a ekranu omogućiti samo pozivanje metode.
Upravljanje stanjem unosa i konrolerima sve treba prmjetit i VIewModel.
Logia provjere se također treba smjesitit u ViewModel. Provejra veličine unosa ili praznog unosa.

2. Što bi se dogodilo kad bi StatistikaEkran u svom initState stvorio novi ZadatciViewModel(ZadatakRepozitorij())

Nastao bi novi, odvojeni ViewModel koji ne bi dijelio stanje s ekranom popisa. Zbog toga bi ekran statistike imao vlastiti popis zadataka, koji bi mogao biti prazan ili sadržavati početne podatke. Promjene napravljene na ekranu popisa ne bi bile vidljive u statistici. Zato oba ekrana moraju koristiti isti ViewModel.

3. Zašto ViewModel izlaže UnmodifiableListView, a ne običnu listu i što bi moglo poći po zlu?

Izlaže se kao UnmodifiableListView kako bi se zaštitili podatci i spriječilo da vanjski slojevi (ekrani i widgeti) izravno mijenjaju listu zadataka.
UI bi mogao neovlašteno mijenjati podatke mimo poslovnih pravila, ne bi se pozivao notifyListeners, a sučelje i stanje bi postali nekonzistentni i izgubili reaktivnost.

4. Što se dogodi s osvježavanjem ekrana ako u metodi promijeniZavrsen izostavite notifyListeners()?

Sučelje se neće osvježiti. Podata će se u pozadini promijeniti, ali korisnik neće vidjeti promejne.







