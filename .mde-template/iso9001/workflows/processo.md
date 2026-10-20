---
mde_type: workflow
title: Un processo diventa un workflow
workflow: processo.workflow.json
---

# Un processo diventa un workflow

## TL;DR

Un processo del sistema qualità descritto in `qualita/processi.md` e segnato «da progettare» diventa la proposta di un
workflow: i passi, chi prepara e chi approva, le prove che restano, le clausole che copre. Il responsabile qualità decide
se si realizza, e lo mette in funzione con il MarkAgent.

- Il responsabile qualità lancia il progettista quando un processo è pronto per diventare un workflow.
- Una proposta da rifare si rifà quando la persona preme «Fai ripartire».
- La teoria del metodo, capitolo «Dal processo al workflow», spiega come si fa a mano o con il MarkAgent.

## Il giro

```plantuml(@workflow, ./processo.workflow.json)
```

## Chi fa che cosa

| Passo | Chi lavora | Che cosa consegna | Chi approva |
|---|---|---|---|
| Proponi il workflow | agente progettista | `qualita/proposte/proposta-<processo>.md` | il responsabile qualità |
| Decidi la proposta | il responsabile qualità | la decisione, nel registro dei giri | — |
