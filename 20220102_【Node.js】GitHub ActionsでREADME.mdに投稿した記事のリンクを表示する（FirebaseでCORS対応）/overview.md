```meramaid
graph TD;
    subgraph dev environment;
        I[fab:fa-apple Macbook]
        J[fab:fa-docker Docker]
    end
    subgraph Firebase;
        K[<img src='https://simpleicons.org/icons/firebase.svg' width='20' /><br>Firebase-tools]
        L(<img src='https://simpleicons.org/icons/googlecloud.svg' width='20' /><br>cloud functions)
    end
    subgraph Landmaster135;
        A[fab:fa-github GitHub Actions]
        B(README.md)
    end
    subgraph feed-fetcher: app;
        C[fab:fa-node feed-fetch]
    end
    subgraph target sites;
        D(<img src='https://simpleicons.org/icons/zenn.svg' width='20' /><br>Zenn)
        E(<img src='https://simpleicons.org/icons/qiita.svg' width='20' /><br>Qiita)
        F(<img src='https://simpleicons.org/icons/wordpress.svg' width='20' /><br>WordPress)
        M(<img src='https://simpleicons.org/icons/wordpress.svg' width='20' /><br>note)
    end
    style D fill:#ffffff,color:#000000,stroke:#000000,stroke-width:2
    style E fill:#ffffff,color:#000000,stroke:#000000,stroke-width:2
    style F fill:#ffffff,color:#000000,stroke:#000000,stroke-width:2
    style K fill:#ffffff,color:#000000,stroke:#000000,stroke-width:2
    style L fill:#ffffff,color:#000000,stroke:#000000,stroke-width:2
    style M fill:#ffffff,color:#000000,stroke:#000000,stroke-width:2
    A -->|Step2. Update| B
    A -->|Step1. Install app| C
    C -->|GET| D
    D -->|Response <br>with feed|C
    C -->|GET| E
    E -->|Response <br>with feed|C
    C -->|GET| F
    F -->|Response <br>with feed|C
    C -->|GET| L
    L -->|Response <br>with feed|C
    L -->|GET| M
    M -->|Response <br>with feed|L
    C -->|clone| I
    I -->|build &<br> copy source| J
    J -->|test source| I
    I -->|command<br>to deploy|K
    I -->|push| C
    K -->|deploy<br>functions| L
```
