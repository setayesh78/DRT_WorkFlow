```mermaid
graph TD;
    User[User] --> |Submits Request| Django;
    Django --> |Fetches Questionnaires| GitHub;
    Django --> |Reads Data| PostgreSQL;
    Django --> |Sends Data to| PostgreSQL;
    Django --> |Updates/Stores Files| GitHub;
    Django --> |Stores Metadata| GitHub;

    subgraph "DRT System"
        Django
        PostgreSQL
    end

    subgraph "DRT Data Store"
        GitHub
    end
