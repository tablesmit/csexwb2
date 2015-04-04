#Using the control in a x86 environment

Typical error messages recieved after registering the COM component and attempting to run the DemoApp:

Retrieving the COM class factory for component
with CLSID {A1FE23EF-03EF-4759-B021-668443C37A24} failed due to the
following error: 80040154 (Class not registered)

The debugger does not support debugging managed and native code at the same
time on this platform.

**ROOTCAUSE**

.NET 2.0 projects, by default, are set to target both the x86 (32-bit) and
x64 (64-bit) platforms. So an application runs as a 64-bit application when
launched on a x64 operating system, and as 32-bit application when launched
on 32-bit operating system.

64-bit applications can't link/use 32-bit libraries (.dll).

DemoApp runs as a 64-bit application, and because it tries to
link to a 32-bit dependency, it fails.

**WORKAROUND**

Solution:

---

  1. Go to Visual Studio 2008 (probably similar in 2005)
  1. In "Solution Explorer" right click on the "DemoApp" project.
  1. Choose the "Properties" menu item
  1. Select the "Build" tab (left side)
  1. In the "General" section set the "Platform target:" to "x86".
  1. Save and clean/rebuild.

  1. Rebuild ComUtilities with x64 (64-bit) support.

Temporary Client Solution:

---

To get applications that were built by others, that use csExWB, that did
not perform the above procedure. You can modify the PE header of the
executable (using the "Corflags.exe" .NET Framework SDK utility) to force
the executable to run in x86 mode on the x64 platform.

Information on "Corflags.exe" can be found here:
http://www.request-response.com/blog/PermaLink,guid,cf345d71-cdc7-46b9-8c1c-eb21581a9222.aspx

The procedure is to:

  1. Go to the Start Menu, and Navigate to the "Microsoft Visual Studio 2008" folder, expand it and under the "Visual Studio Tools" folder, ran the "Visual Studio 2008 Command Prompt".
  1. In the command prompt, navigate to the folder where executable is located.
  1. Run the command "corflags /32BIT+ EXEName.exe"
  1. Run "corflags EXEName.exe" to verify that the "32BIT" flag was set to "1".
  1. You're done! You can now run the application properly.