## Mini-Reddit Clone Documentation

### Project Overview
This project is a mini-Reddit clone, designed to provide RESTful APIs for users to create posts, comment on posts, and upvote/downvote both posts and comments. The goal is to create a simplified version of the popular social platform Reddit.

### Technologies Used
- Node.js with Express.js for the backend server
- MongoDB with Mongoose for the database
- JSON Web Tokens (JWT) for user authentication
- bcrypt.js for password hashing
- Axios for making HTTP requests in the frontend (optional)

### Folder Structure
```
mini-reddit-clone
│   README.md
│   package.json   
│   server.js
│
└───models
│   │   user.js
│   │   post.js
│   │   comment.js
│   
└───routes
│   │   authRoutes.js
│   │   postRoutes.js
│   │   commentRoutes.js
│
└───controllers
│   │   authController.js
│   │   postController.js
│   │   commentController.js
│   
└───middlewares
│   │   authMiddleware.js
│   
└───config
    │   config.js
```

### Features

#### User Authentication [8 marks]
- **Sign Up**:
  - Endpoint: `POST /api/signup`
  - Allows users to register with their username, email, and password.
  - Passwords are securely hashed using bcrypt before storing in the database.

- **Login**:
  - Endpoint: `POST /api/login`
  - Allows registered users to login with their credentials.
  - Returns a JWT token for authenticated requests.

#### Post CRUD Operations [9 marks]
- **Create a Post**:
  - Endpoint: `POST /api/posts`
  - Authenticated users can create new posts with a title and content.

- **Read a Post**:
  - Endpoint: `GET /api/posts/:postId`
  - Allows users to view a specific post by its ID.

- **Update a Post**:
  - Endpoint: `PUT /api/posts/:postId`
  - Allows the author of a post to update its title or content.

- **Delete a Post**:
  - Endpoint: `DELETE /api/posts/:postId`
  - Allows the author of a post to delete it permanently.

#### Comments on Posts with CRUD Operations [9 marks]
- **Create a Comment**:
  - Endpoint: `POST /api/posts/:postId/comments`
  - Users can add comments to a specific post.

- **Read Comments on a Post**:
  - Endpoint: `GET /api/posts/:postId/comments`
  - Allows users to view all comments on a post.

- **Update a Comment**:
  - Endpoint: `PUT /api/posts/:postId/comments/:commentId`
  - Comment authors can update the text of their comments.

- **Delete a Comment**:
  - Endpoint: `DELETE /api/posts/:postId/comments/:commentId`
  - Allows the author of a comment to delete it from the post.

#### Upvoting and Downvoting System for Posts and Comments [9 marks]
- **Upvoting a Post**:
  - Endpoint: `PUT /api/posts/:postId/upvote`
  - Allows users to upvote a post, increasing its upvote count.

- **Downvoting a Post**:
  - Endpoint: `PUT /api/posts/:postId/downvote`
  - Allows users to downvote a post, increasing its downvote count.

- **Upvoting a Comment**:
  - Endpoint: `PUT /api/posts/:postId/comments/:commentId/upvote`
  - Allows users to upvote a comment, increasing its upvote count.

- **Downvoting a Comment**:
  - Endpoint: `PUT /api/posts/:postId/comments/:commentId/downvote`
  - Allows users to downvote a comment, increasing its downvote count.

#### Integration of All Parts [10 marks]
- The project integrates user authentication, post CRUD operations, comment CRUD operations, and the upvoting/downvoting system into a cohesive application.
- The API endpoints are designed to work seamlessly together, providing a full-featured mini-Reddit experience.

### Deployment
The project can be deployed on any platform that supports Node.js applications, such as Heroku, AWS, or DigitalOcean. Here are the steps to deploy:

1. Clone the repository: `git clone https://github.com/your-username/mini-reddit-clone.git`
2. Navigate to the project directory: `cd mini-reddit-clone`
3. Install dependencies: `npm install`
4. Set up your environment variables (e.g., MongoDB URI, JWT secret) in a `.env` file.
5. Start the server: `npm start`

### GitHub Repository
The project's GitHub repository can be found at: https://github.com/MrRushikesh/Rushikesh_Ingale_Node_2_25th_Feb_2024

### Thoughts During Assignment Creation
During the assignment creation, the main focus was on creating a solid backend structure using Node.js and Express.js. The use of MongoDB with Mongoose provided a flexible and scalable database solution for storing user data, posts, and comments.

Implementing user authentication with JWT tokens ensured secure access to the API endpoints. CRUD operations for posts and comments were designed to be straightforward and intuitive for users.

The upvoting and downvoting system added a layer of engagement and interaction to the application, allowing users to express their opinions on posts and comments.

Overall, the project aimed to replicate core functionalities of Reddit while providing a clean and maintainable codebase.

### Future Improvements
- Implement frontend using a modern framework like React.js or Vue.js for a better user interface.
- Add more validation and error handling for robustness.
- Implement pagination for posts and comments to handle large amounts of data efficiently.
- Implement user roles and permissions for more granular control.
  
This concludes the documentation for the Mini-Reddit Clone project. Thank you for reviewing!
