# Jobify

Jobify is a sleek and efficient web application designed to help you manage your job search with ease. Built with **Next.js**, **TypeScript**, and **Tailwind CSS**, it provides a clean, responsive interface to track your job applications, interviews, and rejections.

---

## Features

- **Intuitive Dashboard**: A centralized view to see all your application statuses at a glance.
- **Secure Authentication**: User sign-up and sign-in are handled securely with **Clerk**.
- **Application Tracking**: Log new job applications with key details like company name, position, date applied, and status.
- **Interview Scheduling**: Keep a record of your upcoming interviews, including dates, times, and notes.
- **Rejection Log**: Maintain a log of rejections to track your progress and learn from the experience.
- **Dynamic Data**: Filtering: Use a search input to quickly find specific applications.
- **Pagination**: Navigate through your list of applications with ease, ensuring the application remains fast and responsive even with a large number of entries.
- **Responsive Design**: A beautiful, mobile-friendly interface powered by Tailwind CSS.
- **Type Safety**: Built with TypeScript to ensure a robust and error-free development experience.

---

## Technologies Used

- **Next.js**: A powerful React framework for building fast, full-stack applications.
- **TypeScript**: A superset of JavaScript that adds static typing, enhancing code quality and developer experience.
- **Tailwind CSS**: A utility-first CSS framework for rapidly building custom designs.
- **Clerk**: A complete user management and authentication solution for modern applications.
- **Prisma**: A next-generation ORM for Node.js and TypeScript, used for database access.
- **PostgreSQL**: The relational database used to store application data.
- **Vercel**: The platform used for deployment.

---

## Getting Started

Follow these steps to get a copy of the project up and running on your local machine.

### Prerequisites

You'll need to have Node.js and npm (or yarn) installed.

- **Node.js**: [https://nodejs.org/](https://nodejs.org/)
- **npm**: Comes with Node.js
- **yarn**: `npm install --global yarn`

### Installation

1.  Clone the repository:

    ```bash
    git clone [repository-url]
    cd application-tracker
    ```

2.  Install dependencies:

    ```bash
    npm install
    # or
    yarn
    ```

### Database Setup with Prisma and PostgreSQL

1.  Make sure you have a **PostgreSQL** database running, either locally or hosted.
2.  Set up your database connection string in the `.env.local` file. Replace the example string with your actual database URL.
    ```bash
    DATABASE_URL="postgresql://[user]:[password]@[host]:[port]/[database-name]"
    ```
    For a local instance, it might look like this:
    ```bash
    DATABASE_URL="postgresql://postgres:mysecretpassword@localhost:5432/jobify_db"
    ```
3.  Push the Prisma schema to your database to create the tables.
    ```bash
    npx prisma db push
    ```
4.  Generate the Prisma client based on your schema.
    ```bash
    npx prisma generate
    ```
5.  Add your Clerk API keys to the `.env.local` file. You can get these from your Clerk dashboard.
    ```bash
    NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_your_publishable_key
    CLERK_SECRET_KEY=sk_your_secret_key
    ```

### Running the Development Server

1.  Start the development server:
    ```bash
    npm run dev
    # or
    yarn dev
    ```
2.  Open [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) in your browser to see the application. The page will auto-update as you edit the code.

---

## Project Structure

```
/
├── components/          # Reusable UI components
├── prisma/              # Prisma schema and migrations
├── pages/               # Next.js pages/routes
│   ├── api/             # API routes
│   └── _app.tsx
│   └── index.tsx
├── public/              # Static assets (images, etc.)
├── styles/              # Global styles
├── types/               # TypeScript type definitions
├── .env.local           # Environment variables
├── next.config.js       # Next.js configuration
├── package.json
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

---

## Contributing

We welcome contributions\! Please feel free to open a pull request or submit an issue if you find a bug or have a suggestion for a new feature.

1.  Fork the repository.
2.  Create a new branch: `git checkout -b feature/your-feature-name`
3.  Commit your changes: `git commit -m 'feat: add your feature'`
4.  Push to the branch: `git push origin feature/your-feature-name`
5.  Open a pull request.

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.
