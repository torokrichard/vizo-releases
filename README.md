# Vizo: versiuni pentru Windows

Vizo adună anunțurile de apartamente de vânzare din Brașov (Storia, OLX, Publi24 și altele), le pune pe un singur rând chiar dacă apar pe mai multe site-uri și arată pentru fiecare prețul corect, semnele de negociere, costul real după renovare și naveta.

Aici sunt **doar versiunile gata de instalat**. Codul nu e public.

## Instalare

1. Descarcă `Vizo-<versiune>.zip` din dosarul celei mai noi versiuni din `releases/` (sau folosește linkul direct primit). Dacă o versiune e mai mare de 45 MB, vine în bucăți `.zip.000`, `.001`… care se lipesc într-un singur zip.
2. Dezarhivează și pornește `Vizo\Vizo.exe`. Windows poate arăta „Windows a protejat PC-ul”, pentru că aplicația nu e semnată de un editor cunoscut: alege **Mai multe informații → Rulează oricum**.
3. Prima dată baza e goală: apasă **Actualizează** și Vizo adună anunțurile. Durează câteva minute.

## Ce face și ce nu face

- Rulează **doar pe calculatorul tău**. Serverul ei local răspunde numai la calculatorul tău, nu la alte site-uri.
- Datele tale (anunțuri, notițe, statusuri, setări) stau în `%LOCALAPPDATA%\Vizo\date` și nu pleacă nicăieri.
- **Nu pornește singură** odată cu Windows, decât dacă ceri asta.
- **Actualizări automate și sigure:** la pornire și apoi o dată la 30 de minute, Vizo verifică `manifest.json` din acest repo. O versiune nouă se instalează doar dacă e **semnată** cu cheia autorului (Ed25519), dacă fiecare bucată are exact amprenta (sha256) din manifest și dacă e mai nouă decât cea instalată. Se aplică la următoarea pornire, iar versiunea veche rămâne pentru întoarcere.
- Prețurile sunt **cerute** în anunțuri, nu prețuri de vânzare la notar. „Prețul corect” e o estimare față de anunțuri asemănătoare și are eroarea afișată în aplicație.
- Folosește site-urile de anunțuri ca un vizitator obișnuit, pentru căutarea ta personală. Respectă termenii lor.

## Verificare manuală (opțional)

`manifest.json` conține `version`, amprentele sha256 ale fiecărei bucăți și ale zip-ului întreg și o semnătură Ed25519. Cheia publică e:

```
mtiRBPdA3e8qOOjf8I7fnp///JYpSbA0AZitTPgzmVA=
```
