```mermaid

```mermaid
flowchart LR
    A[feature branch] --> B
    subgraph DEV
        B[deploy-dev]
    end
    B --> C[deploy-stg]      
    C --> D[main] 
    D --> E[Release]
```








```
 



    
