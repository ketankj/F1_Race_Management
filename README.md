# Formula 1 Race Management Database

## Project Description
A comprehensive database management system designed to manage Formula 1 racing data, including entities like Races, Drivers, Teams, Results, Seasons, and Race Sessions. This system facilitates data storage, historical record-keeping, and supports analysis for the Formula 1 community.

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Assumptions](#assumptions)
4. [Entities and Relationships](#entities-and-relationships)
5. [Database Schema and Normalization](#database-schema-and-normalization)
6. [Queries](#queries)
7. [Observations](#observations)
8. [Conclusion](#conclusion)
9. [Contributors](#contributors)

## Introduction

This project, created as part of the CPS 542 Database Management Systems course, manages detailed data associated with Formula 1 racing. The database encompasses entities like Races, Drivers, Teams, Results, Seasons, and Race Sessions, capturing essential information about each entity and the relationships between them. This centralized Formula 1 database enables efficient data management and serves as a robust tool for record-keeping and analytics within the F1 community.

## Project Structure

The project is structured into the following sections:

- **Entities, Attributes, and Keys**: Detailed list of entities, their attributes, and primary/foreign keys.
- **ER Diagram**: Visual representation of entities and their relationships.
- **Relational Schema**: Outline of the database schema for implementation.
- **Normalization**: Database normalization to third normal form (3NF) and Boyce-Codd Normal Form (BCNF) where applicable.
- **SQL Queries**: SQL statements for creating tables, inserting data, and querying the database for analytical insights.

## Assumptions

1. Race durations are measured in minutes (e.g., 120).
2. Circuit lengths are represented in miles.
3. The dataset is for the 2022 Formula 1 season.
4. Season champions are determined by individual driver performance.
5. Only the top two race finishers receive points (25 for the winner, 18 for the runner-up).
6. Teams earn points based on top finishes by drivers.
7. The highest team score designates the team champion; the highest individual score designates the individual champion.

## Entities and Relationships

### Key Entities

1. **Race**: Includes race names, dates, locations, and circuit information.
2. **Driver**: Attributes such as nationality, name, team association, and total individual score.
3. **Team**: Team name, principal details, and team score.
4. **Results**: Driver positions and points earned per race.
5. **Season**: Annual season record with team and individual winners.
6. **RaceSession**: Tracks race sessions, including duration and any changes in duration.

### Relationships

- **One-to-Many** (e.g., one season hosts multiple races).
- **Many-to-Many** (e.g., drivers participate in multiple races, and races involve multiple drivers).
- **One-to-One** (e.g., each race has a unique race session).

## Database Schema and Normalization

The database schema is normalized to maintain data integrity and reduce redundancy:

- **1NF and 2NF**: Ensured atomic values and removed partial dependencies.
- **3NF**: Eliminated transitive dependencies by creating new relations.
- **BCNF**: Where applicable, all non-key attributes depend solely on candidate keys.

### Sample Functional Dependencies and Tables

1. **Race**: `Race_Name` → `{Date, State, Country, Circuit_Name, Year}`
2. **Drivers**: `Driver_ID` → `{Nationality, Name, Total_ind_score, Team_Name, Year}`
3. **Team**: `Team_Name` → `{Principal Name, Team_Score, Year}`

## Queries

### Sample Queries

- **CREATE**: SQL statements for creating tables like `Race`, `Driver`, `Team`, and `Result`.
- **INSERT**: Insertion of initial data, including attributes for each entity.
- **SELECT**: Analytical queries using joins, where clauses, and aggregate functions.

#### Examples:

1. **JOIN Query**: Display results by joining `Driver` and `Team`.
2. **Grouping**: Aggregate race data by country.
3. **Sorting**: Order circuits by length.

## Observations

This project required significant domain understanding of Formula 1, impacting initial design decisions and guiding schema adjustments. Through teamwork and expert guidance, the project evolved, fostering an appreciation for collaborative database design. The ER diagram adjustments, including combining circuit attributes with race data, highlighted real-world challenges in database development.

## Conclusion

The Formula 1 Race Management Database was an insightful project, enhancing our understanding of database principles and teamwork. The dynamic schema redesign process, collaboration with experts, and practical application of design theories provided valuable experience in managing a real-world dataset for Formula 1 racing.

## Contributors

- **Hava Saivedant** (Team Leader)
- **Sheldon Daniel**
- **Ketan Joshi**
- **Spoorthi Bojja**
- **Anant Chanchad**

---

