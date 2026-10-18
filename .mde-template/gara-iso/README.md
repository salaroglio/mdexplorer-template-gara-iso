---
title: Gara con ISO 9001
---

# Gara con ISO 9001

## TL;DR

Un metodo di lavoro per MdExplorer: dal bando alla decisione se partecipare, con il riesame dei requisiti che la ISO 9001
chiede **prima di impegnarsi** con un cliente (8.2.3). Quattro agenti preparano, le persone approvano e decidono, e tutto resta
registrato in git.

- Si sceglie in «Crea nuovo progetto» o si aggiunge a un progetto che c'è già; si aggiorna e ci si può staccare.
- Porta solo la sua cartella (`.mde-template/gara-iso/`) e la sua skill; i file del gruppo nascono una volta in `gare/`.
- Con l'esempio, il progetto nasce con una gara compilata (Pentagroup e il bando di Nordica Crediti, inventati).

## Che cosa porta

| Che cosa | Dove |
|---|---|
| Il workflow della gara | `workflows/gara.md` |
| Le schede dei quattro agenti | `agents/` |
| I ruoli: Account manager, Responsabile tecnico, legale, delivery | il documento delle responsabilità del progetto, come ruoli aperti |
| Le istruzioni per gli agenti del progetto | un blocco in `CLAUDE.md`, `AGENTS.md`, `copilot-instructions.md` |
| I file iniziali del gruppo | `gare/`, copiati una volta da `semi/` |
| La skill del riesame | `.claude/skills/gara-iso-riesame/` |

## Come si comincia

1. Chi risponde di un ruolo scrive nome ed email nel documento delle responsabilità (o dice «È mio» nella città degli agenti).
2. I responsabili compilano il loro capitolo di `gare/profilo-azienda.md`.
3. Il gruppo raccoglie i bandi in `gare/bandi.md` e mette i documenti di gara in `gare/documenti-di-gara/`.
4. L'account manager lancia la ricerca e preme «Avvia il giro» sul bando che merita.

## Che cosa copre della norma

Solo la 8.2 (requisiti per prodotti e servizi), con il rischio della gara (6.1) come voce del riesame. Le versioni successive
aggiungeranno le altre clausole del perimetro: informazioni documentate (7.5), modifiche (8.5.6), non conformità (8.7/10.2),
audit interno (9.2).
