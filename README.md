# E-Health Tabib — Medical Health Management System

A Java desktop application for healthcare management. "Tabib" (طبيب) means "Doctor" in Arabic. The system supports three user roles: patients who record daily health metrics, doctors who monitor their patients, and administrators who manage the medical staff.

## Features

- Role-based access (Patient, Doctor, Administrator)
- Patient health tracking: body temperature (°C), blood pressure (mmHg), weight (kg)
- Custom bar chart visualizations across weeks and days
- Doctor portal: view assigned patients and their health records
- Admin portal: CRUD management for doctor accounts
- Dual database support (PostgreSQL and MySQL)
- Auto-DDL schema provisioning
- In-memory demo mode when no database is available

## Tech Stack

Java SE 21, Java Swing / AWT, SwingX, PostgreSQL, MySQL, JDBC

## Project Structure

```
E-Health-Tabib/
├── README.md
├── LICENSE
├── .gitignore
├── run.bat                  # Windows build & launch script
├── db.properties.example    # Database configuration template
├── schema_postgres.sql      # PostgreSQL schema with seed data
├── icons/                   # GUI image assets
├── lib/                     # JDBC drivers and SwingX library
├── docs/                    # Documentation and legacy files
│   ├── application-screenshots.pdf
│   └── legacy-mysql-schema.sql
└── src/ehealth/             # Java source files
```

## Getting Started

### Prerequisites
- JDK 21+
- PostgreSQL (optional — app works in demo mode without it)

### Database Setup
1. Copy `db.properties.example` to `db.properties`
2. Edit with your database credentials
3. The application auto-creates tables on first run

### Build & Run
- **Windows**: `run.bat`
- **Manual**: `javac -d bin -cp "bin;lib/*" src\ehealth\*.java` then `java -cp "bin;lib/*" ehealth.PreLoginPage`

### Demo Mode
If no database is configured, the app runs with sample data.

## Default Credentials

| Role | Username | Password |
|------|----------|----------|
| Admin | admin | admin |
| Doctor | (register via signup) | — |
| Patient | (register via signup) | — |

## Screenshots

Note that application screenshots are available in `docs/application-screenshots.pdf` (9 pages covering all screens).

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## License

MIT License

## Author

Tayeb Bekkouche — https://github.com/tayebg
