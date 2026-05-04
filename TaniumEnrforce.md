Tanium Enforce Policy Workflow


```mermaid
flowchart TD
    A[Step 1: Developer] --> B[Step 2: Feature Branch]
    B --> C[Step 3: Pull Request]
    C --> D{Step 4: 🔍 AI Agent Code Review & Security Scan}

    D -->|Clean| E[Step 6: CI / Automated Tests]
    D -->|Issues Found| F[Step 5: Request Changes / Auto-Comment]
    F --> D

    E -->|Fail| F
    E -->|Pass| G[Step 7: 👤 Human Approval #1]

    G -->|Approve & Merge| H[⭐ STEP 8: MAIN BRANCH<br>Single Source of Truth - Policy as Code]

    H --> I[Step 9: GitOps Agent Detects Change]
    I --> J[Step 10: Create/Update Policy in Tanium Enforce]
    J --> K[Step 11: Target Computer Groups]
    K --> L[Step 12: Schedule Enforcement]
    L --> M[Step 13: Initial Enforcement]
    M --> N{Step 14: Verify Policy Settings}
    N --> O[Step 15: Verification Outcome]

    O -->|Failed/Incomplete| P[Step 16: Auto-Retry]
    P --> N

    O -->|Success| Q[Step 17: Monitor Compliance]

    Q -->|Issues Detected| R[Step 18: Auto-Remove / Rollback]
    R --> N

    Q -->|Compliant| S[Step 19: 👤 Human Approval #2]
    S --> T[Step 20: Expand Target Groups]
    T --> U[Step 21: ✅ Policy Fully Enforced Across Production]

    classDef blue fill:#1e88e5,stroke:#fff,color:#fff
    classDef orange fill:#f57c00,stroke:#fff,color:#fff
    classDef red fill:#e53935,stroke:#fff,color:#fff
    classDef gray fill:#37474f,stroke:#90a4ae,color:#fff

    class D,G,J,N,O,Q,S blue
    class H orange
    class P,R red
    class A,B,C,E,F,I,K,L,M,T gray
    class U green
