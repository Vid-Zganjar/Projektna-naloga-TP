# Domači NAS na platformi Amahi

![Amahi Logo]([https://www.amahi.org/sites/all/themes/amahi/logo.png](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.amahi.org%2Fpress-kit&psig=AOvVaw18jC_q_GD4ifSffd3EzbK-&ust=1704354010845000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCPiv4M3bwIMDFQAAAAAdAAAAABAD))

## Opis projekta

Domači NAS (Network Attached Storage) omogoča centralizirano shranjevanje in upravljanje podatkov v domačem omrežju. Ta projekt uporablja programsko opremo Amahi za enostavno vzpostavitev in upravljanje domačega strežnika za shranjevanje podatkov.

## Specifikacije strojne opreme

- **Model računalnika:** Dell Inc. OptiPlex 755
- **RAM:** 4GB DDR2
- **Procesor:** Intel Core 2 Duo 2.53GHz
- **Pomnilnik:** 2x 250GB Samsung (za shranjevanje) + 500GB Samsung (za zagon sistema)
- **Operacijski sistem:** Fedora 27

## Namestitev

1. Sestavite računalnik z navedeno strojno opremo.
2. Z uporabo orodja Rufus naložite operacijski sistem Fedora 27 na ustrezni disk.
3. Po namestitvi operacijskega sistema naložite Amahi iz uradne spletne strani [Amahi](https://www.amahi.org/).
4. Generirajte ključ za namestitev Amahi preko spletne strani Amahi.
5. Na sistem Linux naložite Amahi in aktivirajte NAS z generiranim ključem.
6. Izključite DHCP strežnik na vašem usmerjevalniku, saj NAS deluje kot DHCP strežnik.
7. Dostopajte do NAS-a preko različnih možnosti, kot so spletna stran, raziskovalec datotek ali terminal.

## Možnosti dostopa

1. **Spletna stran:**
   - Obiščite spletno stran Amahi, kjer se vpišete in upravljate konfiguracije NAS-a.

2. **Raziskovalec datotek:**
   - Dostopajte do NAS-a preko raziskovalca datotek, kjer lahko pregledujete in nalagate vsebine.

3. **Terminal (Putty):**
   - Uporabite terminal, kot je Putty, za spreminjanje konfiguracij, kot so IP naslovi.

## Opombe

- Za podrobnejša navodila in informacije obiščite [Amahi Wiki](https://wiki.amahi.org/).

**Opozorilo:** Pred spreminjanjem konfiguracij se prepričajte, da imate ustrezno znanje in razumevanje, da preprečite morebitno izgubo podatkov ali težave z delovanjem sistema.
