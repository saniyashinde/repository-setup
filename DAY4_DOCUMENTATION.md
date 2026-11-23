\#Docker Compose Infrastructure Setup



\## 1. Objective

The objective of Day 4 was to containerize the frontend and backend applications and configure the required infrastructure services using Docker Compose.



\## 2. Technologies Used

\- Docker

\- Docker Compose

\- React + Vite

\- FastAPI

\- MongoDB

\- ChromaDB

\- Ollama



\## 3. Docker Services



Five services were configured in the `docker-compose.yml` file.



| Service | Purpose |

|---|---|

| Frontend | Serves the React application |

| Backend | Runs the FastAPI application |

| MongoDB | Stores original uploaded files and metadata |

| ChromaDB | Stores text chunks and embeddings |

| Ollama | Runs the local LLM service |



\## 4. Docker Configuration



\- Created a Dockerfile for the frontend.

\- Created a Dockerfile for the backend.

\- Created `.dockerignore` files.

\- Configured all five services in `docker-compose.yml`.

\- Configured a Docker bridge network named `rag-network`.

\- Configured persistent Docker volumes for MongoDB, ChromaDB and Ollama.

\- Added healthchecks to monitor service status.

\- Configured service dependencies using `depends\_on`.

\- Used environment variables for configuration and credentials.



\## 5. Port Configuration



| Service | Port |

|---|---|

| Frontend | 8081 |

| Backend | 8000 |

| MongoDB | 27018 |

| ChromaDB | 8000 (internal) |

| Ollama | 11434 (internal) |



\## 6. Testing Performed



Executed the following commands:



```powershell

docker compose config --quiet

docker compose up -d

docker compose ps

docker compose logs chromadb --tail=100

```



Frontend URL:

http://localhost:8081



Backend health endpoint:

http://localhost:8000/health



Backend health response:



```json

{

&#x20; "status": "healthy"

}

```



\## 7. Final Result



All five Docker containers started successfully.



\- MongoDB – Healthy

\- ChromaDB – Healthy

\- Backend – Healthy

\- Frontend – Healthy

\- Ollama – Healthy



The frontend and backend were tested successfully. Docker

