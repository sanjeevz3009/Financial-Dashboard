# 📊 Financial Dashboard - Next.js Learning Project

A financial dashboard application built with Next.js, featuring invoice management, and customer tracking. This project was created as part of the [Next.js Learn Course](https://nextjs.org/learn/) to learn modern React and Next.js concepts.

![Next.js](https://img.shields.io/badge/Next.js-15+-black?style=flat&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.7-blue?style=flat&logo=typescript)
![React](https://img.shields.io/badge/React-19+-61DAFB?style=flat&logo=react)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38B2AC?style=flat&logo=tailwind-css)

## Features

- **Invoice Management**: Create, edit, and track invoices with status updates
- **Customer Management**: View and manage customer information
- **Authentication**: Secure login system with NextAuth.js
- **Search & Pagination**: Search functionality with debounced input
- **Responsive Design**: Mobile-first design with Tailwind CSS
- **Server Actions**: Modern data mutations with React Server Actions
- **Loading States**: Skeleton loaders and streaming with React Suspense
- **Error Handling**: Error boundaries and not-found pages

## Tech Stack

- **Framework**: [Next.js](https://nextjs.org/) (App Router)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Authentication**: [NextAuth.js](https://next-auth.js.org/) v5 (Beta)
- **Database**: [PostgreSQL](https://www.postgresql.org/) with [postgres.js](https://github.com/porsager/postgres)
- **Form Validation**: [Zod](https://zod.dev/)
- **Icons**: [Heroicons](https://heroicons.com/)
- **Package Manager**: [pnpm](https://pnpm.io/)

## Project Structure

```zsh
nextjs-dashboard/
├── app/
│   ├── dashboard/          # Dashboard pages and layouts
│   │   ├── (overview)/     # Dashboard home with route group
│   │   ├── customers/      # Customer management
│   │   └── invoices/       # Invoice CRUD operations
│   ├── lib/                # Utilities and data functions
│   │   ├── actions.ts      # Server Actions for mutations
│   │   ├── data.ts         # Database queries
│   │   └── definitions.ts  # TypeScript type definitions
│   ├── ui/                 # Reusable UI components
│   ├── login/              # Authentication pages
│   ├── seed/               # Database seeding route
│   └── layout.tsx          # Root layout
├── public/                 # Static assets
├── auth.config.ts          # NextAuth configuration
└── auth.ts                 # Auth.js setup
```

## Getting Started

### Prerequisites

- Node.js 18.x or later
- pnpm (or npm/yarn)
- PostgreSQL database

### Installation

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd nextjs-dashboard
   ```

2. **Install dependencies**

   ```bash
   pnpm install
   ```

3. **Set up environment variables**

   Create a `.env` file in the root directory:

   ```env
   # Database
   POSTGRES_URL="your-postgres-url"
   POSTGRES_PRISMA_URL="your-postgres-prisma-url"
   POSTGRES_URL_NO_SSL="your-postgres-url-no-ssl"
   POSTGRES_URL_NON_POOLING="your-postgres-url-non-pooling"
   POSTGRES_USER="your-user"
   POSTGRES_HOST="your-host"
   POSTGRES_PASSWORD="your-password"
   POSTGRES_DATABASE="your-database"
   
   # Auth
   AUTH_SECRET="your-secret-key"
   AUTH_URL="http://localhost:3000"
   ```

4. **Seed the database**
   After setting up your database connection, seed it with sample data:

   ```bash
   pnpm dev
   # Then visit http://localhost:3000/seed in your browser
   ```

5. **Start the development server**

   ```bash
   pnpm dev
   ```

   Open [http://localhost:3000](http://localhost:3000) to view the application.

## Available Scripts

- `pnpm dev` - Start development server with Turbopack
- `pnpm build` - Build for production
- `pnpm start` - Start production server
- `pnpm lint` - Run ESLint

## Key Concepts Learned

This project covers essential Next.js and React concepts:

### Next.js Features

- **App Router**: Modern routing with React Server Components
- **File-based Routing**: Including dynamic routes and route groups
- **Server Components**: Default server-side rendering for better performance
- **Server Actions**: Type-safe server mutations without API routes
- **Streaming**: Incremental rendering with Suspense
- **Partial Prerendering**: Static and dynamic content optimization

### React Patterns

- **Server vs Client Components**: Understanding the component boundary
- **Data Fetching**: Server-side data fetching patterns
- **Suspense Boundaries**: Loading states and skeleton screens
- **Error Boundaries**: Graceful error handling
- **Form Handling**: Progressive enhancement with Server Actions

### Database & Validation

- **SQL Queries**: Direct PostgreSQL queries with postgres.js
- **Schema Validation**: Runtime validation with Zod
- **Data Mutations**: CRUD operations with Server Actions

### Styling & UX

- **Tailwind CSS**: Utility-first CSS framework
- **Responsive Design**: Mobile-first approach
- **Accessibility**: ARIA labels and semantic HTML
- **Debouncing**: Optimised search with use-debounce

### Authentication

- **NextAuth.js v5**: Authentication with credentials provider
- **Protected Routes**: Middleware-based route protection
- **Session Management**: Secure user sessions

## Authentication Setup

The application uses NextAuth.js v5 (beta) with credentials provider:

- **Default Login**: Check the seeded data for demo credentials
- **Password Hashing**: bcrypt for secure password storage
- **Middleware Protection**: Routes under `/dashboard` are protected

## Database Schema

The application uses the following main entities:

- **Users**: Authentication and user information
- **Customers**: Customer profiles with contact details
- **Invoices**: Financial records with status (pending/paid)
- **Revenue**: Monthly revenue data for charts

## Learning Journey

This project was built to:

- Learn Next.js 15 with App Router
- Understand Server Components and Server Actions
- React patterns and best practices
- Implement authentication and authorization
- Refresh and deepen React knowledge

## Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Next.js Learn Course](https://nextjs.org/learn)
- [React Documentation](https://react.dev)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## License

This project is for educational purposes.

---
