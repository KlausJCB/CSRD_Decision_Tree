```flowchart TD
    %% ───────── START ────────
    A(["Start / Start"])

    %% ───────── STEP 1 ───────
    B{"Listed on an EU<br>regulated market?<br><br>Notiert an einem<br>EU-geregelten Markt?"}

    %% ───────── STEP 2 (LISTED) ───────
    C{"YES-path:<br>SME test<br>(<= 250 emp, <= 40 m EUR turnover,<br><= 20 m EUR assets)<br><br>
       JA-Pfad:<br>KMU-Test<br>(<= 250 MA, <= 40 M EUR Umsatz,<br><= 20 M EUR Bilanz)"}

    %% ───────── STEP 3 (NON-LISTED) ─────
    D{"NO-path:<br>Large thresholds met?<br>> 250 emp OR > 40 m EUR turnover OR > 20 m EUR assets<br><br>
       NEIN-Pfad:<br>Großkriterien erfüllt?<br>> 250 MA ODER > 40 M EUR Umsatz ODER > 20 M EUR Bilanz"}

    %% ───────── STEP 4 (THIRD-COUNTRY) ──
    E{"Non-EU entity with<br>>= 150 m EUR EU turnover<br>AND EU branch/sub > 40 m EUR?<br><br>
       Nicht-EU-Unternehmen mit<br>>= 150 M EUR EU-Umsatz<br>UND EU-Niederlassung/Tochter > 40 M EUR?"}

    %% ───────── OUTCOMES ─────
    F(["CSRD applies:<br>Full ESRS<br><br>CSRD gilt:<br>Vollständige ESRS"])
    G(["CSRD applies:<br>ESRS LME (listed SME)<br><br>CSRD gilt:<br>ESRS LME (börsennotiertes KMU)"])
    H(["CSRD applies:<br>Third-country ESRS<br><br>CSRD gilt:<br>Drittland-ESRS"])
    I(["Not in scope<br>No CSRD duty<br><br>Nicht erfasst<br>Keine CSRD-Pflicht"])

    %% ───────── FLOW ARROWS ──
    A --> B
    B -- "YES / JA" --> C
    B -- "NO / NEIN" --> D
    C -- "YES / JA" --> G
    C -- "NO / NEIN"  --> F
    D -- "YES / JA" --> F
    D -- "NO / NEIN"  --> E
    E -- "YES / JA" --> H
    E -- "NO / NEIN"  --> I
```
