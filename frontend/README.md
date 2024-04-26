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
![Shemat](https://raw.githubusercontent.com/Bohdan-Orlyk/ZHEKAS_REST_FASTAPI/main/api_diagram.drawio.png?token=GHSAT0AAAAAACQYPIBTAA575FUJ34KFRDS2ZRI4WOA)
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
  - Interfejs użytkownika umożliwia dodawanie, edycję, usuwanie oraz oznaczanie zadań jako wykonane.
  - Umożliwia wygodną interakcję użytkownika z aplikacją za pomocą przeglądarki internetowej.
___
Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more
information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will
remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right
into your project so you have full control over them. All of the commands except `eject` will still work, but they will
point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you
shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't
customize it when you are ready for it.

## Learn More

You can learn more in
the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved
here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved
here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved
here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved
here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved
here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved
here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
