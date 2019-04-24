# Bria Windows Desktop Popup trigger

A very basic HTML/JavaScript node app that listens for Bria API events and does a search for the remote party number on [tel.search.ch](https://tel.search.ch) when a call is received. 

Please note that this application is based on brias own [sample](https://github.com/CounterPathAPI/BriaAPI_Java_Sample_2.0) but improved a little bit. This version can be executed as a node application.

#### Installation notes

Download all project files or clone the git repository.

Once downloaded get all npm packages by executing **_npm install_**

Make sure you have installed node. Therefore if you run **_node server.js_** the application should come up without any exception.

If you now open your browser on http://localhost:8787 a very basic log page should open. By now you should see an security access permission question in your bria application. Please give the rights to access bria. In bria settings you can switch off the security question and allow permanent access.

Probably you would like to run the node application automatically when windows has started. A very simple way to achieve this is installing the node application as a windows service - yes this is possible and actually quite easy:

Run **_npm install -g qckwinsvc_** to install a helper program on your machine. Now just run qckwinsvc without any arguments. The service name and description can be anything you like. The node script path has to point to your server.js file in the downloaded root folder. That's it the service is now installed and whenever you start windows you can open localhost:8787 to view the logs. 

However the popup mechanism is only working when a website has opened localhost:8787. A very elegant way to make sure that always an instance is running is adding a webtab in your bria phone application to http:localhost:8787. Open bria **_Preferences -> Files & Web Tabs_** to add this entry.

If you have a question write me an email,
kind regard,
marco





