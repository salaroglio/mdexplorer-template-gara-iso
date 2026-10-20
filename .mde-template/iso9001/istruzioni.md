## ISO 9001

- `qualita/` è il sistema qualità del gruppo: `processi.md` (i processi e i loro workflow), `proposte/` (le proposte di
  workflow), `audit/` (il piano degli audit, i rapporti, le azioni). Quando ti chiedono del sistema qualità, parti da
  `qualita/processi.md`, e segui la skill `iso9001-processi`.
- I giri sono il workflow `.mde-template/iso9001/workflows/processo.md` (un processo diventa un workflow) e
  `.mde-template/iso9001/workflows/audit.md` (l'audit interno): non far partire tu i loro agenti e non scrivere i loro
  file al loro posto.
- Per mettere in funzione un workflow approvato usa le skill `mde-workflow` e `mde-agent`, e controllalo con lo
  strumento `check_workflow` prima di aggiungerlo al progetto.
- La teoria del metodo, se il progetto l'ha chiesta, sta in `teoria/iso9001/`: usala per spiegare come un processo
  diventa un workflow e come ci si prepara all'audit. Se manca e servirebbe, proponi di scaricarla (strumento
  `add_theory`, id `iso9001`) e scaricala solo dopo il sì della persona.
- Non inventare la norma: descrivi le clausole con parole tue e il loro numero, e rimanda al testo ufficiale.
- I file in `.mde-template/iso9001/` sono del metodo e arrivano con i suoi aggiornamenti: non modificarli.
