ATB12X API Automation Program

# ATB12x API Automation Programs

This repository contains programs and learning resources focused on API automation using **Rest Assured**. 
It is designed for those who want to build strong foundational knowledge and advance their skills in API testing.

## 📚 What You'll Learn

In this repository, you'll find code and examples covering:

- Basics of Rest Assured
- Making API requests using:
    - `GET`
    - `POST`
    - `PUT`
    - `PATCH`
    - `DELETE`
- Performing full **CRUD** operations
- Writing automated tests with **TestNG**
- Effective API test automation strategies

## 🛠 Technologies Used

- **Java**
- **Rest Assured**
- **TestNG**
- **Maven/Gradle** (as applicable)

## 🚀 Getting Started

1. Clone this repository:

   git clone https://github.com/KiranSableQA/ATB12x-api-automation



Sample Code
🔍 GET Request
@Test
public void testGetUser() 
{
 given()
    .when()
    .get("https://reqres.in/api/users/2")
    .then()
    .statusCode(200)
    .log().all();
}


➕ POST Request
@Test
public void testCreateUser() {
JSONObject request = new JSONObject();
request.put("name", "John");
request.put("job", "Engineer");

    given()
        .header("Content-Type", "application/json")
        .body(request.toString())
        .when()
        .post("https://reqres.in/api/users")
        .then()
        .statusCode(201)
        .log().all();
}

📝 PUT Request
@Test
public void testUpdateUser() {
JSONObject request = new JSONObject();
request.put("name", "John");
request.put("job", "Manager");

    given()
        .header("Content-Type", "application/json")
        .body(request.toString())
        .when()
        .put("https://reqres.in/api/users/2")
        .then()
        .statusCode(200)
        .log().all();
}

🔧 PATCH Request
@Test
public void testPatchUser() {
JSONObject request = new JSONObject();
request.put("job", "Senior Engineer");

    given()
        .header("Content-Type", "application/json")
        .body(request.toString())
        .when()
        .patch("https://reqres.in/api/users/2")
        .then()
        .statusCode(200)
        .log().all();
}

❌ DELETE Request
@Test
public void testDeleteUser() 
{
  given()
    .when()
    .delete("https://reqres.in/api/users/2")
    .then()
    .statusCode(204);
}

Folder Structure (Example)
src
├── test
│   ├── java
│   │   └── com.api.tests
│   │       ├── GetRequestTests.java
│   │       ├── PostRequestTests.java
│   │       ├── PutRequestTests.java
│   │       ├── DeleteRequestTests.java
│   │       └── PatchRequestTests.java
│   └── resources
│       └── testng.xml


