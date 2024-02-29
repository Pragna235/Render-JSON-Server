# MERN-Assignment-Render-JSON-Server

* Clone your empty github repository in `VSCode` using the following command
*     git clone repository-url
* Navigate to your repo folder
*     cd folder-name
* Add `package.json` file in the repository folder using the below command
*     npm init -y
* Your `package.json` will be added.
* Install dependencies using :
*     npm i json-server cors json-serve
* Add the below in the `scripts` of package.json
*     "start":"node index.js",
* Create an `index.js` file
* Copy this code into the `index.js` file for experiment or write your own code
*     const jsonServer = require("json-server"); // importing json-server library
      const server = jsonServer.create();
      const router = jsonServer.router("db.json");
      const middlewares = jsonServer.defaults();
      const port = process.env.PORT || 8080; //  chose port from here like 8080, 3001

      server.use(middlewares);
      server.use(router);

      server.listen(port);
* Create another file `.gitignore` and add `node_modules` to it so that github ignores it in the actual repository.
* Create one last file, say `db.json` and open a set of `{}` and add the data that you want to deploy in it.


* After completing the above steps, use these commands to push your code into the repository
*     git add .
*     git commit -m "any comment"
*     git push origin main

### Deployment in RENDER

* Log in to `render.com`
* Select `New Web Serivice`
* Connect your github repository
* Name your API, select the Instance Type and click on `Create Web Service`
