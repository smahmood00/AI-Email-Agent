# 🚀 IntelliMail - AI-Powered Email Client

<div align="center">


[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)


**A minimalistic, AI-powered email client that revolutionizes email management**

</div>

---

## 🎯 Project Overview

I developed **IntelliMail** as a cutting-edge AI-powered email client that transforms how users interact with their email. This full-stack application combines modern web technologies with advanced AI capabilities to create an intelligent, efficient, and user-friendly email management experience.

### ✨ What Makes This Special

🤖 **AI-Driven Intelligence** - Built-in AI assistant powered by OpenAI GPT models for smart email composition, summarization, and responses

🔍 **Advanced RAG Search** - Sophisticated Retrieval Augmented Generation using Orama for lightning-fast, context-aware email search

📧 **Universal Integration** - Seamless connectivity with Gmail, Office365, and other major email providers via Aurinko API

⚡ **Real-time Sync** - Live email synchronization with intelligent threading and organization

💳 **Premium Subscriptions** - Integrated Stripe payment system for advanced features and premium tiers

🎨 **Modern UI/UX** - Sleek, responsive interface with dark mode support and keyboard-first navigation

---

## 🌟 Key Features

### 🤖 AI-Powered Capabilities
- **Smart Email Composition** - AI-assisted writing with auto-completion and suggestions
- **Intelligent Summarization** - Automatically generate concise summaries of long email threads
- **Context-Aware Responses** - AI-generated reply suggestions based on email content and history
- **Advanced Search** - Natural language search queries powered by embeddings and RAG technology

### 📨 Email Management
- **Multi-Provider Support** - Gmail, Office365, and other IMAP/SMTP providers
- **Real-time Synchronization** - Instant email updates across all devices
- **Smart Threading** - Intelligent conversation grouping and organization
- **Advanced Filtering** - Custom labels, categories, and automated sorting
- **Attachment Handling** - Secure file management and preview capabilities

### 🔐 Security & Authentication
- **Clerk Integration** - Secure user authentication and session management
- **OAuth 2.0** - Safe email provider connections without storing passwords
- **Data Encryption** - End-to-end encryption for sensitive email data
- **Privacy Controls** - Granular permissions and data access controls

### 💼 Premium Features
- **Usage Analytics** - Detailed insights into email patterns and productivity
- **Priority Support** - Enhanced customer service for premium users
- **Advanced AI Models** - Access to latest GPT models and features

---

## 🛠️ Tech Stack

### Frontend
- **[Next.js 14](https://nextjs.org/)** - React framework with App Router
- **[TypeScript](https://www.typescriptlang.org/)** - Type-safe development
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first styling
- **[Radix UI](https://www.radix-ui.com/)** - Accessible component primitives
- **[Framer Motion](https://www.framer.com/motion/)** - Smooth animations
- **[React Query](https://tanstack.com/query/latest)** - Server state management

### Backend & Database
- **[Prisma](https://www.prisma.io/)** - Type-safe database ORM
- **[PostgreSQL](https://www.postgresql.org/)** - Robust relational database
- **[tRPC](https://trpc.io/)** - End-to-end typesafe APIs
- **[Zod](https://zod.dev/)** - Schema validation

### AI & Search
- **[OpenAI API](https://openai.com/api/)** - GPT models for AI capabilities
- **[Orama](https://orama.com/)** - Full-text search engine
- **[@xenova/transformers](https://huggingface.co/docs/transformers.js/)** - Client-side ML models
- **Vector Embeddings** - Semantic search capabilities

### External Services
- **[Aurinko API](https://aurinko.io/)** - Email provider integration
- **[Clerk](https://clerk.com/)** - Authentication and user management

### Development Tools
- **[ESLint](https://eslint.org/)** - Code linting
- **[Prettier](https://prettier.io/)** - Code formatting
- **[Turbo](https://turbo.build/)** - High-performance build system

---

## 🏗️ Architecture Overview

```mermaid
graph TB
    A[Next.js Frontend] --> B[tRPC API Layer]
    B --> C[Prisma ORM]
    C --> D[PostgreSQL Database]
    B --> E[OpenAI API]
    B --> F[Aurinko Email API]
    B --> G[Stripe API]
    B --> H[Orama Search Engine]
    A --> I[Clerk Auth]
    J[Email Providers] --> F
    K[Vector Embeddings] --> H
    E --> K
```

### Core Components

1. **Frontend Layer** - Next.js app with server-side rendering and client-side interactions
2. **API Layer** - tRPC endpoints for type-safe client-server communication
3. **Database Layer** - Prisma ORM with PostgreSQL for data persistence
4. **AI Layer** - OpenAI integration for intelligent features
5. **Email Integration** - Aurinko API for multi-provider email access
6. **Search Engine** - Orama with vector embeddings for semantic search
7. **Authentication** - Clerk for secure user management
8. **Payment Processing** - Stripe for subscription management

---

## 📦 Installation & Setup

### Prerequisites

- **Node.js** 18.0 or higher
- **PostgreSQL** database
- **Git** for version control

### 1. Clone the Repository

```bash
git clone https://github.com/smahmood00/AI-Email-Agent.git
cd intellimail
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3. Environment Configuration

Create a `.env.local` file in the root directory:

```env
# Database
DATABASE_URL="postgresql://username:password@localhost:5432/intellimail"

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="pk_test_..."
CLERK_SECRET_KEY="sk_test_..."
NEXT_PUBLIC_CLERK_SIGN_IN_URL="/sign-in"
NEXT_PUBLIC_CLERK_SIGN_UP_URL="/sign-up"

# OpenAI
OPENAI_API_KEY="sk-..."

# Aurinko Email API
AURINKO_CLIENT_ID="your_aurinko_client_id"
AURINKO_CLIENT_SECRET="your_aurinko_client_secret"
AURINKO_SIGNING_SECRET="your_aurinko_signing_secret"

# Nylas
NYLAS_CLIENT_ID="your_nylas_client_id"
NYLAS_API_KEY="your_nylas_api_key"
GRAVATAR_API_KEY="your_gravatar_api_key"

# Stripe
STRIPE_SECRET_KEY="sk_test_..."
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="pk_test_..."
STRIPE_PRICE_ID="price_..."
STRIPE_WEBHOOK_SECRET="whsec_..."

# App Configuration
NEXT_PUBLIC_URL="http://localhost:3001"
```

### 4. Database Setup

```bash
# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma db push

# (Optional) Open Prisma Studio
npx prisma studio
```

### 5. Start Development Server

```bash
npm run dev
```

Visit [http://localhost:3001](http://localhost:3001) to see the application.

---

## 🚀 Usage Examples

### Basic Email Management

1. **Sign Up/Sign In** - Create an account or log in with existing credentials
2. **Connect Email Account** - Link your Gmail or Office365 account via OAuth
3. **Browse Emails** - Navigate through your inbox with threaded conversations
4. **Use AI Features** - Ask the AI assistant to help compose emails or summarize threads

### AI Assistant Commands

```
# Email composition
"Help me write a professional email to decline a meeting"

# Email search
"Find all emails from John about the project proposal"

# Email summarization
"Summarize this email thread for me"
```

### Keyboard Shortcuts

- `Cmd/Ctrl + K` - Open command palette
- `G + I` - Go to inbox
- `G + S` - Go to sent emails
- `C` - Compose new email
- `R` - Reply to email
- `/` - Search emails

---

## 📂 Project Structure

```
intellimail/
├── src/
│   ├── app/                    # Next.js app directory
│   │   ├── (auth)/            # Authentication routes
│   │   ├── api/               # API routes
│   │   ├── mail/              # Main email interface
│   │   └── components/        # Shared components
│   ├── components/            # UI components
│   │   └── ui/               # Reusable UI primitives
│   ├── hooks/                # Custom React hooks
│   ├── lib/                  # Utility functions
│   │   ├── aurinko.ts        # Email API integration
│   │   ├── embeddings.ts     # AI embeddings
│   │   ├── orama.ts          # Search engine
│   │   └── stripe.ts         # Payment processing
│   ├── server/               # Server-side code
│   │   └── api/              # tRPC routers
│   └── styles/               # Global styles
├── prisma/                   # Database schema
├── public/                   # Static assets
└── package.json             # Dependencies
```

---

## 🌐 Deployment

### Vercel Deployment

1. **Connect Repository**
   ```bash
   vercel --prod
   ```

2. **Environment Variables**
   - Add all environment variables in Vercel dashboard
   - Update URLs to production domains

3. **Database**
   - Use Vercel Postgres or external PostgreSQL provider
   - Run migrations on production database

### Docker Deployment

```dockerfile
# Dockerfile included in repository
docker build -t intellimail .
docker run -p 3000:3000 intellimail
```

### Manual Deployment

```bash
# Build the application
npm run build

# Start production server
npm run start
```

---

## 🧪 Development Guidelines

### Code Style

- **TypeScript** - Use strict typing throughout
- **ESLint** - Follow configured linting rules
- **Prettier** - Maintain consistent code formatting
- **Component Structure** - Use functional components with hooks

### Testing

```bash
# Run type checking
npm run type-check

# Run linting
npm run lint

# Format code
npm run format
```

### Database Changes

```bash
# Create migration
npx prisma migrate dev --name migration_name

# Reset database
npx prisma migrate reset

# Deploy migrations
npx prisma migrate deploy
```

---


### Development Setup

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Run in turbo mode
npm run dev --turbo
```

---

## 🙏 Acknowledgments

I built IntelliMail using these excellent tools and services:

- **[Next.js](https://nextjs.org/)** - The React framework for production
- **[OpenAI](https://openai.com/)** - AI models and API
- **[Clerk](https://clerk.com/)** - Authentication infrastructure
- **[Stripe](https://stripe.com/)** - Payment processing platform
- **[Aurinko](https://aurinko.io/)** - Email API integration
- **[Vercel](https://vercel.com/)** - Deployment and hosting
- **[Radix UI](https://www.radix-ui.com/)** - Unstyled, accessible components
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework

---


