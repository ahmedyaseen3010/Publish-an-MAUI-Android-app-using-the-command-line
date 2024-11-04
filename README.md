# Publish an Android App using the Command Line on .NET MAUI

Referenced from the Microsoft documentation and based on experience, here's what you will need to get the .apk file to install your application on Android devices.

<img src="images/AI.png" alt="Alt text" width="300"/>


## Prerequisites

1. **JDK Development Kit**  
   You can download the JDK from [Oracle's website](https://www.oracle.com/java/technologies/downloads/?er=221886#jdk23-windows).

## Steps to Publish Your App

1. **Navigate to the Project Folder**  
   Open the command prompt and change to the directory where your `.csproj` file exists.  
   ```bash
   cd path\to\your\project
2. **Clean Your Project**
  Run the following command to clean your project:
   ```bash
   dotnet clean

3. **Create a Keystore File**
Generate a keystore file with the following command:
   ```bash
    keytool -genkeypair -v -keystore mauiapp4.keystore -alias mauiapp4key -keyalg RSA -keysize 2048 -validity 10000
  replace the mauiapp4 with your project name

4. **Release Your Project**
Use the command below to publish your project:
   ```bash
   dotnet publish -f net8.0-android -c Release -p:AndroidKeyStore=true -p:AndroidSigningKeyStore=mauiapp4.keystore -p:AndroidSigningKeyAlias=mauiapp4key -p:AndroidSigningKeyPass=yourPassword -p:AndroidSigningStorePass=yourPassword

5. **Find Your Output Files**
After the process finishes successfully, navigate to the project bin folder:
    ```bash
   ..\MauiApp4\MauiApp4\bin\Release\net8.0-android

 
## Additional Resources
For more detailed instructions, refer to the official Microsoft documentation on MAUI and Android development.

(https://learn.microsoft.com/en-us/dotnet/maui/android/deployment/publish-cli?view=net-maui-8.0)
