# **Office 365 IP/URL Fetcher**

This repository is to fetch the required IP/URLs from Microsoft for Office 365.

You can copy **src folder** to your PC and run the ***___jar___*** file. 

## Modify the config.xml
By default it is creating a folder and the files under "C:\OFFICE_365_FEEDs". 
  You can modify the path from the conf file:

```
<?xml version = "1.0" encoding = "utf-8"?>
<config>
<!--You can modify the path for Office 365 Files to be created-->
	<office365>
		<main-path>C:\OFFICE_365_FEEDs\</main-path>
		<backup-path>C:\OFFICE_365_FEEDs\Backup\</backup-path>
		<log-path>C:\OFFICE_365_FEEDs\Logs\</log-path>
	</office365>
</config>
```
**IMPORTANT:** _config.xml_ should be at the same path with the _jar_ file!

## How it works?
It generates _**ipv4_List.txt**_, _**ipv6_List.txt**_ and _**url_List.txt**_ under the specified main-path at the config file:

<image src="screenshots/image1.png" witdh=260 height="150">

The app is designed to create backup of the existing files under the Backup path in each run. 
So if it fails you can still have the files or compare between each other in a time:

<image src="screenshots/image2.png" witdh=300 height="200">

Each run it generates logs under specified Log path in the conf file:

<image src="screenshots/image3.png" witdh=220 height="140">

## How to schedule the jar?
You can modify the batch file under the src and use your app folder:
	
```
"C:\CHANGE MY DIRECTORY TO THE PROGRAM FOLDER\office365.jar"
```
As an example:

```
"C:\OFFICE365-APP\office365.jar"
```

You can automate it by creating a task from the Task Scheduler:

<image src="screenshots/image6.png" witdh=650 height="370">

Go to the _"Actions"_:
	
<image src="screenshots/image4.png" witdh=660 height="450">
	
Select the batch file:
	
<image src="screenshots/image5.png" witdh=660 height="350">
