# Dream Libaas E-commerce Platform

A modern e-commerce platform for ethnic wear built with Next.js, Firebase, and Tailwind CSS.

## Features

- User authentication with Firebase Auth
- Admin dashboard for product and order management
- Shopping cart functionality
- Session management
- Responsive design

## Prerequisites

- Node.js 16.x or higher
- Firebase account with Authentication and Firestore enabled
- Firebase service account key

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/dream-libaas.git
cd dream-libaas
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env.local` file in the root directory with the following variables:

```
# Firebase Configuration
NEXT_PUBLIC_FIREBASE_API_KEY=your-api-key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your-auth-domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your-project-id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your-storage-bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your-messaging-sender-id
NEXT_PUBLIC_FIREBASE_APP_ID=your-app-id
NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID=your-measurement-id

# Admin Configuration
ADMIN_EMAILS=admin@example.com,another-admin@example.com

# Firebase Admin SDK Configuration
FIREBASE_CLIENT_EMAIL=your-service-account-email
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nYOUR_PRIVATE_KEY_HERE\n-----END PRIVATE KEY-----\n"
```

### 4. Set up admin access

```bash
npm run setup-admin
```

This will create the service account key file and set up admin privileges for the emails specified in the `ADMIN_EMAILS` environment variable.

### 5. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Admin Access

To access the admin dashboard:

1. Register an account with one of the admin emails specified in `ADMIN_EMAILS`
2. Run the admin setup script: `npm run setup-admin`
3. Log out and log back in to refresh your token
4. Navigate to `/admin` or click on the Admin Dashboard link in the user menu

## Project Structure

```
dream-libaas/
├── public/            # Static assets
├── src/
│   ├── app/           # Next.js app router
│   │   ├── admin/     # Admin dashboard pages
│   │   ├── api/       # API routes
│   │   └── ...        # Other pages
│   ├── components/    # React components
│   ├── context/       # React context providers
│   ├── hooks/         # Custom React hooks
│   ├── middleware/    # Next.js middleware
│   ├── scripts/       # Utility scripts
│   └── services/      # Service layer
├── .env.local         # Environment variables
└── ...                # Config files
```

## Deployment

The application can be deployed to Vercel:

```bash
npm run build
```

For more information on deployment, see the [Next.js deployment documentation](https://nextjs.org/docs/deployment).

## License

This project is licensed under the MIT License - see the LICENSE file for details.
