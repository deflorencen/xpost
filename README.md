## Dokumentacja projektu "XPOST"
___
### 1. Temat projektu aplikacji:
Aplikacja webowa realizująca podstawową funkcjonalność tworzenia postów. \
A także możliwość posiadania przez użytkownika własnej przestrzeni
do przechowywania postów.
___
### 2. Opis projektu:
Aplikacja internetowa posiada prosty i przejrzysty interfejs. \
Posiada możliwość autoryzacji, tworzenia i usuwania postów, a także konto osobiste,\
które zawiera tylko posty od właściciela, a także stronę z listą wszystkich postów.
___
### 3. Wymagania funkcjonalne i niefunkcjonalne:
1. [x] Funkcjonalne:
    - możliwość rejestracji i logowania;
    - istniejące konto osobiste ze śledzeniem własnych postów;
    - isuwanie postów stworzonych przez siebie przy autoryzowaniu;
2. [x] Wymagania niefunkcjonalne:
    - plikacja musi zapewniać szybką reakcję na interakcje użytkownika oraz płynne działanie bez opóźnień.
    - dane osobowe użytkowników (takie jak hasła) muszą być  zaszyfrowany;
    - kod aplikacji musi być pisany zgodnie z najlepszymi praktykami programistycznymi;
___
### 4. Odbiorcy:
Aplikacja jest bardzo prosta w obsłudze. Docelową grupą użytkowników są osoby potrzebujące prostej aplikacji dla tworzenia postów.
___
### 5. Schematy i modele:
W projekcie użyta architektura FastAPI.

![Shemat](https://i.imgur.com/JovICtQ.png)
___
### 6. Dokumentacja API, UI:
Cała interakcja pomiędzy klientem a API odbywa się poprzez JSON. Dodatkowo API wykorzystuje podstawową autoryzację. Dlatego prawie wszystkie punkty końcowe są prywatne i działają wyłącznie dla zarejestrowanych i autoryzowanych użytkowników.

- API
    - Router użytkowników — `/users/`

        - `GET /users/` - `[admin only]` - Pobierz wszystkich użytkowników
        - `POST /users/register/`- `[public]` - Zarejestruj nowych użytkowników
        - `POST /users/login/` - `[public]` - Zaloguj się
        - `POST /users/logout/` - `[autorization required]`- Wyloguj użytkowników
    - Artykuły Router -/articles/
        - `GET /articles/` - `[public]` - Zdobądź wszystkie artykuły
        - `GET /articles/by-user/` - `[autorization required]`- Pobierz artykuły według użytkownika
        - `POST /articles/` - `[autorization required]`- Twórz nowe artykuły
        - `DELETE /articles/{article_id}`- `[autorization required]`- Usuń artykuły
- UI
    - Interfejs użytkownika umożliwia dodawanie, edycję, usuwanie oraz postów.
    - Umożliwia rejestracje i autoryzacje.
___
### 7. Uzasadnienie wyboru technologii:
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
