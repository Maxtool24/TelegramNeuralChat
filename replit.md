# Project Overview

This is a modern full-stack web application built with React, TypeScript, and Express.js, featuring a Telegram-like AI interface. The application provides users with AI-powered features including text processing, image generation, web search, and access to various neural networks.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Framework**: Shadcn/UI components with Tailwind CSS
- **State Management**: TanStack Query (React Query) for server state
- **Routing**: Wouter for lightweight client-side routing
- **Styling**: Tailwind CSS with custom design tokens mimicking Telegram's dark theme

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM with PostgreSQL support
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Management**: In-memory storage with interface for database migration

### Project Structure
```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Page components (Dashboard, AIFeatures, NeuralNetworks)
│   │   ├── lib/           # Utilities and configurations
│   │   └── hooks/         # Custom React hooks
├── server/                # Backend Express application
│   ├── index.ts          # Main server entry point
│   ├── routes.ts         # API route definitions
│   ├── storage.ts        # Data storage abstraction
│   └── vite.ts           # Development server integration
├── shared/               # Shared types and schemas
│   └── schema.ts        # Database schema definitions
└── migrations/          # Database migration files
```

## Key Components

### Authentication System
- User schema with username and password fields
- Zod validation schemas for type safety
- Storage interface supporting both in-memory and database implementations

### AI Features Interface
- **Text Processing**: Text generation, summarization, and checking
- **Image Generation**: AI-powered image creation and design
- **Web Search**: Intelligent search with deep analytics
- **Photo Animation**: Static image animation capabilities

### Neural Network Access
- Integration with multiple AI models:
  - ChatGPT-4o and ChatGPT-4o mini
  - DeepSeek Chat and DeepSeek Reasoner
  - Flux for image generation
  - Runway for video processing
  - Claude Sonnet for advanced reasoning

### UI/UX Design
- Dark theme inspired by Telegram's interface
- Responsive design with mobile-first approach
- Custom color palette with feature-specific accent colors
- Interactive components with hover effects and animations

## Data Flow

1. **Client-Side Routing**: Wouter handles navigation between Dashboard, AI Features, and Neural Networks pages
2. **API Communication**: TanStack Query manages server state and caching
3. **Data Validation**: Zod schemas ensure type safety across client-server boundary
4. **Storage Layer**: Abstracted storage interface allows switching between in-memory and database storage
5. **Development Hot Reload**: Vite middleware integrated with Express for seamless development

## External Dependencies

### Frontend Dependencies
- **UI Components**: Radix UI primitives with Shadcn/UI styling
- **Icons**: Lucide React for consistent iconography
- **Forms**: React Hook Form with Hookform resolvers
- **Animations**: Class Variance Authority for component variants

### Backend Dependencies
- **Database**: Drizzle ORM with Neon Database serverless PostgreSQL
- **Session Management**: Connect-pg-simple for PostgreSQL session storage
- **Development**: tsx for TypeScript execution, esbuild for production builds

### Development Tools
- **Type Checking**: TypeScript with strict configuration
- **Code Quality**: ESLint and Prettier (configured via Replit)
- **Build Process**: Vite for frontend, esbuild for backend bundling

## Deployment Strategy

### Development Environment
- **Platform**: Replit with Node.js 20, Web, and PostgreSQL 16 modules
- **Hot Reload**: Vite development server with Express middleware integration
- **Port Configuration**: Frontend served on port 5000, exposed on port 80

### Production Build
- **Frontend**: Vite builds static assets to `dist/public`
- **Backend**: esbuild bundles server code to `dist/index.js`
- **Database**: Drizzle migrations handled via `npm run db:push`
- **Deployment**: Replit autoscale deployment with build and start commands

### Environment Configuration
- **Database**: CONNECTION_URL environment variable for PostgreSQL
- **Session**: In-memory storage with database migration path available
- **Static Assets**: Express serves built frontend assets in production

## Changelog

Changelog:
- June 26, 2025. Initial setup
- June 26, 2025. Added PostgreSQL database with Drizzle ORM
  - Created users and chats tables with relations
  - Migrated from in-memory storage to DatabaseStorage
  - Added API endpoints for chat management
  - Updated frontend to fetch real data from database

## User Preferences

Preferred communication style: Simple, everyday language.