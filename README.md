# File Manager API

A robust file management API built with Express.js, MongoDB, and Redis. This application allows users to upload, manage and share files with authentication and caching capabilities.

## Technologies

- **Express.js**: Backend framework
- **MongoDB**: Main database for storing user and file information
- **Redis**: Caching and session management
- **Node.js**: Runtime environment

## Key Features

- User authentication and session management
- File upload and storage management
- File access control (public/private)
- Folder structure support
- Image thumbnail generation
- Pagination for file listing

## API Endpoints

### Authentication

- `GET /connect` - User login (Basic Auth)
- `GET /disconnect` - User logout
- `POST /users` - Create new user

### Files

- `POST /files` - Upload a new file
- `GET /files/:id` - Get file by ID
- `GET /files` - List all files (with pagination)
- `PUT /files/:id/publish` - Make file public
- `PUT /files/:id/unpublish` - Make file private
- `GET /files/:id/data` - Get file content

### System

- `GET /status` - Check API status
- `GET /stats` - Get stats about users and files

## Installation

```bash
# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Edit .env with your MongoDB and Redis configurations

# Start the server
npm start
```

## Environment Variables

```
DB_HOST=localhost
DB_PORT=27017
DB_DATABASE=files_manager
FOLDER_PATH=/tmp/files_manager
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to the branch
5. Open a Pull Request
