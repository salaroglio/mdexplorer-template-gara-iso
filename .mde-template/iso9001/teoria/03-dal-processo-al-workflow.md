---
title: Dal processo al workflow
---

# Dal processo al workflow

## TL;DR

Un workflow si costruisce partendo dal processo com'è oggi, non da un modello ideale: lo si descrive in una riga di
`qualita/processi.md`, lo si divide in passi, si decide chi prepara e chi approva ogni passo, e solo alla fine lo si
scrive. L'esempio che segue è la gestione dei reclami.

- Prima la riga del processo (scopo, input, output, responsabile, evidenze), poi i passi, poi il file.
- Un agente prepara, un ruolo approva: ogni passo consegna un file, e ogni decisione è un esito con dei pulsanti.
- Il workflow si scrive con la skill `mde-workflow` e si controlla con lo strumento `check_workflow` prima di usarlo.

## 1. Descrivi il processo in una riga

In `qualita/processi.md` ogni processo del gruppo ha una riga:

| Campo | Che cosa scrivere | Reclami, per esempio |
|---|---|---|
| Scopo | perché il processo esiste, in una frase | rispondere al cliente e togliere la causa del problema |
| Input / output | che cosa lo fa partire, che cosa consegna | un reclamo; la risposta al cliente e, se serve, un'azione correttiva |
| Responsabile | il ruolo che ne risponde | Responsabile qualità |
| Evidenze | che cosa deve restare scritto | il reclamo registrato, l'analisi, la risposta, la decisione |

Se una riga non si riesce a compilare, il problema non è il workflow: è che il processo non è ancora chiaro. Conviene
fermarsi lì e parlarne nel gruppo.

## 2. Dividilo in passi

Scrivi il processo come una sequenza di attività, ognuna con **un solo** responsabile e **un solo** risultato. Per i
reclami:

1. **Registra il reclamo**: chi lo riceve lo descrive, con cliente, data, prodotto o servizio.
2. **Analizza**: che cosa è successo, quale requisito non è stato rispettato, se è un caso isolato.
3. **Decidi**: basta una correzione, o serve un'azione correttiva sulla causa (10.2)?
4. **Rispondi al cliente**: la risposta, approvata da chi ne risponde.
5. **Verifica l'efficacia**, se c'è stata un'azione correttiva: dopo un tempo concordato, il problema si è ripresentato?

Regola utile: se un passo ha due approvatori, sono due passi.

## 3. Decidi chi prepara e chi approva

Per ogni passo, due domande:

- **Lo prepara un agente o lo fa una persona?** Un documento da scrivere (l'analisi, la bozza di risposta) lo prepara un
  agente; una scelta (correggere o agire sulla causa) è un passo di una persona, con gli esiti come pulsanti.
- **Chi approva?** Di norma chi risponde dell'agente; quando la norma vuole un'altra firma, lo dice il workflow con
  l'approvazione di un ruolo («la risposta al cliente la approva il Responsabile qualità»).

| Passo | Chi lavora | Che cosa consegna | Chi approva o decide |
|---|---|---|---|
| Registra | agente del servizio clienti | `qualita/reclami/<codice>.md` | Servizio clienti |
| Analizza | agente del servizio clienti | `qualita/reclami/<codice>-analisi.md` | Responsabile qualità |
| Decidi | Responsabile qualità | esito: «Correzione» o «Azione correttiva» | è la decisione |
| Rispondi | agente del servizio clienti | `qualita/reclami/<codice>-risposta.md` | Responsabile qualità |

I ruoli devono esistere nel documento delle responsabilità, con una persona dietro.

## 4. Definisci gli output come file

Ogni consegna è un file con un percorso fisso, in una cartella che esiste e ha il suo `README.md`. Un percorso con `*`
(`reclami/reclamo-*.md`) va bene quando ogni giro produce un file nuovo. I file sono la prova: devono dire che cosa è
stato fatto, non riassumerlo.

## 5. Decidi che cosa succede quando qualcosa è rifiutato

Un'analisi rifiutata si rifà: è un ciclo «finché non è approvato». Decidi se si ripete senza limite (la scelta di solito
giusta) o al massimo un certo numero di volte, e chi la fa ripartire. Il limite è una decisione delle persone, non del
MarkAgent.

## 6. Scrivi il workflow, e controllalo

Solo adesso si scrive. L'agente `iso9001-progettista` può prepararne la proposta (passi, ruoli, prove); il workflow vero
lo scrivi con il MarkAgent e la skill `mde-workflow`: il documento con `mde_type: workflow` e il suo file `.workflow.json`, più le schede degli agenti che
servono. Poi:

1. lo strumento `check_workflow` di MdExplorer deve rispondere che è valido; ogni avviso va letto;
2. il documento si aggiunge ai workflow del progetto (Impostazioni del progetto, «Documenti dei workflow»);
3. chi risponde del processo lo legge, con il disegno che MdExplorer ne fa, e lo approva;
4. si fa un giro di prova su un caso vero e piccolo, e si aggiusta.

Un giro tiene la versione del workflow con cui è nato: una modifica vale dal giro successivo.

## 7. Aggiorna la riga del processo

Torna in `qualita/processi.md` e scrivi, accanto al processo, il percorso del suo workflow. Così l'elenco dice quali
processi sono già workflow e quali no: è la prima cosa che un auditor interno guarderà.

Vedi anche: [04 — L'esempio della gara](04-l-esempio-della-gara.md),
[06 — Lavorare con il MarkAgent](06-lavorare-con-il-markagent.md).
