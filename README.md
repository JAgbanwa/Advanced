An interesting book on Mathematics for Machine Learning I found [here](https://mml-book.github.io/book/mml-book.pdf). Must read! 

A paper from SR Dahmen that's a must-read is [this](https://arxiv.org/pdf/2209.15492) and [that](https://dspace.library.uu.nl/server/api/core/bitstreams/c0f6921b-b13d-4bdb-aeab-7dc314d0b4d5/content).

A website for Quants: [see](https://quantmemo.com/learn).

A great website for academics: [here](https://researcheracademy.elsevier.com).



# Path Forward — Decision Trees

> Legal points are questions for an immigration lawyer, not conclusions.

## Overview

```mermaid
flowchart TD
    S["Current situation:<br/>research record, no degree, status unresolved"] --> L["Legal consultation<br/>ROS / Stichting LOS / Pauluskerk → immigration lawyer"]
    L --> RA["Route A: Regularize inside NL"]
    L --> RB["Route B: Job offer becomes the permit"]
    BT["Build track:<br/>research + Lean + courses"] --> RB
    BT --> RA
```

## Route A — Regularize from inside the Netherlands

```mermaid
flowchart TD
    A0["Legal consultation with fact sheet:<br/>timeline, Belgium history, family status, documents"] --> A1{"Basis via immediate<br/>family in NL?"}
    A0 --> A2{"Basis via length of stay<br/>and private-life ties?"}
    A0 --> A3{"Belgium: prior status<br/>or Dublin issue?"}

    A1 -->|Yes| AR["Lawyer-led regularization application"]
    A2 -->|Yes| AR
    A3 -->|"Prior status revivable"| AB["Resolve via Belgium<br/>(lawyer-led)"]
    A3 -->|"Dublin applies"| AD["Lawyer assesses transfer risk<br/>before any other step"]

    A1 -->|No| AN{"Any basis at all?"}
    A2 -->|No| AN
    AN -->|No| GOB["Go to Route B"]

    AR --> AP{"Permit granted?"}
    AB --> AP
    AP -->|No| AAP["Appeal options (lawyer)"]
    AAP -->|"Unsuccessful"| GOB
    AP -->|Yes| OPEN["Everything opens"]

    OPEN --> O1["Colloquium doctum<br/>→ degree entry"]
    OPEN --> O2["Exemption-based external PhD<br/>(buitenpromovendus)"]
    OPEN --> O3["Jobs: research software,<br/>formal verification, data"]
    OPEN --> O4["Paid Mathlib contracting"]
```

## Route B — A job offer becomes the permit

```mermaid
flowchart TD
    B0["Hireable track record<br/>(from Build track)"] --> B1{"Concrete offer from a<br/>recognized sponsor?"}

    B1 -->|No| B1N["Keep building:<br/>more PRs, papers, references"]
    B1N --> B1
    B1 -->|"Remote contract only<br/>(e.g. Mathlib Initiative)"| BR["Legal only from a country<br/>where you can work — ask lawyer"]

    B1 -->|Yes| B2["Employer applies: highly skilled migrant<br/>researcher — no salary threshold,<br/>no diploma requirement (confirm)"]
    B2 --> B3["Visa (mvv) normally applied<br/>for from outside NL, e.g. Ghana"]
    B3 --> B4{"Lawyer: can you leave<br/>without an entry ban?"}

    B4 -->|"Yes, safe"| B5["Depart properly → apply from abroad"]
    B4 -->|"No / risk"| B6["Resolve entry-ban risk first,<br/>or explore exceptions (lawyer)"]
    B6 --> B4

    B5 --> B7{"Permit granted?"}
    B7 -->|Yes| B8["Return on researcher permit<br/>→ academic work in NL"]
    B7 -->|No| B9["Reapply / other sponsor /<br/>build from abroad"]
```

## Build Track — what feeds both routes

```mermaid
flowchart TD
    P["Priorities"] --> P1["Sums of three cubes<br/>→ methods paper regardless of outcome"]
    P --> P2["Grechuk project<br/>→ second paper + reference letter"]
    P --> P3["Lean formalization<br/>→ 3–5 merged Mathlib PRs, then reviewing"]

    C["Courses"] --> C1["Academic writing (now)<br/>→ better papers"]
    C --> C2["AI/ML (later), aimed at<br/>autoformalization + Lean"]
    C --> C3["Communication<br/>→ practise via seminars and emails"]

    P1 --> T["Track record:<br/>papers, PRs, references"]
    P2 --> T
    P3 --> T
    C1 --> T
    C2 --> T
    C3 --> T

    T --> OUT1["Route B: someone wants to sponsor you"]
    T --> OUT2["Route A: ready the moment status opens"]
```
