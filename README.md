# Laravel + Vue 3 (JSX) Boilerplate

## Quick Start

### Repository

GitHub: [https://github.com/shubham-ynr/laravue-jsx](https://github.com/shubham-ynr/laravue-jsx)

### Create a New Project

To create a new Laravel + Vue 3 (JSX) project using this boilerplate, run:

```bash
laravel new vue-jsx-app --using=shubham-ynr/laravue-jsx
```

This command will scaffold a new Laravel application with the `shubham-ynr/laravue-jsx` boilerplate, ready for development.

---

## Introduction

This Laravel + Vue boilerplate provides a clean and scalable foundation for building modern web applications using **Laravel** as the backend and **Vue 3 (JSX/Vue)** as the frontend with **Inertia.js**.

Unlike the official TypeScript starter, this boilerplate is built using standard **JSX/Vue**, making it simpler and faster to start for developers who prefer JavaScript.

It combines:

- ⚡ Laravel powerful backend
- ⚛️ Vue 3 (JSX/Vue)
- 🚀 Inertia.js (SPA experience without API complexity)
- 🎨 Tailwind CSS
- 🧩 shadcn-vue components
- 🔗 Ziggy for Laravel route usage inside Vue
- ⚡ Vite for lightning-fast development

This setup allows you to build modern single-page applications while keeping Laravel’s routing, controllers, middleware, and validation system.

---

## Tech Stack

### Backend

- Laravel 12+
- PHP 8.2+
- Inertia.js

### Frontend

- Vue 3 (SFC/JSX)
- Tailwind CSS
- shadcn-vue
- Radix Vue
- Ziggy
- Vite

---

## Features

- Server-side routing with SPA experience
- Laravel named routes available in Vue via Ziggy
- Clean project structure
- Modern UI setup with Tailwind + shadcn-vue
- Hot module reload with Vite
- Production-ready build setup

---

## Routing with Ziggy

This boilerplate integrates **Ziggy**, allowing you to use Laravel named routes inside Vue components.

Example:

```javascript
route("users.index");
route("users.show", 1);
```

## shadcn-vue Component Library

This boilerplate comes pre-configured to use [shadcn-vue](https://www.shadcn-vue.com/), a modern Vue component library built on top of Radix Vue and Tailwind CSS.

### Adding a shadcn-vue Component

To add a new component (e.g., Button) to your project, run:

```bash
npx shadcn-vue@latest add button
```

This will install the component and its dependencies, and generate the files in your project. You can then import and use the component in your Vue code:

```vue
<script setup>
import Button from "@/components/ui/button/Button.vue";

defineProps({
    title: {
        type: String,
        default: "Hello Vue!",
    },
});
</script>

<template>
    <div class="p-6 border rounded-xl shadow-lg bg-card text-card-foreground">
        <h2 class="text-xl font-bold mb-4">{{ title }}</h2>
        <p class="text-muted-foreground mb-4">
            This is a demo component using shadcn-vue and Vue 3.
        </p>
        <Button variant="default" @click="$emit('clicked')"> Click Me </Button>
    </div>
</template>
```

Explore all available components and usage examples in the [shadcn-vue documentation](https://www.shadcn-vue.com/docs/components).

---

## Tailwind CSS

This boilerplate uses [Tailwind CSS](https://tailwindcss.com/) for utility-first styling. Tailwind is already configured and ready to use out of the box.

You can start using Tailwind classes in your Vue components and Blade views immediately. For more details on how Tailwind works with Vite, see the [official Tailwind CSS + Vite guide](https://tailwindcss.com/docs/installation/using-vite).

---

## Inertia.js

This project uses [Inertia.js](https://inertiajs.com/) to provide a modern single-page application (SPA) experience while keeping server-side routing, controllers, and validation. Inertia acts as a bridge between Laravel and Vue, allowing you to build dynamic apps without writing a separate API.

**Key Points:**

- Use Laravel controllers to return Inertia responses.
- Vue pages are rendered as views, with props passed from the backend.
- No need for client-side routing libraries—use Laravel routes as usual.

Learn more in the [Inertia.js documentation](https://inertiajs.com/).

---

## Vite

Vite is used as the build tool for both development and production. It provides lightning-fast hot module replacement (HMR) and optimized builds.

**Common scripts:**

```bash
# Start development server
npm run dev

# Build for production
npm run build

# For dev Server (This will run php artisan serve and npm run dev)
npm run start
```

---

## Ziggy Usage

Ziggy makes Laravel named routes available in your Vue components. This enables you to generate URLs in JavaScript just like you do in PHP.

**Example:**

```javascript
const userUrl = route("users.show", 1); // /users/1
```

See the [Ziggy documentation](https://github.com/tighten/ziggy#usage) for more details.

---

## Project Scripts

The following npm scripts are available:

```json
"scripts": {
	"dev": "vite",
	"build": "vite build",
	"start": "concurrently \"npm run dev\" \"php artisan serve\""
}
```

---

## Directory Structure

- `resources/js/` — Vue app source code (components, pages, hooks, etc.)
- `resources/views/` — Blade templates
- `routes/web.php` — Laravel routes
- `app/Http/Controllers/` — Laravel controllers
- `config/` — Laravel configuration files

---

## Contributing

Feel free to open issues or submit pull requests to improve this boilerplate!
