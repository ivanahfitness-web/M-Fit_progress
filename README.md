# M-progress Borovje – web-stranica

Statična web-stranica osobnog trenera Mateja Hercega (Borovje, Zagreb). HTML, CSS i malo JavaScripta, bez ikakvih dodataka i bez izrade (build) koraka. Spremna je za **GitHub Pages**.

## Sadržaj

| Datoteka / mapa | Što je |
|---|---|
| `index.html` | Stranica na hrvatskom (BMI kalkulator, WhatsApp gumbi, česta pitanja) |
| `en/index.html` | Ista stranica na engleskom (gumb HR \| EN u zaglavlju prebacuje između njih) |
| `slike/` | Fotografije (WebP) i slika za dijeljenje poveznice (`dijeljenje.jpg`) |
| `cjenik/` | Strojno čitljiv cjenik usluga (CSV), povezan u podnožju |
| `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | Ikonice |
| `robots.txt`, `sitemap.xml` | Za tražilice |
| `.nojekyll` | Govori GitHub Pagesu da datoteke objavi točno kakve jesu |

Sve poveznice su relativne, pa stranica radi i na `https://KORISNIK.github.io/REPOZITORIJ/` i na vlastitoj domeni.

## Objava na GitHub Pages

1. Na github.com: **New repository** → naziv npr. `m-progress-borovje` → **Public** → *Create repository*.
2. **Add file → Upload files** → povuci **sav sadržaj ove mape** (ne samu mapu) → *Commit changes*.
   Skrivena datoteka `.nojekyll` se možda neće vidjeti pri povlačenju – nije obavezna, stranica radi i bez nje.
3. **Settings → Pages** → *Source: Deploy from a branch* → *Branch: `main`*, mapa `/ (root)` → *Save*.
4. Za 1–2 minute stranica je na `https://KORISNIK.github.io/m-progress-borovje/`.

### Vlastita domena (npr. www.mprogress.hr)

1. **Settings → Pages → Custom domain** → upiši `www.mprogress.hr` → *Save* (GitHub sam doda datoteku `CNAME`).
2. Kod registrara domene dodaj DNS zapis: `CNAME`, naziv `www`, vrijednost `KORISNIK.github.io`.
3. Kad se domena poveže, uključi **Enforce HTTPS**.

## Obavezno: zamijeni adresu stranice

U četiri datoteke – `index.html`, `en/index.html`, `robots.txt`, `sitemap.xml` – zamijeni svaki
`https://www.DOMENA.hr` pravom adresom, **bez kose crte na kraju**, npr.:

- `https://www.mprogress.hr` (vlastita domena), ili
- `https://KORISNIK.github.io/m-progress-borovje` (GitHub adresa)

Na GitHubu: otvori datoteku → ikonica olovke → `Ctrl+F` … ili lokalno u Notepadu: *Uredi → Zamijeni → Zamijeni sve*.
Adresa se koristi u oznakama za Google, za dijeljenje na WhatsAppu/Facebooku te u `robots.txt` i `sitemap.xml`. Stranica i bez toga radi, ali tražilice i pregledi poveznica trebaju pravu adresu.

## Provjera nakon objave (na mobitelu)

- [ ] Zelena traka „Rezerviraj termin – WhatsApp” na dnu ekrana otvara WhatsApp
- [ ] „Ovo želim →” na kartici cilja otvara WhatsApp s porukom
- [ ] BMI: upiši 78,5 i 180 → *Izračunaj* → gumb „Pošalji rezultat Mateju”
- [ ] HR | EN prebacuje jezik i vraća natrag
- [ ] Telefon, e-mail, Instagram i Google karta otvaraju se ispravno
- [ ] Poveznica „Cjenik usluga (CSV)” u podnožju preuzima datoteku
- [ ] Česta pitanja se otvaraju i zatvaraju
- [ ] Brzina: https://pagespeed.web.dev/
- [ ] Podaci za Google: https://search.google.com/test/rich-results („Lokalna tvrtka” i „Česta pitanja” bez grešaka)
- [ ] Prijavi stranicu u Google Search Console i predaj `sitemap.xml`
- [ ] Naziv, adresa i telefon u Google profilu tvrtke isti kao na stranici: M-progress Borovje, Letovanićka ulica 25, 10000 Zagreb, +385 91 3003 004
- [ ] Poveznica na stranicu u Instagram bio i u Google profil tvrtke

## Fontovi

Anton i Barlow učitavaju se s Google Fonts, pa se pri otvaranju stranice Googleu šalje IP adresa posjetitelja. Tko to želi izbjeći, može fontove preuzeti i staviti u repozitorij.

## Održavanje

- **1. 1. 2027.** – akcija „50% na prva dva treninga” završava: maknuti zelenu traku na vrhu (HR i EN), promijeniti opis za Google (`meta description` i `og:description`) i do 8:00 objaviti novi CSV cjenik (novi datum u nazivu). Stari cjenik ostaviti još 30 dana.
- **Promjena cijene** – na obje stranice (HR i EN) + novi CSV cjenik do 8:00 tog dana.
- Kad stigne treća izjava klijenta, dodati je u sekciju „Iskustva klijenata”.
- Prije objave: pisani pristanak klijenata za izjave i za fotografiju s TRX trakama.

Svaka izmjena: uredi datoteku na GitHubu → *Commit changes* → stranica se osvježi za minutu-dvije.
