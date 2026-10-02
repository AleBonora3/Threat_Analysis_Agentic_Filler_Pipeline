# Progetto1.2DataIntensive

Threat Modeling e STRIDE-AI Analysis di una **Agentic Filler Pipeline Dual-Brain** per Digital Human in tempo reale, con riferimento all'**OWASP Top 10 for Agentic Applications 2026**.

## Descrizione

Questo progetto è stato sviluppato nell'ambito del corso di **Data-Intensive Architectures Security** e analizza dal punto di vista della sicurezza una pipeline agentica progettata per ridurre la latenza percepita nell'interazione con un Digital Human.

L'architettura considerata adotta un modello **Dual-Brain**, composto da:

- **Fast-Brain Agent**, responsabile della generazione immediata di filler verbali e comportamentali;
- **Deep-Brain Agent**, responsabile dell'elaborazione completa della richiesta tramite LLM, RAG e memoria contestuale;
- componenti di **STT/VAD**, **TTS**, **Lip-Synch** e **WebRTC** per la gestione dell'interazione real-time.

L'obiettivo del progetto è identificare le principali superfici di attacco e valutare come i rischi tipici dei sistemi agentici possano manifestarsi in un'architettura real-time e multi-componente.

## Metodologia

L'analisi è stata sviluppata attraverso:

- identificazione degli **asset** del sistema;
- definizione dei **trust boundary**;
- modellazione delle minacce tramite **STRIDE-AI**;
- mapping delle minacce rispetto all'**OWASP Top 10 for Agentic Applications 2026**;
- definizione e prioritizzazione degli scenari di attacco;
- analisi delle mitigazioni e dei controlli di sicurezza;
- applicazione dei principi di **Least Agency**, **Least Privilege**, sandboxing, monitoring e Human-in-the-Loop.

## Principali rischi analizzati

Tra le principali categorie considerate:

- **Agent Goal Hijack**
- **Tool Misuse & Exploitation**
- **Identity & Privilege Abuse**
- **Agentic Supply Chain Vulnerabilities**
- **Memory & Context Poisoning**
- **Insecure Inter-Agent Communication**
- **Cascading Failures**
- **Human-Agent Trust Exploitation**

Particolare attenzione è stata dedicata alle interazioni tra Fast-Brain e Deep-Brain, alla sicurezza della memoria e del contesto RAG, alla propagazione delle informazioni tra componenti e alla gestione dei privilegi nell'orchestrazione.

## Secure Architecture

Il progetto propone una secure architecture basata su un approccio **defense-in-depth**, includendo:

- isolamento degli agenti e dei relativi contesti;
- autorizzazioni granulari tramite IAM;
- comunicazioni protette tra componenti;
- validazione degli input e degli output;
- controllo degli accessi a memoria e tool;
- audit trail e logging;
- continuous monitoring;
- controllo della supply chain tramite SBOM/AIBOM;
- meccanismi di rollback, revoca e contenimento.

## Repository

Il repository contiene la relazione finale, i materiali di progetto e gli artefatti utilizzati per l'analisi e la presentazione.

## Autori

Progetto sviluppato congiuntamente da:

- **Alessio Bonora**
- **Marta Finazzi**

Il lavoro è stato realizzato in collaborazione e la cronologia Git conserva i contributi individuali dei due autori.

## Riferimenti principali

- OWASP Top 10 for Agentic Applications 2026
- OWASP Agentic AI – Threats and Mitigations
- STRIDE-AI
- Materiale del corso di Data-Intensive Architectures Security