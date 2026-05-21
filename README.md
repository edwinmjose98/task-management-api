# AI-Powered Task Management API

A task management system with an AI agent that understands natural language commands.

## Tech Stack

**Backend (Spring Boot)**
- Java 17, Spring Boot 3
- Spring Security + JWT Authentication
- PostgreSQL
- Docker
- Swagger UI

**AI Service (Python)**
- LangChain + LangGraph
- OpenAI GPT-4o-mini
- ChromaDB (RAG/Semantic Search)

## Features

- JWT-based authentication
- Full task CRUD via REST API
- Natural language task management via AI agent
- Semantic search over tasks using RAG + ChromaDB

## How It Works
User: "Create a task to review the Q3 report, high priority, due June 15"
↓
LangChain Agent reads intent
↓
Calls create_task() tool
↓
Spring Boot saves to PostgreSQL
↓
AI replies: "Done! Task created with HIGH priority, due June 15"

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/auth/register | Register user |
| POST | /api/auth/login | Login, get JWT |
| POST | /api/tasks | Create task |
| GET | /api/tasks | Get all tasks |
| GET | /api/tasks/{id} | Get task by ID |
| PUT | /api/tasks/{id} | Update task |
| DELETE | /api/tasks/{id} | Delete task |

## Setup

1. Clone the repo
2. Copy `application-example.properties` to `application.properties` and fill in your DB credentials
3. Run `./mvnw spring-boot:run`

## AI Service Setup

See [task-ai-service](https://github.com/edwinmjose98/task-ai-service) for the Python AI agent.