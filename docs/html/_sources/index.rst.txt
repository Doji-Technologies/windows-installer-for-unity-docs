Windows Installer for Unity: Installer Technology made easy!
============================================================

.. meta::
   :description lang=en: Easily create .msi installation packages for Unity applications.

`Windows Installer for Unity`_ allows developers of Windows applications built with Unity
to easily create .msi installation packages.

Minimal knowledge required
    MSI (Windows Installer) is a complex technology.
    Under the hood, this asset uses WiX, an open source framework that simplifies creating installation
    packages. But WiX itself also has a steep learning curve. Creating an installer that suits
    your needs takes someone with no prior experience a few weeks of learning the ins and outs
    of how MSI installers work. WiX for Unity takes away that complexity, so you can focus on building your
    product instead of dealing with installer technology.

Fully automatable
    Developed with build automation in mind, WiX for Unity can be completely controlled via editor scripting.

.. _Windows Installer for Unity: https://assetstore.unity.com/packages/slug/215960

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Overview

   Introduction <self>
   /msi

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Getting Started

   /getting-started
   /first-installer

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Advanced

   /limitations

FAQ
===

Does my application need an installer?
--------------------------------------

    The truth is, most traditional Unity applications won't need one. For gaming applications, you will probably end up uploading to a platform like Steam or itch.io anyway. Those already handle packaging and distribution for you. 

    Having an installer is mostly useful for enterprise applications, which are nowadays increasingly created with Unity.

    You can read more about the benefits of MSI for this use case :doc:`here </msi>`.


Does having an installer remove the Windows Security popup that can appear when running a Unity application on a different computer?
------------------------------------------------------------------------------------------------------------------------------------

    Having an installer does **not** solve the issue that `Microsoft SmartScreen`_ might notify its users with a message that your app is potentially unsafe. The general advice on how to solve this is, that you should both:

    *  Code-sign your application by purchasing a certificate from a `Certificate Authority`_.
    *  Get your application out to enough users so SmartScreen eventually considers it safe.

    According to `this thread <https://forum.unity.com/threads/windows-10-alert-on-some-machines.427969/>`_ the message can still pop up even when you've code-signed your application. So signing alone seems to be not enough.

    .. _Microsoft SmartScreen: https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview
    .. _Certificate Authority: https://docs.microsoft.com/en-us/windows-hardware/drivers/dashboard/get-a-code-signing-certificate#extended-validation-code-signing-certificates