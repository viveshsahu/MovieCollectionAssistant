# MovieCollectionAssistant

Application to automate movie collection management process using applications like ‘Radarr’, ‘Prowlarr’, ‘qBittorrent’. The app provides ‘Sync Library’ functionality to sync items from the source directory to the destination directory on the same system or to an external NFS or SMB system. 

<img width="1261" height="555" alt="MovieCollectionAssistant_UI" src="https://github.com/user-attachments/assets/4a01f327-60dc-480e-ace7-aba90cee1af9" />

# Hosting
Windows - Run the 'MovieCollectionAssistant.exe' to start the application. The 'MovieCollectionAssistant.exe' can be added to 'Startup Apps' to auto launch the application at system boot.

# Configuration
User needs to modify 'appsettings.json' file to configure all the 3rd party applications.

User can configure any IndexManagerApp, MovieCollectionManagerApp, TorrentClientApp, VPNClientApp to be monitored and managed by MovieCollectionAssistant.

"MovieCollectionManagerApp": {
  "AppName": "Radarr",
  "AppPath": "C:\\ProgramData\\Radarr\\bin\\Radarr",
  "AppUri": "http://localhost:7878",
  "AppApiKey": "986edd100efd4952b1f2db518311cc8c",
  "MaxNoOfAttempts": "5",
  "WaitTimeInMiliseconds": "5000",
  "AppIcon": "/icons/radarricon.png"
}

AppName - Name of the 3rd party application

AppPath - The installation path of the 3rd party application

AppUri - Hosting Url of the 3rd party application

AppApiKey - API key of 3rd party application is needed, if current status is required to display

MaxNoOfAttempts - Maxium number of attempts MovieCollectionAssistant makes to run the 3rd party application

WaitTimeInMiliseconds - Waiting time for MovieCollectionAssistant before it makes next atttempt to run the 3rd party application

AppIcon - Icon location for the 3rd party application


# Sync Feature

"SyncLibraryApp": {
  "AppName": "SyncApp",
  "IsEnabled": true,
  "SyncIntervalInMinutes": 5,
  "SourceFolderPath": "C:\\Users\\vives\\Downloads\\localstorage\\download",
  "DestinationFolderPath": "C:\\Users\\vives\\Downloads\\externalstorage\\Movie Sync",
  "AppIcon": "/icons/syncicon.png"
}

IsEnabled - Toggles the feature

SyncIntervalInMinutes - Autometically syncs items against the set interval

SourceFolderPath - Source path of the downloaded items

DestinationFolderPath - Destination path on the same system or path of an external NFS or SMB system



