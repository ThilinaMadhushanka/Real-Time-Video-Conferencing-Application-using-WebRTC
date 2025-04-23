# WebRTC Video Chat Application

A real-time video conferencing application built with WebRTC, Socket.IO, and Express.js that allows users to create and join video chat rooms, share screens, send messages, and communicate with minimal latency.

## Features

- **Real-time Video & Audio Communication**: Connect with peers through high-quality video and audio streams
- **Screen Sharing**: Share your screen with other participants
- **Text Chat**: Send and receive messages in real-time
- **Room-based Communication**: Create or join specific rooms for private conversations
- **Responsive Design**: Works on desktop and mobile devices
- **Audio/Video Controls**: Easily toggle microphone and camera
- **User Identification**: Display names for all participants

## Technology Stack

- **WebRTC**: For peer-to-peer media communication
- **Socket.IO**: For signaling and managing connections
- **Express.js**: Backend web server
- **HTML/CSS/JavaScript**: Frontend implementation

## Prerequisites

To run this application, you'll need:

- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/webrtc-video-chat.git
   cd webrtc-video-chat
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the server:
   ```
   node server.js
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:3004
   ```

## Usage Guide

### Setting Up a Room

1. Open the application in your browser
2. Enter a room ID of your choice (any alphanumeric string)
3. Click "Join Room"
4. Enter your name when prompted

### Joining an Existing Room

1. Open the application in your browser
2. Enter the room ID shared with you
3. Click "Join Room"
4. Enter your name when prompted

### Using the Controls

- **Mute/Unmute Voice**: Toggle your microphone on/off
- **Mute/Unmute Video**: Toggle your camera on/off
- **Share Screen**: Share your screen with other participants
- **Leave**: End your session and leave the room

### Using the Chat

- Type your message in the chat input box
- Press Enter or click the Send button to send your message
- Chat messages are visible to all participants in the room

## Architecture

The application follows a simple architecture:

- **Client-Side**: HTML/CSS/JavaScript with WebRTC for peer connections
- **Server-Side**: Express.js with Socket.IO for signaling

### WebRTC Flow

1. User creates or joins a room
2. Server notifies existing users about new connection
3. WebRTC signaling (offers/answers) occurs through Socket.IO
4. ICE candidates are exchanged to establish direct peer connections
5. Media streams are transmitted directly between peers

## Development Notes

### Important Components

- `server.js`: The main server file handling socket connections and room management
- `public/index.html`: The main HTML structure
- `public/main.js`: Client-side JavaScript handling WebRTC connections
- `public/main.css`: Styling for the application

### WebRTC Implementation Details

- Using STUN servers for NAT traversal
- Managing peer connections and media tracks
- Handling ICE candidates for establishing connections

## Troubleshooting

### Common Issues

- **Camera/Microphone Access**: Make sure your browser has permissions to access your camera and microphone
- **Connection Issues**: Check your network connection and firewall settings
- **Screen Sharing Not Working**: Ensure your browser supports screen sharing (Chrome, Firefox, Edge)

### Browser Compatibility

This application works best in:
- Google Chrome (latest version)
- Mozilla Firefox (latest version)
- Microsoft Edge (Chromium-based)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- WebRTC community for documentation and examples
- Socket.IO for making real-time communication easier
