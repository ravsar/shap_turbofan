graph LR
    %% --- Style Definitions for a Stylized Look ---
    classDef dataNode fill:#d1e8e2,stroke:#4a7c59,stroke-width:2px,color:#263d31
    classDef traditionalNode fill:#e6f0ff,stroke:#6a8eae,stroke-width:2px,color:#2a3b4c
    classDef aiNode fill:#e8d9f3,stroke:#7d5a94,stroke-width:2px,color:#3c2a47
    classDef compareNode fill:#fdebd0,stroke:#c39d6f,stroke-width:2px,color:#5b4831
    classDef insightNode fill:#ffdde5,stroke:#c06c84,stroke-width:2px,color:#5c333f

    %% --- Panel 1: Input Data ---
    A[("📊<br/><b>1. Input Data</b><br/><small>CMAPSS FD002 Sensor Signals<br/>+ Z-Score Normalization <br/>+ Health Index</small>")]:::dataNode

    %% --- Panel 2: Dual Analysis Pathways ---
    subgraph 2\. Dual Analysis
        direction TB
        B["🛠️<br/><b>Traditional Metrics</b><br/><small>Monotonicity, <br/>Trendability,<br/>Prognosability</small>"]:::traditionalNode
        C["🤖<br/><b>ML + Explainable AI</b><br/><small>Random Forest, <br/>Gradient Boosting<br/>+ SHAP Analysis</small>"]:::aiNode
    end

    %% --- Panel 3: Comparison & Synthesis ---
    D{{"⚖️<br/><b>3. Synthesis & Diagnosis</b><br/><small>Comparing ex-ante metrics<br/>with post-hoc explanations</small>"}}:::compareNode

    %% --- Panel 4: Key Insight & Conclusion ---
    E(("<br/>💡<br/><b>4. Key Insight</b><br/><small>SHAP resolves ambiguities in metrics, revealing the model's <br/>true logic and <br/>vulnerabilities.<br/> </small>")):::insightNode

    %% --- Workflow Connections with Descriptive Labels ---
    A -- "Ex-Ante Feature<br/>Screening" --> B
    A -- "Model Training &<br/>Post-Hoc Explanation" --> C
    B --> D
    C --> D
    D -- "Derive<br/>Conclusions" --> E
