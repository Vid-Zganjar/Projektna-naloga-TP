# Domači NAS z Amahi 11

## Opis projekta

Projekt omogoča vzpostavitev domačega strežnika za shranjevanje podatkov (NAS) s pomočjo programske opreme Amahi 11. S tem postopkom lahko preprosto izkoristite starejši računalnik, kot je Dell Inc. OptiPlex 755, za ustvarjanje učinkovitega domačega NAS-a.

## Specifikacije moje strojne opreme

- **Model računalnika:** Dell Inc. OptiPlex 755
- **RAM:** 4GB DDR2
- **Procesor:** Intel Core 2 Duo 2.53GHz
- **Pomnilnik:** 2x 250GB Samsung (za shranjevanje) + 500GB Samsung (za zagon sistema)
- **Operacijski sistem:** Fedora 27

## Zahteve za namestitev Amahi 11

1. **Strojna oprema:**
   - Računalnik z najmanjšimi zahtevanimi specifikacijami:
     - 1+ GHz CPU, samo 64-bit (brez podpore za 32-bitne sisteme)
     - 10GB diskovnega prostora
     - 1+ GB RAM
     - Vsak dodaten CPU/Memorija/Disk pripomore k boljšemu delovanju
     - Ena žična mrežna vmesna povezava. Brezžične povezave niso podprte v samem strežniku. Brezžična omrežja na odjemalcih so popolnoma podprta.
     - **Opomba o omrežju:** Onemogočite vse, razen enega vmesnika, ki ga boste uporabljali. Podprta je le prva Ethernet naprava. Amahi zahteva, da fizično odstranite ali onemogočite (običajno v BIOS-u) vse dodatne omrežne vmesnike, razen tistega, ki ga nameravate trajno uporabljati.

2. **Programska oprema:**
   - CD/DVD s programsko opremo Amahi.
   
3. **Amahi namestitvena koda:**
   - Ustvarite račun na Amahi, kliknite "Začni graditi nov HDA" in sledite navodilom. Kodo najdete v nadzorni plošči Amahi.

4. **Internetna povezava med namestitvijo:**
   - Kritične posodobitve in konfiguracije se izvajajo med namestitvijo preko omrežja.

## Namestitev

1. Sestavite računalnik z navedeno strojno opremo.
2. Z uporabo orodja Rufus naložite operacijski sistem Fedora 27 na ustrezni disk.
3. Po namestitvi operacijskega sistema sledite korakom na [Amahi Wiki](https://wiki.amahi.org/index.php/Main_Page). V pomoč Vam je lahko tudi ta [video](https://www.addictivetips.com/ubuntu-linux-tips/create-a-linux-nas-with-amahi/).
4. Generirajte ključ za namestitev Amahi preko spletne strani Amahi.
5. Na sistem Linux naložite Amahi in aktivirajte NAS s generiranim ključem.
6. Izključite DHCP strežnik na vašem usmerjevalniku, saj NAS deluje kot DHCP strežnik.
7. Dostopajte do NAS-a preko različnih možnosti, kot so spletna stran, raziskovalec datotek ali terminal.

## Možnosti dostopa

1. **Spletna stran:**
   - Obiščite spletno stran Amahi, kjer se vpišete in upravljate konfiguracije NAS-a.

2. **Raziskovalec datotek:**
   - Dostopajte do NAS-a preko raziskovalca datotek, kjer lahko pregledujete in nalagate vsebine.

3. **Terminal (Putty):**
   - Uporabite terminal, kot je Putty, za spreminjanje konfiguracij, kot so IP naslov NAS strežnika.

## Opombe

- Za podrobnejša navodila in informacije obiščite [Amahi Wiki](https://wiki.amahi.org/).
- Pred spreminjanjem konfiguracij se prepričajte, da imate ustrezno znanje in razumevanje, da preprečite morebitno izgubo podatkov ali težave z delovanjem sistema.
Certainly! Here's the translated version in Slovenian:

---
Certainly! Here's the translation in Slovenian:

---

### 1. Moja namestitev NAS strežnika

- Prenesite [Fedora 27 Server ISO](https://archives.fedoraproject.org/pub/archive/fedora/linux/releases/27/Server/x86_64/iso/Fedora-Server-netinst-x86_64-27-1.6.iso):

- Uporabite rufus, da ISO-datoteko naložite na USB ključ velikosti vsaj 1 GB.

### 2. Ustvarjanje Amahi Računa

- Med namestitvijo Fedore ustvarite nov račun [Amahi](https://www.amahi.org/).
- Shrani generirano namestitveno kodo in informacije o omrežju.

### 3. Razdelitev

- Ročno nastavite particije, da se izognete težavam z LVM postavitvijo.
- Nastavite particijo za koren (mount točka `/`) in po želji tudi particijo za izmenjavo (SWAP).

*Uporabniki UEFI:* Če uporabljate UEFI, ustvarite particijo Fat32 (512 MB) za `/boot/efi` in preostanek namenite SWAP.

### 4. Začetek Namestitve

- Izberite "Minimalna Namestitev" pod "Izbira Programske Opreme".
- Začnite postopek namestitve s klikom na "Začni Namestitev".

### 5. Namestitev Amahi

- Po namestitvi Fedore zagotovite povezljivost z omrežjem s:

  ```
  ping google.com -c3
  ```

- Prenesite in namestite Amahi RPM:

  ```
  sudo -s
  rpm -Uvh https://f25.amahi.org/noarch/hda-release-10.0.0-1.noarch.rpm
  ```

- Namestite orodja Amahi, zamenjajte "VAŠA NAMESTITVENA KODA" z generirano kodo:

  ```
  dnf -y install hda-ctl
  hda-install VAŠA-NAMESTITVENA-KODA
  ```

### 6. Uporaba Amahi

- Dostopajte do spletnega vmesnika svojega Amahi strežnika preko:

  ```
  https://server-lokalni-ip-naslov
  ```

- Če niste prepričani o IP naslovu strežnika, uporabite:

  ```
  ip addr show
  ```

- Prilagodite svoj strežnik preko spletnega vmesnika in raziščite dodatne aplikacije v trgovini Amahi.

---

Prilagodite oblikovanje ali dodajte dodatne podrobnosti, če je potrebno, za vaš GitHub README.
