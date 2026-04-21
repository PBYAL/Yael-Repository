flowchart TD
    A([Start]) --> B[Initialize Score = 0]
    B --> C[Display Categories and Questions]
    C --> D[User Selects Category and Value]

    D --> E{Question Already Used?}
    E -- Yes --> C
    E -- No --> F[Display Question]

    F --> G[Get User Answer]
    G --> H{Is Answer Correct?}

    H -- Yes --> I[Add Points]
    H -- No --> J[Subtract Points]

    I --> K[Update Score]
    J --> K

    K --> L[Mark Question as Used]
    L --> M{All Questions Used?}

    M -- No --> C
    M -- Yes --> N[Display Final Score]

    N --> O([End])
