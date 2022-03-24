Creating your first installer
=============================

Once WiX is setup, creating our first installer is only a few clicks away. We have a few options for this.

#. **Manually creating the installer**

   Creating an installation package for an existing build can be done by clicking the first button in the WiX for Unity Wizard. It will prompt you to select the folder of your Unity build. Next, it will prompt you to choose a name for your installation package (.msi file). After you hit '*Save*', the installer will be generated.

#. **Enabling automatic creation of installation packages**

   WiX for Unity was created with build automation in mind. If you head over to the WiX Settings in the Project settings window. You'll see the option to **'Automatically Create Installer on Build'**. Enabling this, will generate an installer every time you do a build in Unity.

#. **Integration into your own build pipeline**

   While the option above shows, that the process of generating an installer can be completely automated, you might not want to create an installer for every build you do. In case you have your own pipeline and want to control exactly when an installer is created, WiX for Unity can be controlled through editor scripts as well. Creating an installer is as simple as calling

   .. code-block:: java 
    
       WiX.CreateInstaller(buildPath, msiPath);