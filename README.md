# Product Index Technical Flowchart

This flowchart shows a simplified technical workflow for updating product indexes and pushing them to AB Tasty. It highlights the main steps, as well as where API, documentation, and maintenance are involved.

```mermaid
flowchart TD
    %% Main workflow
    A[Fetch catalogue from Centra] --> B[Append custom attributes to products]
    B --> C[Add video URLs, labels, localised text per store]
    C --> D[Create store-specific indexes UK, US, etc.]
    D --> E[Push indexes to AB Tasty]
    E --> F[AB Tasty creates copies of indexes]
    F --> G[AB Tasty replaces live indexes]

    %% Styling for clarity
    classDef api fill:#f9f,stroke:#333,stroke-width:1px;
    classDef doc fill:#ff9,stroke:#333,stroke-width:1px;
    classDef maint fill:#9f9,stroke:#333,stroke-width:1px;

    class T api;
    class M doc;
    class N maint;
