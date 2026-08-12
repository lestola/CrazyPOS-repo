### 1. Lisää pakettivarasto järjestelmään

Aja seuraava komento päätetylassa (terminal) pääkäyttäjänä (`sudo`):

```bash
sudo cat <<EOF ## ### (Releases)]([https://github.com/lestola/CrazyPOS-repo/releases](https://github.com/lestola/CrazyPOS-repo/releases))** (`.exe`) **[Julkaisut --- -asennustiedosto. -sivulle. /etc/yum.repos.d/crazypos.repo 1. 2. 3. Asennus Asennusohje EOF Käynnistä-valikkoon. Lataa Päivitä Repository Siirry Suorita Windows Windows-ympäristöön [crazypos] `CrazyPOS-UniCenta-vX.X-windows-installer.exe` ``` ```bash asenna asennusohjelma asennusohjelmana, baseurl="[https://lestola.github.io/CrazyPOS-repo/x86_64/](https://lestola.github.io/CrazyPOS-repo/x86_64/)" dnf enabled="1" gpgcheck="1" gpgkey="[https://lestola.github.io/CrazyPOS-repo/RPM-GPG-KEY-unicenta](https://lestola.github.io/CrazyPOS-repo/RPM-GPG-KEY-unicenta)" install ja jaellaan joka käynnistysskriptit luo makecache name="CrazyPOS" ohjeita. pikakuvakkeen riippuvuudet. ruudulle seuraa sisältää sovellus sudo tarvittavat tee tulevia työpöydälle unicenta uusin valmiina välimuisti | 🪟> **Huomio:** Varmista, että koneelle on asennettu Java Runtime Environment (JRE 11 tai uudempi) sovelluksen suorittamista varten.

---

## 🔄 Automaattiset taustapäivitykset (Linux / `dnf-automatic`)

Jos haluat kassapäätteen päivittyvän aina automaattisesti, kun uusi versio julkaistaan:

1. Asenna `dnf-automatic`:
   ```bash
   sudo dnf install -y dnf-automatic
