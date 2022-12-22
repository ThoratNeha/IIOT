# IIOT
 ## Introduction
The industrial internet of things (IIoT) refers to the extension and use of the internet of things (IoT) in industrial sectors and applications. With a strong focus on machine-to-machine (M2M) communication, big data, and machine learning, the IIoT enables industries and enterprises to have better efficiency and reliability in their operations. The IIoT encompasses industrial applications, including robotics, medical devices, and software-defined production processes.


## **Setting up the development environment for IIOT**
### Installing Dependencies

you will need to install Node.js, React and MQTT

### 1. Installation of Node.js
#### Step-1: Download the installer

Download the windows installer from [NodeJs official website](https://nodejs.org/en/). Make sure you have downloaded the latest version of NodeJs. It includes the NPM package manager.<br>
Here, we are choosing the 64-bit version of the Node.js installer<br>


<img width="580" alt="nodeV" src="https://user-images.githubusercontent.com/112370237/208826356-87cd4711-9212-4d32-9deb-4c21bc32cb3a.png"><br>


The LTS (Long-term Support) version is highly recommended for you. After the download of the installer package, install it with a double-click on it.<br>

#### Step 2: Install Node.js and NPM


<img width="580" alt="npm" src="https://user-images.githubusercontent.com/112370237/208828959-74860e50-4bbf-43e4-8cb9-540dacaf9ec0.png"><br>


After choosing the path, double-click to install .msi binary files to initiate the installation process. Then give access to run the application.

You will get a welcome message on your screen and click the “Next” button. The installation process will start.<br>
- Choose the desired path where you want to install Node.js.<br>
- 

<img width="580" alt="path" src="https://user-images.githubusercontent.com/112370237/208829982-6f394672-0998-4081-9701-e90b363aecfd.png"><br>


- By clicking on the Next button, you will get a custom page setup on the screen. Make sure you choose npm package manager , not the default of Node.js runtime . This way, we can install Node and NPM simultaneously.
You should have 143MB of space to install Node.js and npm features.

The following features will be installed by default:
- Node.js runtime
- Npm package manager
- Online documentation shortcuts
- Add to Path
  
<img width="580" alt="setup" src="https://user-images.githubusercontent.com/112370237/208833691-17a0ffba-7beb-4b8d-8e36-45ba843055f5.png"><br>


- Bang! The setup is ready to install Node and NPM. Let’s click on the Install button so hard!
  
<img width="580" alt="install" src="https://user-images.githubusercontent.com/112370237/208834409-4b8b5c95-e8a3-4678-ae37-2a2340e00147.png"><br>


#### Step 3: Check Node.js and NPM version
- If you have a doubt whether you have installed everything correctly or not, let’s verify it with “Command Prompt”.
- Open the command Prompt
- Command Prompt window will appear on the screen.
- To confirm Node installation, type **_`node -v`_** command.
  
```
node -v
```
- A package manager called npm. It is automatically included in your installation of Node. You need to have an npm version of at least 5.2.
- To confirm NPM installation, type **_`npm -v`_** command.
  
```npm -v```
  
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
  
<img width="580" alt="react" src="https://user-images.githubusercontent.com/112370237/208906793-7688946d-f2ce-4b14-862c-bf4e3227e4c7.png"><br>


### 2 Installation of Mosquitto(MQTT)
#### Step-1: Download the eclipse mosquitto 
- To install manually you will need to download the files from Eclipse Mosquitto(MQTT) version 1.6.12a. Here is the [link](https://mosquitto.org/files/binary/win64/mosquitto-1.6.12a-install-windows-x64.exe)<br>
- After that you can see the mosquitto setup window on your screen then click on next<br>

<img width="580" alt="setup" src="https://user-images.githubusercontent.com/112370237/209064690-0482d893-9656-4e05-a098-4d2351298489.png"><br>

- In the “Choose Components” page, tick the box that will install Mosquitto as a “Service.”<br>
  
<img width="580" alt="service" src="https://user-images.githubusercontent.com/112370237/209065577-25dca10f-a673-4ef5-9c41-c9ab581e79b1.png"><br>


- By default, the location of installation will be set at C:\ program files\mosquitto. If you want to install the service somewhere else, you can browse to that particular location.
  
<img width="580" alt="install" src="https://user-images.githubusercontent.com/112370237/209066600-c4e2bd52-ac08-4788-b1e8-9d1da359dc8a.png"><br>

- Click on “Finish” to complete the process.
  
#### Step-2: Starting Mosquitto on Windows
- Open a command prompt and type command `mosquitto -v` will let you start in verbose mode, and you can thus see the console messages.
  
```
mosquitto -v
```
  
![Screenshot (18)](https://user-images.githubusercontent.com/112370237/209069715-a3e5ee3f-98b2-4161-8401-1fa27de468b4.png)


### MQTT Explorer
  
MQTT Explorer is a comprehensive MQTT client that provides a structured overview of your MQTT topics and makes working with devices/services on your broker dead-simple.
#### Step-3: Download the MQTT Explorer version 0.4.0 .
 - The main page is shown in the figure below, with the topic search bar and connection configuration at the top. On the lower left of the page, it is the tree structure of the topic, and on the right, it is the Publish column, Subscribe column, Payload column, and History information control column.


<img width="580" alt="sys" src="https://user-images.githubusercontent.com/112370237/209113420-4b9aa2c1-4c91-46fa-8a25-ad5a2fbd3ec9.png">
 

#### Step-4: MQTT connection/subscription
##### Initialization page
The configuration page will pop up when you enter MQTT Explorer for the first time.
  
<img width="580" alt="connect" src="https://user-images.githubusercontent.com/112370237/209099119-3bd9b3b3-da34-4f00-bfca-20303a70cf17.png">
  
#### Step-5: Create a connection
 Click Connections to create a new connection, and fill in the Host, the port as 1883, and the protocol as MQTT protocol.
  
<img width="680" alt="connection" src="https://user-images.githubusercontent.com/112370237/209106278-e55fe6ed-dbbd-4510-80a3-1aa14743610e.png">
 
 #### Step-6: Subscribe to a topic
 Then, click Advanced. And enter a test subscription topic with the name test/1, and the result is shown in the figure below.
 
 <img width="580" alt="topic" src="https://user-images.githubusercontent.com/112370237/209124847-b117f1ec-92a6-4a84-ac8f-617a1d89ac23.png">
 
 #### Step-7: MQTT message publishing
After the connection is established, enter in the topic box at the bottom right corner of the page, and enter some text, and then click Publish to send the message.
 - Receive subscription messages
 
After the publish is successful, the message just published will be received in the Value card at the top right.

<img width="580" alt="messege" src="https://user-images.githubusercontent.com/112370237/209126487-8b848930-14c9-40eb-9580-bfabcb407cc1.png">





  
 

 
  
 






