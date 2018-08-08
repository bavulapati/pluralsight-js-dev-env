>[Tools](./Tools-decisions.md)
#   Environment setup
*   **Git**
    *   Create a repository in *GitLab* with README.md
    *   Clone the repository
    *       $ git clone gitlab.com/remoterepo as repo
    *   Add the .gitignore file to ignore *node modules* and *temporary files/directories*
*   **Node**
    *   Install node. Node can be installed [here](https://nodejs.org/en)
    *   Node and npm installation can be verified with
    *       $ node -v
    *       $ npm -v
    *   Initialize node project with
    *       $ cd project_dir
    *       $ npm init
    *   *package.json* file will be created
*   **Node Security**
    *   Create npm script to check node modules vulnerabilities
    *       "check": "npm audit"
*   **Electron**
    *   Install electron as dev dependency
    *       $ npm install electron -D
*   **TypeScript**
    *   Install typescript and tslint as dev dependencies as they are peer-dependent
    *       $ npm install typescript tslint -D
    *   Initialize project with typescript
    *       $ ./node_modules/.bin/tsc --init
    *   *tsconfig.json* will be created
    *   Create npm script to compile typescript files to ecmascript6 js files
    *       "build-ts": "tsc"
*   **TSLint**
    *   Initialize project with tslint
    *       $ ./node_modules/.bin/tslint --init
    *   *tslint.json* will be created
    *   Create npm script for linttslint
    *       "tslint": "tslint -c ttslinttsconfig.json"
*   **Build**
    *   Create npm script combining audit, lint & tsc
    *       "build": "npm run check && npm run tslint && npm run build-ts"
*   **VS Code task runner**
    *   Press Cmd + Shift + B
    *   Select npm build
    *   Select no parsing of output
    *   *tasks.json* will be created
    *   Make display output true
    *   Add an identifier
    *   Make it default task
*   **Start**
    *   Create npm script for launching the project
    *       "start": "npm run build && electron ."
*   **Debug**
    *   Go to Debug tab of VS Code 
    *   Click on gear icon to configure the debug task
    *   Select node as the launch type
    *   launch.json will be created
    *   Add electron executable as specified [here](https://electronjs.org/docs/tutorial/debugging-main-process-vscode)
    *   Enable source mapping in *tsconfig.json*
    *   Specify the output directory in *tsconfig.json*
    *   Specify the entry js file in *package.json*
    *   Specify the preLaunchTask as build task as mentioned in tasks.json
*   **Package**
    *   Install electron-builder as dev dependency
    *       $ npm install electron-builder -D
    *   Place the icon.png in *build/icons* folder
    *   Place other icons in build folder following [this](https://www.electron.build/icons)
    *   Add the build configuration in *package.json*
    *   target platform, package, architecture, etc.,
    *   Create npm script for packaging project
    *       "pack": "build -l"