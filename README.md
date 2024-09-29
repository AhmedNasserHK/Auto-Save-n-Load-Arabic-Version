### OVERVIEW

Computer rentals are typically configured with Deep Freeze to prevent any installations or changes after a restart, which also means that data from offline games is not saved. This application solves this issue by saving game data to a shared network folder, ensuring that game progress is preserved even after system restarts.

**Auto-Save-n-Load** is a VB.NET application that provides a secure and efficient way to manage game data and user sessions across different users on a shared network. It handles authentication folder management for game saves, and user-specific configurations, allowing each user to have separate game save folders.

# Features
- **Effortless Registration and Login**: Users can easily register and log in to their accounts, ensuring that their game progress is automatically saved on the server for seamless access.
- **User Login / Public Save Directory**: Players can choose between a personal login for private saves or access a public directory for shared game progress.
- **Dynamic Game Directory Management**: Admin can manually add their game directories, or simply click the `Update"` button to automatically retrieve the latest game list available on the github repository:

---

## Installation and Setup

### Prerequisites
- .NET 6 (https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- Windows OS
- Administrative privileges (required for symbolic link creation)

### Setup Instructions

#### 1. Share a Folder on the Network
Before you begin, ensure that a shared folder is available on your network to store user and game data. Follow the instructions for sharing a folder in Windows:
- [How to share a folder over a network (Windows 10/11)](https://support.microsoft.com/en-us/windows/file-sharing-over-a-network-in-windows-b58704b2-f53a-4b82-7bc1-80f9994725bf#ID0EBD=Windows_11)

Make sure that all users who need access to the application have the necessary permissions to read from and write to this shared folder.

#### 2. Download the Application
- Go to the [latest release](https://github.com/raizar24/Auto-Save-n-Load/releases).
- Download the zip file.

#### 3. Install the Application
- Extract the files from the zip.
   
#### 4. Set Up the XML Files
- Create a shared folder on your network or local machine.
- Edit `settings.xml` using  `notepad` and  provide the shared folder network link

#### `settings.xml` (Sample)
`192.168.1.100` is IP address of pc Server while `saves` is the name of the shared folder
```xml
<?xml version="1.0" encoding="utf-8" ?>
<Variable>
  <sharedFolder>\\192.168.1.100\Saves\</sharedFolder>
</Variable>
```
`YourComputerName` is your computer name of pc Server
```xml
<?xml version="1.0" encoding="utf-8" ?>
<Variable>
  <sharedFolder>\\YourComputerName\Saves\</sharedFolder>
</Variable>
```

#### 5. Run the Application
- Execute the application.
- Ensure administrative privileges are granted to allow symbolic link creation.

#### Setting default Password: 123123

### Client-Side Setup Instructions

#### 1. Create a Shortcut
- Create a shortcut file of the application on your desktop.
- Right-click the shortcut, select `Properties`, and check the box for `Run as administrator` under the `Shortcut tab`.

#### 2. Copy the Shortcut to Startup
- Press `Win + R` to open the Run dialog.
- Type `shell:startup` and press Enter.
- Copy the shortcut you created in the previous step and paste it into the Startup folder.



