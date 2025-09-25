# Campus-Course-Records-Manager
CCRM is a console-based Java SE application that enables educational institutions to manage students, courses, enrollments, and grades. It supports GPA calculation, transcript generation, CSV import/export, backups, Lambdas and reports using Streams and NIO.2, while demonstrating OOP, design patterns, exceptions, and modern Java features.


Key Features Include :

CLI-based interactive menu
Student & Course Management
Enrollment and Grade Recording
GPA Calculation & Transcript Generation
CSV Import/Export and Backup Utilities
Reports using Streams & Filtering

How to Run?
Required JDK Version : Java SE 17 or above

# Compile all source files
javac -d out $(find src -name "*.java")
# Run the program
java -cp out src.edu.ccrm.cli.Main
# Run with assertions enabled
java -ea -cp out src.edu.ccrm.cli.Main


Evolution of JAVA

1995 – Java 1.0 by Sun Microsystems (“Write Once, Run Anywhere”)

1998 – Java 2: J2SE, J2EE, J2ME platforms introduced

2004 – Java 5 adds generics, annotations, enhanced for-loops

2014 – Java 8 introduces Lambdas, Streams, Date/Time API

2017 – Java 9 introduces modularity and JShell

2021+ – Modern Java adds records, pattern matching, virtual threads


Java ME vs SE vs EE Comparison

Feature	Java ME (Micro)	Java SE (Standard)	Java EE / Jakarta EE (Enterprise)

Target Platform :	Embedded & Mobile |	Desktops & Console |Servers & Cloud Applications
APIs : Lightweight subset	| Core Java Libraries | Adds Servlets, JSP, JPA, etc.
Use Cases : IoT, feature phones	Standalone apps (like ARM)	Banking, e-commerce, enterprise
Example :	IoT devices |	Campus-Course-Records-Manager |	Spring / Jakarta EE Web Apps

The Campus-Course-Records-Manager uses Java SE as it is a console-based desktop application.


JDK, JRE, JVM 

JDK (Java Development Kit): Full toolkit for Java developers (compiler, libraries, JRE).

JRE (Java Runtime Environment): Includes JVM and libraries needed to run Java programs.

JVM (Java Virtual Machine): Executes bytecode by converting it into machine code at runtime.


Workflow:

Source Code (.java) → [JDK Compiler javac] → Bytecode (.class)  
Bytecode → [JVM in JRE] → Machine Code → Execution


Install & SetUp Java on Windows

Steps:
1. Download JDK from Oracle or OpenJDK.
2. Install and set JAVA_HOME in Environment Variables.
3. Add %JAVA_HOME%\bin to the PATH.
4. Verify installation:

java -version
javac -version



Eclipse Setup Steps

1. Open Eclipse IDE → File > New > Java Project
2. Enter project name: Campus-Course-Records-Manager
3. Create src/ and package structure.
4. Right-click Main.java → Run As → Java Application

Syllabus Topic	File/Class/Method

Encapsulation : Student.java, Course.java (private fields + getters/setters)
Inheritance	: Person.java → Student.java, Instructor.java
Abstraction	: Person.java (abstract class)
Polymorphism :	TranscriptService.java, toString() overrides
Interfaces : StudentService.java, CourseService.java
Streams & Lambdas	CourseServiceImpl.java, ReportService.java
Enums	Semester.java, Grade.java
Singleton	AppConfig.java, DataStore.java
Builder	Course.Builder
Custom Exceptions : DuplicateEnrollmentException.java, MaxCreditLimitExceededException.java
File I/O (NIO.2)	ImportExportService.java, BackupService.java
Recursion	FileUtil.java (recursive directory size)
Assertions	Course.Builder, Student.java



Sample Data Files : students.csv , courses.csv, instructors.csv
Import Data:
java -cp out src.edu.ccrm.cli.Main --import data/students.csv


Project Structure

CAMPUS-COURSE-AND-RECORDS-MANAGER
├─ src/
│  └─ edu/
│     └─ ccrm/
│        ├─ cli/              # Command-line interface classes (main entry points, CLI parsers)
│        ├─ config/           # Configuration files, environment settings, constants
│        ├─ exceptions/       # Custom exception classes
│        ├─ model/            # enums / interfaces / value/ entities
│        ├─ service/          # Logic and service classes
│
├─ data/
│  ├─ backups/                # Backup data files
│  └─ exports/                # Exported results, reports, etc.
│
├─ data_test/                 # Courses, Instructors and Students sample CSV files
├─ README.md
├─ USAGE.md
└─ .gitignore
