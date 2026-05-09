# Universal-Studios-Colombia
Project Overview
This project involves the creation and management of a NoSQL Data Lake for Universal Studios Colombia's online record store. The primary goal was to design a flexible database architecture using MongoDB to store and manipulate information about musical artists, their albums, and tracks.

Summary of Tasks
- Task 1: Initial Setup: Implementation of the initial database structure and importing the baseline data provided for the record label's catalog.

- Task 2: Data Expansion and Integrity: Adding new musical content to the database while ensuring data integrity. This included standardizing data types (e.g., converting strings to integers for numeric fields) and updating associated metadata.

- Task 3: Data Maintenance and Cleanup: Performing deletion operations to simulate real-world catalog updates. This involved removing specific tracks from each album and deleting an entire collection to manage storage and relevance.

Data Model Structure
The data is organized in collections per artist/album, following a document-oriented model. Each document contains:

- Track Metadata: Title, duration (in seconds), and release year.

- Artist Info: Name and origin.

- Media References: Paths to album cover images stored within the repository.

- Data Consistency: Strict enforcement of types (Int32/Int64 for numbers and Strings for text) to facilitate future data analysis.

Design Decisions
- Collection Strategy: We chose to group documents by artist to optimize query performance for catalog browsing.

- Asset Management: Images are stored in a dedicated directory structure (Fotos_albums/) with paths referenced in the database, ensuring the Data Lake remains lightweight and portable.

- Standardization: During the update phase, we prioritized Data Integrity by using MongoDB's Schema analysis tools to unify numeric formats.

Findings, Challenges, and Lessons Learned
- Findings: We discovered that MongoDB's flexible schema allows for rapid iteration of the catalog, which is essential for a dynamic industry like music.

- Challenges: Managing cross-platform file paths and maintaining repository structure (folders vs. flat files) in GitHub was initially difficult but resolved through consistent naming conventions.

- Lessons Learned: We gained hands-on experience in the ETL (Extract, Transform, Load) process, specifically focusing on data cleaning before analysis in Data Science workflows.

How to Replicate this Exercise
Prerequisites
- MongoDB Compass installed.

- A GitHub account to clone this repository.

Installation & Import
1. Clone the Repository: Download the files from the main, actualizaciones, and eliminaciones branches.

2.Import Data:

- Open MongoDB Compass.

- Create a new database named UniversalStudios.

- Import the JSON files found in the JSON_Actualizados/ folder into their respective collections.

3. Verification: Use the Schema tab in Compass to analyze the data types and ensure integrity.
