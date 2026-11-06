# Pannello Qui

Una pagina sola che mostra, per ogni app Qui, se i dati sono aggiornati: https://quivicino.github.io/Pannello/

Per ogni app legge, direttamente dal browser:
- la data dei dati pubblicati (`dati/indice.json`, per Parking `osm/indice.json` e `ztl.json`);
- l'esito dell'ultimo giro programmato del workflow `pubblica.yml` (API pubblica di GitHub Actions);
- lo spazio su GitHub: dimensione del repository (`size` dall'elenco dei repository) e dell'ultima pubblicazione Pages (artifact `github-pages`), riletto ogni 6 ore;
- per Distributori, l'esito dell'ultimo giro del piano B sul computer: la riga `pc-controllo:` che `pc/scarica_mimit.ps1` scrive nella descrizione della release `dati-mimit`, e la data dell'ultimo invio dei CSV.

Bollino verde = tutto ok, giallo = dati più vecchi del previsto, rosso = scaricamento fallito o dati non leggibili.
Le soglie e l'elenco delle app sono in cima allo script di `index.html` (costante `APP`).

Pubblicazione: Impostazioni → Pages → Source: **GitHub Actions**.
