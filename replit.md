# D-OneCash - Digital Finance Platform

## Overview

D-OneCash is a comprehensive digital finance platform that enables blockchain-integrated financial services with a focus on cryptocurrency lending, digital payments, and secure asset management. The application provides a modern web interface for managing digital wallets, sending money, processing payments, and accessing various financial services.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI primitives with Tailwind CSS for styling
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation
- **Styling**: Tailwind CSS with custom component system

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript for type safety
- **API Design**: RESTful API with JSON communication
- **Session Management**: In-memory sessions with optional Replit Auth integration
- **File Structure**: Modular route handling with centralized error management

### Database Layer
- **Primary Database**: PostgreSQL with Drizzle ORM
- **Connection**: Neon serverless PostgreSQL via connection pooling
- **Fallback Storage**: In-memory storage system for development
- **Schema Management**: Type-safe schema definitions with automatic migrations

## Key Components

### Authentication System
- **Session-based Authentication**: Server-side session management
- **Optional Replit Auth**: OIDC integration for Replit deployments
- **Demo Mode**: Built-in demo user for development and testing
- **Face ID Simulation**: Frontend face recognition simulation for modern UX

### Wallet Management
- **Multi-currency Support**: USD balance management with planned crypto integration
- **Transaction History**: Complete audit trail of all financial operations
- **QR Code Payments**: Generate and scan QR codes for contactless payments
- **Virtual Cards**: Digital card management system

### Financial Services
- **Money Transfers**: Email, phone, and username-based transfers
- **Cryptocurrency Loans**: BTC collateral lending with USDC loans
- **Investment Platform**: Cryptocurrency buying/selling with staking options
- **Business Terminal**: Payment processing for merchants
- **Inheritance System**: Digital asset inheritance planning

### Contact Management
- **Address Book**: Secure contact storage for frequent transfers
- **Favorites System**: Quick access to preferred contacts
- **Import Functionality**: Bulk contact import capabilities

## Data Flow

### Request Processing
1. Client requests pass through Express middleware
2. Route handlers validate input using Zod schemas
3. Database operations use Drizzle ORM with type safety
4. Response data is serialized and returned to client
5. Client updates UI state via TanStack Query

### State Management
- **Server State**: TanStack Query manages API data with caching
- **Local State**: React useState and useContext for UI state
- **Form State**: React Hook Form for complex form management
- **Wallet Context**: Centralized wallet data across components

### Real-time Updates
- **Optimistic Updates**: Immediate UI feedback for user actions
- **Query Invalidation**: Automatic data refresh after mutations
- **Error Handling**: Comprehensive error boundaries and user feedback

## External Dependencies

### Core Dependencies
- **@radix-ui/**: Complete UI component library for accessibility
- **@tanstack/react-query**: Server state management and caching
- **drizzle-orm**: Type-safe database ORM with PostgreSQL support
- **zod**: Runtime type validation and schema definition
- **wouter**: Lightweight routing library
- **tailwindcss**: Utility-first CSS framework

### Development Dependencies
- **vite**: Fast build tool with HMR support
- **typescript**: Static type checking
- **tsx**: TypeScript execution for server development
- **esbuild**: Fast JavaScript bundler for production

### Optional Integrations
- **Stripe**: Payment processing (configured but not implemented)
- **PayPal**: Alternative payment method (configured but not implemented)
- **Twilio**: SMS notifications (configured but not implemented)

## Deployment Strategy

### Replit Deployment (Primary)
- **Runtime**: Node.js 20 with PostgreSQL 16
- **Build Process**: `npm run build` for production assets
- **Start Command**: `npm run start` for production server
- **Environment**: Configured via Replit secrets and environment variables

### Alternative Platforms
- **Vercel**: Frontend-focused deployment with serverless functions
- **Railway**: Full-stack deployment with managed PostgreSQL
- **DigitalOcean**: Traditional server deployment option

### Environment Configuration
- **Database**: PostgreSQL connection string required
- **Sessions**: Secure session secret for authentication
- **Optional**: Replit Auth configuration for OIDC
- **Development**: Local development with hot reloading

### Build Process
1. Frontend assets compiled with Vite
2. Backend code bundled with esbuild
3. Static assets served from `dist/public`
4. Server runs from `dist/index.js`

## User Preferences

Preferred communication style: Simple, everyday language.

## Changelog

Changelog:
- June 15, 2025. Initial setup