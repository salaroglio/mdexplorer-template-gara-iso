---
mde_type: workflow
title: La gara, dal bando alla decisione
workflow: gara.workflow.json
---

# La gara, dal bando alla decisione

## TL;DR

Questo documento dice come le persone della gara e i loro agenti si passano il lavoro, da quando un bando compare a quando
l'account manager decide se partecipare. È il riesame dei requisiti che la ISO 9001 chiede **prima di impegnarsi** con un
cliente (8.2.3): la decisione, con chi l'ha presa e quando, resta registrata.

- L'account manager lancia la ricerca sui bandi e preme «Avvia il giro» sul bando che merita; ogni responsabile avvia la sua
  scheda (tecnica, contrattuale, delivery) e la approva.
- Il riesame dei requisiti parte da solo quando le tre schede sono approvate; poi l'account manager decide con un pulsante.
- Una scheda rifiutata si rifà quando la persona preme «Fai ripartire», senza un limite di volte.

## Il giro

```plantuml(@workflow, ./gara.workflow.json)
```

## Che cosa chiede la norma, e dove sta

| ISO 9001 | Dove sta nel giro |
|---|---|
| 8.2.1 comunicazione con il cliente | le «Domande per il committente» di ogni scheda |
| 8.2.2 requisiti, compresi quelli cogenti | le schede e la sezione «Requisiti» del riesame |
| 8.2.3.1 riesame prima di impegnarsi | il passo «Riesame dei requisiti» e la decisione della persona |
| 8.2.3.2 registrazione del riesame | il documento del riesame in git e la decisione nel registro dei giri, con chi, quando e il commit approvato |
| 6.1 rischi e opportunità | la sezione «Rischi» del riesame |

## Chi fa che cosa

| Passo | Chi lavora | Chi avvia | Chi approva |
|---|---|---|---|
| Cerca i bandi | agente dell'account manager | l'account manager, quando vuole | l'account manager, con «Avvia il giro» su un bando |
| Scheda tecnica, contrattuale, delivery | l'agente di ciascun responsabile | il responsabile, quando arriva la richiesta | lo stesso responsabile |
| Riesame dei requisiti | agente dell'account manager | parte da solo | l'account manager |
| Decidi se partecipare | l'account manager | arriva in posta | è la decisione |

Le persone vere stanno nel documento delle responsabilità del progetto: chi risponde di un ruolo lo dichiara lì.
