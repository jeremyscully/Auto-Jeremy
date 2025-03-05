# Auto-Jeremy Architecture Diagram

```mermaid
graph TD
    subgraph "User Interface"
        A[Web Dashboard]
    end

    subgraph "API Layer"
        B[API Gateway / Authentication]
    end

    subgraph "Domain Modules"
        C1[SQL Server Module]
        C2[Power BI Module]
        C3[.NET Service Module]
        C4[.NET Web Module]
        C5[DB Admin Module]
        C6[Architecture Docs Module]
    end

    subgraph "Core Services"
        D[Orchestration Engine]
    end

    subgraph "Storage"
        E1[Configuration DB]
        E2[Template Repository]
        E3[Logging Store]
    end

    A --> B
    B --> C1
    B --> C2
    B --> C3
    B --> C4
    B --> C5
    B --> C6
    C1 --> D
    C2 --> D
    C3 --> D
    C4 --> D
    C5 --> D
    C6 --> D
    D --> E1
    D --> E2
    D --> E3
```

This diagram illustrates the high-level architecture of the Auto-Jeremy system, showing the relationships between the different components:

1. **User Interface**: The web dashboard that users interact with
2. **API Layer**: Handles authentication and routes requests to appropriate modules
3. **Domain Modules**: Specialized modules for each technical domain
4. **Core Services**: The orchestration engine that coordinates tasks
5. **Storage**: Various storage services for configuration, templates, and logs