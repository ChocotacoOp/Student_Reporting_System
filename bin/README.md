# Student Management Application

In this application, we can add student ,there marks,semester &  See multiple reports of students.
- Average Percentage of whole class in recent semester
- Average marks of Students in a subject
- Top 2 Consistent Students across all semesters (Maximum average marks) 


# Functionalities
-   Add Student
-   Add subject and number to student
-   Get Average Percentage of whole class in recent semester
- Get Average marks of Students in a subject
- Get top 2 Consistent Students across all semesters (Maximum average marks) 

## Backend Work
-  Proper Exception Handling, and Input Validation
-  Data Stored in the database(mySQL)

## Installation and Run
-   Before running the API server, we should update the database config inside the application.properties file.
-   Update the port number, username and password as per your local database config.
```
server.port=8888
spring.datasource.url=jdbc:mysql://localhost:3306/studentsdb
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.username=root
spring.datasource.password=1234
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.mvc.pathmatch.matching-strategy = ANT_PATH_MATCHER
```

# Tech Stacks

-   Java Core
-   Spring Data JPA
-   Spring Boot
-   Hibernate
-   MySQL


# Backend

## Student Controller

#### POST : /addStudent
```
{
    "studentId": 1,
      "name": "Rajat Santra",
      "fatherName": "Dipak Santra",
      "email": "rajat123@gmail.com",
      "mobileNumber": "9382695437",
      "gender": "MALE"
    
}
```


#### Get : /avarageParcentage
```
{
  "current semester" : 2,
  "Parcentage of hole class" : 65
}
```

#### Get : /avarageParcentageofeachsub/{studentiId}
```
{
  "Name": "Rajat Santra"
  "English" : 71,
  "Math" : 85,
  "Science" : 78
}
```

#### Get : /topperfomer
```
{
  "Rajat" : 85,
  "Santra" : 65
}
```


