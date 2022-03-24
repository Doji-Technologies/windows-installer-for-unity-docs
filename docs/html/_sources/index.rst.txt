Windows Installer for Unity: Installer Technology made easy!
============================================================

.. meta::
   :description lang=en: Easily create .msi installation packages for Unity applications.

`Windows Installer for Unity`_ allows developers of Windows applications built with Unity
to easily create .msi installation packages.

Minimal knowledge required
    MSI (Windows Installer) is a complex technology.
    While this asset does use WiX, an open source framework that simplifies creating installation
    packages, WiX itself has a steep learning curve. Creating even a basic installer that suits
    your needs takes someone with no prior experience a few weeks of learning the ins and outs
    of installers. WiX for Unity takes away that complexity, so you can focus on building your
    product instead of dealing with installer technology.

Fully automatable
    Developed with build automation in mind, WiX for Unity can be completely controlled via editor scripting.

.. _Windows Installer for Unity: https://assetstore.unity.com/packages/slug/215960

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Overview:

   Introduction <self>
   /msi

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Getting Started:

   /getting-started
   /first-installer

FAQ
===

Does my application need an installer?
--------------------------------------

    The truth is, most traditional Unity applications won't need one. For gaming applications, you will probably end up uploading to a store like Steam, which already handles packaging and dstribution. 

    Having an installer is mostly useful for enterprise applications, which are nowadays increasingly created with Unity.

    You can read more about the benefits of MSI for this use case :doc:`here </msi>`.