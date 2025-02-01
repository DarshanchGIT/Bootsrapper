### Documentation of Commands

1. **Initialise new node project(this will create new package.json)**
    
    ```bash
    pnpm init
    
    ```
    
2. **Install dependencies:**
    
    ```bash
    *Necessary one's for TS:* pnpm add tyepscript ts-node @types/node nodemon
    *Dependencies of your choice:* pnpm add express @types/express
    
    ```
    
3. **Initialising typescript:(this will create tsconfig.json)**
    
    ```bash
    pnpm tsc --init
    *DESCRIPTIION: change rootDir to './src' and outDir  to './dist'*
    
    ```
    
4. **Make folders and files**
    
    ```bash
    mkdir src
    touch index.ts
    mkdir dist
    
    ```
    
5. Modify package.json  
    
    ```bash
    **Changes:**
    1. *Add dev script to get realtime server through Nodemon*
    2*. Automatic build from ./src/index.ts to ./dist/index.js
    
    PACKAGE.json will look something like this:-
    
    {
      "name": "mytest",
      "version": "1.0.0",
      "description": "",
      "main": "index.ts",
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "dev": "nodemon ./dist/index.js",
        "build":"npx tsc"
      },
      "keywords": [],
      "author": "",
      "license": "ISC",
      "dependencies": {
        "@types/express": "^5.0.0",
        "@types/jsonwebtoken": "^9.0.8",
        "express": "^4.21.2",
        "jsonwebtoken": "^9.0.2",
        "nodemon": "^3.1.9",
        "ts-node": "^10.9.2",
        "typescript": "^5.7.3"
      }
    }*
    ```
    
6. Run Commands
    
    ```json
    pnpm run build(for build process)
    pnpm run dev(listen the server)
    ```
