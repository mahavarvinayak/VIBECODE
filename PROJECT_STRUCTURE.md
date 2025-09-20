# VIBECODE Platform - Complete Project Structure

This document outlines the complete directory and file structure for the VibeCode platform, a dynamic code generation platform with AI integration.

## Project Overview

VibeCode is a full-stack TypeScript platform that combines React frontend with Node.js backend, AI integration, and comprehensive tooling for code generation and live preview.

## Directory Structure

```
vibecode-platform/
│
├── package.json              # Root workspace configuration
├── tsconfig.json            # Root TypeScript configuration
├── README.md                # Project documentation
├── PROJECT_STRUCTURE.md     # This file
│
├── frontend/                # React TypeScript frontend
│   ├── package.json         # Frontend dependencies (React, Vite, etc.)
│   ├── tsconfig.json        # Frontend TypeScript config
│   ├── vite.config.ts       # Vite configuration
│   ├── index.html           # Main HTML entry point
│   │
│   ├── public/              # Static assets
│   │   ├── favicon.ico
│   │   ├── logo.svg
│   │   └── manifest.json
│   │
│   ├── src/
│   │   ├── main.tsx         # Application entry point
│   │   ├── App.tsx          # Main application component
│   │   ├── index.css        # Global styles
│   │   │
│   │   ├── pages/           # Page components
│   │   │   ├── index.tsx    # Home page
│   │   │   ├── project/
│   │   │   │   └── [id].tsx # Dynamic project page
│   │   │   └── auth/        # Authentication pages
│   │   │       ├── login.tsx
│   │   │       └── register.tsx
│   │   │
│   │   ├── components/      # Reusable UI components
│   │   │   ├── PromptBox.tsx     # AI prompt input component
│   │   │   ├── CodeEditor.tsx    # Monaco code editor wrapper
│   │   │   ├── LivePreview.tsx   # Live code preview component
│   │   │   ├── Sidebar.tsx       # Navigation sidebar
│   │   │   ├── Header.tsx        # App header
│   │   │   ├── Footer.tsx        # App footer
│   │   │   └── common/           # Common UI components
│   │   │       ├── Button.tsx
│   │   │       ├── Modal.tsx
│   │   │       └── Loader.tsx
│   │   │
│   │   ├── hooks/           # Custom React hooks
│   │   │   ├── useAuth.ts   # Authentication hook
│   │   │   ├── useAPI.ts    # API interaction hook
│   │   │   ├── useWebSocket.ts   # WebSocket hook
│   │   │   └── useCodeGeneration.ts  # Code generation hook
│   │   │
│   │   ├── context/         # React context providers
│   │   │   ├── AuthContext.tsx   # User authentication context
│   │   │   ├── ThemeContext.tsx  # UI theme context
│   │   │   └── ProjectContext.tsx # Project state context
│   │   │
│   │   ├── styles/          # Styled components and themes
│   │   │   ├── globalStyles.ts   # Global styled-components
│   │   │   ├── theme.ts          # Theme configuration
│   │   │   └── components/       # Component-specific styles
│   │   │
│   │   ├── utils/           # Utility functions
│   │   │   ├── api.ts       # API helper functions
│   │   │   ├── storage.ts   # Local storage utilities
│   │   │   └── validation.ts     # Form validation utilities
│   │   │
│   │   └── types/           # TypeScript type definitions
│   │       ├── api.ts       # API response types
│   │       ├── project.ts   # Project-related types
│   │       └── user.ts      # User-related types
│   │
│   └── dist/                # Built frontend assets (generated)
│
├── backend/                 # Node.js TypeScript backend
│   ├── package.json         # Backend dependencies (Express, etc.)
│   ├── tsconfig.json        # Backend TypeScript config
│   ├── server.ts            # Main server entry point
│   │
│   ├── src/
│   │   ├── app.ts           # Express application setup
│   │   ├── server.ts        # Server initialization
│   │   │
│   │   ├── routes/          # API route handlers
│   │   │   ├── index.ts     # Main routes export
│   │   │   ├── auth.ts      # Authentication routes
│   │   │   ├── projects.ts  # Project management routes
│   │   │   ├── aiRouter.ts  # AI integration routes
│   │   │   └── keys.ts      # API key management routes
│   │   │
│   │   ├── controllers/     # Business logic controllers
│   │   │   ├── authController.ts     # Authentication logic
│   │   │   ├── projectController.ts  # Project management
│   │   │   ├── aiController.ts       # AI service integration
│   │   │   └── userController.ts     # User management
│   │   │
│   │   ├── models/          # Database models
│   │   │   ├── User.ts      # User model
│   │   │   ├── Project.ts   # Project model
│   │   │   ├── Template.ts  # Code template model
│   │   │   └── APIKey.ts    # API key model
│   │   │
│   │   ├── middleware/      # Express middleware
│   │   │   ├── auth.ts      # Authentication middleware
│   │   │   ├── validation.ts # Request validation
│   │   │   ├── errorHandler.ts # Error handling
│   │   │   └── rateLimiter.ts  # Rate limiting
│   │   │
│   │   ├── services/        # External service integrations
│   │   │   ├── aiService.ts # AI model integration
│   │   │   ├── authService.ts # Authentication service
│   │   │   └── emailService.ts # Email notifications
│   │   │
│   │   ├── utils/           # Backend utilities
│   │   │   ├── logger.ts    # Logging utility
│   │   │   ├── crypto.ts    # Encryption utilities
│   │   │   ├── validation.ts # Data validation
│   │   │   └── database.ts  # Database utilities
│   │   │
│   │   └── types/           # Backend TypeScript types
│   │       ├── express.d.ts # Express type extensions
│   │       ├── api.ts       # API type definitions
│   │       └── database.ts  # Database type definitions
│   │
│   └── dist/                # Compiled backend code (generated)
│
├── ai/                      # Python AI service
│   ├── requirements.txt     # Python dependencies
│   ├── main.py             # FastAPI main application
│   ├── langchain_router.py # LangChain integration router
│   ├── generate_code.py    # Code generation logic
│   │
│   ├── models/             # AI model configurations
│   │   ├── __init__.py
│   │   ├── openai_model.py # OpenAI integration
│   │   ├── claude_model.py # Anthropic Claude integration
│   │   └── local_model.py  # Local LLM integration
│   │
│   ├── prompts/            # AI prompt templates
│   │   ├── __init__.py
│   │   ├── code_generation.py # Code generation prompts
│   │   ├── code_review.py     # Code review prompts
│   │   └── debugging.py       # Debugging prompts
│   │
│   ├── utils/              # AI service utilities
│   │   ├── __init__.py
│   │   ├── preprocessors.py   # Input preprocessing
│   │   ├── postprocessors.py  # Output post-processing
│   │   └── validators.py      # Response validation
│   │
│   └── tests/              # AI service tests
│       ├── __init__.py
│       ├── test_models.py
│       └── test_generation.py
│
├── database/               # Database related files
│   ├── migrations/         # Database migration scripts
│   │   ├── 001_initial_schema.sql
│   │   ├── 002_add_projects_table.sql
│   │   └── 003_add_templates_table.sql
│   │
│   ├── seeds/              # Database seed data
│   │   ├── users.sql
│   │   ├── projects.sql
│   │   └── templates.sql
│   │
│   └── schema.sql          # Complete database schema
│
├── scripts/                # Development and deployment scripts
│   ├── setup.sh            # Project setup script
│   ├── dev.sh              # Development environment startup
│   ├── build.sh            # Production build script
│   ├── deploy.sh           # Deployment script
│   ├── test.sh             # Test runner script
│   └── db-migrate.sh       # Database migration script
│
├── docker/                 # Docker configuration
│   ├── Dockerfile.frontend # Frontend Docker configuration
│   ├── Dockerfile.backend  # Backend Docker configuration
│   ├── Dockerfile.ai       # AI service Docker configuration
│   ├── docker-compose.yml  # Multi-service orchestration
│   ├── docker-compose.dev.yml  # Development environment
│   └── .dockerignore       # Docker ignore patterns
│
├── docs/                   # Project documentation
│   ├── API.md              # API documentation
│   ├── DEPLOYMENT.md       # Deployment guide
│   ├── DEVELOPMENT.md      # Development setup guide
│   └── ARCHITECTURE.md     # System architecture
│
├── tests/                  # Integration and E2E tests
│   ├── e2e/                # End-to-end tests
│   ├── integration/        # Integration tests
│   └── fixtures/           # Test data fixtures
│
├── .github/                # GitHub Actions and templates
│   ├── workflows/          # CI/CD workflows
│   │   ├── ci.yml          # Continuous integration
│   │   ├── cd.yml          # Continuous deployment
│   │   └── test.yml        # Test automation
│   │
│   ├── ISSUE_TEMPLATE/     # Issue templates
│   └── PULL_REQUEST_TEMPLATE.md # PR template
│
├── .gitignore              # Git ignore patterns
├── .env.example            # Environment variables template
├── .eslintrc.js            # ESLint configuration
├── .prettierrc             # Prettier configuration
└── LICENSE                 # Project license
```

## Key Technologies

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and building
- **Monaco Editor** for code editing
- **Styled Components** for styling
- **Zustand** for state management
- **React Query** for API state management
- **React Hook Form** with Zod validation

### Backend
- **Node.js** with TypeScript
- **Express.js** framework
- **Socket.IO** for real-time communication
- **JWT** for authentication
- **Prisma** or **TypeORM** for database ORM
- **PostgreSQL** database

### AI Service
- **Python FastAPI** for AI service
- **LangChain** for LLM orchestration
- **OpenAI GPT** / **Anthropic Claude** integration
- **Pydantic** for data validation

### Infrastructure
- **Docker** for containerization
- **Docker Compose** for local development
- **GitHub Actions** for CI/CD
- **Nginx** for reverse proxy (production)

## Getting Started

1. **Setup**: Run `npm run install:all` to install all dependencies
2. **Development**: Run `npm run dev` to start all services
3. **Building**: Run `npm run build` to create production builds
4. **Docker**: Use `npm run docker:up` for containerized development

## Development Workflow

1. Frontend and backend run concurrently in development
2. AI service runs separately (Python FastAPI)
3. Real-time code generation and preview
4. Hot reload for all services
5. Integrated testing and linting

This structure provides a scalable, maintainable foundation for the VibeCode platform with clear separation of concerns and modern development practices.
