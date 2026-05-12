Standard Git Ops

```mermaid
flowchart LR
    A[Step 1: Developer] --> B[Step 2: Feature Branch]
    B --> C[Step 3: Pull Request]
    C --> D{Step 4: 🔍 AI Agent<br>Code Review & Security Scan}

    D -->|Clean| E[Step 6: CI / Automated Tests]
    D -->|Issues Found| F[Step 5: Request Changes / Auto-Comment]
    F --> D

    E -->|Fail| F
    E -->|Pass| G[Step 7: 👤 Human Approval #1]

    G -->|Approve & Merge| H[⭐ STEP 8: MAIN BRANCH<br>Single Source of Truth]

    H --> I[Step 9: GitOps Agent Detects Change]
    I --> J[Step 10: Deploy to Staging]
    J --> K{Step 11: Staging T
    ests}

    K -->|Fail| L[Step 12: Rollback / Fix]
    L --> K

    K -->|Pass| M[Step 13: 👤 Human Approval #2]
    M --> N[Step 14: GitOps Agent Sync to Production]
    N --> O[Step 15: 🚀 Production Environment]

    classDef blue fill:#1e88e5,stroke:#fff,color:#fff,rx:10
    classDef orange fill:#f57c00,stroke:#fff,color:#fff,rx:10
    classDef gray fill:#455a64,stroke:#90a4ae,color:#fff,rx:10

    class D,G,M blue
    class H orange
    class A,B,C,E,F,I,J,K,L,N gray
    class O green

