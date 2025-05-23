## Project Documentation: "XPOST"
___
### 1. Project Topic:
A web application that implements basic functionality for creating posts,
as well as providing users with their own space to store posts.
___
### 2. Project Description:
The web application features a simple and user-friendly interface.
It includes functionality for user authentication, creating and deleting posts,
as well as a personal account that displays only the owner's posts,
and a page with a list of all posts.
___
### 3.Functional and Non-functional Requirements:

✅ Functional Requirements:
- Ability to register and log in;
- Existing personal account with tracking of own posts;
- Deletion of user-created posts when authenticated;

✅ Non-functional Requirements:
- Aapplication must provide a fast response to user interactions and operate smoothly without delays;
- Users' personal data (such as passwords) must be encrypted;
- The application code must be written according to best programming practices;
___
### 4. Target Audience:
The application is very easy to use.
The target user group consists of individuals who need a simple tool for creating posts.
___
### 5. Schemas and Models:
The project uses the FastAPI architecture.

![Shemat](https://i.imgur.com/JovICtQ.png)
___
### 6. API and UI Documentation:
All interaction between the client and the API takes place via JSON.
Additionally, the API uses basic authentication.
As a result, almost all endpoints are private and function only for registered and authenticated users.

- API
    - User Router  — `/users/`

        - `GET /users/` - `[admin only]` - Get all users
        - `POST /users/register/`- `[public]` - Register new users
        - `POST /users/login/` - `[public]` -  Log in
        - `POST /users/logout/` - `[autorization required]`- Log out users
    - Artykuły Router -/articles/
        - `GET /articles/` - `[public]` - Retrieve all articles
        - `GET /articles/by-user/` - `[autorization required]`- Retrieve articles by user
        - `POST /articles/` - `[autorization required]`- Create new articles
        - `DELETE /articles/{article_id}`- `[autorization required]`-  Delete articles
- UI
    - The user interface allows adding, editing, and deleting posts.
    - It also supports user registration and authentication.
___
### 7. Justification for Technology Choice:
- Library: React.js, Axios
- Framework: FastAPI
- Database ORM: SQLModel
- ( Based on - SQLAlchemy (2.0.28) )
- ASGI Server: uvicorn (0.29.0)
- Data Validation: Pydantic (2.6.4)
- Dependency Injection: FastAPIs dependency injection mechanism
- Testing Framework: pytest (8.1.1)

Ten stos zapewnia kompleksowy zestaw narzędzi do tworzenia asynchronicznych aplikacji internetowych za pomocą FastAPI, w tym interakcję z bazą danych, sprawdzanie poprawności danych, testowanie i dodatkowe narzędzia do konfiguracji i renderowania szablonów.
___
### 8. Dodatkowe elementy:
- Axios to biblioteka JavaScript, która umożliwia wykonywanie zapytań sieciowych (HTTP) zarówno z poziomu przeglądarki internetowej, jak i środowiska Node.js. Jest to popularne narzędzie wykorzystywane głównie w aplikacjach internetowych do komunikacji z serwerami API.
