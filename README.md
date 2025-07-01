# Vibe Coding Projects - Next.js Starter Kit

This is a boilerplate project for vibe coding projects, providing a modern full-stack foundation with authentication, database, styling, and AI capabilities.

## What's Included

- **Next.js** - React framework for production
- **NextAuth + Google Provider** - Authentication with Google OAuth
- **Postgres Database + Drizzle ORM** - Type-safe database operations
- **Shadcn + Tailwind** - Beautiful UI components and utility-first CSS
- **Langchain & LangGraph** - AI features (Text & Image Gen, Structured Output, Agents, etc)
- **Vercel Blob Storage** - File storage solution

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Git** - [Download Git](https://git-scm.com/downloads)
- **Node.js** (version 18 or higher) - [Download Node.js](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn** - [Install Yarn](https://yarnpkg.com/getting-started/install)

## Getting Started

### 1. Clone the Repository

```bash
# Clone this repository
git clone <your-repo-url>

# Navigate to the project directory
cd nextjs-vibe-starter-kit
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3. Environment Setup

Copy the environment variables file and configure your settings:

```bash
cp .env.example .env.local
```

Fill in your environment variables:
- Database connection string
- NextAuth configuration
- Google OAuth credentials
- AI Provider keys
- Other required API keys

### 4. Database Setup

Set up your Postgres database and run migrations:

```bash
npm run db:push
# or
yarn db:push
```

### 5. Run the Development Server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

