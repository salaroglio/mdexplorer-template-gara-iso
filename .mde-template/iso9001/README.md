---
title: ISO 9001
---

# ISO 9001

## TL;DR

Un metodo di lavoro per MdExplorer: il sistema di gestione per la qualità come insieme di workflow fatti bene. I processi
si descrivono in `qualita/processi.md`, un agente propone come farne dei workflow, un altro prepara l'audit interno con
le prove che i giri lasciano in git; le persone approvano e decidono.

- Si sceglie in «Crea nuovo progetto», sopra lo strato comune, o si aggiunge a un progetto che c'è già.
- Con l'esempio, il progetto nasce anche con il workflow della gara (riesame dei requisiti, 8.2.3) e una gara compilata.
- La teoria, se la chiedi, arriva in `teoria/iso9001/`: un sistema ISO 9001 visto come workflow, clausola per clausola.

## Che cosa porta

| Che cosa | Dove |
|---|---|
| I due workflow: un processo diventa un workflow, l'audit interno | `workflows/` |
| Le schede dei due agenti: progettista, assistente dell'auditor interno | `agents/` |
| I ruoli: Responsabile qualità, Auditor interno, Direzione | il documento delle responsabilità, come ruoli aperti |
| Le istruzioni per gli agenti del progetto | un blocco in `CLAUDE.md`, `AGENTS.md`, `copilot-instructions.md` |
| I file iniziali del gruppo | `qualita/`, copiati una volta da `semi/` |
| La skill dei processi | `.claude/skills/iso9001-processi/` |
| La teoria | `teoria/`, copiata in `teoria/iso9001/` se la chiedi |

## Come si comincia

1. Chi risponde dei ruoli li prende nel documento delle responsabilità (o dice «È mio» nella città degli agenti).
2. Con il MarkAgent descrivete i processi in `qualita/processi.md`; segnate «da progettare» quelli da trasformare.
3. Il responsabile qualità lancia il progettista, legge le proposte, mette in funzione i workflow approvati.
4. Scrivete il piano degli audit in `qualita/audit/README.md`; l'auditor interno lancia l'audit quando arriva la data.

## Da «Gara con ISO 9001»

Fino alla 1.2.0 questo metodo era «Gara con ISO 9001» (id `gara-iso`) e portava solo la gara. Dalla 2.0.0 la gara è
l'esempio del metodo, nel ramo `esempio`. Un progetto creato con `gara-iso` resta com'è: non si aggiorna a `iso9001`,
che è un altro template.
