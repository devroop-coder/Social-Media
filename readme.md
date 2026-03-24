# Social Media Backend API

A Node.js backend API for a social media platform built with Express.js, MongoDB, and ImageKit.

## Features

- **Post Creation**: Create posts with images and captions
- **Image Upload**: Upload and store images using ImageKit
- **Database**: MongoDB integration for data persistence
- **File Handling**: Multer for efficient file processing

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB (Mongoose ODM)
- **File Storage**: ImageKit
- **File Upload**: Multer
- **Environment**: dotenv

## Installation

1. Clone the repository
```bash
git clone <repository-url>
cd "Social Media"
```

2. Install dependencies
```bash
npm install
```

3. Create a `.env` file in the root directory with your configuration:
```
MONGODB_URI=your_mongodb_connection_string
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_URL_ENDPOINT=your_imagekit_url_endpoint
```

## Getting Started

Start the server:
```bash
node server.js
```

The server will run on `http://localhost:3000`

## API Endpoints

### Create Post
- **Endpoint**: `POST /create-post`
- **Description**: Create a new post with an image and caption
- **Request**:
  - `image` (file): Image file to upload
  - `caption` (string): Caption for the post
- **Response**:
  ```json
  {
    "message": "Post created successfully",
    "post": {
      "_id": "...",
      "image": "image_url",
      "caption": "post_caption",
      "createdAt": "timestamp"
    }
  }
  ```

## Project Structure

```
├── server.js              # Entry point
├── package.json           # Dependencies
├── .env                   # Environment variables
├── src/
│   ├── app.js             # Express app configuration
│   ├── db/
│   │   └── db.js          # Database connection
│   ├── models/
│   │   └── post.model.js  # Post schema and model
│   └── services/
│       └── storage.service.js  # Image upload service
└── readme.md              # This file
```

## Dependencies

- **express** - Web framework
- **mongoose** - MongoDB ODM
- **multer** - File upload middleware
- **@imagekit/nodejs** - Image management service
- **dotenv** - Environment variable management

## Development

To add more endpoints or features, follow the existing structure:
1. Define models in `src/models/`
2. Create services in `src/services/`
3. Add routes in `src/app.js`

## License

ISC

## Author

Developed by **Devroop**

All rights and licenses to Devroop.
