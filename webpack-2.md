# Webpack
## Understanding how React Webpack works?
Like `create-React-app`, React Webpack is also a command-line tool used to create a bundle of assets (files and code). It doesn't run on the browser or the server. It takes all the JS files and other assets, transforming them into one large file. Now, this compressed file can be sent to the browser or the server depending on which rendering style you have set up for your website. React webpack file is typically configured through a file labeled `webpack.config.js.` This is the place where all the configurations will take place.

<img width="780" alt="12" src="https://user-images.githubusercontent.com/112370237/210058556-e153fea1-d846-4e6e-af72-e3eb486ff9d4.png"><br>

## React Webpack Components 
You should familiarize yourself with some of the React webpack terms and what they mear which will help you understand what is `webpack.config.js` in React. 
### 1. Entry
As the name suggests, entry refers to the `entry` point of your React app. The React ap architecture can be visualized as a tree. All React components branch out from `App.js.` An `app.js` is found inside the index.js file. Webpack enters your React app via this `index.js` file and creates a dependency graph to understand what files are needed to load first.
### 2. Loader
Loaders are important in webpack. They work like compilers that check for different kinds of files and match them with their appropriate loaders for handling them. This is what a loader configuration would look like:<br>

<img width="780" alt="15" src="https://user-images.githubusercontent.com/112370237/210060049-8c264377-fe0a-4bfe-a771-c20ad8d185f7.png"><br>

you check the `module` part of the above code, it takes a list of rules that can be used for different purposes. At times you need more than one type of loader for working on a file like loading a CSS file. The rule for loading a CSS file is like this:<br>
<img width="780" alt="17" src="https://user-images.githubusercontent.com/112370237/210060444-7b2a91b7-22b1-461e-a0a1-e3d1d29e2113.png"><br>

As you can see, both `CSS-loader` and `style-loader` are being used for processing this file. Though we write style-loader first and `CSS-loader` second, they get loaded in the reverse order. Initially, the `css-loader` process will work, and then the `style-loader` will work on the output created by the `class-loader`.
### 3. Output
`Output` is relatively easy to understand. After completing all the processes, your React webpack creates a bundle file. We specify the name and the location of the final `output` file using the output function.
### 4. Plugins
Webpacks use Plugins like you would use third-party vendors to power any React App. These plugins have immense power, and they can enter the React app process during any stage and boost its productivity, Scalability, and performance. Here is what importing a **plugin in your React webpack app** looks like:<br>
 
 <img width="780" alt="19" src="https://user-images.githubusercontent.com/112370237/210061133-d291d661-c290-49ba-882f-fdb654bc0a37.png"><br>

Here we installed a plugin named `HTML-webpack-plugin`. This plugin helps developers include their webpack bundles in the body using `script` tags.
5. Mode in React Webpack
Mode is a simple yet very important concept to understand for React-webpack. It hel developers use different setups when they are in development and production modes. This what it looks like in code:<br>
<img width="780" alt="21" src="https://user-images.githubusercontent.com/112370237/210062176-48d2608d-3325-4510-ab7b-c9a418b3eea1.png"><br>

If you set the mode to `production`, the output bundle gets minified and optimized. 
### 6. Development Server 
And finally, you should know about development server. When developing your React app, it can be annoying and inefficient if the app compiles every time you change something. To avoid that you need to use `devServer` for your application.<br>

<img width="780" alt="22" src="https://user-images.githubusercontent.com/112370237/210062598-60d9ac2a-7a7f-473b-965c-18bf45b86fb3.png"><br>

This setup will serve your application from the `dist` you set up earlier as your output.

## Install Webpack in React
Now that we understand the **role of webpack in React**, we should look at the React with Webpack installation process. We can add webpack config to create-react-app, but this would again limit the customization and freedom we would have if we created a React app using webpack from scratch. **Installing React webpack** will help you gain complete control over the configuration and open up the scope of customization.

### 1. Install npm int | Installing dependencies
Assuming you already have the latest Node.js and npm version installed in your system, the first thing you need to install is npm init. Although VS Code is a popular choice, you can use whichever code editor you want. Start by running this process:

```$ npm init -y
```
Doing so creates a starter package and creates a package.json file as well. All the dependencies needed to build your App will be listed here. Next, we want to create a basic React application, for which we need two libraries React & React DOM. We can add them as dependencies using
npm:
```
$ npm i react react-dom --save
```
Now we can add a webpack for bundling our App together. Webpack is also needed for its hot reloading replacement feature. Here is how to install webpack-react in your project:
```
$ npm i webpack webpack-dev-server webpack-cli --save--dev
```
The save dev command tells the React app that these are just 'dev' dependencies.
### 2. Set up Project Structure 
You would have a `package.json` file and a `package-lock.json` file in your root. Next, we will create some empty files that we will be populating later. Now you should set your project in a way that it looks like the structure shown below:

<img width="780" alt="25" src="https://user-images.githubusercontent.com/112370237/210064132-258767b1-760f-4b36-b1a9-96890b15f18b.png">

### 3. Create a simple React App 
Now that we have all the assets in place let's populate those folders we created earlier with proper codes to test how they function on the browser.

<img width="780" alt="26" src="https://user-images.githubusercontent.com/112370237/210064301-e72d4106-8d6a-46b9-a577-4c2a8fb99a14.png">
This basic Hello World app is supposed to render a `<h>` tag that says 'Hello World' on the page. But if you try adding an index.js file to your HTML file like this:

<img width="780" alt="27" src="https://user-images.githubusercontent.com/112370237/210067089-d1436434-b5a3-4434-aceb-674c0d5cd820.png">

The code won't work. Your browser will shoot a blank page. Your browser doesn't know how to import App from the ./App directory. The browser can only load static JS files. Hence, webpack configuration is needed for converting your React app into readable code that browsers can understand.
### 4. Utilizing Loaders 
As discussed above, loaders are an essential part of **React Webpack** as they can be used for compiling complex JSX files to browser understandable JavaScript files. We will use the babel- loader for this task. Install babel-loader by writing this code:
```
npm i -D @babel/core @babel/preset-env @babel/preset-react babel-loader
```
 We have installed babel, two presets, and the babel-loader needed to load our JSX files.

### 5. Configure React-Webpack
Now we need to configure **webpack React** for instructing it to use Babel during bundling process for understanding the JSX files:

<img width="780" alt="29" src="https://user-images.githubusercontent.com/112370237/210067536-855a9340-caee-42fc-8727-8d25177cb133.png">

Here we instructed webpack to use babel-loader whenever it finds a file with js or JSX extension.
### 6. Bundle your React App
Now we need to add a script to our `package.json` file which allows us to build our App whenever needed seamlessly:

<img width="780" alt="31" src="https://user-images.githubusercontent.com/112370237/210067969-28439fcf-800b-40d0-9a95-e625ca8d2517.png"><br>

 Now run the build using this commanad
 ```npm run build
 ```
 This will create the main.js file in the dist folder of your project root. Now we can attach this bundled JS to our HTML: <br>
 ### 6.1 Manually running bundled App
 Once you have added the script tags mentioned above, open the index.html in the browser, and now you will see the Hello World! text on the browser.<br>
 
 <img width="780" alt="32" src="https://user-images.githubusercontent.com/112370237/210068629-5b4f4364-6499-4dd4-a0f1-b26108da76c1.png"><br>
 

### 6.2 Using HtmlWebpackPlugin
The above method is great for adding bundled JS to your HTML. However, it is not practical in real life. Any real app will have multiple webpack plugins for chunking your JS files. Hence manually importing all bundling scripts to HTML will be cumbersome and futile. Instead, we can automate the process by installing a powerful React plugin named HTML-webpack-plugin by running the following command:
``` 
npm i -D HTML-webpack-plugin
```
Modify our project configuration file for adding this plugin by running the following code:<br>

<img width="461" alt="34" src="https://user-images.githubusercontent.com/112370237/210125341-7597e8a4-189b-426b-8a84-c880a94ac4b2.png"><br>


By running this code, we included the plugin and gave it a template HTML that has the webpack attached to the bundled JS after the build. After this, we can remove the <script> tag from the src/index.html directory. Now run the build using:
```
 npm build
```
You will see that the index.html file is also generated alongside main.js in the dist folder when you do this.
### Wrapping up!
This is all you need to know about **React Webpack!** Make sure to be sure webpack with React if you are working on a large-scale app project that needs customization, Scalability, and complex configurations to ensure your React app can handle all the demands and performs seamlessly without any bottlenecks.


