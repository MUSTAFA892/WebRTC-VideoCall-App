
# WebRTC Video Call App

This project is a web-based video calling application utilizing WebRTC technology to enable real-time peer-to-peer communication between users.

## Features

- **Real-Time Video Calls**: Connect with others through live video streaming.
- **Peer-to-Peer Communication**: Direct connection between users without the need for intermediary servers.
- **Responsive Design**: Accessible on various devices with adaptive layouts.

## Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/): JavaScript runtime for server-side operations.
- [npm](https://www.npmjs.com/): Node package manager, typically included with Node.js.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/MUSTAFA892/WebRTC-VideoCall-App.git
   ```

2. **Navigate to the Project Directory**:

   ```bash
   cd WebRTC-VideoCall-App
   ```

3. **Install Dependencies**:

   - For the server:

     ```bash
     cd server
     npm install
     ```

   - For the client:

     ```bash
     cd ../client
     npm install
     ```

## Usage

1. **Start the Server**:

   ```bash
   cd server
   npm start
   ```

2. **Start the Client**:

   In a new terminal window:

   ```bash
   cd client
   npm start
   ```

3. **Access the Application**:

   Open your web browser and navigate to `http://localhost:3000` to use the video call app.

## Project Structure

- `client/`: Contains the front-end React application.
- `server/`: Houses the back-end Node.js server with WebSocket integration.

## JSX Files Overview

The React components are structured as follows:

### `App.jsx`

This is the root component of the React application. It sets up the main structure and routing for the app.

- **Imports**: Imports necessary modules and components, including React, React Router (`BrowserRouter`, `Routes`, `Route`), and the `VideoCall` component.
- **Component Structure**: Wraps the application in a `BrowserRouter` to enable routing. Defines routes using `Routes` and `Route`, mapping paths to components.
- **Routing**: Typically, the main route (`/`) renders the `VideoCall` component, which manages the core video calling functionality.

### `VideoCall.jsx`

This component manages the video call interface and functionality.

- **State Management**: Utilizes React's `useState` and `useEffect` hooks to manage component state and side effects.
- **Peer Connection**: Establishes a WebRTC peer connection using the `RTCPeerConnection` API. Handles the creation of offer and answer SDP (Session Description Protocol) messages for initiating and responding to connection requests.
- **Media Streams**: Accesses the user's media devices (camera and microphone) using `navigator.mediaDevices.getUserMedia`. Displays local and remote video streams in `video` elements.
- **Signaling**: Communicates with the signaling server (typically via WebSockets) to exchange SDP messages and ICE (Interactive Connectivity Establishment) candidates, facilitating the peer-to-peer connection setup.

### `Chat.jsx`

This component provides a text chat interface alongside the video call.

- **State Management**: Manages chat messages and input using React's `useState` hook.
- **Message Handling**: Sends and receives chat messages through the signaling server, allowing text communication between connected peers.
- **UI Elements**: Renders a list of chat messages and an input field for composing new messages. Handles form submission to send messages.

## Technologies Used

- **Front-End**:
  - React: For building the user interface.
  - HTML/CSS: Structure and styling of the application.

- **Back-End**:
  - Node.js: Server-side JavaScript runtime.
  - WebSocket: For real-time communication between clients.

- **WebRTC**: Enables peer-to-peer video and audio communication directly between browsers.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes with descriptive messages.
4. Push your branch and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

