# 🎮 COMPASS Games List

A comprehensive game tracking application that allows users to manage their video game collection, categorize games, track progress, and organize gaming platforms.

## 📝 Description

COMPASS Games List is a full-stack web application designed for gamers who want to maintain an organized digital catalog of their video game collection. The application helps users track their gaming progress, categorize games, and manage their gaming platforms - providing insights into their gaming habits and collection.

## 🤝 Contributors

- [Yago Ronchi](https://github.com/Yagoks5)
- [Yuri Knebel](https://github.com/YuriKnebel1)
- [Victor Junior](https://github.com/VictorJunior-creator)
- [Thalles Fabian](https://github.com/thallesfabian)
- [Wilians](https://github.com/wilians01)

## ✨ Features & Functionalities

### User Management

- User registration and authentication
- Secure login with JWT authentication
- User profile management

### Game Management

- Add, edit, and delete games
- Track game status (Playing, Done, Abandoned)
- Mark games as favorites
- Record acquisition and completion dates
- Add game descriptions and cover images

### Categories Management

- Create custom game categories
- Organize games by category
- Filter games by category

### Platform Management

- Track gaming platforms (consoles, PC, etc.)
- Record platform details (company, acquisition year)
- Organize games by platform

### Dashboard

- View game statistics and insights
- Track gaming progress across platforms
- See recent activity

## 🛠️ Technologies Used

### Backend

- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **TypeScript** - Strongly typed programming language
- **Prisma** - Next-generation ORM for Node.js and TypeScript
- **PostgreSQL** - Database
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing

### Frontend

- **React 19** - UI library
- **TypeScript** - Type safety
- **React Router v7** - Routing
- **React Query (TanStack Query)** - Data fetching and state management
- **Vite** - Next-generation frontend tooling
- **React Toastify** - Toast notifications
- **React Icons** - Icon library
- **Axios** - HTTP client

### Others
- **Docker**
- **Nginx**

## 📁 Project Structure

### Backend

```
└── 📁backend
        └── .dockerignore
        └── .env.example
        └── .eslintrc.json
        └── .gitignore
        └── .prettierrc
        └── Dockerfile
        └── package-lock.json
        └── package.json
        └── 📁prisma
            └── schema.prisma
        └── 📁src
            └── app.ts
            └── 📁controllers
                └── authController.ts
                └── categoryController.ts
                └── dashboardController.ts
                └── gameController.ts
                └── platformController.ts
                └── userController.ts
            └── 📁middleware
                └── auth.middleware.ts
                └── error.middleware.ts
                └── validation.middleware.ts
            └── 📁routes
                └── authRoutes.ts
                └── categoryRoutes.ts
                └── dashboardRoutes.ts
                └── gameRoutes.ts
                └── platformRoutes.ts
                └── userRoutes.ts
            └── server.ts
            └── 📁services
                └── auth.service.ts
                └── category.service.ts
                └── dashboard.service.ts
                └── game.service.ts
                └── platform.service.ts
            └── 📁types
                └── api.types.ts
                └── auth.types.ts
                └── category.types.ts
                └── dashboard.types.ts
                └── express.d.ts
                └── game.types.ts
                └── platform.types.ts
                └── user.types.ts
            └── 📁utils
                └── auth.utils.ts
                └── jwt.utils.ts
                └── pagination.utils.ts
                └── validation.utils.ts
        └── tsconfig.json
```

### Frontend

```
frontend/
└── 📁frontend
        └── .dockerignore
        └── .gitignore
        └── .prettierrc
        └── Dockerfile
        └── eslint.config.js
        └── index.html
        └── nginx.conf
        └── package-lock.json
        └── package.json
        └── 📁public
            └── 📁images
                └── favicon.png
                └── icons_1-bg.png
                └── icons_2-bg.png
                └── icons_3-bg.png
                └── login-bg.svg
                └── logo-icon.svg
                └── warning.png
        └── README.md
        └── 📁src
            └── App.css
            └── App.tsx
            └── 📁components
                └── AuthBackground.css
                └── AuthBackground.tsx
                └── CategoryModal.css
                └── CategoryModal.tsx
                └── ConfirmationModal.css
                └── ConfirmationModal.tsx
                └── GameModal.css
                └── GameModal.tsx
                └── Logo.css
                └── Logo.tsx
                └── PlatformModal.css
                └── PlatformModal.tsx
                └── ProtectedRoute.css
                └── ProtectedRoute.tsx
                └── PublicRoute.tsx
                └── Sidebar.css
                └── Sidebar.tsx
            └── 📁contexts
                └── AuthContext.tsx
            └── custom-toast.css
            └── 📁hooks
                └── useDashboard.ts
                └── useInvalidateCache.ts
            └── index.css
            └── 📁lib
                └── queryClient.ts
            └── main.tsx
            └── 📁pages
                └── Categories.css
                └── Categories.tsx
                └── DashboardPage.css
                └── DashboardPage.tsx
                └── Games-styles.css
                └── Games.css
                └── Games.tsx
                └── LoginPage.css
                └── LoginPage.tsx
                └── Platforms.css
                └── Platforms.tsx
                └── RegisterPage.css
                └── RegisterPage.tsx
            └── 📁services
                └── api.ts
                └── categoryService.ts
                └── dashboardService.ts
                └── gameService.ts
            └── 📁types
                └── platform.ts
            └── vite-env.d.ts
        └── tsconfig.app.json
        └── tsconfig.json
        └── tsconfig.node.json
        └── vite.config.ts
```

## 🚀 Setup & Installation

### Prerequisites
Make sure you have installed:
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
  
### Backend Setup

### Environment Configuration

Copy the backend environment file:
```bash
cp backend/.env.example backend/.env

Run with Docker
To build and run both services:
docker-compose up --build
Frontend will be available at: http://localhost:80 Backend API at: http://localhost:3333

## 🧪 Available Scripts
   Backend
      cd backend
      npm install
      npx prisma generate
      npm run dev
   Frontend
      cd frontend
      npm install
      npm run dev

##🗂️ Prisma Migration (Optional)
   To apply migrations manually:
      cd backend
      npx prisma migrate dev

## 📊 Database Schema

The application uses the following data models:

- **User**: Stores user account information
- **Game**: Tracks individual games with status, dates, and relationships
- **Category**: Organizes games into custom categories
- **Platform**: Tracks gaming platforms with details

## 🔄 API Endpoints

### Authentication

- `POST /auth/register` - Register a new user
- `POST /auth/login` - Log in a user

### User

- `GET /user` - Get current user profile
- `PUT /user` - Update user profile

### Games

- `GET /games` - Get all games for current user
- `POST /games` - Add a new game
- `PUT /games/:id` - Update a game
- `DELETE /games/:id` - Delete a game

### Categories

- `GET /categories` - Get all categories for current user
- `POST /categories` - Add a new category
- `PUT /categories/:id` - Update a category
- `DELETE /categories/:id` - Delete a category

### Platforms

- `GET /platforms` - Get all platforms for current user
- `POST /platforms` - Add a new platform
- `PUT /platforms/:id` - Update a platform
- `DELETE /platforms/:id` - Delete a platform

### Dashboard

- `GET /dashboard` - Get dashboard statistics

## 📄 License

This project is licensed under the ISC License.
