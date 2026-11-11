<div align="center">



\# 🎬 ReelTime



\### Discover your next favorite movie.



A modern full-stack movie application built with a React client, a Spring Boot API, and MongoDB-powered movie data.



\[!\[GitHub](https://img.shields.io/badge/GitHub-Repository-181717?logo=github\&logoColor=white)](https://github.com/zynfaria/full-stack-movie-project)

\[!\[React](https://img.shields.io/badge/React-18-61DAFB?logo=react\&logoColor=white)](https://react.dev/)

\[!\[Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1-6DB33F?logo=springboot\&logoColor=white)](https://spring.io/projects/spring-boot)

\[!\[MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?logo=mongodb\&logoColor=white)](https://www.mongodb.com/)

\[!\[Java](https://img.shields.io/badge/Java-20-ED8B00?logo=openjdk\&logoColor=white)](https://www.java.com/)



</div>



\---



\## Overview



ReelTime is a movie discovery app where users can browse a collection of films, view movie details, watch trailers, and submit reviews. The project combines:



\- A React front-end for a cinematic browsing experience

\- A Java + Spring Boot REST API for movie and review management

\- MongoDB for structured data persistence



This repository is designed as a full-stack learning and showcase project, blending UI design with backend functionality.



\---



\## Tech Stack



| Layer | Technology |

| --- | --- |

| Front-end | React 18, React Router, Axios, Bootstrap, Material UI |

| Back-end | Java 20, Spring Boot 3.1, Spring Web |

| Database | MongoDB |

| Build Tools | npm, Maven |

| Environment Config | Java properties + environment variables |



\---



\## Project Structure



```text

full-stack-movie-project/

├── back-end/

│   └── movie-client/

│       └── movie-gold-v1/          # React movie web app

│

├── front-end/

│   └── movies/                     # Spring Boot API

│       └── src/

│           ├── main/

│           └── test/

│

├── README.md

└── .gitignore

```



> Note: The current repo layout places the React client under `back-end/` and the Java backend under `front-end/`.



\---



\## Features



\- Browse a curated movie collection

\- View detailed movie information

\- Watch movie trailers

\- Submit and store user reviews

\- REST API for movie and review operations

\- MongoDB integration for persistent film data



\---



\## Prerequisites



Before you begin, make sure you have:



\- Node.js and npm installed

\- Java 20 installed

\- MongoDB access configured

\- A terminal or IDE with Git support



\---



\## Environment Setup



The backend reads these environment variables for MongoDB connectivity:



```bash

MONGO\_DATABASE

MONGO\_USER

MONGO\_PASSWORD

MONGO\_CLUSTER

```



They are configured in:



```text

front-end/movies/src/main/resources/application.properties

```



Example configuration pattern:



```properties

spring.data.mongodb.database=${MONGO\_DATABASE}

spring.data.mongodb.uri=mongodb+srv://${MONGO\_USER}:${MONGO\_PASSWORD}@${MONGO\_CLUSTER}

```



Make sure to keep your credentials private and do not hardcode them into the repository.



\---



\## Running the Application



\### 1) Start the backend API



```bash

cd front-end/movies

./mvnw spring-boot:run

```



For Windows:



```bash

cd front-end\\movies

mvnw.cmd spring-boot:run

```



The API runs on:



```text

http://localhost:8080

```



\---



\### 2) Start the React client



Open a second terminal:



```bash

cd back-end/movie-client/movie-gold-v1

npm install

npm start

```



The app should run at:



```text

http://localhost:3000

```



The client is set to communicate with the backend at:



```text

http://localhost:8080

```



\---



\## API Endpoints



Base URL:



```text

http://localhost:8080/api/v1

```



| Method | Endpoint | Description |

| --- | --- | --- |

| GET | `/movies` | Get all movies |

| GET | `/movies/{imdbId}` | Get a movie by IMDb ID |

| POST | `/reviews` | Create a review |



Example review request:



```bash

curl -X POST http://localhost:8080/api/v1/reviews \\

&#x20; -H "Content-Type: application/json" \\

&#x20; -d '{"reviewBody":"Great movie and smooth experience!","imdbId":"movie-id"}'

```



\---



\## Common Commands



\### Front-end (React)

```bash

cd back-end/movie-client/movie-gold-v1

npm start

npm test

npm run build

```



\### Back-end (Spring Boot)

```bash

cd front-end/movies

./mvnw test

./mvnw package

./mvnw spring-boot:run

```



\---



\## Future Improvements



\- Add environment example file (`.env.example`)

\- Implement search and filtering

\- Improve form validation for reviews

\- Add more movie detail pages and categories

\- Add production-ready deployment configuration

\- Expand automated test coverage



\---



\## Contributing



Contributions are welcome. If you want to improve the app, open an issue or submit a pull request.



\---



\## License



This project currently does not specify a license. If you plan to share or distribute it publicly, it is recommended to add an open-source license such as MIT.



\---



<div align="center">



Built for movie lovers. 🍿



</div>

