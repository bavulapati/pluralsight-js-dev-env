>[Tools](./Tools-decisions.md)
# Project folder structure
* viewer
    *   **.vscode** -   files related to Visual studio code
    *   **build**   -   files used by electron-builder
    *   **css**     -   files related to styling
    *   **dist**    -   files, the distributables generated by electron-builder. Will not be in the git tracking
    *   **fonts**   -   All the fonts used
    *   **html**    -   The UI pages
    *   **images**  -   The images used in the UI
    *   **node_modules**    -   The project dev and production dependencies. This will be populated when we do npm install. This will not be in the git tracking
    *   **release** -   The js files generated from the ts files. This will be populated when we build the project. This will not be in the git tracking
    *   **src** -   The ts files that we write our code in
    *   ***.gitignore***    -   The file which will have the information of the folders/files to ignore tracking
    *   ***CONTRIBUTING.md***   -   The guidelines for gitlab
    *   ***LINCENSE***  - The lincense of usage for the repository
    *   ***package-lock.json*** -   generated and used by electron
    *   ***package.json***  -   the project metadata will be in this
    *   ***README.md*** -   description about the project
    *   ***tsconfig.json*** -   the configuration used by typescript
    *   ***tslint.json***   -   the configuration used by ts-lint