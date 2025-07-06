# Connectly App

Connectly App (based on Mirotalk) is a free, browser-based WebRTC video call solution, providing secure peer-to-peer audio/video conferencing with modern features and integrations. It is designed to be user-friendly, scalable, and easily deployable, with capabilities for chat, authentication, and more.

---

## Features

- High-quality video and audio calls via WebRTC
- Peer-to-peer and group conferencing
- Real-time chat functionality
- User authentication (OpenID Connect support)
- Integration with OpenAI services (ChatGPT, etc.)
- Secure communications with encryption
- Admin and moderation features
- Easy deployment with Docker and Node.js
- REST API with Swagger UI documentation
- Email notifications (via nodemailer)
- Environment-based configuration

---

## Technologies Used

- **Node.js** (server runtime)
- **Express.js** (web framework)
- **Socket.io** (real-time communication)
- **WebRTC** (video/audio streaming)
- **OpenAI** (AI integrations)
- **OpenID Connect (OIDC)** (authentication)
- **Docker** (containerization, optional)
- **Axios, dotenv, helmet, cors, compression, uuid, chokidar, js-yaml, swagger-ui-express** (various utilities)
- **Mocha, Nodemon, Prettier** (development tools)

For full dependencies, see [`package.json`](./package.json).

---

## Setup and Installation (Windows)

> **Note:** Run all commands in a terminal with Administrator privileges.

1. **Clone the repository:**
   ```powershell
   git clone https://github.com/Sa1f27/connectly-app.git
   cd connectly-app
   ```

2. **Configure environment variables:**
   - Ensure a `.env` file exists at the root. If missing, the setup script will copy `.env.template` to `.env` (edit as needed).

3. **Install Node.js (if not installed):**
   - Download from [https://nodejs.org/](https://nodejs.org/) and install.

4. **Install dependencies & run setup script:**
   - You can use the provided PowerShell script:
     ```powershell
     .\install.ps1
     ```
   - This will:
     - Ensure `.env` exists
     - Install Node.js dependencies (`npm install`)
     - Start the server (`npm start`)

---

## How to Run the Project

### Using npm (after setup)

```powershell
npm start
```
- The server will start, typically on port 3000 (customize in `.env` if needed).

### Development Mode (with hot reload):

```powershell
npm run start-dev
```

### Running with Docker

```powershell
npm run docker-build
npm run docker-run
```

Or, for advanced Docker usage (with mounted volumes and environment):

```powershell
npm run docker-run-vm
```

---

## Example Usage

- Open your browser and navigate to:  
  ```
  http://localhost:3000/
  ```
- Register/login (if authentication is enabled).
- Start or join a video call room.
