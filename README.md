# gyant-crud

GYANT Crud Challenge

## Installation

*Note: This application was developed using [Node.js](https://nodejs.org/) version 13.*

Download or clone this repository and:

### 1. Install Dependencies

Install all needed dependencies:
```sh
$ npm i
```

### 2. Set Environment Variables

You can choose to set env variables while starting the server, or you can create a `.env` file by creating a duplicate of `.env.sample`.

*Note: Due to the nature of the project, a `.env` file is already included.*

### 3. Start the server

After following the previous steps, you can start the application with:
```sh
$ npm start
```

*Note: The server will be available on port `3000`.* 

## Notes

There is already a user created in the database:
```json
{
    "name": "Doctor Who",
    "email": "who@doctor.com",
    "password": "qwerty"
}
```

After you review every case it might be useful to drop the collection and repopulate, so that you can test the application again with a clean state.
To do so, please complete the following requests:
1. DELETE http://localhost:3000/cases
2. POST http://localhost:3000/cases/import
