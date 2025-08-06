# TeslaInvest Platform

## Overview

TeslaInvest is a comprehensive investment platform focused on Tesla stock and related financial products. The application provides real-time Tesla stock tracking, investment portfolio management, curated Tesla news, and financial analysis tools. It features a modern web interface with professional investment dashboards, risk assessment tools, and interactive market data visualizations.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

The frontend is built using React with TypeScript and follows a component-based architecture:

- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI primitives with shadcn/ui design system for consistent, accessible components
- **Styling**: Tailwind CSS with custom Tesla-branded color palette and responsive design
- **State Management**: TanStack Query (React Query) for server state management and data fetching
- **Build Tool**: Vite for fast development and optimized production builds

The application uses a single-page application (SPA) architecture with component-based sections including navigation, hero section, investment plans, dashboard, news feed, and financial tools.

### Backend Architecture

The backend follows a RESTful API pattern built with Express.js:

- **Framework**: Express.js with TypeScript for type-safe server development
- **API Design**: RESTful endpoints for investment plans, portfolio data, Tesla news, and stock information
- **Data Layer**: Abstract storage interface with in-memory implementation for development
- **Error Handling**: Centralized error middleware with proper HTTP status codes
- **Development Server**: Vite integration for hot module replacement in development

The server implements a modular route structure with separate handlers for different business domains (investments, portfolios, news, stock data).

### Data Storage Solutions

The application uses a flexible storage architecture:

- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema Definition**: Centralized schema definitions in TypeScript using Drizzle
- **Development Storage**: In-memory storage implementation with mock data for development
- **Migration System**: Drizzle Kit for database schema migrations
- **Connection**: Neon Database serverless PostgreSQL for production

The schema includes tables for users, investment plans, portfolios, news articles, and real-time stock data with proper relationships and data types.

### Authentication and Authorization

Currently implements a basic user system:

- **User Management**: User registration and authentication endpoints
- **Session Handling**: PostgreSQL session storage with connect-pg-simple
- **Data Access**: User-specific portfolio and investment data isolation

### External Dependencies

The application integrates several key external services and libraries:

- **Neon Database**: Serverless PostgreSQL database hosting
- **Recharts**: Chart library for financial data visualization
- **Embla Carousel**: Touch-friendly carousel components
- **React Hook Form**: Form handling with validation
- **Zod**: Runtime type validation and schema validation
- **Date-fns**: Date manipulation and formatting utilities

The frontend uses a comprehensive UI component library built on Radix UI primitives, providing accessible and customizable interface elements for complex financial interfaces.