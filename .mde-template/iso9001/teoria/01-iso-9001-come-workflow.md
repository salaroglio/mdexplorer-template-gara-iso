---
title: ISO 9001 come workflow
---

# ISO 9001 come workflow

## TL;DR

La ISO 9001 chiede di gestire il lavoro per processi: ognuno con i suoi input e output, chi ne risponde, e le prove che
è stato fatto come previsto. Un workflow di MdExplorer contiene già queste tre cose, e la storia in git conserva le
prove senza lavoro in più. Resta fuori ciò che nessun workflow può dire da solo: se i processi sono quelli giusti.

- Processo = workflow: i passi sono le attività, i ruoli sono le responsabilità, gli esiti sono le decisioni.
- L'evidenza che l'auditor chiede è il registro dei giri e i commit approvati, non un modulo compilato a parte.
- La direzione, il contesto e il miglioramento restano lavoro delle persone: il workflow li rende visibili, non li fa.

## L'idea

Un sistema di gestione per la qualità, in fondo, risponde a tre domande per ogni attività che conta:

1. **Che cosa entra e che cosa esce?** Il bando entra, la decisione se partecipare esce. Il reclamo entra, la risposta
   al cliente e l'eventuale azione correttiva escono.
2. **Chi ne risponde?** Non «l'ufficio», ma un ruolo preciso, con una persona dietro.
3. **Come si dimostra che è andata così?** Con qualcosa di scritto, datato, attribuibile a qualcuno.

Un workflow di MdExplorer risponde alle stesse tre domande, ma in un formato che si esegue:

| Domanda della norma | Nel workflow |
|---|---|
| Che cosa entra e che cosa esce | gli `inputs` e gli `outputs` di ogni passo: file del progetto, con il loro percorso |
| Chi ne risponde | il ruolo di ogni passo di una persona (`person`) e di ogni approvazione (`approval.by`), legato a persone vere nel documento delle responsabilità |
| Come si dimostra | ogni consegna approvata è un commit; ogni decisione è un esito registrato con chi, quando e su quale commit |

Per questo il metodo dice: **la gestione di un progetto con la ISO 9001 è, alla fine, un workflow fatto bene**.

## Come è fatto un workflow

Un workflow è un documento markdown (con `mde_type: workflow`) che lo spiega alle persone, più un file JSON che
MdExplorer esegue. Il JSON elenca i passi:

- **un passo di un agente**: un agente prepara un documento; la persona che risponde di quell'agente, o un altro ruolo,
  lo approva;
- **un passo di una persona**: un ruolo legge ciò che riceve e chiude il passo con un esito, cioè un pulsante («Partecipiamo»
  / «Non partecipiamo», «Risolto» / «Serve un'azione correttiva»);
- **i giri ripetuti**: un documento rifiutato si rifà, finché non è approvato.

Gli agenti **preparano**, le persone **approvano e decidono**. MdExplorer passa il lavoro da un passo all'altro con regole
fisse, e non lascia che un agente decida da solo chi viene dopo.

## Perché l'auditor ci trova quello che cerca

Un auditor non vuole vedere procedure scritte bene: vuole vedere che il lavoro **è andato** come le procedure dicono.
Con un workflow di MdExplorer le prove nascono mentre si lavora:

- il documento consegnato, nella versione approvata, con il suo commit;
- chi lo ha approvato, da quale computer, quando;
- l'esito della decisione, con la persona che ha premuto il pulsante;
- i rifiuti e i rifacimenti, con il motivo scritto da chi ha rifiutato;
- la versione del workflow con cui il giro è nato: un giro tiene il workflow che aveva all'inizio, anche se poi cambia.

Questo è l'**informazione documentata conservata** di cui parla la 7.5: identificata, datata, attribuita, protetta dalle
modifiche non autorizzate perché ogni cambiamento resta nella storia di git.

## Che cosa un workflow non copre

Un workflow ben fatto copre molto, non tutto. Restano alle persone:

- **il contesto e le parti interessate** (clausola 4): quali processi servono davvero, per chi, con quali confini;
- **la leadership** (clausola 5): la politica per la qualità, gli obiettivi, l'impegno della direzione;
- **le risorse e le competenze** (7.1, 7.2): che le persone sappiano fare ciò che il ruolo chiede;
- **il giudizio**: un riesame approvato in fretta resta un riesame fatto male, anche se è registrato.

Il workflow rende questi punti **visibili**: un ruolo senza persona, un passo approvato in un minuto, un processo senza
workflow. Non li risolve.

## Il punto di partenza

Il primo passo non è scrivere un workflow: è descrivere i processi che il gruppo ha già, uno per riga, in
`qualita/processi.md`. Il documento [03 — Dal processo al workflow](03-dal-processo-al-workflow.md) spiega come, e il
[04 — L'esempio della gara](04-l-esempio-della-gara.md) mostra un processo già diventato workflow.

Vedi anche: [02 — Le clausole che contano](02-le-clausole-che-contano.md).
