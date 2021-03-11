# WeNote-NJSServer
Server component of the WeNote app.

WeNote app: 


# Author
Alexandre Miguel Marques Pereira


# What is this?
This is a part of the project WeNote. Although this project was developed with a team of 4 people, I was the only one writing the server, therefore all the code present is written by me. 

This is the server which supports the real time needs of the WeNote React Native application. It is responsible for keeping track of files, users, and interactions between the different components. The server was developed due to a need of using websockets to keep clients updated in real time.

This project was developed in a purely academic context, and is in no way a serious attempt at a production ready server. The server isn't safe, nor scalable (data wise), in any way. This was something custom made to fit a very specific purpose.


# How does it work?
There are two main components to the server: the first is the data storage and handling component, and the second is the event or synchronization component.

The server keeps all data in memory. This includes user details, files, notifications, and whatever else it may need. This internal memory has to be saved (manually, through the web control panel), in order to serialize the data into a format that the server will (automatically) look for and read upon starting up. The server is responsible for the creation of all resources.

The event component keeps a list of every logged in user, control panel, and file currently in use, and handles quick communication between all those elements. As an example, this component is responsible for sending a notification to a user if they're added to a file's user list, and to tell the client when a different user starts editing that same file. Most of the events are also sent to the control panel.


# Control panel
We can access the control panel by accessing the resource "control_panel.html" through a browser. The default server porn is 7501. The control panel is a convenient way to watch over the internal data currently in the server. This panel shows us every user, file, notification, as well as indicators for when users are online, and files are being edited. In addition, this control panel also allows us to send notifications and register new users and files.


# Grade
Although this component wasn't graded explicitly, the overall project WeNote, which makes use of this component, was graded with a 95/100.

