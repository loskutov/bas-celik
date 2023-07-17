# Baš Čelik

**Baš Čelik** je čitač elektronskih ličnih karata. Program je osmišljen kao zamena za zvaničnu aplikaciju *Čelik*. Nažalost, zvanična aplikacija može se pokrenuti samo na Windows operativnom sistemu, dok BašČelik funkcioniše na tri operativna sistema (Windows/Linux/OSX).

![Interfejs](assets/ui.png)

Aplikacija bi trebalo da podržava očitavanje svih ličnih karata, ali za sada nije testirana na starim (izdate pre avgusta 2014. godine), kao ni na najnovijim (izdate nakon februara 2023. godine). Unapred sam zahvalan za bilo kakvu povratnu informaciju.

## Upotreba

Povežite čitač za računar i pokrenite aplikaciju. Ubacite ličnu kartu u čitač. Aplikacija će pročitati informacije sa lične karte i prikazati ih kroz interfejs. Tada možete sačuvati PDF pritiskom na donje desno dugme.

Kreirani PDF dokument izgleda maksimalno približno dokumentu koji se dobija sa zvaničnom Čelik aplikacijom.

Ako u bilo kom trenutku dođe do greške, informacija o grešci će se ispisati u donjem levom uglu.

## Pokretanje na Linuksu

Aplikacija zahteva instalirane `ccid` i `opensc`/`pcscd` pakete. Nakon instalacije ovih paketa, neophodno je i pokrenuti `pcscd` servis:

```
sudo systemctl start pcscd
sudo systemctl enable pcscd
```

## Preuzimanje 

Izvršne datoteke poslednje verzije programa možete preuzeti sa [Releases](https://github.com/ubavic/bas-celik/releases)  stranice.

## Kompilacija

Potrebno je posedovati samo `go` kompajler. Nakon preuzimanja repozitorijuma, dovoljno je pokrenuti

```
go build main.go
```

### Kroskompilacija

Uz pomoć [fyne-cross](https://github.com/fyne-io/fyne-cross) programa moguće je na jednom operativnom sistemu iskompajlirati program za sva tri operativna sistema. Ovaj program zahteva Docker na vašem operativnom sistemu.

## Planirane nadogradnje

 + Očitavanje vozačke dozvole i zdravstvene knjižice
 + Omogućavanje potpisivanja dokumenata sa ključem smeštenim na kartici

## Licenca 

Program i izvorni kôd su objavljeni pod [*MIT* licencom](LICENSE).

Font `free-sans-regular` je objavljen pod [*SIL Open Font* licencom](assets/LICENSE).
