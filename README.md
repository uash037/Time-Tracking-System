# Bro.Code — Time Tracking System

A planned Java web application for tracking time spent on tasks and viewing daily/task-wise summaries.

**Status:** Planning stage. The architecture and schema are proposals; the Java application and working database connection have not been implemented yet.

## Team
- Team: Bro.Code
- Leader: Ashwani Upadhyay
- Members: Daksh Chaudhary, Mukesh Singh, Biswas Babu

## Planned stack
- Java
- Java Servlets and JSP
- JDBC
- MySQL
- HTML, CSS, JavaScript
- Maven and Apache Tomcat

## Planned features
- User registration/login with session handling
- Create, edit and archive tasks
- Start, pause and stop timers
- Persist time entries in MySQL
- Daily and task-wise reports
- Responsive dashboard and task pages

## Structure
```text
time-tracking-system/
├── README.md
├── database/schema.sql
├── pom.xml
└── src/main/
    ├── java/com/brocode/timetracker/
    │   ├── model/
    │   ├── dao/
    │   ├── service/
    │   ├── servlet/
    │   ├── filter/
    │   └── util/
    └── webapp/
        ├── assets/css/
        ├── assets/js/
        └── WEB-INF/views/
```

## Requirements
Install a JDK compatible with the chosen Servlet/JSP API, MySQL Server, Maven, and a compatible Apache Tomcat version. Use an IDE such as IntelliJ IDEA or Eclipse.

## Database setup
1. Start MySQL.
2. Run `database/schema.sql` in MySQL Workbench or the MySQL CLI.
3. Configure the JDBC URL, username, and password through environment variables or a local config file excluded from Git.
4. Never commit secrets or plaintext passwords.

The schema creates `brocode_time_tracker` with `users`, `tasks`, and `time_entries`.

## Planned run steps
After application code and `pom.xml` are implemented:
1. Clone the repository.
2. Configure local database credentials.
3. Import `database/schema.sql`.
4. Run `mvn clean package`.
5. Deploy the generated WAR to Tomcat.
6. Open the local URL documented by the team.

## Code quality and security
- Separate servlet, service, DAO, model and view responsibilities.
- Use `PreparedStatement` for SQL parameters.
- Hash passwords; never store plaintext passwords.
- Validate inputs on the server.
- Use transactions when needed.
- Exclude credentials, IDE files and build output from Git.
- Test timer calculations, validation and DAO operations.

## Review 1
Presentation includes problem statement, objectives, Java web architecture, workflow, database design, JDBC flow, UI/UX, repository structure, rubric mapping and next steps.
