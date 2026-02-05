# Product Index Technical Flowchart

This flowchart shows a simplified technical workflow for updating product indexes and pushing them to AB Tasty. The steps involving AB Tasty are highlighted in blue.

```mermaid
flowchart TD
    %% Main workflow
    A[Fetch catalogue from Centra] --> B[Append custom attributes to products]
    B --> C[Add video URLs, labels, localised text per store]
    C --> D["Create store-specific indexes - UK / US"]
    D --> E[Push indexes to AB Tasty]
    E --> F[AB Tasty creates copies of indexes]
    F --> G[AB Tasty replaces live indexes]

    %% Styling for clarity
    classDef api fill:#f9f,stroke:#333,stroke-width:1px;
    classDef doc fill:#ff9,stroke:#333,stroke-width:1px;
    classDef maint fill:#9f9,stroke:#333,stroke-width:1px;
    classDef tasty fill:#9cf,stroke:#333,stroke-width:2px;  %% Highlight AB Tasty steps

    %% Assign classes individually
    class T api;
    class M doc;
    class N maint;
    class E tasty;
    class F tasty;
    class G tasty;
