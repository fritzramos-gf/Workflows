

```mermaid
flowchart LR
    markdown["🌿 feature branch"]
        fb_pr["Dev Pull Request\nReview Required"]
    

    subgraph DEV["🛠️ DEV  —  deploy-dev"]
        dev_q["Queue workflow\nRun workflow"]
    end

    subgraph STG["🧪 STG  —  deploy-stg"]
        stg_pr["Deployment/DevOps\nPull Request\nReview Required"]
        stg_q["Queue workflow\nApproval Required\nRun workflow"]
        stg_pr --> stg_q
    end

    subgraph PROD["🚀 PROD  —  main"]
        prod_pr["Deployment/DevOps\nPull Request\nReview Required"]
        prod_q["Queue workflow\nApproval Required\nRun workflow"]
        prod_pr --> prod_q
    end

    subgraph RB["♻️ Rollback  —  Release"]
        rb["Manual trigger\nSelect environment\nQueue workflow\nApproval Required\nRun workflow"]
    end

    FB -->|"merge PR"| DEV
    DEV -->|"merge PR"| STG
    STG -->|"merge PR"| PROD
    PROD -->|"tag release"| RB

    note["📁 Folder: Recommended to organize code for each\nitem into separate folders in the repository\nto maintain a clear structure."]

    style FB fill:#e8f4fd,stroke:#2196F3,color:#000
    style DEV fill:#e8f5e9,stroke:#4CAF50,color:#000
    style STG fill:#fff8e1,stroke:#FF9800,color:#000
    style PROD fill:#fce4ec,stroke:#E91E63,color:#000
    style RB fill:#f3e5f5,stroke:#9C27B0,color:#000
    style note fill:#f9f9f9,stroke:#ccc,color:#555,font-size:11px
