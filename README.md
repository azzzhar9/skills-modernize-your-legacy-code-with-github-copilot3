# Student Accounts COBOL Project Documentation

...existing documentation...

---

## Sequence Diagram: Student Account Data Flow

```mermaid
sequenceDiagram
    participant User
    participant STUDACC.CBL
    participant STUDTRAN.CBL
    participant STUDRPT.CBL
    participant Database

    User->>STUDACC.CBL: Create/Update/Delete Student Account
    STUDACC.CBL->>Database: Store/Retrieve Student Data
    User->>STUDTRAN.CBL: Submit Transaction (Payment/Charge)
    STUDTRAN.CBL->>Database: Update Account Balance
    STUDTRAN.CBL->>STUDACC.CBL: Validate Student Account
    User->>STUDRPT.CBL: Request Account Report
    STUDRPT.CBL->>Database: Query Account Data
    STUDRPT.CBL