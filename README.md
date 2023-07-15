https://www.notion.so/Node-js-e94226d1131040bdb71bd1b241c13801?pvs=4


# 1) Installation

- [ ]  Installer via le site Node.js → mais pour changer de version si plusieurs travaux avec versions différentes, il faudra désinstaller et ré installer
    
    [Node.js](https://nodejs.org/en)
    

- [ ]  Installer via NVM → Node Version Manager car permet de passer de version en version facilement
- [ ]  Utile quand on travaille sur plusieurs versions
    
    https://github.com/nvm-sh/nvm
    
    ### Install & Update Script
    
    To **install** or **update** nvm, you should run the [install script](https://github.com/nvm-sh/nvm/blob/v0.39.3/install.sh). To do that, you may either download and run the script manually, or use the following cURL or Wget command:
    
    ```jsx
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
    ```
    

# 2) Creation Serveur de base

- [ ]  Le site Node.js propose de la doc et un canva de base

```jsx
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

# 3) Initialiser un projet avec NPM

- [ ]  NPM → Node Packages Manager

### Basic NPM Commands

- `npm init`: Initializes a new npm package and creates a package.json file
- `npm install <package_name>`: Installs a package locally
- `npm install -g <package_name>`: Installs a package globally
- `npm install --save <package_name>`: Installs a package and saves it to your package.json file as a dependency
- `npm install --save-dev <package_name>`: Installs a package and saves it to your package.json file as a development dependency
- `npm update <package_name>`: Updates a package
- `npm uninstall <package_name>`: Uninstalls a package

- [ ]  Le package Express → on peut l’installer en local

- [ ]  Utilisation des Scripts dans le package json pour se faliciter la vie
    
    exemple : créer un script pour clear le terminal et lancer le serveur
    
    ajout de la ligne → "dev" : "clear && nodemon index.js",
    
    ```jsx
    {
      "name": "projet_test_npm",
      "version": "1.0.0",
      "description": "",
      "main": "index.js",
      "scripts": {
        "dev" : "clear && nodemon index.js",
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "author": "geogoss",
      "license": "MIT",
      "dependencies": {
        "express": "^4.18.2"
      }
    }
    ```
    
    Et dans le terminal → npm run dev



    