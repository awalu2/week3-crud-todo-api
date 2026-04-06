# Todo API

A simple CRUD Todo API built for Week 3 of the presentation2 project. This RESTful API supports creating, reading, updating, and deleting todo items while keeping the implementation lightweight and easy to extend.

## Features

- Create new todo items with title, description, and status.
- Retrieve all todos or a single todo by ID.
- Update todo fields including text and completion status.
- Delete todo items by ID.
- RESTful endpoint design for easy integration with front-end apps.
- Input validation and consistent JSON response format.
- Lightweight and easy to extend for additional features.

## Getting Started

### Prerequisites

- Node.js 14+ or compatible runtime
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project folder:
   ```bash
   cd week3-crud-todo-api
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
   or
   ```bash
   yarn install
   ```

### Running the API

Start the server:
```bash
npm start
```

The API should run on the configured port, typically `http://localhost:3000`.

## API Endpoints

### Create a Todo

- Method: `POST`
- URL: `/todos`
- Body:
  ```json
  {
    "title": "Buy groceries",
    "description": "Milk, eggs, bread",
    "completed": false
  }
  ```
- Response: created todo item with ID.

### Get All Todos

- Method: `GET`
- URL: `/todos`
- Response: array of todo items.

### Get Todo by ID

- Method: `GET`
- URL: `/todos/:id`
- Response: single todo item.

### Update Todo

- Method: `PUT`
- URL: `/todos/:id`
- Body:
  ```json
  {
    "title": "Buy groceries and snacks",
    "description": "Milk, eggs, bread, chips",
    "completed": true
  }
  ```
- Response: updated todo item.

### Delete Todo

- Method: `DELETE`
- URL: `/todos/:id`
- Response: success message after deletion.

## Data Model

Each todo item typically contains:

- `id` - Unique identifier
- `title` - Short description of the task
- `description` - Detailed information about the task
- `completed` - Boolean status for completion
- `createdAt` / `updatedAt` - Timestamps (if supported)

## Development

During development, use:
```bash
npm run dev
```

This command usually runs the server with automatic reload support.

## Testing

If tests are included, run:
```bash
npm test
```

## Notes

- This project is designed for learning CRUD operations and API design.
- Expand it by adding authentication, persistence with a database, or filtering and pagination.

## License

This project is open source and available for use and modification.
