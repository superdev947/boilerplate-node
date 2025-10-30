# Node.js TypeScript Boilerplate

A production-ready backend boilerplate built with Node.js, TypeScript, Express, MongoDB, and Redis. This project provides a solid foundation for building scalable REST APIs with modern best practices and developer-friendly tooling.

## 🚀 Features

- **TypeScript** - Full TypeScript support with strict type checking
- **Express.js** - Fast, unopinionated web framework
- **MongoDB** - NoSQL database integration with Mongoose ODM
- **Redis** - In-memory data store for caching
- **Security** - Helmet.js for securing Express apps
- **CORS** - Cross-Origin Resource Sharing enabled
- **Compression** - Response compression middleware
- **Hot Reload** - Fast development with ts-node-dev
- **Path Aliases** - Clean imports with TypeScript path mapping
- **ESLint** - Code quality and style checking
- **Environment Variables** - Configuration management with dotenv

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **MongoDB** (running locally or remote connection)
- **Redis** (running locally or remote connection)

## 🛠️ Installation

1. **Clone the repository**

```bash
git clone <repository-url>
cd boilerplate-node
```

2. **Install dependencies**

```bash
npm install
```

3. **Configure environment variables**

Create a `.env` file in the root directory:

```env
PORT=3003
MONGODB_URI=mongodb://127.0.0.1:27017/your-database-name
WORKER=main
```

## 🏃 Running the Application

### Development Mode

Run with hot-reload enabled:

```bash
npm run dev
```

### Production Mode

Start the application:

```bash
npm start
```

### Build for Production

Compile TypeScript to JavaScript:

```bash
npm run build
```

The compiled files will be in the `dist` directory.

## 📁 Project Structure

```
boilerplate-node/
├── src/
│   ├── index.ts              # Application entry point
│   ├── system/               # Core system modules
│   │   ├── config.ts         # Configuration management
│   │   ├── express.ts        # Express server setup
│   │   ├── mongo.ts          # MongoDB connection
│   │   ├── redis.ts          # Redis connection
│   │   └── index.ts          # System module exports
│   └── workloads/            # Business logic and routes
│       └── index.ts          # Workload entry point
├── package.json              # Project dependencies
├── tsconfig.json             # TypeScript configuration
└── README.md                 # Project documentation
```

## 🔧 Configuration

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Server port | `3003` |
| `MONGODB_URI` | MongoDB connection string | `mongodb://127.0.0.1:27017/casino` |
| `WORKER` | Worker identifier | - |

### TypeScript Configuration

The project uses modern TypeScript settings:
- **Target**: ESNext
- **Module**: NodeNext
- **Strict mode**: Enabled
- **Path aliases**: `src/*` for clean imports

## 🧩 Architecture

### Bootstrap Flow

1. **Initialize** - Connect to MongoDB and Redis
2. **Configure** - Load Express middlewares (Helmet, CORS, Compression)
3. **Run** - Start the HTTP server
4. **Load** - Initialize workloads and routes

### Middleware Stack

The Express server is configured with:
- **Helmet** - Security headers
- **Compression** - Response compression
- **JSON Parser** - Request body parsing
- **URL Encoder** - Form data parsing
- **CORS** - Cross-origin requests

## 📝 Development

### Code Linting

Run ESLint to check code quality:

```bash
npm run lint
```

### Adding Routes

Add your routes and business logic in the `src/workloads` directory. Import and initialize them in `src/index.ts`.

### Path Aliases

Use clean imports with the `src/*` alias:

```typescript
import { config } from "src/system/config";
import { someUtil } from "src/utils/helper";
```

## 🏗️ Building

The build process:
1. Removes the old `dist` directory
2. Compiles TypeScript files to JavaScript
3. Outputs to the `dist` directory

## 📦 Dependencies

### Core Dependencies
- `express` - Web framework
- `mongoose` - MongoDB ODM
- `redis` - Redis client
- `dotenv` - Environment configuration
- `helmet` - Security middleware
- `cors` - CORS middleware
- `compression` - Response compression
- `ethers` - Ethereum library
- `cron` - Job scheduling
- `cross-fetch` - Cross-platform fetch

### Development Dependencies
- `typescript` - TypeScript compiler
- `ts-node` - TypeScript execution
- `ts-node-dev` - Development with hot reload
- `eslint` - Code linting
- `@typescript-eslint/*` - TypeScript ESLint support

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
