***I create this server to refresh my Golang knowledge!***

```mermaid
flowchart TB
    %% DevOps Block
    subgraph DevOps
        Docker["Docker"]
        GHA["GitHub Actions"]
        Playwright["Playwright E2E"]
    end

    %% Persistence Block
    subgraph Persistence
        Prisma["Prisma ORM"]
        DB[("PostgreSQL")]
        Prisma --> DB
    end

    %% Data Sources Block
    subgraph DataSources["Data Sources"]
        CG_REST["CoinGecko REST API"]
        CG_WS["CoinGecko WebSocket"]
    end

    %% Browser Block
    subgraph Browser
        UI["React 19 UI"]
        WS_Client["WebSocket Client"]
        WS_Client --> UI
    end

    %% Server Block
    subgraph Server["Next.js Server"]
        SC["Server Components"]
        API["API Routes"]
        Cache["In-Memory Cache"]
        SC --> API
        API --> Cache
    end

    %% AI Pipeline Block
    subgraph AI["AI Pipeline"]
        Quant["Quant Engine<br/>17 Indicators"]
    end

    %% Cross-Component Connections
    UI --> API
    API --> UI
    CG_WS --> WS_Client
    CG_REST --> Prisma
    CG_REST --> API
    AI --> API

    %% Custom Styling
    style Docker fill:#0080ff,stroke:#fff,stroke-width:1px,color:#fff
    style UI fill:#2a081a,stroke:#ff007f,stroke-width:1px,color:#ff007f
    style Quant fill:#12052b,stroke:#5c24ff,stroke-width:1px,color:#a27bff
    style DB fill:#1e4976,stroke:#4193d0,stroke-width:1px,color:#fff
```
