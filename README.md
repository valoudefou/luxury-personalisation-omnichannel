# Product Index Technical Flowchart

This flowchart shows a simplified technical workflow for updating product indexes and pushing them to AB Tasty. The steps involving AB Tasty are highlighted in blue.

```mermaid
flowchart TD
    %% Main workflow
    A[Fetch catalogue from Centra] --> B[ME+EM act as Middleman Append custom attributes to products]
    B --> C[Add video URLs, labels, localised text per store]
    C --> D[Create store-specific indexes UK, US, etc.]
    D --> E[Push indexes to AB Tasty]
    E --> F[AB Tasty creates copies of indexes]
    F --> G[AB Tasty replaces live indexes]

    %% Annotations
    B -.-> T[Tasty API: Users push product updates]
    D -.-> M[Documentation: Store-specific index guidelines]
    E -.-> N[Maintenance: Monitor index pushes & updates]

    %% Styling for clarity
    classDef api fill:#f9f,stroke:#333,stroke-width:1px;
    classDef doc fill:#ff9,stroke:#333,stroke-width:1px;
    classDef maint fill:#9f9,stroke:#333,stroke-width:1px;
    classDef tasty fill:#9cf,stroke:#333,stroke-width:1px;  %% Highlight AB Tasty steps

    class T api;
    class M doc;
    class N maint;
    class E,F,G tasty;  %% Apply blue highlight to AB Tasty steps
