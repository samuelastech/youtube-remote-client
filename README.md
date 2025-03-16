# YouTube Remote Control Client

A web-based client application for remotely controlling YouTube playback. This client connects to a Go-based server that controls YouTube via system events.

## Features

- Real-time control of YouTube playback via WebSocket connection
- Dynamic server connection management
- Playback controls:
  - Play/Pause
  - Next/Previous video
  - Volume control
  - Open YouTube URLs

## Usage

1. Enter the WebSocket server URL (e.g., `ws://localhost:8082/ws`)
2. Click "Connect" to establish connection with the server
3. Once connected, you can:
   - Enter a YouTube URL and click "Open URL" to open it in Chrome
   - Use playback controls (Play/Pause, Previous, Next)
   - Adjust volume using the slider or +/- buttons

## Server

This client works with the YouTube Remote Control server located at `samuelastech/youtube-remote`. The server:
- Listens on port 8080 for WebSocket connections
- Controls YouTube via system events (AppleScript on macOS)
- Handles commands for playback control

## Cross-Computer Control

One of the key features of this application is the ability to control YouTube playback from any computer on the network:

1. Run the server on the computer where YouTube will be controlled
2. Make sure the server is accessible on your network (check firewall settings if needed)
3. From any other computer on the network:
   - Open the client in a web browser
   - Connect to the server using its network address (e.g., `ws://192.168.1.100:8080/ws`)
   - Control YouTube playback remotely
