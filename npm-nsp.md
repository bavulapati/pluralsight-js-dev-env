>[Tools](./Tools-decisions.md)
# node, npm, nvm, nsp
* nvm can be used to manage different versions of node
* npm comes with node installation. Node can be installed [here](https://nodejs.org/en)
* node and npm installation can be verified with
*       node -v
*       npm -v
* nsp can be used for scanning the packages for security
*       $ npm install -D nsp 
* preffered place for nsp check is at npm start. This slows down the starting of application but can avoid a lot of rework
*       $ nsp check
* node uses package.json for understanding the dependencies and metadata which can be generated using 
*       npm init
* electron can be installed using
*       npm install electron
