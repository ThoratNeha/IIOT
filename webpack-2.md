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
Webpacks use Plugins like you would use third-party vendors to power any React App. These plugins have immense power, and they can enter the React app process during any stage and boost its productivity, Scalability, and performance. Here is what importing a plugin in your React webpack app looks like:<br>
 
 <img width="780" alt="19" src="https://user-images.githubusercontent.com/112370237/210061133-d291d661-c290-49ba-882f-fdb654bc0a37.png"><br>
 
 


