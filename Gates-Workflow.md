```mermaid
flowchart LR
    A[feature branch] ----> B
    subgraph DEV
        B[deploy-dev]
    end
    B ----> C
    subgraph STG
        C[deploy-stg]
    end
    
    C ----> D[main] 
    D ----> E[Release]









```
 



    
