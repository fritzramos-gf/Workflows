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
    
    C ----> D
    subgraph PROD
        D[main]
    end

    D ----> E
    subgraph ROLLBACK
         E[Release]
    end









```
 



    
