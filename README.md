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

## How it works?
The app is designed to create backup of the existing files under the Backup path in each run. 
So if it fails you can revert the files or compare between each other:

<image src="screenshots/image2.png" witdh=300 height="200">

Each run it generates logs under specified Log path in the conf file:

<image src="screenshots/image3.png" witdh=220 height="140">
