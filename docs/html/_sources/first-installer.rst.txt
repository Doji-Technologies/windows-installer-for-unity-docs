Creating your first installer
=============================

Once WiX is set up, creating our first installer is only a few clicks away. We have a few options for this.

#. **Manually creating the installer**

   Creating an installation package for an existing build can be done by clicking the first button in the WiX for Unity Wizard. It will prompt you to select the folder of your Unity build. Next, it will prompt you to choose a name for your installation package (.msi file). After you hit '*Save*', the installer will be generated.

#. **Enabling automatic creation of installation packages**

   WiX for Unity was created with build automation in mind. If you head over to the WiX Settings in the Project settings window. You'll see the option to **'Automatically Create Installer on Build'**. Enabling this, will generate an installer every time you do a build in Unity.

#. **Integration into your own build pipeline**

   While the option above shows, that the process of generating an installer can be completely automated, you might not want to create an installer for every build you do. In case you use custom build scripts and want to control exactly when an installer is created, WiX for Unity can be controlled through editor scripts as well. Creating an installer is as simple as calling ``WiX.CreateInstaller(report);`` where *'report'* is a `BuildReport`_ object that Unity passes to scripts implementing the `IPostprocessBuildWithReport`_ interface. A complete sample might look like this:

   .. code-block:: C#
      :linenos:
      :emphasize-lines: 19

      using UnityEditor;
      using UnityEditor.Build;
      using UnityEditor.Build.Reporting;

      public class MyCustomBuildProcessor : IPostprocessBuildWithReport {

         public int callbackOrder { get { return 0; } }

         public void OnPostprocessBuild(BuildReport report) {
            if (!WiX.IsPlatformSupported) {
               return;
            }

            if (report.summary.platform != BuildTarget.StandaloneWindows &&
               report.summary.platform != BuildTarget.StandaloneWindows64) {
               return;
            }

            WiX.CreateInstaller(report);
         }
      }

   .. _IPostprocessBuildWithReport: https://docs.unity3d.com/ScriptReference/Build.IPostprocessBuildWithReport.OnPostprocessBuild.html
   .. _BuildReport: https://docs.unity3d.com/ScriptReference/Build.Reporting.BuildReport.html