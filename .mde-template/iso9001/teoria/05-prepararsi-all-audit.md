---
title: Prepararsi all'audit
---

# Prepararsi all'audit

## TL;DR

L'audit interno (9.2) è il controllo che il sistema fa su se stesso prima che lo faccia un ente esterno. In MdExplorer
lo prepara l'agente `iso9001-auditor`: legge i processi, i workflow, i registri dei giri e la storia in git, e scrive un
rapporto che una persona approva. Le non conformità trovate diventano azioni correttive (10.2), con un loro workflow.

- Le evidenze ci sono già: documenti approvati, esiti registrati, commit. L'audit controlla che dicano la cosa giusta.
- I rilievi tipici sono pochi e ricorrenti: ruoli senza persona, processi senza workflow, approvazioni troppo rapide.
- Un'azione correttiva si chiude solo quando qualcuno ha verificato che abbia funzionato.

## Che cosa chiede la norma

L'organizzazione fa audit interni a intervalli pianificati, con criteri e perimetro definiti, con auditor che non
controllano il proprio lavoro, e conserva i risultati. Il riesame di direzione (9.3) usa poi quei risultati per decidere.
Il metodo non stabilisce ogni quanto: è una scelta del gruppo, da scrivere nel piano degli audit in `qualita/audit/`.

## L'agente `iso9001-auditor`

Lavora per chi ha il ruolo di auditor interno. Prende dal piano in `qualita/audit/README.md` il primo audit «da fare» (quali processi, quale periodo) e legge:

- `qualita/processi.md`: i processi e i loro workflow;
- il documento delle responsabilità: chi ha quale ruolo;
- i workflow del progetto e i registri dei loro giri nel periodo;
- la storia in git dei documenti consegnati.

Consegna un rapporto in `qualita/audit/`: che cosa ha controllato, che cosa ha trovato, con le prove. **Non decide**: la
persona che ha il ruolo legge, verifica i punti dubbi e approva il rapporto. L'indipendenza la garantisce chi approva,
non l'agente.

## Le evidenze da mostrare

| L'auditor chiede | Dove si trova |
|---|---|
| chi ha fatto questa attività, e con quale ruolo | il registro del giro e il documento delle responsabilità alla data del giro |
| il documento su cui si è deciso | il commit approvato indicato nella decisione |
| che la procedura seguita fosse quella in vigore | la versione del workflow salvata dal giro quando è nato |
| che cosa è successo quando qualcosa non andava | i rifiuti con il loro motivo, e la versione rifatta |
| chi ha cambiato una regola, e quando | la storia in git del documento o del workflow |

## Come leggere la storia

Per un giro: si parte dal registro dei giri, si apre la decisione, si segue il commit indicato fino al documento. Per un
documento di regole (un workflow, il profilo dell'azienda): la storia in git dice ogni modifica, con autore e data. Una
modifica senza una ragione scritta nel messaggio è già un piccolo rilievo.

## I rilievi tipici

| Rilievo | Che cosa significa | Clausola |
|---|---|---|
| un ruolo nei workflow senza persona | nessuno risponde di quel passo | 5.3 |
| un processo in `qualita/processi.md` senza workflow né evidenze | il processo non è sotto controllo | 4.4 |
| approvazioni fatte in pochi secondi, sempre dalla stessa persona | il controllo forse è solo formale | 8.2.3 |
| un riesame senza la sezione dei rischi | i rischi non sono stati considerati dove si decide | 6.1 |
| un workflow cambiato senza ragione scritta | la modifica non è stata controllata | 7.5, 8.5.6 |
| un'azione correttiva chiusa senza verifica | non si sa se ha funzionato | 10.2 |

## Dalla non conformità all'azione correttiva

Per ogni non conformità la 10.2 chiede di reagire, capire la causa, decidere un'azione, attuarla e verificare che sia
stata efficace. Conviene farne un workflow, con passi e esiti:

1. **Registra** la non conformità, con la prova (un agente prepara, l'auditor approva).
2. **Analizza la causa**: perché è successo, non solo che cosa (il responsabile del processo approva).
3. **Decidi l'azione**: un passo di una persona, con l'azione e la data entro cui verificarla.
4. **Verifica l'efficacia**: dopo la data, il problema si è ripresentato? Esiti: «Efficace» o «Non efficace»; nel secondo
   caso si torna all'analisi.

La [03 — Dal processo al workflow](03-dal-processo-al-workflow.md) spiega come costruirlo; il MarkAgent può proporne la
prima versione.

## Prima dell'audit esterno

- Un audit interno completo nel periodo, con il rapporto approvato e le azioni aperte in corso.
- Un riesame di direzione (9.3) che abbia letto quei risultati, con il suo verbale.
- `qualita/processi.md` aggiornato: ogni processo con il suo responsabile, il suo workflow o la ragione per cui non ne ha.

Questa guida aiuta a prepararsi; il giudizio sulla conformità lo dà l'ente di certificazione.

Vedi anche: [02 — Le clausole che contano](02-le-clausole-che-contano.md),
[06 — Lavorare con il MarkAgent](06-lavorare-con-il-markagent.md).
