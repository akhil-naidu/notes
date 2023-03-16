We need to initiate a nodejs project for which we take advantage of the inbuilt command `npm init -y`; this allows one to create a `package.json` file with default values. The `package.json` tracks all the dependencies and dev dependencies of the respective project.

Apart from tracking the dependencies and dev dependencies, `package.json` also has other important information relevant to the project. Few of them were:

* `Name` and `Version` of the Project
* `Dependecies` and `Dev Dependencies`
* `type` => Which helps in the syntax of import and export packages
* and not but not the least, the `scripts`

1. Name and version are not sensitive, but are used to identify and track the progress of the application we are developing.
2. Dependencies are the core installations using npm, which are mandatory for the production, while dev dependencies are more like helper installations for making the process of development seemless. A quick example would be usage of the `nodemon`, for automatically starting the server whenever any js file relaods.
3. To install a dependency named packagename, you need to use the command, `npm i packagename` or `npm install packagename`. Similarly to unstall a dev dependency named devpackagename, `npm i devpackagename --save-dev`
4. Finally, `scripts` are used to take advantage of the installed packages within the project itself. Not all dependecies can be inslled system wide to use them in terminal. Again `nodemon` can be of a good example. To explain a bit more, I cannot use the command `nodemon app.js` in my terminal directly! nodemon is a package that is restricted to project itself and the linux or the server terminal cannot identify it. It is useful to run a terminal command that is installed within the project itself, as the installation is not avaibale in the operating system.
5. Whenever, we use the command which starts with `npm`, it will always look into the `package.json` file within the folder and try to execute the command.

### examples:
`npm i` => It will look into the dependencies and devdependencies of the `package.json` file and download them within the `node_modules` folder. It also creates a `package-lock.json` file to track the versions of the core dependencies and peer dependencies. Where core dependencies are the dependencies which we are trying to install and peer dependecies are dependencies used for making our core dependencies.

`npm i express` => It will download the necessary files and store them in the `node_modules` folder and updates the `dependencies` object within the `package.json` file.

`npm i nodemon --save-dev` => It will download the necessary files and store them in the `node_modules` folder and updates the `devDependencies` object within the `package.json` file.

`npm run dev` => Will look into the `scripts` object in the `package.json` file and look for the **value** of the `dev` key and executes it in the terminal.
