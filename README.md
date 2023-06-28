<h1 align = "center"> Doctor-Patient Management System </h1>

<p align="center">
<a href="Java url">
    <img alt="Java" src="https://img.shields.io/badge/Java->=8-darkblue.svg" />
</a>
<a href="Maven url" >
    <img alt="Maven" src="https://img.shields.io/badge/maven-3.0.5-brightgreen.svg" />
</a>
<a href="Spring Boot url" >
    <img alt="Spring Boot" src="https://img.shields.io/badge/Spring Boot-3.0.6-brightgreen.svg" />
</a>
  </p>

* This is a backend application for a Doctor-Patient management system. It provides APIs to add doctors, add patients with their symptoms, and suggest doctors based on patient's symptoms and location.

## Technologies Used
* Java
* Spring Boot
* Hibernate





## Database Configuration
* To connect to a MySQL database, update the application.properties file with the appropriate database URL, username, and password. The following properties need to be updated:
```
spring.datasource.driverClassName=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/doctor_patient_db
spring.datasource.username=<your_database_username>
spring.datasource.password=<your_database_password>
spring.jpa.show-sql = true
spring.jpa.hibernate.ddl-auto = update

spring.jpa.properties.hibernate.show_sql=true
spring.jpa.properties.hibernate.use_sql_comments=true
spring.jpa.properties.hibernate.format_sql=true

```

>## Data flow
In this project, we have four layers-
* **Controller** - The controller layer handles the HTTP requests, translates the JSON parameter to object, and  the request and transfer it to the business (service) layer. In short, it consists of views i.e., frontend part.
* **Service** -The business layer handles all the business logic. It consists of service classes and uses services provided by data access layers.
* **Repository** - This layer mainatains the CRUD operations are performed
* **Model** - This layer consists basically the class level things- the various classes required for the project and these classes consists the attributes to be stored.

>## API Endpoints

### Adding a Doctor
* Endpoint: POST /api/doctors
* Request Body: JSON representing the doctor details
* Example:

```
{
  "id": 1,
  "name": "Rushi nagare",
  "city": "nashik",
  "email": "rushi@gmail.com",
  "phoneNumber": "8788514199",
  "speciality": "ORTHOPEDIC"
}

```

### Adding a Patient
* Endpoint: POST /api/patients
* Request Body: JSON representing the patient details
* Example:
```
{
  "id": 1,
  "name": "pallavi",
  "city": "nashik",
  "email": "pallavi@gmail.com",
  "phoneNumber": "6767545678",
  "symptom": "LEG_PAIN"
}

```

## Project Summary
The Doctor-Patient Management System is a backend application designed to facilitate the management of doctors and patients in a healthcare setting.
The system provides various APIs to add doctors, 
add patients with their symptoms, and suggest doctors based on patient symptoms and location.
