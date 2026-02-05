```flowchart TD
    A[Query catalogue on Centra] --> B[Append custom attributes to each product]
    B --> C[Add video URLs, labels, localised text per store]
    C --> D[Create store-specific index for each store: UK / US]
    D --> E[Push all indexes to AB Tasty]
    E --> F[AB Tasty creates a copy of each index]
    F --> G[AB Tasty replaces live index once ready]

    %% Additional annotations
    B -.-> T[Tasty API: Needed for users to push product updates]
    D -.-> M[Documentation: Guides for creating store-specific indexes]
    E -.-> N[Maintenance: Monitor index pushes and AB Tasty updates]

    %% Optional styling for emphasis
    classDef api fill:#f9f,stroke:#333,stroke-width:1px;
    classDef doc fill:#ff9,stroke:#333,stroke-width:1px;
    classDef maint fill:#9f9,stroke:#333,stroke-width:1px;

    class T api;
    class M doc;
    class N maint;```
