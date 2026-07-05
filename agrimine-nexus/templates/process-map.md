# Process Map — <WF-ID> (BPMN)

| Field | Value |
|-------|-------|
| Process | |
| Related workflow | WF- |
| Notation | BPMN 2.0 |

## Diagram
```mermaid
flowchart TD
    A([Start]) --> B[Step 1]
    B --> C{Decision}
    C -->|Yes| D[Step 2a]
    C -->|No| E[Step 2b]
    D --> F([End])
    E --> F
```

## Swimlanes / roles
## Data objects (ENT-) at each step
## Systems touched (current vs proposed)
## Bottlenecks (cited)
## Evidence
- [SRC-…]
