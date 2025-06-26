```mermaid
flowchart TD
    A([Start / Start])

    %% STEP 1
    B{Listed on an EU<br>regulated market?<br><br>Notiert an einem<br>EU-geregelten Markt?}

    %% STEP 2 – LISTED PATH
    C{If **YES**:<br>Qualifies as SME?<br>(≤ 250 emp.; ≤ €40 m turnover;<br>≤ €20 m assets)<br><br>
      Falls **JA**:<br>Gilt als KMU?<br>(≤ 250 MA; ≤ 40 M € Umsatz;<br>≤ 20 M € Bilanz)}

    %% STEP 3 – NON-LISTED PATH
    D{If **NO**:<br>Exceeds 2 of 3 “large”<br>thresholds?<br>> 250 emp.; > €40 m turnover;<br>> €20 m assets<br><br>
      Falls **NEIN**:<br>Überschreitet 2 von 3<br>Großkriterien?<br>> 250 MA; > 40 M € Umsatz;<br>> 20 M € Bilanz}

    %% STEP 4 – THIRD-COUNTRY PATH
    E{If **NO** to both:<br>Non-EU parent with<br>≥ €150 m EU turnover<br>**and** EU branch/sub<br>(> €40 m turnover)?<br><br>
      Falls **NEIN** bei beiden:<br>Nicht-EU-Unternehmen mit<br>≥ 150 M € EU-Umsatz **und**<br>EU-Niederlassung/Tochter<br>(> 40 M € Umsatz)?}

    %% OUTCOMES
    F([CSRD applies:<br>**Full ESRS**<br><br>CSRD gilt:<br>**Vollständige ESRS**])
    G([CSRD applies:<br>**ESRS LME** (listed SME)<br><br>CSRD gilt:<br>**ESRS LME** (börsennotiertes KMU)])
    H([CSRD applies:<br>**Third-country ESRS**<br><br>CSRD gilt:<br>**Drittland-ESRS**])
    I([Not in scope –<br>no CSRD reporting<br><br>Nicht erfasst –<br>keine CSRD-Pflicht])

    %% FLOW
    A --> B
    B -- YES / JA --> C
    B -- NO  / NEIN --> D

    C -- YES / JA --> G
    C -- NO  / NEIN --> F    %% listed but not SME → Full ESRS

    D -- YES / JA --> F      %% large private entity → Full ESRS
    D -- NO  / NEIN --> E

    E -- YES / JA --> H
    E -- NO  / NEIN --> I
```
