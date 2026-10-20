---
title: Le clausole che contano
---

# Le clausole che contano

## TL;DR

Questa è la mappa tra le clausole della ISO 9001:2015 che toccano il lavoro di tutti i giorni e le cose di MdExplorer che
le coprono: ruoli, documenti, workflow, storia in git. Le clausole sono descritte con parole nostre e con il loro numero:
per il testo esatto si legge la norma.

- Ruoli e responsabilità (5.3) stanno nel documento delle responsabilità; le prove (7.5) in git.
- Requisiti (8.2), modifiche (8.5.6), non conformità (8.7, 10.2) e audit (9.2) diventano workflow con esiti.
- Contesto, leadership e riesame di direzione restano lavoro delle persone, ma lasciano anch'essi documenti nel progetto.

## Come leggere la tabella

Per ogni clausola: che cosa chiede, in breve; dove sta in un progetto MdExplorer; che cosa mostrare a un auditor. Una
clausola non elencata non è meno importante: è solo meno legata al modo in cui il gruppo passa il lavoro.

## Organizzazione e responsabilità

| Clausola | Che cosa chiede | Dove sta in MdExplorer |
|---|---|---|
| 4.4 processi del sistema | conoscere i processi, i loro input e output, chi ne risponde, come si controllano | `qualita/processi.md`, una riga per processo; un workflow per ogni processo che passa di mano |
| 5.3 ruoli e responsabilità | assegnare e comunicare chi ha quale responsabilità | il documento delle responsabilità del progetto: ruolo, persona, email, agenti |
| 7.2 competenza | persone competenti per il ruolo, con prove | il documento delle responsabilità dice chi; la prova della competenza va tenuta a parte |

Il documento delle responsabilità è una tabella: il **ruolo** è il nome che i workflow usano, la persona è chi ne risponde
oggi. Quando qualcuno cambia incarico si cambia una riga, e la storia in git dice da quando.

## Rischi e informazioni documentate

| Clausola | Che cosa chiede | Dove sta in MdExplorer |
|---|---|---|
| 6.1 rischi e opportunità | considerare i rischi che possono impedire i risultati, e agire | una voce fissa dei documenti di riesame: la sezione «Rischi», come nel riesame della gara |
| 7.5 informazioni documentate | tenere scritto ciò che serve, identificato, aggiornato, protetto | i documenti markdown del progetto; la storia in git dice chi ha cambiato che cosa, e quando |

La 6.1 non chiede un registro dei rischi separato da tutto il resto: chiede che i rischi siano considerati dove si decide.
Metterli come sezione obbligatoria di un documento che un ruolo approva è il modo più semplice per dimostrarlo.

La 7.5 distingue tra ciò che si **mantiene** (le regole: procedure, workflow, profilo dell'azienda) e ciò che si
**conserva** (le registrazioni: riesami fatti, esiti, verbali). In MdExplorer le prime sono documenti che cambiano con
versioni approvate; le seconde sono i documenti consegnati nei giri, che non si riscrivono.

## Attività operative

| Clausola | Che cosa chiede | Dove sta in MdExplorer |
|---|---|---|
| 8.2.2 e 8.2.3 requisiti e loro riesame | capire che cosa chiede il cliente e riesaminarlo prima di impegnarsi, registrando l'esito | un workflow come quello della gara: schede, riesame, decisione con esito |
| 8.5.6 controllo delle modifiche | riesaminare e controllare le modifiche, registrando chi le ha autorizzate | un workflow «modifica»: richiesta, analisi dell'impatto, approvazione di un ruolo |
| 8.7 output non conformi | identificare ciò che non va e decidere che cosa farne | un passo di una persona con esiti: correggere, rifare, accettare in deroga, scartare |

Il riesame dei requisiti della gara è l'esempio completo: lo legge il documento
[04 — L'esempio della gara](04-l-esempio-della-gara.md).

## Valutazione e miglioramento

| Clausola | Che cosa chiede | Dove sta in MdExplorer |
|---|---|---|
| 9.1 monitoraggio e misura | decidere che cosa misurare e analizzarlo | i registri dei giri: quanti, quanto tempo, quanti rifiuti |
| 9.2 audit interno | controllare a intervalli pianificati che il sistema funzioni | un giro dell'agente `iso9001-auditor`, con il rapporto in `qualita/audit/` |
| 9.3 riesame di direzione | la direzione riesamina il sistema e decide | un passo di una persona del ruolo Direzione, con il verbale come documento prodotto |
| 10.2 non conformità e azioni correttive | reagire, trovare la causa, correggere, verificare che abbia funzionato | un workflow con esiti: analisi della causa, azione, verifica dell'efficacia |

## Che cosa resta fuori dai workflow

- **La clausola 4** (contesto e parti interessate) e la **5.2** (politica per la qualità): sono documenti che la direzione
  scrive e approva. Nel progetto stanno in `qualita/`, come ogni altro documento, con la loro storia.
- **La 7.1** (risorse, infrastrutture, strumenti di misura): dipende dal lavoro dell'azienda; il metodo non la modella.
- **L'applicabilità**: se una clausola non si applica, va detto e motivato. È una decisione delle persone.

Vedi anche: [01 — ISO 9001 come workflow](01-iso-9001-come-workflow.md),
[03 — Dal processo al workflow](03-dal-processo-al-workflow.md),
[05 — Prepararsi all'audit](05-prepararsi-all-audit.md).
