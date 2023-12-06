# IIOT
 ## Introduction
The industrial internet of things (IIoT) refers to the extension and use of the internet of things (IoT) in industrial sectors and applications. With a strong focus on machine-to-machine (M2M) communication, big data, and machine learning, the IIoT enables industries and enterprises to have better efficiency and reliability in their operations. The IIoT encompasses industrial applications, including robotics, medical devices, and software-defined production processes.


## **Setting up the development environment for IIOT**
### Installing Dependencies

you will need to install Node.js, React and MQTT

## 1. Installation of Node.js
### Step-1: Download the installer

Download the windows installer from [NodeJs official website](https://nodejs.org/en/). Make sure you have downloaded the latest version of NodeJs. It includes the NPM package manager.<br>
Here, we are choosing the 64-bit version of the Node.js installer<br>

<p align="center">
<img width="580" height="400" alt="nodeV" src="https://user-images.githubusercontent.com/112370237/208826356-87cd4711-9212-4d32-9deb-4c21bc32cb3a.png"></p><br>


The LTS (Long-term Support) version is highly recommended for you. After the download of the installer package, install it with a double-click on it.<br>

### Step 2: Install Node.js and NPM

<p align="center">
<img width="580" height="400" alt="npm" src="https://user-images.githubusercontent.com/112370237/208828959-74860e50-4bbf-43e4-8cb9-540dacaf9ec0.png"></p><br>


After choosing the path, double-click to install .msi binary files to initiate the installation process. Then give access to run the application.

You will get a welcome message on your screen and click the “Next” button. The installation process will start.<br>
- Choose the desired path where you want to install Node.js.<br>
 
<p align="center">
<img width="580" height="400" alt="path" src="https://user-images.githubusercontent.com/112370237/208829982-6f394672-0998-4081-9701-e90b363aecfd.png"></p><br>


- By clicking on the Next button, you will get a custom page setup on the screen. Make sure you choose npm package manager , not the default of Node.js runtime . This way, we can install Node and NPM simultaneously.
You should have 143MB of space to install Node.js and npm features.

The following features will be installed by default:
- Node.js runtime
- Npm package manager
- Online documentation shortcuts
- Add to Path


<p align="center">
<img width="580" height="400" alt="setup" src="https://user-images.githubusercontent.com/112370237/208833691-17a0ffba-7beb-4b8d-8e36-45ba843055f5.png"></p><br>


- Bang! The setup is ready to install Node and NPM. Let’s click on the Install button so hard!


<p align="center">
<img width="580" height="400" alt="install" src="https://user-images.githubusercontent.com/112370237/208834409-4b8b5c95-e8a3-4678-ae37-2a2340e00147.png"></p><br>


### Step 3: Check Node.js and NPM version
- If you have a doubt whether you have installed everything correctly or not, let’s verify it with “Command Prompt”.
- Open the command Prompt
- Command Prompt window will appear on the screen.
- To confirm Node installation, type **_`node -v`_** command.
  
```
node -v
```
- A package manager called npm. It is automatically included in your installation of Node. You need to have an npm version of at least 5.2.
- To confirm NPM installation, type **_`npm -v`_** command.
  
```
npm -v
```
  
![cmd](https://user-images.githubusercontent.com/112370237/208838322-154ff311-cc66-430a-9eab-19babc54c84b.png)

If the installation went well it will give you the version you have installed
The NodeJs installation is completed
  
### Step-4: Now in the terminal run the below command: 
```
npm install -g create-react-app  
```
  
![Screenshot (12)](https://user-images.githubusercontent.com/112370237/208892276-e561d53d-d7bf-4142-b534-93b9fe93125d.png)

It will globally install react app for you. To check everything  went well run the command 

### Step 5: Now in the terminal run the below command: 
```
create-react-app --version  
```
  
![Screenshot (10)](https://user-images.githubusercontent.com/112370237/208842637-dfb39cda-ed2a-48e8-842b-30ac9c731325.png)

  
### Step-6: You can now create a new React application by typing:
```
npx create-react-app my-app
```
where my-app is the name of the folder for your application. This may take a few minutes to create the React application and install its dependencies.
  
![Screenshot (13)](https://user-images.githubusercontent.com/112370237/208897682-017b6ab8-af1b-4a46-935d-d78594497008.png)

  
Let's quickly run our React application by navigating to the new folder and typing npm start to start the web server and open the application in a browser:
```
cd my-app
npm start
```
You should see the React logo and a link to "Learn React" on [http://localhost:30000](http://localhost:30000) in your browser. We'll leave the web server running while we look at the application with VS Code.


<p align="center">
<img width="580" height="400" alt="react" src="https://user-images.githubusercontent.com/112370237/208906793-7688946d-f2ce-4b14-862c-bf4e3227e4c7.png"></p><br>


## 2 Installation of Mosquitto(MQTT)
### Step-1: Download the eclipse mosquitto 
- To install manually you will need to download the files from Eclipse Mosquitto(MQTT) version 1.6.12a. Here is the [link](https://mosquitto.org/files/binary/win64/mosquitto-1.6.12a-install-windows-x64.exe)<br>
- After that you can see the mosquitto setup window on your screen then click on next<br>


<p align="center">
<img width="580" height="400" alt="setup" src="https://user-images.githubusercontent.com/112370237/209064690-0482d893-9656-4e05-a098-4d2351298489.png"></p><br>


- In the “Choose Components” page, tick the box that will install Mosquitto as a “Service.”<br>


<p align="center">
<img width="580" height="400" alt="service" src="https://user-images.githubusercontent.com/112370237/209065577-25dca10f-a673-4ef5-9c41-c9ab581e79b1.png"></p><br>


- By default, the location of installation will be set at C:\ program files\mosquitto. If you want to install the service somewhere else, you can browse to that particular location.


<p align="center">
<img width="580" height="400" alt="install" src="https://user-images.githubusercontent.com/112370237/209066600-c4e2bd52-ac08-4788-b1e8-9d1da359dc8a.png"></p><br>

- Click on “Finish” to complete the process.
  
### Step-2: Starting Mosquitto on Windows
- Open a command prompt and type command `mosquitto -v` will let you start in verbose mode, and you can thus see the console messages.
  
```
mosquitto -v
```
  
![Screenshot (18)](https://user-images.githubusercontent.com/112370237/209069715-a3e5ee3f-98b2-4161-8401-1fa27de468b4.png)


### MQTT Explorer
  
MQTT Explorer is a comprehensive MQTT client that provides a structured overview of your MQTT topics and makes working with devices/services on your broker dead-simple.
### Step-3: Download the MQTT Explorer version 0.4.0 .
 - The main page is shown in the figure below, with the topic search bar and connection configuration at the top. On the lower left of the page, it is the tree structure of the topic, and on the right, it is the Publish column, Subscribe column, Payload column, and History information control column.


<p align="center">
<img width="580" height="400" alt="sys" src="https://user-images.githubusercontent.com/112370237/209113420-4b9aa2c1-4c91-46fa-8a25-ad5a2fbd3ec9.png"></p>
 <br>

### Step-4: MQTT connection/subscription
#### Initialization page
The configuration page will pop up when you enter MQTT Explorer for the first time.


<p align="center">
<img width="580" height="400" alt="connect" src="https://user-images.githubusercontent.com/112370237/209099119-3bd9b3b3-da34-4f00-bfca-20303a70cf17.png"></p><br>
  
  
### Step-5: Create a connection
 Click Connections to create a new connection, and fill in the Host, the port as 1883, and the protocol as MQTT protocol.
 
 
<p align="center">
<img width="580" height="400" alt="connection" src="https://user-images.githubusercontent.com/112370237/209106278-e55fe6ed-dbbd-4510-80a3-1aa14743610e.png"></p><br>
 
### Step-6: Subscribe to a topic
 Then, click Advanced. And enter a test subscription topic with the name test/1, and the result is shown in the figure below.
 
 
 <p align="center">
 <img width="580" height="400" alt="topic" src="https://user-images.githubusercontent.com/112370237/209124847-b117f1ec-92a6-4a84-ac8f-617a1d89ac23.png"></p>
 
 
### Step-7: MQTT message publishing
After the connection is established, enter in the topic box at the bottom right corner of the page, and enter some text, and then click Publish to send the message.
 - Receive subscription messages
 
After the publish is successful, the message just published will be received in the Value card at the top right.


<p align="center">
<img width="580" height="400" alt="messege" src="https://user-images.githubusercontent.com/112370237/209126487-8b848930-14c9-40eb-9580-bfabcb407cc1.png"></p><br>


### 3 Installation of WampServer

[WampServer](https://www.wampserver.com/en/) is a local server package for Windows, allowing you to install and host web applications that use `Apache`, `PHP` and `MySQL`.

This article will walk you through the steps to install WampServer on your computer.

### Step-1: Downloading WampServer

Download the installer file for the [latest version of WampServer](https://www.wampserver.com/en/), and save the file to your computer.<br>

<p align="center">
<img width="580" height="400" alt="wamp" src="https://user-images.githubusercontent.com/112370237/209310900-67d06274-f51b-478e-8d20-a9be5c8d639d.png"></p><br>

### Step-2: Installing WampServer

To start the installation process, you need to open the folder where you saved the file, and **double-click the installer file**. A security warning window will open, asking if you are sure you want to run this file. **Click Run** to start the installation process.

Next you will see the Welcome To The WampServer Setup Wizard screen. **Click Next** to continue the installation.<br>
 
<p align="center">
<img width="580" height="400" alt="wset" src="https://user-images.githubusercontent.com/112370237/209313426-435e9001-9675-4784-b073-d1e3ebc232a0.png"></p><br>

The next screen you are presented with is the License Agreement. Read the agreement, check the radio button next to I accept the agreement, then **Click Next** to continue the installation.<br>

<p align="center">
<img width="580" height="400" alt="agree" src="https://user-images.githubusercontent.com/112370237/209315507-952da764-daab-47e0-af98-62cde196bee8.png"></p><br>

Next you will see the Select Destination Location screen. Unless you would like to install WampServer on another drive, you should not need to change anything. **Click Next**  to continue.

<p align="center">
<img width="580" height="400"  alt="wpath" src="https://user-images.githubusercontent.com/112370237/209318264-c4eb8f5f-3e60-4c93-9d90-4bffe881abfa.png"></p><br>

The next screen you are presented with is the Select Additional Tasks screen. You will be able to select whether you would like a Quick Launch icon added to the taskbar or a Desktop icon created once installation is complete. Make your selections, then **click Next** to continue.
Next you will see the Ready To Install screen. You can review your setup choices, and change any of them by clicking Back to the appropriate screen, if you choose to. Once you have reviewed your choices, **click Install** to continue.<br>
 
<p align="center">
<img  width="580" height="400"  alt="winstall" src="https://user-images.githubusercontent.com/112370237/209319839-39a1cc2c-c5b9-4a9e-8050-ac1d891b60ff.png"></p><br>

The installation process will take a while but it should get done in a few minutes.<br>

<p align="center">
<img  width="580" height="400" alt="ext" src="https://user-images.githubusercontent.com/112370237/209320667-1046df11-cea8-4564-8dd6-09455521c46e.png"></p><br>

The Installation Complete screen will now appear. Check the Launch WampServer Now box, then click Finish to complete the installation.<br>

<p align="center">
<img width="580" height="400"  alt="wlaunch" src="https://user-images.githubusercontent.com/112370237/209321908-a22e778e-7e02-4cd2-bf60-c6ed2510558b.png"></p><br>

### Step-2: Configuration: 
Now, we have to configure the WAMP contents we installed. Once installed, you will mostly get a notification from the firewall asking whether the newly installed software should get the permission to use your network. Give it the permission and next find the option in your hidden taskbar icons or in the windows start menu. The color of the symbol corresponds to the status the server is in:

- Red- Can mean the WAMP server is temporarily deactivated or there is some sort of hindrance that is not allowing it to work
- Orange- Can mean it is idle or, like red, there is something that didn’t get installed properly. 
- Green- The server is active and ready to use.<br<

### Step-3: Testing WampServer
Once you have completed the installation process, test that your installation is working properly by going to [http://localhost/]() in your browser. You should see the WampServer homepage displayed.<br>

Now you are ready to go! Go ahead and create your first WAMP server project.

### 3 Installation of PM2
### Step-1: Installation: 
 Type command:
 npm install -g pm2

### Step-2: Put programs on windows start-up:
Type Command:
npm install pm2-windows-startup -g

### Step-3: Save Program:
Type Command:
pm2 save














  
 

 
  
 






