# Webpack
Webpack is used to compile JavaScript modules. Once [installed](https://webpack.js.org/guides/installation/), you can interact with webpack either from its CLI or API. If you're still new to webpack, please read through the core concepts and this comparison to learn why you might use it over the other tools that are out in the community
## Basic steps 
First let's create a directory, initialize npm, [install webpack locally](https://webpack.js.org/guides/installation/), and install the webpack-cli (the tool used to run webpack on the command line):
![Screenshot (46)](https://user-images.githubusercontent.com/112370237/209629081-d734ee44-a473-4d7a-a703-12bc04f850b6.png)
Now we'll create the following directory structure, files and their contents:

### project
![Screenshot (47)](https://user-images.githubusercontent.com/112370237/209640770-7639cc4e-b5f9-453c-b6e8-a1946f58a833.png)
### src/index.js
![Screenshot (47)](https://user-images.githubusercontent.com/112370237/209640863-5d38970b-4d14-4760-9085-c64ea5d4b92a.png)
### index.html
![Screenshot (48)](https://user-images.githubusercontent.com/112370237/209641670-8787f1ea-10af-47f7-9a39-cc9f6fd421fd.png)<br>

We also need to adjust our `package.json` file in order to make sure we mark our package as `private`, as well as removing the main entry. This is to prevent an accidental publish of your code.
### package.json
![Screenshot (49)](https://user-images.githubusercontent.com/112370237/209642715-7656332f-67cc-4e5f-9b97-973d6614366e.png)

In this example, there are implicit dependencies between the `<script>` tags. Our `index.js` file depends on lodash being included in the page before it runs. This is because `index.js` never explicitly declared a need for `lodash`; it assumes that the global variable `_` exists.

There are problems with managing JavaScript projects this way:

-It is not immediately apparent that the script depends on an external library.
-If a dependency is missing, or included in the wrong order, the application will not function properly.
-If a dependency is included but not used, the browser will be forced to download unnecessary code.
-Let's use webpack to manage these scripts instead.

##Creating a Bundle
First we'll tweak our directory structure slightly, separating the "source" code (`./src`) from our "distribution" code (`./dist`). The "source" code is the code that we'll write and edit. The "distribution" code is the minimized and optimized output of our build process that will eventually be loaded in the browser. Tweak the directory structure as follows:

### project
![Screenshot (50)](https://user-images.githubusercontent.com/112370237/209644610-b00660c3-89d9-4a19-b35e-1ca2f8160544.png)<br>
To bundle the `lodash` dependency with `index.js`, we'll need to install the library locally:
```
npm install --save lodash
```
Now, let's import `lodash` in our script:

### src/index.js

