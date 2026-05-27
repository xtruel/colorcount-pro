# ColorCount Pro

**Conta oggetti per colore tramite fotocamera + calcolatrice scientifica integrata.**

Single-file web app (HTML + vanilla JS, zero dipendenze). Funziona offline, su mobile e desktop, in qualsiasi browser moderno. Ideale per magazzino, agricoltura, laboratorio, controllo qualità, didattica.

![ColorCount Pro](preview/cover.png)

## ✨ Features

- 📷 **Conteggio da fotocamera** — accesso diretto alla fotocamera posteriore del telefono
- 🖼️ **Conteggio da immagine** — carica una foto qualsiasi dalla galleria
- 🎨 **8 categorie di colore** — rosso, arancio, giallo, verde, ciano, blu, viola, rosa
- 🔍 **Sensibilità regolabile** — slider per soglia colore, dim. minima oggetto, risoluzione di analisi
- 🧮 **Calcolatrice scientifica completa** — sin/cos/tan/asin/acos/atan, log/ln, √/∛, x², potenze, fattoriale, π, e, Ans, memoria
- 🔗 **Variabili colore nei calcoli** — usa `G`, `R`, `Y`, `O`, `B`, `C`, `P`, `K` direttamente nelle formule (es. `G - Y + B*2`)
- 🌗 **Tema dark moderno** ottimizzato mobile-first
- ⚡ **Zero backend, zero tracking, zero dipendenze CDN** — un singolo file `index.html`
- 🌐 **Offline-ready** — funziona dopo il primo caricamento

## 🚀 Demo live

👉 **https://xtruel.github.io/colorcount-pro/**

## 📦 Installazione

Non serve nessun build step. Basta servire il file `docs/index.html`.

```bash
# qualsiasi web server statico
cd docs
python -m http.server 8000
# oppure
npx serve .
```

### GitHub Pages

Il file `docs/index.html` è già pronto. In **Settings → Pages**:
- Source: **Deploy from a branch**
- Branch: **main** / Folder: **/docs**

### Hosting

Funziona su: Netlify, Vercel, Cloudflare Pages, GitHub Pages, Surge, S3, qualsiasi static host.

> ⚠️ **HTTPS obbligatorio** per l'accesso fotocamera (limitazione del browser, non dell'app). `localhost` funziona anche in HTTP.

## 🧮 Esempi di formule

| Formula                       | Significato                              |
|------------------------------|------------------------------------------|
| `G - Y`                      | Verdi meno gialli                        |
| `R + G + B`                  | Totale rosso + verde + blu               |
| `(G * 100) / (G + R + Y)`    | Percentuale verdi sul totale             |
| `sqrt(G^2 + R^2)`            | Norma euclidea                           |
| `sin(π/4) * G`               | Mix matematico/colore                    |
| `Ans * 2`                    | Raddoppia il risultato precedente        |

## 🎯 Casi d'uso

- Conta pillole / capsule per colore in farmacia
- Conta semi o granaglie in agricoltura
- Conta componenti elettronici (resistenze, LED) per colore
- Conta perline, bottoni, oggetti in vendita all'ingrosso
- Verifica controllo qualità (oggetti conformi vs scarti per colore)
- Didattica matematica (formule applicate a dati reali)

## ⚙️ Personalizzazione

Tutto il codice è in un solo file `docs/index.html`, ~700 righe ben commentate.

- **Aggiungere nuovi colori** → modifica l'array `COLORS` (riga ~270)
- **Cambiare tema** → tutte le variabili colore sono nel `<style>` in testa
- **Cambiare lingua** → sostituisci le stringhe italiane (cerca `lang="it"`)

## 📋 Requisiti tecnici

- Browser moderno (Chrome ≥ 90, Firefox ≥ 88, Safari ≥ 14, Edge ≥ 90)
- HTTPS per la fotocamera (non richiesto per upload immagine)
- Nessun framework, nessun build tool, nessuna libreria esterna

## 📄 Licenza

Vedi [LICENSE.md](LICENSE.md).

- **Regular License** — uso su 1 progetto/dominio personale o di un cliente
- **Extended License** — uso commerciale illimitato, rivendita inclusa

## 🛠️ Roadmap / idee per estensione

- [ ] Esportazione CSV/Excel dei conteggi
- [ ] Calibrazione colore personalizzata (color picker)
- [ ] Conteggio multiplo (somma più scatti in batch)
- [ ] Storico sessioni con localStorage
- [ ] PWA installabile con manifest + service worker

## 👤 Autore

Made with ❤️ — per supporto o personalizzazioni, contatta tramite il marketplace dove hai acquistato lo script.

---

**ColorCount Pro v1.0** — Single-page web app
