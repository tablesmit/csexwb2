csEXWB is a C# .NET 2.0 control that creates, hosts and sinks the events of the original Webbrowser control (Not .NET or any other wrapper). Advanced customization and total control over the Webbrowser control are achieved via implementation of a number of interfaces, along with the addition of many methods, properties, events and a COM library.

Here are some of the features of this control:

  * Can easily be extended by adding other interfaces and methods, unlike .NET or any other Webbrowser wrapper
  * All the basics expected from a Webbrowser wrapper are implemented
    * Setting/getting UI, and DL control flags
    * Handling of context menus, keyboard, registry, security manager, script errors, popups, authentication, security problems, font size, messageboxes, file downloads
  * Monitor HTTP and HTTPS request and response headers for all resources, images, sounds, scripts, etc, with the opportunity to add your own headers
  * When a resource has been fully downloaded and read by MSHTML engine
  * Built in onload and onunload events for top level and any frames/iframes
  * Frameset aware. All the relevant routines check for frames
  * Full drag and drop support
  * Perform automation tasks, click button, check radio, select list items,...
  * Load HTML content specifying BaseURL
  * Use the control as an MSHTML editor
  * MSHTML as a UI-less HTML parser helper class
  * Has no dependencies on MSHTML interop. All of the interfaces, enums and structs are defined within the project

A comprehensive demo that demonstrates how to use most of the functionality offered by this control beyond the basics.

  * An HTTP and HTTPS request and response header viewer
  * A complete DOM viewer.
  * Multi tab simulation.
  * Cookies and Cache viewer and remover, per site or all,
  * File download status viewer.
  * Retrieve information from document object.
  * An HTML editor with edit, source, and preview panes. Many editing functionalities, internal and external drag drop, font, color, inserting items such as table, reading and setting properties such as table cell, underline text ...
  * An UI\_Less HTML parser
  * How to use window.external function
  * Popup handling
  * HTMLDialogs handling
  * Find and highlight
  * Webbrowser automation
  * Basic authentication