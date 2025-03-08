# PUG Academic Service Portal

A comprehensive student information portal for Presbyterian University Ghana, designed to provide students with seamless access to academic information and university services.

## Features

- Responsive web application with mobile-first design
- Custom branding with navy blue and white color scheme
- Authentication and personalized dashboard
- Student information management system
- Course schedule viewing
- Assessment tracking
- Payment integration with Paystack
- Email verification with SendGrid

## Prerequisites

- Node.js (v16 or higher)
- PostgreSQL (v12 or higher)
- npm or yarn package manager

## Local Development Setup

1. Clone the repository:
```bash
git clone [repository-url]
cd pug-portal
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:
```env
DATABASE_URL=postgresql://[username]:[password]@localhost:5432/[database-name]
SENDGRID_API_KEY=[your-sendgrid-key]
PAYSTACK_SECRET_KEY=[your-paystack-key]
SESSION_SECRET=[random-string]
```

4. Set up the database:
- Create a new PostgreSQL database
- Update the DATABASE_URL in .env with your database credentials
- Push the schema to the database:
```bash
npm run db:push
```

5. Start the development server:
```bash
npm run dev
```

The application will be available at http://localhost:5000

## Project Structure

- `/client` - Frontend React application
- `/server` - Backend Express server
- `/shared` - Shared types and schemas
- `/public` - Static assets

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run db:push` - Push schema changes to database

## Environment Setup

### Database
The application uses PostgreSQL as its database. Make sure to:
1. Install PostgreSQL locally
2. Create a new database
3. Update the DATABASE_URL in your .env file

### Email Service
We use SendGrid for email verification. To set it up:
1. Create a SendGrid account
2. Get an API key
3. Add it to your .env file as SENDGRID_API_KEY

### Payment Integration
Paystack is used for payment processing. To set it up:
1. Create a Paystack account
2. Get your test/live API keys
3. Add the secret key to your .env file as PAYSTACK_SECRET_KEY
