

```mermaid
flowchart LR
    A["🌿 feature branch"] -- > B["🛠️ DEV  —  deploy-dev"]       
    B -- > C["🧪 STG  —  deploy-stg"]      
    C --> D["🚀 PROD  —  main"] 
    D --> E["♻️ Rollback  —  Release"]
 



    
