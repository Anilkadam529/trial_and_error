
```mermaid
graph TD
    A[Analyst Creates Ticket] --> B(Backlog - Workload & Prio Board);
    B --> C{Thursday 2 PM Review};
    C -- Important --> D[Ready Status];
    C -- Not Important --> B;
    D --> E{Real Urgency Prioritization};
    E --> D;
    D --> F{Monday Weekly Meeting};
    F -- Available Capacity --> G[Data Engineer Selects Top Ticket(s)];
    G --> H[Data Engineering Work];
    
