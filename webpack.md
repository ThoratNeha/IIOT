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
![Screenshot (51)](https://user-images.githubusercontent.com/112370237/209646211-ed41a005-5dc0-4e4e-afde-4f495dff9476.png)
Now, since we'll be bundling our scripts, we have to update our `index.html` file. Let's remove the lodash `<script>`, as we now import it, and modify the other `<script>` tag to load the bundle, instead of the raw `./src` file:

### dist/index.html
![Screenshot (52)](https://user-images.githubusercontent.com/112370237/209646593-9194c758-83dc-4d58-8125-b4eaefaa9330.png)

In this setup, `index.js` explicitly requires `lodash` to be present, and binds it as `_` (no global scope pollution). By stating what dependencies a module needs, webpack can use this information to build a dependency graph. It then uses the graph to generate an optimized bundle where scripts will be executed in the correct order.

With that said, let's run `npx webpack`, which will take our script at `src/index.js` as the entry point, and will generate `dist/main.js` as the output. The `npx` command, which ships with Node 8.2/npm 5.2.0 or higher, runs the webpack binary (`./node_modules/.bin/webpack`) of the webpack package we installed in the beginning:
![Screenshot (53)](https://user-images.githubusercontent.com/112370237/209647213-2dc48c43-3e39-4b1c-9f47-55b9eef4166a.png)
Open `index.html` from the dist directory in your browser and, if everything went right, you should see the following text: `'Hello webpack'`.
## Modules
The [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) statements have been standardized in [`ES2015`](https://babeljs.io/docs/en/learn/). They are supported in most of the browsers at this moment, however there are some browsers that don't recognize the new syntax. But don't worry, webpack does support them out of the box.

Behind the scenes, webpack actually **"transpiles"** the code so that older browsers can also run it. If you inspect `dist/main.js`, you might be able to see how webpack does this, it's quite ingenious! Besides `import` and `export`, webpack supports various other module syntaxes as well, see Module `API` for more information.

## Using a Configuration
As of version 4, webpack doesn't require any configuration, but most projects will need a more complex setup, which is why webpack supports a [configuration file](https://webpack.js.org/concepts/configuration). This is much more efficient than having to manually type in a lot of commands in the terminal, so let's create one:

### project
![Screenshot (54)](https://user-images.githubusercontent.com/112370237/209650598-519b7ae2-f487-48aa-889b-38a100230d50.png)
### webpack.config.js
![Screenshot (54)](https://user-images.githubusercontent.com/112370237/209650692-40167a58-8c5e-4914-9fa1-619d082c172b.png)
Now, let's run the build again but instead using our new configuration file:
![Screenshot (55)](https://user-images.githubusercontent.com/112370237/209650960-85c2c008-6c0e-4cae-83bc-34ed988d375a.png)
A configuration file allows far more flexibility than CLI usage. We can specify loader rules, plugins, resolve options and many other enhancements this way. See the [configuration documentation](https://webpack.js.org/configuration) to learn more.
## NPM Scripts
Given it's not particularly fun to run a local copy of webpack from the CLI, we can set up a little shortcut. Let's adjust our package.json by adding an npm [script](https://docs.npmjs.com/cli/v9/using-npm/scripts):

### package.json

![Screenshot (56)](https://user-images.githubusercontent.com/112370237/209651436-1037f7e9-aea1-4ea7-84c5-28d2ecf248c6.png)
Now the `npm run build` command can be used in place of the `npx` command we used earlier. Note that within `scripts` we can reference locally installed npm packages by name the same way we did with `npx`. This convention is the standard in most npm-based projects because it allows all contributors to use the same set of common scripts.

Now run the following command and see if your script alias works:
```
$ npm run build
```
![Screenshot (57)](https://user-images.githubusercontent.com/112370237/209651798-5c0b5e88-3684-4dad-a210-8286394758ad.png)
 Now your project should look like this:

### project
![Screenshot (58)](https://user-images.githubusercontent.com/112370237/209652055-c3a44129-0623-4284-86ba-2ff3e46e177d.png)


