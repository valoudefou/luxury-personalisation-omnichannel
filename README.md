 mermaid
flowchart TD
    A[Query catalogue on Centra] --> B[Append custom attributes to each product]
    B --> C[Add Video URLs, Labels, Localised Text per store]
    C --> D[Create store-specific index for each store UK, US]
    D --> E[Push all indexes to Algolia]
    E --> F[Algolia creates a copy of each index]
    F --> G[Algolia replaces live index once ready]
