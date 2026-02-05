# Technical Product Index Flowchart

This flowchart describes the detailed technical workflow for querying the catalogue, enhancing products with custom attributes, creating store-specific indexes, and pushing them to AB Tasty. It also shows where the Tasty API, documentation, and maintenance are involved.

```mermaid
flowchart TD
    %% Data source
    A[Centra Catalogue] --> B[Fetch product data]

    %% Data processing
    B --> C[Append custom attributes]
    C --> C1[Add video URLs]
    C --> C2[Add labels]
    C --> C3[Add localised text per store]

    %% Store-specific branching
    C1 --> D1[Create UK index]
    C2 --> D2[Create US index]

    %% Push to AB Tasty
    D1 --> E1[Push UK index to AB Tasty]
    D2 --> E2[Push US index to AB Tasty]

    %% AB Tasty processing
    E1 --> F1[AB Tasty creates copy of UK index]
    E2 --> F2[AB Tasty creates copy of US index]
    F1 --> G1[AB Tasty replaces live UK index]
    F2 --> G2[AB Tasty replaces live US index]

    %% Annotations
    C -.-> T[Tasty API: Users push product updates]
    D1 -.-> M[Documentation: Guides for creating store-specific indexes]
    D2 -.-> M
    E1 -.-> N[Maintenance: Monitor index pushes and AB Tasty updates]
    E2 -.-> N

    %% Optional styling
    classDef api fill:#f9f,stroke:#333,stroke-width:1px;
    classDef doc fill:#ff9,stroke:#333,stroke-width:1px;
    classDef maint fill:#9f9,stroke:#333,stroke-width:1px;

    class T api;
    class M doc;
    class N maint;
