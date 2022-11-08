Limitations
===========

MSI usually packs all source files into a single, self-contained .msi file by using .cab archives. However, the .cab archive format has some size limitations:

* No one file in a CAB can exceed 2GB
* Maximum size of all files in one folder (compressed) 2GB
* Maximum size of a CAB file (compressed) 2GB
* Maximum number of files in a single CAB 64K:

(`Source`_)

Especially with media-rich Unity applications, it's pretty easy to hit the 2GB limit, which results in the following behaviour:

Installers larger than 2GB can be created, but those will not be a single, self-contained .msi file. Creating an installer larger than 2GB will instead result in an installer package that consists of more than a single file. Here is an image of what the installer files will look like:

.. image:: /_static/images/loose-files-msi.jpg
   :alt: MSI Installation Files

Users will have to download both the .msi file as well as the PFiles64/PFiles folder in order to install the application. This is a limitation of the .msi format itself and can not be worked around.

.. note::
   You might have noticed, that even single files larger than 2GB are not natively supported by MSI. But certain assets of your Unity build (Lightmaps, Texture Atlases, etc.) might easily exceed 2GB. Windows Installer for Unity works around this limitation by automatically splitting such large files at build time and creating a custom action which merges these split files back together at installation time.


.. _Source: http://www.msifaq.com/a/1043.htm