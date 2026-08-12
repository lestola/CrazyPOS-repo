# CrazyPOS (UniCenta oPOS) – Pakettivarasto & Asennusohje

Tämä repositorio toimii julkisena pakettivarastona ja jakelukanavana mukautetulle **CrazyPOS** (UniCenta oPOS) -kassajärjestelmälle. 

Asennuspakettien kääntäminen ja julkaisu tapahtuvat automaattisesti jokaisen koodipäivityksen yhteydessä.

---

## 🐧 Linux (AlmaLinux, Fedora, RHEL, Rocky Linux)

Linux-asennus käyttää virallista RPM-pakettivarastoa. Pakettien hallinta ja päivitykset hoituvat suoraan järjestelmän omalla `dnf`- tai `yum`-työkalulla.

### 1. Lisää pakettivarasto järjestelmään

Aja seuraava komento päätetylassa (terminal) pääkäyttäjänä (`sudo`):

```bash
sudo cat <<EOF ## ### (Windows (`.exe`), (dnf-automatic) **[Releases --- --now -asennustiedosto. -sivulle. -y / /etc/yum.repos.d/crazypos.repo 1. 10 11) 2. 3. 4. Asenna Asennus Asennusohje: Automaattiset CrazyPOS EOF Jos Julkaisut](https://github.com/lestola/CrazyPOS-repo/releases)** Käynnistä Käynnistä-valikkoon. Lataa Muokkaa Päivitä Repository Siirry Windows Windows-ympäristöön [commands] [crazypos] `/etc/dnf/automatic.conf` `CrazyPOS-UniCenta-vX.X-windows-installer.exe` ```

 ```bash ```ini `dnf-automatic`: aina apply_updates="yes" asenna asennus asennusohjelma asennusohjelmana aseta automaattisesti baseurl="https://lestola.github.io/CrazyPOS-repo/x86_64/" dnf dnf-automatic dnf-automatic.timer enable enabled="1" gpgcheck="1" gpgkey="https://lestola.github.io/CrazyPOS-repo/RPM-GPG-KEY-unicenta" haluat install ja jaellaan joka julkaistaan: kassapäätteen kun käynnistysskriptit luo makecache name="CrazyPOS" ohjeita. pakettivaraston pikakuvakkeen päivittyvän päälle: riippuvuudet. ruudulle seuraa sisältää sovellus sovellus: sudo systemctl tarvittavat taustapalvelu: taustapäivitykset tee tiedostoa tulevia työpöydälle unicenta uusi uusin valmiina versio välimuisti | 🪟> **Huomio:** Varmista, että koneelle on asennettu Java Runtime Environment (JRE 11 tai uudempi) sovelluksen suorittamista varten.

---

## 🔄 Julkaisuprosessi (CI/CD)

Kaikki pakettiversiot käännetään automaattisesti GitHub Actions -ympäristössä:
* **RPM-paketti:** Käännetään Mavenilla, allekirjoitetaan GPG-avaimella ja indeksoidaan tälle Pages-sivustolle.
* **EXE-asennusohjelma:** Käännetään Mavenilla ja pakataan Inno Setup -työkalulla suoraan GitHub Releases -osioon.
