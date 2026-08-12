# CrazyPOS (UniCenta oPOS) – Pakettivarasto & Asennusohje

Tämä repositorio toimii julkisena pakettivarastona ja jakelukanavana mukautetulle **CrazyPOS** (UniCenta oPOS) -kassajärjestelmälle. 

Asennuspakettien kääntäminen ja julkaisu tapahtuvat automaattisesti jokaisen koodipäivityksen yhteydessä.

---

## 🐧 Linux (AlmaLinux, Fedora, RHEL, Rocky Linux)

Linux-asennus käyttää virallista RPM-pakettivarastoa. Pakettien hallinta ja päivitykset hoituvat suoraan järjestelmän omalla `dnf`- tai `yum`-työkalulla.

### 1. Lisää pakettivarasto järjestelmään

Aja seuraava komento päätetylassa (terminal) pääkäyttäjänä (`sudo`):

```bash
sudo cat <<EOF | sudo tee /etc/yum.repos.d/crazypos.repo
[crazypos]
name=CrazyPOS Repository
baseurl=https://lestola.github.io/CrazyPOS-repo/x86_64/
enabled=1
gpgcheck=1
gpgkey=https://lestola.github.io/CrazyPOS-repo/RPM-GPG-KEY-unicenta
EOF
