## Node v18

## A  App Node App using NodeJs, Express, Mongo, using Typescript

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts
`npm run dev`<br>

## Create a .env root of the project
```env
PORT=8004
MONGOURI=mongodb://localhost:27017/
REMOTEURI=<YOUR_REMOTE_URL>
NODE_ENV=devlopment
JWTKEY=<YOUR_JWT_KEY>
TZ = Asia/Calcutta
```

## Upload API

`http://localhost:8004/capture-global`<br>

```javascript
form-data
body {
  captureImage:File
}
```

## Global quick snippets for VS-Code for this project

`asyncf`<br>
`logs`<br>

### Rest Client Configuration

install rest client vscode extension.
`https://marketplace.visualstudio.com/items?itemName=humao.rest-client` <br>

```http
# Example GET request
GET https://api.example.com/users

# Example POST request with JSON body
POST https://api.example.com/users
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com"
}
```

```http
@base_url = https://api.example.com

### GET Request - Users Endpoint ###
GET {{base_url}}/users

### POST Request - Create User Endpoint ###
POST {{base_url}}/users
Content-Type: application/json

{
    "username": "john_doe",
    "email": "john@example.com"
}

### GET Request - Specific User Endpoint ###
GET {{base_url}}/users/123
```

### Mongoose model example using typescript.

```typescript
import { Document, Schema, model } from 'mongoose';

// Interface representing the user structure
interface User extends Document {
  username: string;
  email: string;
  password: string;
  // You can add other fields as needed
}

// Define a mongoose schema based on the interface
const UserSchema = new Schema<User>({
  username: { type: String, required: true },
  email: { type: String, required: true },
  password: { type: String, required: true },
  // Define other schema fields here
});

// Create and export the Mongoose model
const UserModel = model<User>('User', UserSchema);

export default UserModel;
```
