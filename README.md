# MongoDB Project

This project demonstrates a complete NoSQL workflow from Database creation and schema design, to data insertion, indexing, manipulations, aggregations and optimization - using **MongoDB Compass** and **PyMongo** in Python.

---

## Project Highlights

- NoSQL schema design
- Data modeling and insertion
- Index creation
- CRUD operations
- Advanced querying and filtering
- Aggregation pipelines
- Query Optimization

---

## Built With

| Tool            | Purpose                         |
|:----------------|--------------------------------:|
| MongoDB         | NoSQL database                  |
| MongoDB Compass | GUI for database management     |
| PyMongo         | Python-MongoDB driver           |
| Python          | Scripting language              |

---

## Project Workflow

### Step 1: Connecting with PyMongo
Connected using the following connection string:
```python
from pymongo import MongoClient
client = MongoClient('mongodb://localhost:27017/')
# Create and use the database
db = client['eduhub_db']
```

### Step 2: Database Design & Data Collections
- Created and designed the following collections with schema:
  - users
  - courses
  - lessons
  - assignments
  - submissions
  - enrollments

### Step 3: Data Insertion
- Created and inserted sample data into all collections.
- Populated:
  - Users (students and instructors)
  - Courses
  - Enrollments
  - Lessons
  - Assignments and submissions
 
### Step 4: Indexing
Created indexes to improve performance and avoid duplicates:
- Unique index on `userId`, `email`, `CourseId`, `enrollmentId`, `lessonId`, `assignemtId` and `submissionId`
 
### Step 5: The Basic CRUD Operations

#### Create Operations
- Added a new user
- Created a new course
- Enrolled a new student
- Added a new lesson to an existing course

#### Read Operations
Queried for:
- All active students
- Course details with instructor info
- All courses by category
- Students enrolled in a specific course
- Courses using title _(partial match)_

#### Update Operations
- Updated a user's profile information
- Marked courses as published
- Updated assignment grades
- Added tags to an existing course

#### Delete Operations
Deleted:
- A user by setting isActive to false
- An enrollment record
- A lesson from a course

### Step 6: Complex Queries
Filtered:
- Courses within a price range
- Users by registration date range
- Courses with specific tags using _$in operator_
- Assignments with specific due dates

### Step 7: Aggregation Pipelines
Created aggregation pipelines for:
- Course enrollment statistics
- Student performance analysis
- Instructor course/activity summary

### Step 8: Query Optimization
- Identified slow queries using _.explain()_
