```mermaid
    graph TD;
    subgraph Landmaster135;
        A[GitHub Actions]
        B(README.md)
    end
    subgraph feed-fetcher app;
        C(<img src='img/zenn.png' width='40' height='40' /><br>Zenn)
    end
    A -->|Step2. Update| B
    A -->|Step1. Install app| C
```

