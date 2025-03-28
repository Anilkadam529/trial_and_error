
```mermaid
graph TD
    A[Analyst Creates Ticket] --> B["Backlog -\nWorkload &\nPrio Board"];
    B --> C{Thursday 2 PM Review};
    subgraph Thursday Meeting Participants
        C1[Data VP]
        C2[Team Lead]
        C3[Lead Expert]
    end
    C --> D{Important?};
    D -- Yes --> E[Ready Status];
    D -- No --> B;
    E --> F{Real Urgency Prioritization};
    F --> E;
    E --> G{Monday Weekly Meeting};
    subgraph Monday Meeting Participants
        G1[Data Engineers]
    end
    G --> H{Available Capacity?};
    H -- Yes --> I["Select Top Ticket(s)"];
    H -- No --> G;
    I --> J[Data Engineering Work];

    classDef meetingBox fill:#f9f,stroke:#333,stroke-width:2px;
    class C1,C2,C3,G1 meetingBox;
    class B,C,D,E,F,G,H,I,J defaultBox;
