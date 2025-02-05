# Fertilizer Recommendation System (Client & Server)

## Overview

The **Fertilizer Recommendation System** is a web-based application designed to provide tailored fertilizer recommendations for different crops based on various factors like growth stage, soil properties, climate, and more. It consists of a **frontend** built with React and a **backend** powered by Flask, using Prolog for inference.

### Features

- **Real-time Fertilizer Recommendations** based on multiple parameters.
- **Interactive UI** allowing users to input their crop and environmental data.
- **Backend Inference Engine** using Prolog to calculate optimal fertilizer recommendations.

## Tech Stack

- **Frontend**: React, JSX, Vite (with `fetch` for API requests)
- **Backend**: Flask, Python, SWI-Prolog
- **Docker**: For containerization and deployment

## Installation

To get started with the project locally, follow the steps below:

### 1. Clone the Repository

```bash
git clone --recurse-submodules https://github.com/Programming-Sai/Fertilizer-Recommendation-System-Client-Server.git
cd Fertilizer-Recommendation-System-Client-Server
```

> [!NOTE]
> If you have already cloned the repository without --recurse-submodules, you can initialize the submodules separately with:

```bash
git submodule update --init --recursive
```

## Repositories

- **Frontend**: [Fertilizer Recommendation System Client](https://github.com/Programming-Sai/Fertilizer-Recommendation-System.git)
- **Backend**: [Fertilizer Recommendation System Server](https://github.com/Programming-Sai/Fertilizer-Recommendation-Engine-PROLOG.git)

### 2. Set Up the Backend

1. Navigate to the `server` directory.

   ```bash
   cd server
   ```

2. Install the necessary dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Start the backend server:

   ```bash
   python scripts/server.py
   ```

   The backend should now be running at `http://localhost:5000`.

### 3. Set Up the Frontend

1. Navigate to the `client` directory.

   ```bash
   cd client
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the frontend:

   ```bash
   npm run dev
   ```

   The frontend should now be accessible at `http://localhost:3000`.

### 4. Running the Full Application Using Docker

1. From the root directory, run:

   ```bash
   docker-compose up --build
   ```

   - To stop it you can run

   ```bash
     # Ctrl + C  # If running in the foreground
     docker-compose down  # To stop and remove containers
   ```

   This will build and run the frontend and backend containers.

## Usage

Once both the frontend and backend are running, you can navigate to `http://localhost:3000` in your browser and start using the application.

### How to Use

- Navigate to `Predict` from the Navbar to get to the parameters form
- Input the required crop, environmental and soil parameters.
- Click **Get Recommendations** to receive fertilizer recommendations tailored to your inputs.
