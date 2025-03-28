
```mermaid
graph TD
    A[Analyst Creates Ticket] --> B(Backlog - Workload & Prio Board);
    B --> C{Thursday 2 PM Review};
    subgraph Thursday Meeting Participants
        C1[Data VP];
        C2[Team Lead];
        C3[Lead Expert];
    end
    C --> D{Important?};
    D -- Yes --> E[Ready Status];
    D -- No --> B;
    E --> F{Real Urgency Prioritization};
    F --> E;
    E --> G{Monday Weekly Meeting};
    subgraph Monday Meeting Participants
        G1[Data Engineers];
    end
    G --> H{Available Capacity?};
    H -- Yes --> I["Data Engineer Selects Top Ticket(s)"];
    H -- No --> G;
    I --> J[Data Engineering Work];
