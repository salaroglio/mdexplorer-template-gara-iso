---
mde_type: workflow
title: L'audit interno
workflow: audit.workflow.json
---

# L'audit interno

## TL;DR

L'audit interno (ISO 9001, 9.2) del piano in `qualita/audit/README.md`: l'agente prepara il rapporto con una prova per
ogni rilievo, l'auditor interno lo verifica e lo approva, la direzione decide le azioni (10.2).

- L'auditor interno lancia l'agente quando arriva l'audit «da fare» del piano.
- Chi approva il rapporto non deve rispondere dei processi controllati: l'indipendenza la garantisce la persona, non l'agente.
- Rapporto e azioni restano in `qualita/audit/`, le decisioni nel registro dei giri.

## Il giro

```plantuml(@workflow, ./audit.workflow.json)
```

## Chi fa che cosa

| Passo | Chi lavora | Che cosa consegna | Chi approva |
|---|---|---|---|
| Prepara il rapporto | agente dell'auditor interno | `qualita/audit/audit-<data>.md` | l'auditor interno |
| Decidi le azioni | la direzione | `qualita/audit/azioni-<data>.md` e la decisione | — |
