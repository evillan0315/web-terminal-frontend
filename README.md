# Terminal Frontend

A React-based frontend application for interacting with the `node-websocket` terminal server.

This project was generated using the Codejector LLM Code Generator

## Features

-   **Interactive Terminal**: Powered by XTerm.js, providing a full-featured pseudo-terminal experience.
-   **WebSocket Communication**: Connects to the backend via Socket.IO for real-time command execution and output streaming.
-   **Material UI**: Utilizes Material UI v6 for a clean and responsive user interface.
-   **Tailwind CSS**: Uses Tailwind CSS v4 for utility-first styling and responsive design.
-   **Nanostores**: Lightweight state management for global application state.
-   **Dark/Light Mode**: Supports theme switching.

## Prerequisites

-   Node.js (v18 or higher)
-   npm or Yarn
-   The `node-websocket` backend server running (typically on `http://localhost:3003`)

### Optional: Install GitHub CLI (gh CLI) on Ubuntu

If you need to interact with GitHub repositories from your terminal, you can install the GitHub CLI.

1.  Add GitHub's GPG key:
    ```bash
    curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /etc/apt/keyrings/githubcli-archive-keyring.gpg
    ```

2.  Add the GitHub CLI repository to your system's sources:
    ```bash
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
    ```

3.  Update your package list and install `gh`:
    ```bash
    sudo apt update
    sudo apt install gh
    ```

## Installation

1.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

## Configuration

Create a `.env` file in the project root directory (if it doesn't exist) and configure the WebSocket server URL:

```env
VITE_WS_URL=http://localhost:3003
```

Adjust `VITE_WS_URL` if your backend is running on a different address or port.

## Running the Frontend

1.  **Ensure the `node-websocket` backend server is running.**

2.  **Start the frontend development server:**
    ```bash
    npm run dev
    ```

    This will usually open the application in your browser at `http://localhost:5173` (or another available port).

## Project Structure

```
/
├── .env
├── .eslintrc.cjs
├── index.html
├── package-lock.json
├── package.json
├── postcss.config.js
├── README.md
├── src/
│   ├── api/                  (API client for potential REST calls)
│   │   └── fetch.ts
│   ├── components/
│   │   ├── icons/            (Custom SVG icons)
│   │   │   └── CarbonTerminal.tsx
│   │   └── Terminal/         (Terminal-related components and logic)
│   │       ├── api/          (Placeholder for terminal REST APIs, currently minimal)
│   │       │   └── terminal.ts
│   │       ├── services/     (Terminal-specific Socket.IO service)
│   │       │   └── terminalSocketService.ts
│   │       ├── stores/       (Terminal-specific nanostore)
│   │       │   └── terminalStore.ts
│   │       ├── types/        (Type definitions for terminal communication)
│   │       │   └── terminal.ts
│   │       ├── Terminal.tsx
│   │       ├── TerminalDialog.tsx
│   │       ├── TerminalSettingsDialog.tsx
│   │       └── TerminalToolbar.tsx
│   ├── services/             (General application services)
│   │   ├── authService.ts
│   │   └── socketClientFactory.ts
│   ├── stores/               (Global nanostores for application state)
│   │   ├── authStore.ts
│   │   ├── fileTreeStore.ts
│   │   ├── logStore.ts
│   │   └── themeStore.ts
│   ├── utils/                (General utility functions)
│   │   └── persistentAtom.ts
│   ├── App.tsx               (Main application component, sets up routing and theming)
│   ├── main.tsx              (Entry point)
│   └── index.css             (Tailwind base styles)
├── tailwind.config.ts
├── tsconfig.json
├── tsconfig.node.json
├── vite-env.d.ts
└── vite.config.ts
```

## 📧 Contact

Eddie Villanueva - [evillan0315@gmail.com](mailto:evillan0315@gmail.com)  
[LinkedIn](https://www.linkedin.com/in/eddie-villalon/)  
[GitHub](https://github.com/evillan0315)  