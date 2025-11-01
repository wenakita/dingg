# Dingg Prisma Database

This directory contains the Prisma schema and migrations for the Dingg Farcaster mini-app.

## Setup

1. Copy `.env.example` to `.env` and fill in your database URL:
   ```bash
   cp .env.example .env
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run migrations:
   ```bash
   npx prisma migrate deploy
   ```

4. Generate Prisma Client:
   ```bash
   npx prisma generate
   ```

## Development

### Create a new migration
```bash
npx prisma migrate dev --name your_migration_name
```

### Reset database (WARNING: Deletes all data)
```bash
npx prisma migrate reset
```

### Open Prisma Studio (Database GUI)
```bash
npx prisma studio
```

## Schema

The database tracks:
- **Users**: Farcaster users who interact with the app
- **Interactions**: User actions and events
- **Frames**: Frame renders and analytics (optional)

## Production

For production deployments, set the `DATABASE_URL` environment variable and run:
```bash
npx prisma migrate deploy
```

This will apply all pending migrations without prompting.

