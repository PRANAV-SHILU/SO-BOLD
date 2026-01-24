# React Practice VeyondTech

> [!IMPORTANT]
> **WORK IN PROGRESS**
> This is my first developed site in React after learning the library. I am applying what I have learned to build this project.

## Overview

This project is a web application built with **React** and **Vite**, utilizing **React Router** for navigation. It represents a milestone in my learning journey, transitioning from vanilla web development to modern frontend frameworks.

## 🛠️ Tech Stack

- **Framework**: [React](https://react.dev/) (v19)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Routing**: [React Router](https://reactrouter.com/) (v7)
- **Linting**: ESLint

## 🏗️ Architecture & Features

### 1. Client-Side Routing

The application uses **React Router v7** for seamless client-side navigation.

- **`src/routes.jsx`**: Defines the central route configuration.
- **Nested Routes**: Utilizes nested functionality (e.g., `NewsLayout` wrapping category and news lists).
- **Dynamic Routing**: Supports dynamic segments like `/news/:id` and `/post/:postid`.
- **404 Handling**: Global "Page Not Found" strategies utilizing `*` path and `errorElement`.

### 2. Data Loading (Loaders)

This project leverages React Router 6.4+ **Data Loaders** to fetch data _before_ rendering route components.

- **`src/loaders/`**: Contains specific loader functions:
  - `NewsListLoader`: Fetches list of news items.
  - `categoryLoader`: Fetches available news categories.
  - `PostLoader`: Fetches details for a specific post.

_Note: 404 and Error handling pages are also implemented (`PageNotFound.jsx`, `ErrorElementPage.jsx`)._

### 3. Component Structure

- **Global Layouts**: `App.jsx` acts as the root layout (incorporating `Header` and `Footer`).
- **Reusable Components**: Located in `src/components/` (e.g., `Header.jsx`, `Footer.jsx`).
- **Pages**: Top-level route views in `src/pages/`.

## 📂 Detailed Project Structure

```
src/
├── components/       # Reusable UI components (Header, Footer)
├── layouts/          # Wrapper layouts (e.g., NewsLayout)
├── loaders/          # API fetch logic decoupled from UI
├── pages/            # Main views
│   ├── news/         # News-related sub-pages
│   ├── About.jsx     # Static pages
│   └── ...
├── App.jsx           # Root component (Layout)
├── routes.jsx        # Router configuration
└── main.jsx          # Entry point
```
