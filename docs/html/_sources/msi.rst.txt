The Key Benefits of MSI
=======================

Others have done a way better job at summarizing the benefits (and shortcomings!) of Windows Installer technology.
Most notably a person named Stein Åsmul who has provided one of the most `comprehensive summaries`_.

In short:
**MSI (Windows Installer)** is the **standard for corporate deployment** since it offers `a number of corporate benefits of major significance`_ compared to previous installation technologies. The benefits center around **reliable remote management** and **standardization** - crucial corporate deployment concerns.

In brief the most important, **specific benefits** are probably:

#. **Reliable silent running** (standardized & completely suppressible GUI)
#. **Implicitly available uninstall** (a nightmare when dealing with legacy setups)
#. **Transparency** (installer's semi-transparent and inspectable nature - except compiled CAs)
#. **Elevated installation rights** (no messy temporary admin rights)
#. **Standardized command line** (no hunting for "secret" switches)
#. **Administrative installation** (file extract - essential for corporate repackaging)
#. **Verbose logging** (helpful and verbose indeed :-) )
#. **Standardized package customization** (transforms - database fragments)
#. **Rollback support** (can undo changes for failed installs)
#. **Inventory** (management and reporting: full registration of what is installed and where)
#. **Active Directory / GP integration**

Altogether this yields MSI's overall benefit: **reliable, remote management of deployment for busy system administrators in large, corporate environments.** Crucial benefits, despite the technology's complexity and quirkiness.

.. _comprehensive summaries: https://serverfault.com/questions/11670/the-corporate-benefits-of-using-msi-files/274609#274609
.. _a number of corporate benefits of major significance: https://serverfault.com/questions/11670/the-corporate-benefits-of-using-msi-files/274609#274609