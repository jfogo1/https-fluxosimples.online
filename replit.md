# FluxoSimples - Financial Management Application

## Overview

FluxoSimples is a comprehensive financial management application built as a full-stack web application designed specifically for Brazilian small businesses. It provides users with tools to track income and expenses, visualize cash flow through charts, manage financial transactions, control accounts payable/receivable, receive intelligent alerts, and forecast cash flow. The application features a modern, responsive design with dark/light theme support and is fully localized in Brazilian Portuguese with proper currency formatting.

## Recent Changes (August 2025)

- ✅ **Complete Authentication System**: Implemented full login/registration system with session management
- ✅ **Simplified Authentication**: Removed Google OAuth integration and simplified to username/password only authentication
- ✅ **User Account Management**: Added user profiles with company information, username, email, and password authentication
- ✅ **Protected Routes**: Secured all API endpoints with authentication middleware to protect user data
- ✅ **Login/Register Pages**: Created beautiful, responsive authentication pages with form validation (Google login removed)
- ✅ **Session Persistence**: Implemented secure session management with 24-hour expiration and Passport session handling
- ✅ **User Interface Integration**: Added user info display and logout functionality to dashboard header
- ✅ **Auto-redirect After Registration**: Users are automatically redirected to dashboard after successful account creation
- ✅ **Demo Account**: Provided demonstration account (demo/123456) for easy testing
- ✅ **Dark/Light Theme System**: Implemented complete theme toggle with localStorage persistence
- ✅ **Smart Alerts Panel**: Added intelligent notifications for cash flow warnings and financial insights
- ✅ **Bills Management**: Created comprehensive accounts payable/receivable tracking with due dates and status management
- ✅ **Enhanced Financial Dashboard**: Improved all components with dark mode support and better responsive design
- ✅ **Feedback System**: Added floating feedback button for user suggestions and bug reports
- ✅ **Sample Data**: Populated application with realistic sample bills and alerts for demonstration
- ✅ **API Expansion**: Extended backend with full CRUD operations for bills and alerts management
- ✅ **Financial Summary Enhancement**: Improved getSummary calculation to include paid/received bills in balance calculations
- ✅ **Transactions Section Removal**: Removed transactions page completely due to lack of utility as requested by user
- ✅ **Exclusive Owner Access**: Implemented username-specific access control for subscription monitoring
- ✅ **Owner Account Created**: Created exclusive account for site owner (username: "jfogo") with special privileges
- ✅ **Security Enhancement**: Changed from role-based to username-specific authentication for maximum security
- ✅ **Admin Panel Restriction**: Only the site owner can access subscription monitoring and admin features

## User Preferences

Preferred communication style: Simple, everyday language.
Target audience: Brazilian small business owners, focusing on practical financial management needs.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript for type safety and modern development
- **UI Library**: Radix UI components with shadcn/ui styling system for consistent, accessible interface components
- **Styling**: Tailwind CSS with custom CSS variables for comprehensive dark/light theming and responsive design
- **Theme System**: Custom theme provider with localStorage persistence and system preference detection
- **State Management**: TanStack Query (React Query) for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Forms**: React Hook Form with Zod validation for type-safe form handling
- **Charts**: Chart.js integration for financial data visualization and cash flow forecasting
- **Internationalization**: Brazilian Portuguese localization with proper currency formatting (BRL)
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Framework**: Express.js with TypeScript for RESTful API development
- **Storage Pattern**: Repository pattern with interface-based storage abstraction
- **Current Storage**: In-memory storage implementation with sample data for development and demonstration
- **API Design**: Comprehensive RESTful endpoints for:
  - Transaction management (CRUD operations, date range queries)
  - Bills to receive management (client accounts, due dates, status tracking)
  - Bills to pay management (supplier accounts, payment tracking)
  - Smart alerts system (financial warnings, cash flow forecasts)
- **Sample Data**: Pre-populated realistic sample bills and alerts for immediate testing
- **Validation**: Zod schemas shared between frontend and backend for consistent data validation
- **Error Handling**: Centralized error handling middleware with proper HTTP status codes

### Data Layer Architecture
- **ORM**: Drizzle ORM configured for PostgreSQL with type-safe database operations
- **Schema Management**: Comprehensive schema definitions including:
  - Enhanced user profiles with theme preferences
  - Extended transaction records with client associations and auto-categorization
  - Bills to receive/pay with due date tracking and status management
  - Smart alerts system with severity levels and read status
- **Database**: PostgreSQL configured through Neon Database serverless connection
- **Migrations**: Drizzle Kit for database schema migrations and management
- **Data Validation**: Drizzle-Zod integration for runtime schema validation
- **Sample Data**: Structured sample data generation for realistic testing environment

### Authentication & Session Management
- **Session Storage**: Express-session with in-memory storage for development
- **User Management**: Simplified authentication system supporting username/password only
- **OAuth Integration**: Google OAuth completely removed for simplified authentication
- **Security**: Secure session management with 24-hour expiration and protected API routes
- **User Profiles**: Support for manually created username/password accounts only

### Development & Build Architecture
- **Monorepo Structure**: Client, server, and shared code organization
- **Development Server**: Vite dev server with Express API proxy
- **Production Build**: Separate client (Vite) and server (esbuild) build processes
- **Hot Reload**: Development-optimized with Vite HMR and server restart capabilities
- **Type Safety**: Shared TypeScript configuration across all packages

## External Dependencies

### Database Services
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **PostgreSQL**: Primary database for persistent data storage

### UI & Styling Dependencies
- **Radix UI**: Comprehensive accessible component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library for consistent iconography
- **shadcn/ui**: Pre-built component system built on Radix UI

### Development & Runtime Dependencies
- **TanStack Query**: Server state management and data fetching
- **React Hook Form**: Form state management with validation
- **Zod**: Runtime type validation and schema definition
- **Chart.js**: Data visualization for financial charts
- **Wouter**: Lightweight routing solution
- **date-fns**: Date manipulation and formatting utilities

### Build & Development Tools
- **Vite**: Frontend build tool and development server
- **esbuild**: Fast JavaScript bundler for server builds
- **Drizzle Kit**: Database migration and schema management CLI
- **TypeScript**: Static type checking across the entire application

### Replit Integration
- **Replit Plugins**: Development environment integration with error overlays and cartographer for enhanced debugging
- **Development Banner**: Replit development mode indicators