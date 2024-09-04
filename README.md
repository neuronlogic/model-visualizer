# Custom Model Visualizer

## Overview

This project provides a custom model visualizer inspired by Netron. It includes a web interface to visualize machine learning models and supports integration with a backend API. The backend server can be managed with PM2 for background operations.

## Getting Started

### Prerequisites

- Node.js (v18.x or later)
- npm (Node Package Manager)
- PM2 (for managing background processes)[Optional]

### Configuration

1. **Update Backend URL**

   Modify the backend URL in the `source/config.js` file:

   ```javascript
    API_URL: 'your_backend_url'
   ```
   Example:
   ```javascript
    API_URL: 'http://localhost:8081'
   ```

### Running the Project

1. **Start the Development Server**

   ```bash
   npm run server
   ```

   This command will start the development server, and you can access the web interface through your browser.

2. **Using PM2 for Background Server**[Optional]

   To run the server as a background process with PM2:

   ```bash
   pm2 start start.sh --name "model-visualizer"
   ```

   This command will start the server with PM2, allowing you to manage it more efficiently in the background.

### Scripts

- **Start Server**: `npm run server`
- **Start with PM2**: `pm2 start start.sh --name "model-visualizer"`

### Project Structure

- `source/config.js`: Configuration file where the backend URL is set.
- `start.sh`: Script to start the server for PM2.