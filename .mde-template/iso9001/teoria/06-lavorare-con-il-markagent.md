---
title: Lavorare con il MarkAgent
---

# Lavorare con il MarkAgent

## TL;DR

Il MarkAgent è l'assistente con cui parli in MdExplorer: legge questa teoria, i documenti del progetto e i workflow, e ti
aiuta a capire e a costruire. Il metodo aggiunge due agenti: `iso9001-progettista`, che propone un workflow a partire da
un processo, e `iso9001-auditor`, che prepara l'audit interno. Tutti e tre propongono; le persone approvano.

- Al MarkAgent si chiede di spiegare, di confrontare, di fare la prima bozza: non di decidere.
- Il progettista scrive workflow con la skill `mde-workflow` e li controlla con `check_workflow`; l'auditor scrive rapporti.
- Ogni cosa che entra nel progetto passa da un'approvazione di una persona, ed è registrata.

## Che cosa chiedere al MarkAgent

Per capire:

- «Spiegami la 8.5.6 con un esempio del nostro lavoro.»
- «Che differenza c'è tra correzione e azione correttiva?»
- «Leggi il workflow della gara e dimmi quale passo copre la 8.2.3.2.»

Per guardare il progetto con gli occhi di un auditor:

- «Quali ruoli dei workflow non hanno una persona nel documento delle responsabilità?»
- «Quali processi di `qualita/processi.md` non hanno ancora un workflow?»
- «Fammi le domande che un auditor farebbe sul nostro processo dei reclami.»

Per costruire:

- «Aiutami a trasformare il nostro processo di gestione dei reclami in un workflow.»
- «Proponi i passi per il controllo delle modifiche, chi prepara e chi approva.»

Se questa teoria non è ancora nel progetto, il MarkAgent può proporti di scaricarla: la copia arriva in `teoria/iso9001/`
con un commit, dalla versione del metodo che il progetto usa.

## L'agente `iso9001-progettista`

Lavora per il responsabile qualità. Lo si lancia con il workflow «Un processo diventa un workflow»: legge in
`qualita/processi.md` i processi segnati «da progettare», il documento delle responsabilità e questa teoria, e per
ciascuno consegna una **proposta** in `qualita/proposte/`: i passi, chi prepara e chi approva, i documenti che restano
come prove, le clausole che il processo copre, e che cosa serve per realizzarlo (agenti nuovi, il workflow).

Le decisioni che non spettano a lui (chi approva, quante volte si rifà un passo) le lascia come domande aperte. Il
workflow vero lo scrive poi la persona con il MarkAgent (skill `mde-workflow` e `mde-agent`), e lo controlla con lo
strumento `check_workflow` prima di aggiungerlo al progetto.

La persona legge la proposta, la corregge se vuole, e la approva. Poi la aggiunge ai workflow del progetto: da quel
momento il workflow lavora.

## L'agente `iso9001-auditor`

Lavora per chi ha il ruolo di auditor interno. Prende il primo audit «da fare» del piano in `qualita/audit/README.md`, legge processi, responsabilità, workflow,
registri dei giri e storia in git, e consegna un rapporto in `qualita/audit/` con le prove di ogni rilievo. Il documento
[05 — Prepararsi all'audit](05-prepararsi-all-audit.md) dice che cosa cerca. Non controlla il lavoro della persona per cui
lavora: chi approva il rapporto deve essere indipendente dal processo controllato.

## Che cosa non fanno

- Non approvano niente: un'approvazione è sempre di una persona, dal suo computer.
- Non decidono chi viene dopo: i passaggi li fa il workflow.
- Non inventano la norma: quando un punto è dubbio lo dicono, e rimandano al testo ufficiale.
- Non cambiano un workflow già in uso senza dirlo: una modifica vale dal giro successivo, e va approvata come la prima
  versione.

## Un modo di lavorare che funziona

1. Una persona e il MarkAgent descrivono insieme i processi in `qualita/processi.md`.
2. Si sceglie il processo che fa più paura in un audit, non il più facile.
3. Il progettista propone il workflow; la persona lo rilegge con il MarkAgent, domanda per domanda.
4. Si fa un giro di prova vero e piccolo, e si aggiusta.
5. Dopo qualche giro, l'auditor fa un audit interno su quel processo.
6. Si passa al processo successivo.

Vedi anche: [03 — Dal processo al workflow](03-dal-processo-al-workflow.md), [README](README.md).
