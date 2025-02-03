### Documentation of Commands

1. **Create a Vite project:**
    
    ```bash
    pnpm create vite@latest
    
    ```
    
2. **Install dependencies:**
    
    ```bash
    pnpm install
    
    ```
    
3. **Start the development server:**
    
    ```bash
    pnpm run dev
    
    ```
    
4. **Install Tailwind CSS (specific version) with `PostCSS` and `Autoprefixer`:**
    
    ```bash
    pnpm install tailwindcss@3.4.17 postcss autoprefixer
    
    ```
    
5. **Initialize Tailwind CSS configuration file:**
    
    ```bash
    npx tailwindcss init -p
    
    ```
    
6. Create `jsconfig.json` in root folder
    
    ```json
    {
        "compilerOptions": {
          // ...
          "baseUrl": ".",
          "paths": {
            "@/*": [
              "./src/*"
            ]
          }
          // ...
        }
    }
    ```
    
7. Edit `vite.config.js`
    
    ```jsx
    import path from "path";
    import react from "@vitejs/plugin-react";
    import { defineConfig } from "vite";
    
    export default defineConfig({
      plugins: [react()],
      resolve: {
        alias: {
          "@": path.resolve(__dirname, "./src"),
        },
      },
    });
    ```
7.2. Edit `tailwind.config.js`
    
    ```jsx
    module.exports = {
  content: [
    "./src/**/*.{js,ts,jsx,tsx}",
    "./public/index.html",         
  ],
  theme: {
    extend: {},
  },
  plugins: [],
};
    ```
    
8. Initialize `Shadcn`
    
    ```bash
    pnpm dlx shadcn@latest init
    ```
    
9. Now start importing component like this…
    
    ```bash
    pnpm dlx shadcn@latest add button
    ```
    

May be sometimes your `postcss` doesnt show up so you can run this command

```bash
npx tailwindcss init -p
```
