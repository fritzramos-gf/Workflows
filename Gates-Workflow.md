```mermaid
flowchart LR
    A[feature branch] ----> B
    A ~~~ C["Dev\nPull Request\nReview Required"]
    C ~~~ B
    subgraph DEV
        B[deploy-dev]
    end
     C ~~~ G["Queue workflow
        \nRun workflow"]

    B ---> D
    G ~~~ H["Deployment/DevOps\nPull Request\nReview Required"]
    H ~~~ D
    subgraph STG
        D[deploy-stg]
    end
    D ---> E
    H ~~~ I["Queue workflow\nApproval Required\nRun workflow"]
    subgraph PROD
        E[main]
    end
    I ~~~ J["Queue workflow\nApproval Required\nRun workflow"]
    E ---> F
    J ~~~ K["Deployment/DevOps\nPull Request\nReview Required"] 
    subgraph ROLLBACK
        F[Release]
    end
    K ~~~ L["Manual trigger\nSelect environment\nQueue workflow\nApproval Required\nRun workflow"]
    









```
 



    
