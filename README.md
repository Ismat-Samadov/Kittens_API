# Kittens API

This is a simple Ruby on Rails application that serves as an API for managing kitten data. It allows you to perform CRUD operations on kitten records via JSON requests.

## Setup Instructions

Follow these steps to set up and run the Kittens API locally:

### Prerequisites

Make sure you have the following installed:

- Ruby (version 2.7.0 or higher)
- Rails (version 6.0.0 or higher)
- Git

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Ismat-Samadov/Kittens_API.git
   ```

2. Navigate into the project directory:

   ```bash
   cd Kittens_API
   ```

3. Install dependencies:

   ```bash
   bundle install
   ```

4. Create and migrate the database:

   ```bash
   rails db:create
   rails db:migrate
   ```

### Usage

To run the application, start the Rails server:

```bash
rails server
```

The API endpoints will be available at `http://localhost:3000/kittens`.

### API Endpoints

- **GET /kittens**: Retrieve a list of all kittens.
- **GET /kittens/:id**: Retrieve a specific kitten by its ID.
- **POST /kittens**: Create a new kitten record.
- **PUT /kittens/:id**: Update an existing kitten record.
- **DELETE /kittens/:id**: Delete a kitten record.

### Testing the API

You can test the API endpoints using tools like `curl` or Postman. Here are some examples:

#### Retrieve all kittens

```bash
curl http://localhost:3000/kittens
```

#### Retrieve a specific kitten

```bash
curl http://localhost:3000/kittens/1
```

#### Create a new kitten

```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"Fluffy","age":2,"cuteness":9,"softness":8}' http://localhost:3000/kittens
```

#### Update an existing kitten

```bash
curl -X PUT -H "Content-Type: application/json" -d '{"name":"Snowball","age":3,"cuteness":10,"softness":9}' http://localhost:3000/kittens/1
```

#### Delete a kitten

```bash
curl -X DELETE http://localhost:3000/kittens/1
```

## Acknowledgements

This project is part of the Ruby on Rails Course by [The Odin Project](https://www.theodinproject.com/). Special thanks to the instructors for providing the guidance and resources.