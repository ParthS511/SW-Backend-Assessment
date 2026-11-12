# UNSW Bionic Heart | Software Techincal Assesment

This assesment aims to gauge your current technical ability and give you a practical introduction to some of what we do here in UNSW Bionic Hearts. 

## Task
Implement the `POST /tasks` endpoint in `server.js`. It should read `title`, `description`, and `userId` from the JSON request body, validate the required fields, and check that the user exists in the provided mock `users` array.

If the request is valid, create a task with a unique ID, add it to the `tasks` array, and return it with HTTP `201 Created`. Return `400 Bad Request` for a missing or blank title or a missing user ID, and `404 Not Found` if the user does not exist. Tasks are stored in memory and will be cleared when the server restarts.

## Testing
1. Start the server in a terminal:
   ```bash
   node server.js
   ```
2. In a second terminal, run the success-case test:
   ```bash
   node test.js
   ```

The test sends a valid task request for user ID `1` and checks that the endpoint returns HTTP `201` with a task ID, the expected title, and the user ID. It prints `POST /tasks passed` if those checks succeed. If the test fails, make sure the server is running and the endpoint is implemented.
