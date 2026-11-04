# Pannello Qui

Una pagina sola che mostra, per ogni app Qui, se i dati sono aggiornati: https://quivicino.github.io/Pannello/

Per ogni app legge, direttamente dal browser:
- la data dei dati pubblicati (`dati/indice.json`, per Parking `osm/indice.json` e `ztl.json`);
- l'esito dell'ultimo giro programmato del workflow `pubblica.yml` (API pubblica di GitHub Actions);
- per Distributori, la data dell'ultimo invio del piano B dal computer (release `dati-mimit`).

Bollino verde = tutto ok, giallo = dati più vecchi del previsto, rosso = scaricamento fallito o dati non leggibili.
Le soglie e l'elenco delle app sono in cima allo script di `index.html` (costante `APP`).

Pubblicazione: Impostazioni → Pages → Source: **GitHub Actions**.
