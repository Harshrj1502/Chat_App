# Chat App

A React chat client backed by an Express API, MongoDB, and Tencent Cloud Chat.

## Requirements

- Node.js and npm
- A MongoDB connection string
- Tencent Cloud Chat SDK app ID and secret key

## Configuration

Create `server/.env` with the server settings:

```env
PORT=8000
FRONTEND_URL=http://localhost:3000
MONGO_URI=mongodb://localhost:27017/chat_app
TRTC_APP_ID=your_app_id
TRTC_SECRET_KEY=your_secret_key
```

Create `frontend/.env` with the client settings:

```env
REACT_APP_API_URL=http://localhost:8000/api
REACT_APP_TRTC_APP_ID=your_app_id
```

Keep real credentials in these local environment files; they are excluded from Git.

## Run locally

Start the API in one terminal:

```sh
cd server
npm install
npm start
```

Start the React client in another terminal:

```sh
cd frontend
npm install
npm start
```

The client runs at `http://localhost:3000` and the API listens on port `8000` by default. The API health endpoint is `/api/health`.