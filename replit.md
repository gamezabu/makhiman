# Luxe Jewelry E-commerce Platform

## Overview

This is a full-stack jewelry e-commerce platform built with React (Vite) on the frontend and Express.js on the backend. The application showcases luxury jewelry products with a modern, elegant design and provides a complete shopping experience including product browsing, cart management, and inquiry forms.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom jewelry-themed color palette
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React Context for cart state, TanStack Query for server state
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (@neondatabase/serverless)
- **API**: RESTful endpoints for products, cart, and inquiries
- **Development**: Hot module replacement with Vite middleware in development

### Database Schema
The application uses three main tables:
- **products**: Core jewelry inventory with detailed specifications (metal, stone, carat, setting)
- **cart_items**: Shopping cart functionality with product references and quantities
- **inquiries**: Customer inquiry form submissions with contact details and preferences

## Key Components

### Product Management
- Comprehensive product catalog with categories (rings, necklaces, earrings, bracelets)
- Rich product details including multiple images, specifications, and pricing
- Category-based browsing and individual product pages

### Shopping Cart
- Persistent cart state using React Context
- Add/remove items with size selection support
- Cart drawer component for quick access
- Real-time cart count display in header

### User Interface
- Responsive design optimized for jewelry showcase
- Elegant typography using Playfair Display and Lato fonts
- Custom color scheme (champagne, charcoal, off-white, rose-gold)
- Interactive components with hover effects and animations

### Customer Inquiries
- Contact form for custom jewelry requests
- Structured inquiry data collection (jewelry type, budget range, specifications)
- Form validation and submission handling

## Data Flow

1. **Product Display**: Server renders product data from PostgreSQL via Drizzle ORM
2. **Cart Operations**: Client-side cart state synchronized with backend API
3. **Data Fetching**: TanStack Query manages server state with caching and background updates
4. **Form Submissions**: Contact forms use React Hook Form with Zod validation before API submission

## External Dependencies

### UI and Styling
- **Radix UI**: Accessible component primitives
- **Tailwind CSS**: Utility-first styling framework
- **Lucide React**: Icon library for consistent iconography
- **Embla Carousel**: Touch-friendly carousel components

### Development Tools
- **Drizzle Kit**: Database schema management and migrations
- **TSX**: TypeScript execution for development server
- **ESBuild**: Fast JavaScript bundling for production

### Database and Hosting
- **Neon Database**: Serverless PostgreSQL hosting
- **Replit**: Development and deployment platform

## Deployment Strategy

### Development Environment
- Uses `tsx` for running TypeScript server with hot reload
- Vite dev server with middleware mode for frontend
- Environment variables for database connection

### Production Build
- Frontend: Vite builds static assets to `dist/public`
- Backend: ESBuild bundles server code to `dist/index.js`
- Single-server deployment serving both API and static files

### Environment Configuration
- Development: `NODE_ENV=development` with hot reload
- Production: `NODE_ENV=production` with optimized builds
- Database: `DATABASE_URL` environment variable for PostgreSQL connection

## User Preferences

Preferred communication style: Simple, everyday language.

## Changelog

Changelog:
- June 16, 2025. Initial setup