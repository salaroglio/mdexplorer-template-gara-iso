---
name: iso9001-processi
description: "I processi del sistema qualità ISO 9001 in MdExplorer: com'è fatto qualita/processi.md, com'è fatta la proposta di workflow di un processo (qualita/proposte/) e il piano degli audit (qualita/audit/README.md). Usala quando descrivi un processo, ne proponi o ne rivedi il workflow, o prepari un audit interno."
---

# I processi del sistema qualità

L'idea del metodo: un sistema ISO 9001 è in gran parte un insieme di **processi fatti bene**, e un processo che passa di
mano in mano è un **workflow** di MdExplorer. Chi prepara (un agente) e chi approva (una persona di un ruolo) sono scritti;
ogni giro resta nel registro dei giri e in git, ed è la prova che l'audit chiede (7.5).

## `qualita/processi.md`

Una tabella, una riga per processo:

| Colonna | Che cosa c'è |
|---|---|
| Processo | il nome, breve: «Gestione dei reclami» |
| Scopo e confini | a che cosa serve, dove comincia e dove finisce |
| Input / output | che cosa entra, che cosa esce |
| Responsabile | il ruolo che ne risponde, come in `responsabilita.md` |
| Prove | i documenti che il processo lascia |
| Workflow | il percorso del suo documento di workflow; «da progettare»; o «nessuno», con il perché |

## La proposta `qualita/proposte/proposta-<processo>.md`

- `## TL;DR`: tre righe e tre punti, scritto per ultimo.
- `## Il processo`: la riga di `processi.md`, ripresa.
- `## I passi`: una tabella con **passo**, **chi prepara** (agente, nuovo o esistente), **che cosa consegna** (il percorso
  del file), **chi approva** (il ruolo), **se viene rifiutato** (si rifà, quante volte).
- `## Le prove`: che cosa resta e dove, per ogni passo: il documento, la decisione nel registro dei giri.
- `## Le clausole`: le clausole ISO 9001 che il processo copre, con il numero e una riga di perché.
- `## Domande aperte`: ciò che deve decidere la persona.
- `## Per realizzarlo`: gli agenti nuovi da scrivere (skill `mde-agent`) e il workflow (skill `mde-workflow`, poi lo
  strumento `check_workflow`).

## Il piano degli audit `qualita/audit/README.md`

Una tabella: **audit** (la data prevista), **perimetro** (i processi), **periodo** (da quando a quando), **stato** («da
fare», «fatto: audit-<data>.md»). L'agente dell'auditor interno prepara il primo «da fare». Chi approva il rapporto non
risponde dei processi controllati.
