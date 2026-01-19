# Bolt JS Installation Store Template

## Overview
This template provides a starting point for building applications using the Bolt framework for Slack, integrated with Prisma for database management. It is designed to be easily customizable for various use cases.

## Features
- **Prisma Integration**: Utilize Prisma for database interactions with a PostgreSQL adapter.
- **Environment Configuration**: Load environment variables using dotenv.
- **Slack App Framework**: Built on the Slack Bolt framework for easy Slack app development.

## Getting Started

### Prerequisites
- Node.js (version 14 or higher)
- PostgreSQL database (installed and running)
- A Slack app created in your Slack workspace

### Database Setup
1. Ensure PostgreSQL is installed and running on your system.
2. Create a new database for the application:
   ```bash
   createdb your_database_name
   ```
   Or using psql:
   ```sql
   CREATE DATABASE your_database_name;
   ```
3. Update your `.env` file with the correct `DATABASE_URL` pointing to this database.

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd bolt-js-install-store-template
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up your environment variables in a `.env` file:
   ```plaintext
   DATABASE_URL=your_database_url
   SLACK_BOT_TOKEN=your_slack_bot_token
   SLACK_SIGNING_SECRET=your_slack_signing_secret
   ```

### Running the Application
- To start the application in development mode:
  ```bash
  npm run dev
  ```
- To start the application in production mode:
  ```bash
  npm start
  ```

### Prisma Setup
- Generate Prisma client:
  ```bash
  npm run prisma:generate
  ```
- Run migrations:
  ```bash
  npm run prisma:migrate
  ```

## Customization
- Modify the `src/index.js` file to implement your application's logic.
- Update the `prisma/schema.prisma` file to define your database schema.

## Acknowledgments
- [Slack Bolt](https://slack.dev/bolt)
- [Prisma](https://www.prisma.io/)