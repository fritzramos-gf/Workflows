

```mermaid
flowchart TD
    A["🌿 feature branch"] -- > B["🛠️ DEV  —  deploy-dev"]
        
    C["🧪 STG  —  deploy-stg"]      
    D["🚀 PROD  —  main"] 
    D["♻️ Rollback  —  Release"]
 



    note["📁 Folder: Recommended to organize code for each\nitem into separate folders in the repository\nto maintain a clear structure."]

    style FB fill:#e8f4fd,stroke:#2196F3,color:#000
    style DEV fill:#e8f5e9,stroke:#4CAF50,color:#000
    style STG fill:#fff8e1,stroke:#FF9800,color:#000
    style PROD fill:#fce4ec,stroke:#E91E63,color:#000
    style RB fill:#f3e5f5,stroke:#9C27B0,color:#000
    style note fill:#f9f9f9,stroke:#ccc,color:#555,font-size:11px
