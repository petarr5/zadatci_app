# zadatci_app

## Osnovni podaci
- **Ime i prezime:** Petar Vladić
- **Kolegij:** Napredni razvoj aplikacija za mobilne uređaje
- **Vježba:** Vježba 5 Docker i Supabase na Oracle Cloudu
- **Operacijski sustav:** Windows 
- **Flutter verzija:** Flutter 3.47.7 
- **Dart verzija:** Dart SDK version: 3.13.5
- **Korišteni uređaj:** Android emulator 
- **Oracle Linux image:** Oracle Linux 9 (aarch64)
- **Oracle Linux shape:** VM.Standard.A1.Flex (Ampere, Arm — 2 OCPU, 12 GB RAM, 200 GB Boot Volume)
- **Supbase:** self-hosted/v0.8.4   

## Odgovori na pitanja za provjeru razumijevanja

1. Provjera razumijevanja 1: u README objasnite što je Always Free instanca i zašto za Supabase
ne smijete odabrati Micro shape.
    
    Always Free instca je besplatna usluga koji nam Orcacle nudi. Kao što je prsitup serverim, bazi podataka, virtualnim mašinama.
    Micor shape nećemo odabrati jer nema dovoljno jezgri i RAM memorije za našu Supabase uslugu.

2. Provjera razumijevanja 2: u README objasnite razliku između Docker slike (image) i kontejnera
te zašto se podaci baze moraju držati u volumenu.

Docker slika jeste osnovna baza koja sadrži kod i sve ostale podtrebne datoteke kako bi mogli pokrenuti aplikaciju.
Docker konejner dobivamo kada pokrenemo sliku, odnosno to je aktivna instca slike.
Podatke spremamo u volumen kako da ih trajno sačuvamo. Budući da kontejner sve podatke čuva privermeno dok ne bude izbirasn ili ažuriran.

3. Provjera razumijevanja 3: u README navedite što rade servisi Postgres, REST (PostgREST), Auth,
Storage i Studio te što je gateway na portu 8000.

Postgres je relacijska baza podataka u koju spremamo naše podatke trajno.
REST omogućuje čitanje, pisanje, izmjenu ili brisanje podatka u bazi
Auth upravalja registracijom, prijavom korisnika, te također upravlja JWT tokenom
Storage služi za pohranu i preuzimanje datoteka
Studio web sučelje koje nam služi za upravljanje bazom podataka, tablicama, SQL upitima i drugim postavkama projketa.
Gateway na port 8000 jedinstven točka preko koja prima sve vanjeske zahjteve, provejrava upite i dalje ih prosljeđuje odgovarajućem unutarnjem servisu.

4.  Provjera razumijevanja 4: što bi aplikacija prikazala da u skripti nema politike "anon cita", i zašto
nema poruke o pogrešci?

Aplikacija bi prikazala prazan popis podataka. razlog tomu je što je uključen RLS, a ne postoji poltika koja dopušta čitanje što znači da u bazi nema niti jedne tablice kojoj korisnik ima pravo pristupa.

5. Provjera razumijevanja 5: zašto ViewModel mijenja lokalni popis tek nakon što izvor uspije, a ne
prije? Što bi korisnik vidio da je obrnuto, a veza padne?

Time se osigurava da su uvijek pravi i ispravni podaci prikazani koji se podudaraju s onima u bazi podataka. U suprotnom korisnik bi vidio da je usješno obavio promjenu nad podacima iako je stanje u bazi isto, te bi pri ponovnom učitavanju stranice opet vidio stare podatke.

6. Provjera razumijevanja 6: zašto se u aplikaciju stavlja publishable, a ne secret ključ, i što bi se
dogodilo kad bi secret ključ završio u repozitoriju?

Koristi se javni ključ kako bi se poštovale ovlasti koje su korisnicma dane, ako bi u kojem sčlučaju to bio secret ključ korisnik bi imao mogućnosti da radi što hoće s podacima u bazi.








