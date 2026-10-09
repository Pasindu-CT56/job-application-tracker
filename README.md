
# Job Application Tracker

A work-in-progress Kanban-style job application tracker built with Next.js, React, Better Auth, MongoDB, and Mongoose.

## Features

- Email and password sign-up and sign-in.
- Automatic creation of a personal `Job Hunt` board after registration.
- Default workflow columns: Wish List, Applied, Interviewing, Offer, and Rejected.
- Add applications with company, position, location, salary, URL, tags, description, and notes.
- Persist boards, columns, and applications in MongoDB.
- View applications in a dashboard Kanban layout.
- Protect the dashboard and application creation flow with the authenticated session.

## Tech Stack

- Next.js 16 App Router
- React 19 and TypeScript
- Better Auth with the MongoDB adapter
- MongoDB and Mongoose
- Tailwind CSS
- Radix UI and Lucide React

## Prerequisites

- Node.js 20 or newer
- A MongoDB database, local or hosted

## Getting Started

Install dependencies:

```bash
npm install
```

Create a `.env.local` file in the project root:

```env
MONGODB_URI=mongodb://127.0.0.1:27017/job-application-tracker
```

For MongoDB Atlas, replace the value with your Atlas connection string.

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000), create an account, and continue to the dashboard.

## Available Scripts

```bash
npm run dev      # Start the development server
npm run build    # Create a production build
npm run start    # Start the production server
npm run lint     # Run ESLint
```

## Project Structure

```text
app/
	api/auth/       Better Auth API route
	dashboard/      Protected Kanban dashboard
	sign-in/        Sign-in page
	sign-up/        Registration page
components/       Dashboard, forms, navigation, and UI components
lib/
	actions/        Server actions for application changes
	auth/           Better Auth setup and client helpers
	models/         Mongoose models for boards, columns, and applications
	db.ts           Cached MongoDB connection
```

## Current Status

The project is not finished yet. The authentication flow, initial board creation, dashboard loading, and new application persistence are implemented.

### In Progress

- Connect edit, move, delete, and column-delete controls to server actions.
- Add validation and user-facing error messages to the application form.
- Improve loading, empty, and error states.
- Add tests for authentication, board initialization, and application persistence.
