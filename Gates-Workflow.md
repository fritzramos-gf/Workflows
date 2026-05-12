```mermaid

flowchart LR
    A[feature branch]
    subgraph  [DEV]
             B[deploy-dev]
    end
    A --> B
         

    B --> C[deploy-stg]      

    C --> D[main] 

    D --> E[Release]









```
 



    
