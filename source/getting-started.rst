Initial Setup
=============

This document will aid you in setting up `Windows Installer for Unity`_, but you can also just follow the steps in the WiX for Unity Wizard, which will guide you through the necessary steps. It will automatically open, once you have imported the asset from the Asset Store, but you can always open the wizard by going to Window -> WiX -> Wix for Unity Wizard or alternatively, by using the keyboard shortcut :kbd:`Alt` + :kbd:`w`.

   .. figure:: /_static/images/menubar.jpg
      :width: 100%
      :align: center
      :alt: WiX for Unity Wizard in Unity's menu bar

When you've imported the package for the first time, it is necessary to install WiX. WiX is an open source framework that builds Windows installation packages (.msi) from XML source code. It is installed as a `.NET Tool <https://dotnet.microsoft.com/en-us/download>`_, which is why having .NET 3.1 or higher is one of the system requirements.


#. **Installing the .NET SDK**
   
   In the wizard, select 'Install recommended version' and download the newest version of the .NET SDK.
   At the time of this writing, the recommended version is `.NET 6.0 <https://dotnet.microsoft.com/en-us/download>`_

   This step is only necessary, if you don't already have a suitable version of .NET SDK installed.

   .. figure:: /_static/images/wizard_0.jpg
      :width: 60%
      :align: center
      :alt: WiX Wizard .NET Installation

   .. note::
      In case the wizard does not advance to the next step after installing the .NET SDK, or you are getting an error that "*'wix' is not recognized as an internal or external command*" at a later point, please try restarting your machine.

#. **Installing WiX**

   Next, hit the 'Install WiX' button and WiX will be installed in the background.

   .. figure:: /_static/images/wizard_1.jpg
      :width: 60%
      :align: center
      :alt: WiX Wizard WiX Installation

#. **Profit**

That's it. After these steps you've successfully installed WiX and are good to go. The main screen of the wizard should look something like this:

   .. figure:: /_static/images/wizard_2.jpg
      :width: 60%
      :align: center
      :alt: WiX Wizard

In the next chapter we'll go through the steps to create an installer for your project.

.. _Windows Installer for Unity: https://assetstore.unity.com/packages/slug/215960
.. _NET 60: https://dotnet.microsoft.com/en-us/download