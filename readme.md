# TaskManager

This project was recently completed as part of my final assignments leading up to my exams. The task was to create a "task manager" using the React framework, functioning as a back-office where an admin can manage tasks and assign them to different employees. The project features admin/user login functionality and the ability to view, add, and assign tasks.

The backend is fully functional, while the frontend still needs a few final touches. You can find the frontend here: [TaskManager Frontend](https://github.com/Ungkarl/taskmanager-front). Both the frontend and backend are required to see the full result.

Here’s how to set up the backend. It requires a local MongoDB installation on your computer.

## Getting Started

Follow these steps:

### 1. Create a `.env` and `.env.local` file in the root of the project.

Insert the following content:

//Secret Variables for use in Server Application.
NODE_ENV=development

SERVER_PORT=3042 SERVER_HOST=http://localhost:3042

MONGODB_URI=mongodb://127.0.0.1:27017/mcdm-taskmanager

//JWT
JWT_EXPIRES_IN="1h" JWT_SECRET="8e18fa26acc704d3ca37fea29e17e8e024423a7c3eab4b76390a94ac579c20f0"

### 2. Run Seed in NPM Scripts.

Click the 'NPM Script' button in Visual Studio Code or use the following command: npm run seedAll

### 3. Open Mongo Compass.

Open Mongo Compass and view your "mcdm-taskmanager" database.

### 4. Start the server.

Run the "start" script in Visual Studio Code under 'NPM Scripts'.

### 5. Open Postman.

Import the `postman_01.json` file labeled as "Backend Taskmanager".  
Create a TaskManager environment in Postman, and add `api_local_path` set to `http://localhost:3042`.  
Also, create a `token` variable and use it when calling the "auth/signin" route.

Test the `Get Users` endpoint to ensure everything is working correctly.
