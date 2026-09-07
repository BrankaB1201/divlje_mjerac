# Divlje — teren

Dvije stranice. **`prijava.html`** je radna prijava otpada; **`index.html`** je
mjerač točnosti kojim se provjerava ono na čemu prijava stoji.

## Prijava

    https://raw.githack.com/BrankaB1201/divlje_mjerac/main/prijava.html

Slikaj otpad — položaj se hvata **u trenutku okidanja**, jer telefon ga u sliku
ne upisuje. Ako točka nije na pravom mjestu, dodirni satelitsku snimku gdje
otpad stvarno leži; bilježi se i koliko si je pomaknula. Odaberi vrstu i
količinu, dopiši opis.

Prijava se **prvo sprema na telefon** pa tek onda šalje kroz izbornik
dijeljenja — slika i koordinate odu e-poštom. Bez signala čeka u redu i pošalje
se kad je otvoriš. Ovo je namjerno verzija **bez poslužitelja**: dovoljna da se
prijava napravi i pošalje, a ništa se ne skuplja na tuđem računalu.

Uz svaku prijavu ide i to koliko je očitanje bilo staro i je li točka ucrtana
rukom — jer bez toga koordinata izgleda pouzdanije nego što jest.

# Mjerač točnosti

Jedna stranica koja mjeri koliko GNSS na mobitelu stvarno promašuje na
zadanom mjestu. Nije dio aplikacije — mjerni je alat.

    https://raw.githack.com/BrankaB1201/divlje_mjerac/main/index.html

Stani na mjesto, pritisni **Pokreni mjerenje** i pusti minutu-dvije, bez
hodanja. Stranica onda pokazuje:

- **prijavljenu točnost** — ono što telefon tvrdi, u metrima;
- **krug pogreške u mjerilu**, s mjernom crtom, i preko njega **svako pojedino
  očitanje** ucrtano u odnosu na prosjek — tako se vidi slaže li se tvrdnja s
  onim što se stvarno događa;
- **stvarno rasipanje** — najveću udaljenost pojedinog očitanja od prosjeka,
  dok stojiš na mjestu. Jedini broj koji telefon ne procjenjuje;
- **vrijeme do prvog položaja** i do pragova od 20 i 10 m — mjeri hladni start,
  pa se isplati probati jednom s podacima i jednom u zrakoplovnom načinu;
- **kompas**, da se vidi koliko smjer pleše prije nego se na njega osloni
  procjena „vidim ga s ceste, cca 40 m".

Sve ostaje u kartici preglednika. Ništa se nikamo ne šalje i ništa se ne sprema.

Mora se otvoriti kao samostalna stranica preko HTTPS-a. U okviru unutar tuđe
stranice preglednik geolokaciju odbija bez pitanja, pa `raw.githack.com` link
gore radi, a ugrađena inačica ne bi.

Pripada projektu **Divlje** — karta divljih odlagališta u Šibensko-kninskoj
županiji. Zašto je točnost uopće pitanje piše u `design/geo/lokacija.md` tog
projekta.
