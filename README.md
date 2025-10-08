# Agency Web Application

This is a web application for an agency that showcases its services, projects, and blog posts. It includes an admin dashboard for managing content and integrates with various APIs for enhanced functionality.

## Project Structure

```
agency-web/
├── prisma/
│   ├── schema.prisma       # Defines the database schema
│   ├── seed.ts             # Script to seed the database with initial data
│   └── migrations/          # Holds migration files for database schema changes
├── src/
│   ├── pages/               # Contains all the pages of the application
│   │   ├── index.tsx        # Main entry point for the web application
│   │   ├── servicios.tsx     # Services page
│   │   ├── proyectos.tsx      # Projects page
│   │   ├── blog/             # Blog related pages
│   │   │   ├── index.tsx     # Lists all blog posts
│   │   │   └── [slug].tsx     # Renders a specific blog post
│   │   ├── contacto.tsx      # Contact form page
│   │   └── admin/            # Admin dashboard pages
│   │       ├── index.tsx     # Admin dashboard entry point
│   │       ├── proyectos.tsx  # Manage projects
│   │       └── posts.tsx      # Manage blog posts
│   ├── components/           # Reusable components
│   │   ├── ui/               # UI components
│   │   │   ├── Navbar.tsx     # Navigation bar component
│   │   │   ├── Footer.tsx     # Footer component
│   │   │   ├── Card.tsx       # Card component
│   │   │   ├── Modal.tsx      # Modal component
│   │   │   └── Button.tsx     # Button component
│   │   └── forms/            # Form components
│   │       ├── ContactForm.tsx # Contact form component
│   │       └── QuoteForm.tsx   # Quote request form component
│   ├── lib/                  # Library functions
│   │   ├── prisma.ts         # Initializes Prisma client
│   │   ├── auth.ts           # Authentication logic
│   │   ├── hubspot.ts        # HubSpot API integration
│   │   └── utils.ts          # Utility functions
│   ├── styles/               # Stylesheets
│   │   ├── globals.css       # Global CSS styles
│   │   └── tailwind.css      # Tailwind CSS styles
│   ├── types/                # TypeScript types
│   │   └── index.ts          # Exports TypeScript types
│   ├── middleware.ts         # Middleware functions
│   └── pages/api/           # API routes
│       ├── auth/            # Authentication routes
│       │   └── [...nextauth].ts # NextAuth.js authentication
│       ├── proyectos/        # Project-related API routes
│       │   ├── index.ts      # Projects API
│       │   └── [id].ts       # Specific project API
│       ├── posts/            # Blog post-related API routes
│       │   ├── index.ts      # Posts API
│       │   └── [id].ts       # Specific post API
│       ├── contacto.ts       # Contact form API
│       └── crm.ts           # CRM-related API
├── public/                  # Public assets
│   └── images/              # Public images
├── .env.example             # Environment variables template
├── package.json             # Project dependencies and scripts
├── tsconfig.json            # TypeScript configuration
├── .eslintrc.js             # ESLint configuration
├── .prettierrc              # Prettier configuration
└── README.md                # Project documentation
```

## Getting Started

1. Clone the repository:
   ```
   git clone <repository-url>
   cd agency-web
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Set up your environment variables by copying `.env.example` to `.env` and filling in the required values.

4. Run the database migrations:
   ```
   npx prisma migrate dev
   ```

5. Seed the database (if applicable):
   ```
   npx ts-node prisma/seed.ts
   ```

6. Start the development server:
   ```
   npm run dev
   ```

## Contributing

Feel free to submit issues and pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License. See the LICENSE file for details.