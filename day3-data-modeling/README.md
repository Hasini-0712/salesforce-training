1. Difference Between App, Object, Record, and Field
Ans: In Salesforce, an App is a collection of related tools, tabs, and objects used for a specific business purpose such as managing sales or student data. An Object is like a database table that stores related information. For example, a Student object stores all student details. A Record is a single entry inside an object, such as one student’s information. A Field is a single piece of data inside a record, such as Name, Email, Age, or Phone Number. These components work together to organize and manage data efficiently in Salesforce.
2. Standard vs Custom Objects
Ans: Standard objects are the default objects already provided by Salesforce for common business activities. Examples include Account, Contact, Lead, and Opportunity. These are mainly used in CRM systems. Custom objects are objects created by users according to specific business needs. For example, in a college management system, objects like Student, Faculty, Course, and Department can be created as custom objects. Standard objects support general business operations, while custom objects allow organizations to build systems based on their own requirements.
3. Your College Data Model
Ans: Objects
Student
Faculty
Course
Department
Relationships
One Department can have many Students.
One Department can have many Faculty members.
One Faculty can teach many Courses.
One Course can contain many Students.
Lookup relationships are used because the objects are connected but can still exist independently.
Department
   |
   |---- Student
   |
   |---- Faculty
              |
              |---- Course
4. Formula Fields
Ans: 1. Full Name
This formula field combines First Name and Last Name automatically.
Why should this be calculated automatically?
It saves time and reduces typing mistakes while displaying the complete student name properly.
2. Remaining Seats
Formula: Total Seats - Filled Seats
Why should this be calculated automatically?
The system automatically updates the remaining seats whenever students enroll in a course, improving accuracy.
3. Percentage
Formula: (Obtained Marks / Total Marks) * 100
Why should this be calculated automatically?
Automatic percentage calculation reduces manual work and prevents mathematical errors.
5. Validation Rules
Ans: 1. Email Cannot Be Empty
This validation rule prevents saving student or faculty records without an email address.
What problem does this prevent?
It prevents communication issues caused by missing email information.
2. Student Age Cannot Be Negative
This rule ensures that users cannot enter invalid negative age values.
What problem does this prevent?
It maintains accurate and realistic student information.
3. Course Seats Cannot Exceed Limit
This validation rule blocks users from adding more students than the available seat capacity.
What problem does this prevent?
It prevents overbooking and maintains proper course management.
6. Reflection – Why Structured Enterprise Data Matters
Ans: Structured enterprise data helps companies organize and manage information properly. It improves accuracy, reduces duplicate data, and makes reporting easier. Relationships between objects help businesses connect related information efficiently. Unlike random spreadsheets, structured systems like Salesforce allow companies to store large amounts of data securely and retrieve it quickly. Formula fields and validation rules also help automate calculations and maintain data quality, making business processes faster and more reliable.
