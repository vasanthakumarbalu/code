```mermaid
graph LR
    A[External Users] --> B(Power Pages);
    C[Internal Users] --> D(Model-Driven App);
    E[Custom UI] --> D;
    F[Dataverse] --> D;
    F --> B;
    F --> E;
    D --> E;
    D --> G(Power Automate);
    E --> G;
    G --> H[Microservices/Azure Functions];
    B --> H;
    E --> H;
    H --> I[Azure API Management];
    I --> J[External Systems];
    K[Canvas App] --> E;
    D --> K;
    K --> G;

    subgraph "Power Platform"
        D;
        E;
        G;
        B;
        F;
        K;
    end

    subgraph "Microservices Layer"
        H;
        I;
        J;
    end
