# JOINT — GitHub Pages

Esportazione per **Cosin1966/joint**.
Indirizzo previsto: https://cosin1966.github.io/joint/

## Pubblicazione

1. Estrarre lo ZIP.
2. Caricare il contenuto della cartella `cognition-in-action-lab` nella radice del repository, includendo `.github/workflows/pages.yml` e `.nojekyll`. Non caricare lo ZIP stesso e non aggiungere una cartella esterna.
3. Nel repository aprire **Settings → Pages → Build and deployment → Source → GitHub Actions**.
4. Eseguire il commit sul branch `main`. Il workflow **Deploy GitHub Pages** pubblica il sito. Se necessario avviarlo dalla scheda Actions con **Run workflow**.

Il pacchetto è pronto; questa esportazione non ha modificato né pubblicato il repository GitHub.

## Contenuti

- `index.html` e le sei cartelle delle altre pagine: sito statico completo, modificabile direttamente senza compilazione.
- `assets/site.css`: foglio di stile compilato originale, inclusi gli stili responsive.
- `assets/fonts`: caratteri Geist e Geist Mono originali, disponibili localmente.
- `images`, `logos`, `people/*.jpg` e SVG: tutte le risorse originali.
- `original-source`: copia integrale del progetto React/TypeScript originale, con testi, componenti, CSS sorgente, configurazioni e risorse; esclusa la cronologia Git. Questa cartella è conservata per sviluppo e non viene pubblicata dal workflow.
- `EXPORT-VERIFICATION.json`: controllo delle sette pagine, conservazione del testo e riferimenti locali.

La versione statica mantiene l'HTML e il CSS effettivamente pubblicati. La navigazione utilizza collegamenti HTML standard e il menu mobile mantiene il controllo nativo `<details>`. Gli script di navigazione Vinext e i metadati di anteprima sono rimossi perché richiedono il server originale; le pagine non dipendono da tale server. Le immagini e i caratteri sono inclusi nel pacchetto. I collegamenti esterni alle pubblicazioni restano invariati.

I percorsi sono predisposti per `/joint/`. Se cambia il nome del repository o si usa un dominio personalizzato, aggiornare questo prefisso negli HTML e nel CSS. Per un'anteprima locale, servire la cartella superiore con `python3 -m http.server 8000` e visitare `http://localhost:8000/joint/`.

Per modifiche immediate su GitHub Pages, aggiornare gli HTML e `assets/site.css`. Le modifiche ai TSX in `original-source` richiedono una nuova esportazione statica: il workflow incluso pubblica gli HTML pronti, non compila il progetto server originale.
