# RingSathi Technical Guide

This guide provides a deeper dive into the architecture, technical decisions, and structure of the RingSathi project.

## 🏗 Architecture Overview

RingSathi is built on a modern full-stack TypeScript ecosystem, utilizing Next.js App Router for both server-rendered and statically generated pages.

### Core Technologies

- **Framework**: Next.js 15 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **Database**: SQLite (via `@libsql/client`)
- **ORM**: Prisma
- **Search**: Fuse.js for client-side fuzzy search

## 📂 Project Structure

- `src/`: Contains all application source code.
  - `app/`: Next.js App Router pages and layouts.
  - `components/`: Reusable React components.
  - `lib/`: Utility functions and shared logic.
- `prisma/`: Prisma schema and database migration/seed scripts.
- `public/`: Static assets (images, icons, etc.).
- `android-app/`: Dedicated directory for the native Android application build.

## 🧠 AI & Verification Engine

RingSathi employs an advanced verification engine that combines:

1. **Automated Scraping**: Periodically gathers data for verification against community standards.
2. **Community Reporting**: A mechanism for users to flag issues, managed through our Prisma database.
3. **Fuzzy Search & Regional Detection**: Leveraging Fuse.js and customized regional logic to ensure users see locally relevant and highly accurate content.

## 🚀 Deployment Strategy

The application is configured for deployment on multiple platforms:

- **Vercel**: Optimal for Next.js continuous deployment and hosting.
- **Firebase**: Project includes configurations (`firebase.json`) for Firebase hosting integration (`ringsathi.web.app`).

## 🛠 Database Management

We use Prisma with a local SQLite database for development, which can be easily adapted to Turso or other providers in production via `@libsql/client`.

- Generate Prisma Client: `npx prisma generate`
- Run Migrations: `npx prisma db push` (or `migrate dev`)
- Seed Database: `npx tsx prisma/seed.ts`
