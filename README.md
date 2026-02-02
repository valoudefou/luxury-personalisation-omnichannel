```mermaid
flowchart TD
  %% =========================
  %% DIOR ABANDONED BASKET JOURNEY
  %% Same colour palette as your reference image
  %% =========================

  A[Step 1: Customer browses Dior website<br/>Discovers products, compares, hesitates<br/>Adds item(s) to basket<br/><b>Clear intention to purchase</b> (AdaptiveCX)]
  --> B[Step 2: Basket abandonment<br/>Leaves at checkout due to interruption, hesitation, reassurance needed<br/><b>Result:</b> basket pending, no purchase]

  B --> C[Step 3: Personalised follow up email<br/>Message tailored to situation:<br/>• Basket reminder<br/>• Stores near you (drive to store)<br/>• Speak to an adviser<br/>• Product recommendations<br/><b>Goal:</b> reduce hesitation and reopen path to purchase]

  C --> D{Step 4: After email<br/>Customer chooses a path}

  %% Scenario A: Back to website
  D -->|Scenario A: Return to website| A1[Basket recalled and put into context<br/>Reassurance info: price, delivery, availability, returns<br/>Complementary products suggested<br/>Browsing history remembered]
  A1 --> A2{Purchase happens online?}
  A2 -->|Yes| Z[Success<br/>End of journey]
  A2 -->|No| N1[No purchase yet<br/>Softer follow up possible]

  %% Scenario B: Drive to store
  D -->|Scenario B: Drive to store| B1[Find nearest store<br/>Get assistance<br/>Reserve or finalise purchase in store]
  B1 --> B2{Purchase happens in store?}
  B2 -->|Yes| Z
  B2 -->|No| N1

  %% Scenario C: Human help
  D -->|Scenario C: Need a human| C1[Contact Customer Service or request call back<br/>Adviser sees context:<br/>basket contents, viewed items, complements]
  C1 --> C2{Purchase happens after advice?}
  C2 -->|Yes| Z
  C2 -->|No| N1

  %% =========================
  %% STYLES (beige + gold + grey like your image)
  %% =========================
  classDef step fill:#F6EFE6,stroke:#CBBBAA,color:#2B2B2B,stroke-width:1px;
  classDef decision fill:#EFE5DA,stroke:#CBBBAA,color:#2B2B2B,stroke-width:1px;
  classDef success fill:#D7B46A,stroke:#B89343,color:#FFFFFF,stroke-width:1px;
  classDef neutral fill:#F4F4F4,stroke:#D0D0D0,color:#2B2B2B,stroke-width:1px;

  class A,B,C,A1,B1,C1 step;
  class D,A2,B2,C2 decision;
  class Z success;
  class N1 neutral;
```
