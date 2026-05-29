# Bethesda Tool Pack

**Autore:** OldGamerDarthy, ovvero Luigi Sestili Spurio  
**Marchio:** OGD  
**Licenza:** GNU General Public License v3.0  
**Piattaforma principale:** Windows / PowerShell  
**Stato:** progetto in costruzione  

Bethesda Tool Pack e' una raccolta di script, utility e strumenti di supporto pensati per giochi Bethesda, con particolare attenzione a installazioni moddate, diagnostica, raccolta log e procedure di troubleshooting.

L'obiettivo del pack e' avere una cassetta degli attrezzi pratica: piccoli tool mirati, avviabili facilmente, utili per capire cosa non va, raccogliere informazioni e preparare report leggibili senza dover fare ogni controllo a mano.

## Obiettivi

- Centralizzare script utili per giochi Bethesda.
- Aiutare nella diagnosi di crash, freeze, errori di modding e problemi di configurazione.
- Raccogliere log, report, dump e informazioni di sistema in modo ordinato.
- Rendere le operazioni ripetitive piu' semplici tramite menu guidati.
- Mantenere ogni tool leggibile, modificabile e distribuibile come script PowerShell.

## Tool inclusi

### Beth Crash Analyzer - Skyrim AE

**File:** `BethCrashAnalyzer2.2SkyrimAE.ps1`  
**Versione:** 2.2  
**Gioco target:** Skyrim Special Edition / Anniversary Edition  

Tool per monitorare Skyrim AE/SE durante una sessione di gioco, analizzare log Papyrus e SKSE, raccogliere eventi crash Windows, creare report e archivi ZIP finali.

Funzioni principali:

- menu clickabile Windows Forms;
- fallback con menu testuale PowerShell;
- rilevamento automatico di Skyrim tramite Steam;
- percorso gioco impostabile manualmente;
- avvio tramite SKSE quando presente;
- monitoraggio del processo `SkyrimSE.exe`;
- abilitazione Papyrus logging con backup di `Skyrim.ini`;
- raccolta di log, dump, diagnostica sistema, plugin SKSE, `plugins.txt` e `loadorder.txt`;
- report finale e archivio ZIP della sessione.

## Struttura consigliata del pack

```text
BethesdaToolPack\
  README.md
  LICENSE.md
  tools\
    SkyrimAE\
      BethCrashAnalyzer2.2SkyrimAE.ps1
      README.md
  docs\
  examples\
```

Per ora i file possono stare anche sul Desktop durante lo sviluppo. Quando il pack crescera', conviene spostarli in una cartella unica con la struttura sopra.

## Uso rapido

Per avviare un tool PowerShell:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\NomeTool.ps1
```

Esempio:

```powershell
.\BethCrashAnalyzer2.2SkyrimAE.ps1
```

## Linee guida per i tool

Ogni tool del Bethesda Tool Pack dovrebbe avere:

- un nome chiaro;
- una versione interna;
- un README dedicato;
- output salvati in cartelle ordinate;
- modalita' guidata tramite menu;
- opzioni da riga di comando quando utile;
- nessuna modifica distruttiva senza conferma;
- backup automatici quando modifica file di configurazione;
- report leggibili anche senza aprire lo script.

## Idee future

- Analyzer per Fallout 4.
- Analyzer per Starfield.
- Tool di backup configurazioni e load order.
- Tool di pulizia log.
- Launcher unico del Bethesda Tool Pack.
- Esportazione report in Markdown o HTML.

## Licenza

Bethesda Tool Pack e' distribuito con licenza **GNU General Public License v3.0**.

Vedi `LICENSE.md` per i dettagli.

## Crediti

Creato e mantenuto da **OldGamerDarthy**, ovvero **Luigi Sestili Spurio**, marchio **OGD**.  
Documentazione e sviluppo assistiti con Codex ed Antigravity.
