# IIOT
## Introduction
The industrial internet of things (IIoT) refers to the extension and use of the internet of things (IoT) in industrial sectors and applications. With a strong focus on machine-to-machine (M2M) communication, big data, and machine learning, the IIoT enables industries and enterprises to have better efficiency and reliability in their operations. The IIoT encompasses industrial applications, including robotics, medical devices, and software-defined production processes.
## **Setting up the development environment for IIOT**
### Installing Dependencies
you will need to install Node.js, react and MQTT
### 1. Node.js
#### Step-1: Download the installer
Download the windows intaller from [NodeJs official website](https://nodejs.org/en/). Make sure you have downloaded the latest version of NodeJs. It includes the NPM package manager.<br>
Here, we are choosing the 64-bit version of the Node.js installer<br>

<img width="680" alt="nodeV" src="https://user-images.githubusercontent.com/112370237/208826356-87cd4711-9212-4d32-9deb-4c21bc32cb3a.png"><br>

The LTS (Long-term Support) version is highly recommended for you. After the download of the installer package, install it with a double-click on it.<br>
Now .msi file will be downloaded to your browser. Choose the desired location for that.<br>
#### Step 2: Install Node.js and NPM
<img width="680" alt="npm" src="https://user-images.githubusercontent.com/112370237/208828959-74860e50-4bbf-43e4-8cb9-540dacaf9ec0.png"><br>
After choosing the path, double-click to install .msi binary files to initiate the installation process. Then give access to run the application.

You will get a welcome message on your screen and click the “Next” button. The installation process will start.<br>
- Choose the desired path where you want to install Node.js.
<img width="680" alt="path" src="https://user-images.githubusercontent.com/112370237/208829982-6f394672-0998-4081-9701-e90b363aecfd.png"><bt>
- By clicking on the Next button, you will get a custom page setup on the screen. Make sure you choose npm package manager , not the default of Node.js runtime . This way, we can install Node and NPM simultaneously.
You should have 143MB of space to install Node.js and npm features.

The following features will be installed by default:
- Node.js runtime
- Npm package manager
- Online documentation shortcuts
- Add to Path
  
<img width="680" alt="setup" src="https://user-images.githubusercontent.com/112370237/208833691-17a0ffba-7beb-4b8d-8e36-45ba843055f5.png"><br>
- Bang! The setup is ready to install Node and NPM. Let’s click on the Install button so hard!
  
<img width="680" alt="install" src="https://user-images.githubusercontent.com/112370237/208834409-4b8b5c95-e8a3-4678-ae37-2a2340e00147.png"><br>
#### Step 3: Check Node.js and NPM version
- If you have a doubt whether you have installed everything correctly or not, let’s verify it with “Command Prompt”.
- Open the command Prompt
- Command Prompt window will appear on the screen.
- To confirm Node installation, type **_node -v_** command.
  
  ```
  node -v
  ```
- A package manager called npm. It is automatically included in your installation of Node. You need to have an npm version of at least 5.2.
- To confirm NPM installation, type **_npm -v_** command.
  
  ```
  npm -v
  ```
  
 ![cmd](https://user-images.githubusercontent.com/112370237/208838322-154ff311-cc66-430a-9eab-19babc54c84b.png)
  If the installation went well it will give you the version you have installed
 The NodeJs installation is completed
  
  #### Step-4: Now in the terminal run the below command: 
  ```
  npm install -g create-react-app  
  ```
  
  ![Screenshot (12)](https://user-images.githubusercontent.com/112370237/208892276-e561d53d-d7bf-4142-b534-93b9fe93125d.png)
It will globally install react app for you. To check everything  went well run the command 

#### Step 5: Now in the terminal run the below command: 
```
  create-react-app --version  
```
  
  ![Screenshot (10)](https://user-images.githubusercontent.com/112370237/208842637-dfb39cda-ed2a-48e8-842b-30ac9c731325.png)
  
  #### Step-6: You can now create a new React application by typing:
  ```
  npm create-react-app my-app
  ```
  where my-app is the name of the folder for your application. This may take a few minutes to create the React application and install its dependencies.
  
  ![Screenshot (13)](https://user-images.githubusercontent.com/112370237/208897682-017b6ab8-af1b-4a46-935d-d78594497008.png)
  
  Let's quickly run our React application by navigating to the new folder and typing npm start to start the web server and open the application in a browser:
  ```
 cd my-app
 npm start
  ```
  You should see the React logo and a link to "Learn React" on [http://localhost:30000](http://localhost:30000) in your browser. We'll leave the web server running while we look at the application with VS Code.
  
<img width="680" alt="react" src="https://user-images.githubusercontent.com/112370237/208906793-7688946d-f2ce-4b14-862c-bf4e3227e4c7.png">

  
 






