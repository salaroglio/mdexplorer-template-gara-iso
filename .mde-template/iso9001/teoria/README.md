---
title: La teoria del metodo ISO 9001
---

# La teoria del metodo ISO 9001

## TL;DR

Questa cartella spiega come un sistema di gestione per la qualità ISO 9001 diventa, in MdExplorer, un insieme di
workflow fatti bene: chi prepara, chi approva, che cosa resta scritto. Si legge da soli o con il MarkAgent, e con il
MarkAgent si costruiscono i workflow veri del gruppo.

- Sei documenti brevi, da leggere in ordine la prima volta; poi si torna a quello che serve.
- Il punto di partenza è un'idea sola: un processo ISO 9001 ben descritto è già quasi un workflow.
- È una guida di lavoro: non sostituisce la norma, né il giudizio di un ente di certificazione.

## Che cosa trovi qui

| Documento | Di che cosa parla | Quando leggerlo |
|---|---|---|
| [01 — ISO 9001 come workflow](01-iso-9001-come-workflow.md) | l'idea: processi, responsabilità ed evidenze diventano passi, ruoli e commit | per primo |
| [02 — Le clausole che contano](02-le-clausole-che-contano.md) | le clausole della norma accanto alle cose di MdExplorer che le coprono | quando ti chiedi «dove sta questo, per l'auditor?» |
| [03 — Dal processo al workflow](03-dal-processo-al-workflow.md) | il procedimento passo per passo, con l'esempio dei reclami | quando costruisci un workflow nuovo |
| [04 — L'esempio della gara](04-l-esempio-della-gara.md) | il workflow della gara letto come modello: che cosa prova ogni passo | per vedere un workflow finito |
| [05 — Prepararsi all'audit](05-prepararsi-all-audit.md) | l'audit interno, le evidenze da mostrare, le azioni correttive | prima di un audit, interno o esterno |
| [06 — Lavorare con il MarkAgent](06-lavorare-con-il-markagent.md) | che cosa chiedere, e i due agenti del metodo | sempre, quando lavori |

## L'ordine di lettura

1. Leggi il documento 01: dice perché questo metodo funziona, e dove si ferma.
2. Scorri il 02 senza fermarti su ogni riga: ti serve sapere che la tabella esiste.
3. Prima di costruire il tuo primo workflow leggi il 03 e il 04 insieme: il 03 dice come si fa, il 04 mostra il
   risultato.
4. Il 05 serve quando l'audit si avvicina, ma conviene leggerlo presto: dice che cosa l'auditor guarderà, quindi che
   cosa i workflow devono lasciare scritto.
5. Il 06 è il manuale d'uso dei due agenti del metodo e del MarkAgent.

## Come usarla con il MarkAgent

Il MarkAgent legge questi documenti come li leggi tu. Puoi chiedergli di spiegarti un punto, di applicarlo al tuo caso,
o di fare il primo passo insieme a te. Qualche esempio di richiesta:

- «Spiegami con parole semplici che cosa chiede la 8.2.3 e dove sta nel nostro progetto.»
- «Aiutami a trasformare il nostro processo di gestione dei reclami in un workflow.»
- «Leggi `qualita/processi.md` e dimmi quali processi non hanno ancora un responsabile o un'evidenza.»
- «Fammi le domande che farebbe un auditor sul workflow della gara.»

Il MarkAgent propone; **le persone decidono**. Un workflow entra nel progetto solo quando chi risponde del processo lo
ha letto e approvato, e quando lo strumento `check_workflow` di MdExplorer dice che è valido.

## Le parole

| Parola | Che cos'è | In MdExplorer |
|---|---|---|
| Processo | un insieme di attività che trasforma degli input in output | un workflow |
| Responsabile di processo | chi risponde di come il processo funziona | un ruolo nel documento delle responsabilità |
| Informazione documentata | ciò che va tenuto scritto (7.5) | i documenti del progetto e la loro storia in git |
| Evidenza | la prova che una cosa è stata fatta | un documento approvato, un esito registrato, un commit |
| Audit interno | il controllo che il sistema fa su se stesso (9.2) | un giro con l'agente `iso9001-auditor` |

## Che cosa non trovi qui

- Il testo della norma: va letto nell'edizione ufficiale che l'azienda possiede.
- Una lista di documenti obbligatori da riempire: la norma chiede risultati e prove, non moduli.
- La certificazione: la rilascia un ente accreditato, dopo il suo audit.
