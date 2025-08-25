## Sequence Diagram: Student Account Data Flow

```mermaid
sequenceDiagram
    participant User
    participant main.cob
    participant operations.cob
    participant data.cob
    participant Database

    User->>main.cob: Start accounting operation
    main.cob->>operations.cob: Request business logic (e.g., payment, report)
    operations.cob->>data.cob: Access/modify student account data
    data.cob->>Database: Read/write student account records
    operations.cob->>main.cob: Return operation result
    main.cob->>User: