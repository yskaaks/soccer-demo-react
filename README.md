# React WebSockets Streaming App README
[![ru](https://img.shields.io/badge/lang-ru-yellow.svg)](https://github.com/yskaaks/soccer-demo-react/blob/main/README.ru.md)

## Project Overview

This React project demonstrates how to establish a WebSocket connection to stream data (specifically images) from a server (in this case, a Python WebSocket server) to a React application in real-time. The app receives base64 encoded image data for four different streams, decodes it, and displays the images on a webpage. If a stream's data is not available, a placeholder image is displayed instead.

## Getting Started

### Prerequisites

- Node.js (v12.x or higher recommended)
- A modern web browser that supports ES6 and WebSockets
- A running WebSocket server on `ws://localhost:5678` that sends image data encoded in base64 format, separated by semicolons (`;`)

### Installation

1. Clone the repository to your local machine:
```bash
git clone https://github.com/yskaak/soccer-demo-react
```
2. Navigate to the project directory:
```bash
cd Soccer-Analysis-Dashboard
```
3. Install the required npm packages:
```bash
npm install
```

### Running the Application

1. Start the React application:
```bash
npm start
```
This command runs the app in development mode. Open [http://localhost:3000](http://localhost:3000) to view it in your browser. The page will reload when you make changes.

## Project Structure

- `src/App.js`: Contains the main React component that manages the WebSocket connection and renders the image streams.
- `src/App.css`: Provides basic styling for the layout of the streaming images.
- `public/images/link.png`: Placeholder image shown when a stream's data is not available.
- `public/placeholder-image.jpg`: Displayed when an image fails to load.

## Key Features

- **Real-time Streaming**: The app connects to a WebSocket server at `ws://localhost:5678` and listens for incoming messages containing image data.
- **Dynamic Image Decoding**: Upon receiving a message, the app decodes the base64 encoded image data for each of the four streams and updates the UI to display these images.
- **Error Handling**: If an image fails to load (e.g., broken data), a generic placeholder image is used instead.

## Customizing the Application

- **WebSocket Server URL**: To change the WebSocket server's URL, modify the connection string in the `useEffect` hook within `src/App.js`.
- **Styling**: Customize the layout and styling by editing `src/App.css`.
- **Placeholder Images**: Replace `public/images/link.png` and `public/placeholder-image.jpg` with your own images if needed.

## Technologies Used

- React.js for the frontend UI.
- Bootstrap for responsive layout and styling.
- The WebSocket API for real-time communication between the client and server.

## Support

For any additional help or to report issues, please contact the project maintainers or submit an issue on the GitHub repository page.