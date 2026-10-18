---
name: gara-iso-riesame
description: "Come si scrive il riesame dei requisiti prima di impegnarsi con un cliente (ISO 9001, 8.2.3): requisiti espliciti, impliciti e cogenti, capacità di soddisfarli, rischi, raccomandazione. Usala quando scrivi o rivedi gare/schede/riesame.md o quando ti chiedono se un'offerta è stata riesaminata."
---

# Il riesame dei requisiti (ISO 9001, 8.2.3)

Prima di impegnarsi a fornire un prodotto o un servizio — per una gara, **prima di presentare l'offerta** — l'azienda
riesamina i requisiti e si chiede se è in grado di soddisfarli. L'esito si **registra** (8.2.3.2). In questo metodo la
registrazione è fatta di due cose: il documento `gare/schede/riesame.md` in git, e la decisione della persona nel registro dei
giri di MdExplorer, con chi, quando e il commit approvato.

## Che cosa deve contenere

`gare/schede/riesame.md` ha queste sezioni, in quest'ordine:

- `## TL;DR`: tre righe e tre punti, scritto per ultimo.
- `## Il bando`: codice, titolo, committente, scadenza dell'offerta e giorni che mancano dalla data di lavoro; i percorsi del
  documento di gara, della ricerca e delle tre schede approvate.
- `## Raccomandazione`: *andare*, *andare a condizioni* oppure *non andare*, con il motivo in due righe. È una proposta: decide
  la persona.
- `## I cinque criteri`: una tabella con i criteri 1 e 5 come li ha giudicati la ricerca e i criteri 2, 3 e 4 come li hanno
  chiusi le schede (esito e scheda da cui viene).
- `## Requisiti` (8.2.2), in tre tabelle con sezione del documento di gara e stato (coperto, parziale, non coperto, da chiarire):
  - **espliciti**: ciò che il bando chiede per iscritto;
  - **impliciti**: ciò che il cliente si aspetta anche se non lo scrive (per esempio la continuità di un servizio esistente);
  - **cogenti**: leggi, norme e certificazioni obbligatorie, prese dalle sezioni «Requisiti cogenti» delle schede.
- `## Capacità di soddisfarli` (8.2.3.1): per area (tecnica, contratto, delivery) che cosa manca e se si può colmare prima
  della scadenza o della consegna.
- `## Rischi` (6.1): i rischi aperti per area, il più grave di ciascuna, e le opportunità se ce ne sono.
- `## Punti da chiarire con il committente` (8.2.1): elenco numerato, con area e sezione del documento di gara.
- `## Dove le schede si contraddicono`: quando due schede dicono cose diverse sullo stesso punto, scrivilo qui.
- `## Da verificare da te`: tre punti in cui il riesame è meno sicuro.

## Regole

- Ogni dato cita la **scheda** o la **sezione** del documento di gara da cui viene: l'auditor deve poterlo ritrovare.
- Non inventare: ciò che le schede e il documento di gara non dicono è «da chiarire».
- Il riesame non decide: la decisione è della persona, nel passo «Decidi se partecipare» del workflow.
- Se dopo il riesame il bando cambia (chiarimenti, rettifiche che toccano i requisiti — 8.2.4), il giro si rifà: le schede e il
  riesame si riscrivono, e la storia di git conserva le versioni di prima.
