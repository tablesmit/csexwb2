## Properties ##

  * WBDOCDOWNLOADCTLFLAG - get set - DOC\_DOWNLOAD\_CONTROL\_FLAGS
  * DownloadImages - get set - shortcut for DOCDOWNLOADCTLFLAG.DLIMAGES
  * DownloadSounds - get set - shortcut for DOCDOWNLOADCTLFLAG.BGSOUNDS
  * DownloadActiveX - get set - shortcut for DOCDOWNLOADCTLFLAG.NO\_DLACTIVEXCTLS
  * DownloadJava - get set - shortcut for DOCDOWNLOADCTLFLAG.NO\_JAVA
  * DownloadFrames - get set - shortcut for DOCDOWNLOADCTLFLAG.NO\_FRAMEDOWNLOAD
  * DownloadScripts - get set - shortcut for DOCDOWNLOADCTLFLAG.NO\_SCRIPTS
  * WBDOCHOSTUIFLAG - get set - DOC\_HOST\_UI\_FLAGS
  * Border3DEnabled - get set - Webbrowser 3D border
  * ScrollBarsEnabled - get set - Webbrowser Scrollbars
  * WBDOCHOSTUIDBLCLK - get set - DOC\_HOST\_UI\_DBLCLK
  * TextSize - get set - Webbrowser zoom property
  * CanGoBack - get - can navigate backward
  * CanGoForward - get - can navigate forward
  * WebbrowserObject - get - Document object of Webbrowser control
  * SendSourceOnDocumentCompleteWBEx - get set - fires DocumentCompleteEX event rather than DocumentComplete. DocumentCompleteEX event has one additional parameter which contains the source of the pDisp document object at the time DocmentComplete was called
  * IEServerHwnd - get - Internet Explorer\_Server HWND
  * ShellEmbedingHwnd - get - ShellEmbedding HWND
  * ShellDocObjectHwnd - get - ShellDocObject HWND
  * RegisterAsDropTarget - get set - Webbrowser default drag drop
  * RegisterForInternalDragDrop - get set - Instructs the control to take over drag drop. Uses WBDragxxx and WBDropxxx events to notify the client
  * RegisterAsBrowser - get set - Registers Webbrowser as a top-level browser for target name resolution
  * Silent - get set - whether the Webbrowser control can show dialog boxes
  * LocationName - get - name of the resource that Webbrowser control is currently displaying
  * LocationUrl - get set - URL of the resource that Webbrowser control is currently displaying
  * Busy - get - indicating whether the Webbrowser control is engaged in a navigation or downloading operation
  * OffLine - get set - currently operating in offline mode
  * ReadyState - get - retrieves Readystate of the Webbrowser control
  * ThumbImage - get - Contains a thumb image of the Webbrowser or null
  * ObjectForScripting property. Allows JavaScript functions in an HTML page to call methods and properties of a an instance class passed to this property. Same as ObjectForScripting of C# Webbrowser wrapper control. An example of how to use this property has been provided in WinExternal class of frmMain
  * DocumentTitle - Sets or retrieves the title of the document
  * DocumentSource - Sets or retrieves the HTML source of the document
  * UseInternalDownloadManager - Set to true, default, to allow the control to take over file downloads. FileDownloadExxxx events are fired instead of FileDownload event. This functionality is achieved via COM library which implements IDownloadManager interface. The download routines account for redirect and Content\_Disposition header
  * FileDownloadDirectory Default file download directory. Set to users 

&lt;EM&gt;

MyDocuments

&lt;/EM&gt;

 folder by default. Used only if UseInternalDownloadManager property is set to true
## Methods ##
### Basic ###
These methods are self explanatory

  * public void Navigate(string URL)
  * public void Navigate(string URL, BrowserNavConstants Flags)
  * public void Navigate(string URL, BrowserNavConstants Flags, string TargetFrameName)
  * public void Navigate(string URL, BrowserNavConstants Flags, string PostData)
  * public void Navigate(string URL, string PostData)
  * public void Navigate(string URL, byte[.md](.md) PostData)
  * public void Navigate2(string URL)
  * public void Stop()
  * public bool GoBack()
  * public bool GoForward()
  * public void GoHome()
  * public void GoSearch()
  * public void Refresh2(RefreshConstants Level)
  * public bool SelectAll()
  * public bool Clear()
  * public bool ClearSelection()
  * public bool Copy()
  * public bool Paste()
  * public bool Cut()
  * public bool Undo()
  * public bool Redo()
  * public bool Delete()
  * public bool PasteSpecial()
  * public bool Spell()
  * public bool NewWindow()
  * public bool Print()
  * public bool Print2()
  * public bool Properties()
  * public bool PrintPreview()
  * public bool PrintPreview2()
  * public bool PageSetup()
  * public void SaveAs()
  * public bool Find()
  * public bool IEOptions()
  * public bool ViewSource()
  * public void OrganizeFavorites()
  * public void PrivacySettings()
  * public void LanguageDialog()
  * public void ProgramAccessAndDefaults()
  * public void AddToFavorites()
  * public void ImportExport()
  * public void SendLinkByEmail()
  * public void SendPageByEmail()
  * public void SendShortcutToDesktop()
### Extended ###
Note: In a frameset, bTopLevel parameter determines whether to use the top level document or attempt to find and use the active document

  * public bool LoadUrlIntoBrowser(String url) - Loads a URL into browser using IPersistMoniker interface
  * public bool LoadHtmlIntoBrowser(string html, string sBaseUrl) - Loads HTML content into browser using LoadHTMLMoniker class and IPersistMoniker interface, allowing client to set the baseurl
  * public bool LoadHtmlIntoBrowser(string html) - Loads HTML content into browser using IPersistStreamInit interface, baseurl, is set to about:blank by MSHTML
  * public void ShowCertificateDialog() - If available, displays certificate for current website
  * public Image DrawThumb(int W, int H, System.Drawing.Imaging.PixelFormat pixFormat) - Uses IE\_Server HWND to draw a thumb image of the Webbrowser control. Faster than other methods with one draw back. It only works if the Webbrowser control is in front of Zorder
  * public Image DrawThumb2(int W, int H, System.Drawing.Imaging.PixelFormat pixFormat) - Uses IViewObject interface obtained from IHTMLDocument2 to draw a thumb image of the Webbrowser control
  * public void SaveBrowserImage(string sFileName, System.Drawing.Imaging.PixelFormat pixFormat, System.Drawing.Imaging.ImageFormat format) - Saves Webbrowser image
  * public bool HasFocus()
  * public void SetFocus()
  * public void SetFocusBody()
  * public bool FindInPage(string sFind, bool DownWard, bool MatchWholeWord, bool MatchCase, bool ScrollIntoView) - Finds a match. Returns true, if found, else false. In a frameset, it attempts to find and use the active document.
  * public int FindAndHightAllInPage(string sFind, bool MatchWholeWord, bool MatchCase, int cbackColor, int cForeColor) - Finds and highlights all matches. Returns number of matches found. In a frameset, it attempts to find and use the active document.
  * public int FindAndHightAllInPage(string sFind, bool MatchWholeWord, bool MatchCase, string cbackColor, string cForeColor)
  * public int FindAndHightAllInPage(string sFind, bool MatchWholeWord, bool MatchCase, Color cbackColor, Color cForeColor)
  * public bool IsCommandEnabled(string sCmdId) - Wrapper for IHTMLDocument2::queryCommandEnabled
  * public bool SetDesignMode(string sMode)
  * public string GetDesignMode()
  * public IHTMLElement GetActiveElement() - Returns the active element or null. Accounts for frames
  * public IHTMLDocument2 GetActiveDocument() - Returns the active document or null. Accounts for frames
  * public string GetTitle(bool bTopLevel) - Wrapper for IHtmlDocument2::title
  * public string GetTitle(IWebBrowser2 thisBrowser)
  * public string GetText(bool bTopLevel) - Wrapper for IHTMLDocument3::outerText
  * public string GetText(IWebBrowser2 thisBrowser)
  * public string GetSource(bool bTopLevel) - Wrapper for IHTMLDocument3::outerHTML
  * public string GetSource(IWebBrowser2 thisBrowser)
  * public IHTMLElementCollection GetImages(bool bTopLevel) - Wrapper for IHTMLDocument2::images
  * public IHTMLElementCollection GetAnchors(bool bTopLevel) - Wrapper for IHTMLDocument2::anchors
  * public string GetSelectedText(bool bTopLevel, bool ReturnAsHTML) - Returns selection as plain text or HTML.
  * public IHTMLElement ElementFromPoint(bool bTopLevel, int X, int Y) - Wrapper for IHTMLDocument2::elementFromPoint
  * public bool ExecCommand(bool bTopLevel, string CmdId) - Wrapper for IHTMLDocument2::execCommand
  * public bool QueryCommandState(bool bTopLevel, string CmdId) - Wrapper for IHTMLDocument2::queryCommandState
  * public bool OleCommandExec(bool bTopLevel, MSHTML\_COMMAND\_IDS CmdID) - Wrapper for IHTMLDocument2::IOleCommandTarget::Exec
  * public object QueryCommandValue(string CmdID) - Wrapper for IHTMLDocument2::queryCommandValue
  * public bool QueryCommandState(bool bTopLevel, string CmdId) - Wrapper for IHTMLDocument2::queryCommandState
  * public IHTMLElement GetElementByID(bool bTopLevel, string idval) - Wrapper for IHTMLDocument3::getElementById
  * public IHTMLElementCollection GetElementsByTagName(bool bTopLevel, String tagname) - Wrapper for IHTMLDocument3::getElementsByTagName
  * public IHTMLElementCollection GetElementsByName(bool bTopLevel, string elemname) - Wrapper for IHTMLDocument3::getElementsByName
  * public object execScript(bool bTopLevel, string ScriptName, string ScriptLanguage) - Wrapper for IHTMLWindow2::execScript
  * public bool OleCommandExec(bool bTopLevel, MSHTML\_COMMAND\_IDS CmdID, object pvaIn) - Wrapper for IHTMLWindow2::execScript which accepts a parameter
  * public object InvokeScript(string ScriptName, object[.md](.md) Data) - Invokes a script within the HTML page
  * public object InvokeScript(IWebBrowser2 wb, string ScriptName, object[.md](.md) Data) - Invokes a script within the HTML page
  * public bool IsFrameset()
  * public int FramesCount()
  * public List&lt;IWebBrowser2&gt; GetFrames() - Returns a List populated with the IWebbrowser interfaces of the frames
  * public bool CreateInternetShortCut(string LocalFileName, string URL, string Description, string IconFileName, int IconIndex) - Attempts to create an Internet shortcut
  * public string ResolveInternetShortCut(string InternetShortCutPath) - Attempts to resolve an Internet shortcut
  * public bool ClearHistory() - Clears IE history
  * public void ActivateHTMLEvents(HTMLEventType EventType, int[.md](.md) HTMLEventDispIds) - Activates either HTMLdocument or HTMLWindow events
  * public void DeactivateHTMLEvents(HTMLEventType EventType) - Deactivates previously activated HTMLDocument or HTMLwindow events
  * public int DownloadFile(string Url) Attempts to download a file asynch. </CODE />FileDownloadExXXX </CODE />events are used for notifications. Return value is a unique id for this download that can be used to stop the download
  * public void StopFileDownload(int dlUID) Stops a file download that was started by calling DownloadFile method
  * public void StartHTTPAPP() Call to start receiving HTTP request and response headers via ProtocolHandlerOnResponse and ProtocolHandlerOnBeginTransaction events
  * public void StopHTTPAPP() Call to stop ProtocolHandlerOnResponse and ProtocolHandlerOnBeginTransaction events for HTTP protocol
  * public void StopHTTPSAPP() Call to stop ProtocolHandlerOnResponse and ProtocolHandlerOnBeginTransaction events for HTTPS protocol
  * public void StartHTTPSAPP() Call to start receiving HTTPS request and response headers via ProtocolHandlerOnResponse and ProtocolHandlerOnBeginTransaction events
  * void SetAllowHTMLDialogs() - default true - set allow or disallow flag for HTML dialogs launched using showModelessDialog() and showModalDialog() methods using CBT Window Hook
  * bool GetAllowHTMLDialogs() - get allow or disallow flag for HTML dialogs launched using showModelessDialog() and showModalDialog() methods using CBT Window Hook
  * public bool AutomationTask\_PerformClickButton(string btnname) - Performs a click on a Button element with given name
  * public bool AutomationTask\_PerformClickLink(string linkname) - Performs a click on a Link element with given name
  * public bool AutomationTask\_PerformEnterData(string inputname, string strValue) - Enters strValue into an input element with given name
  * public bool AutomationTask\_PerformEnterDataTextArea(string inputname, string strValue) - Enters strValue into a textarea element with given name
  * public bool AutomationTask\_PerformSubmitForm(string formname) - Submits a form with given name
  * public bool AutomationTask\_PerformSelectList(string selectname, string listitemvalue) - Selects a list item element with given listitemvalue
  * AutomationTask\_PerformSelectRadio(string radioname) - Selects a radio or checkbox element with given radioname
## Events ##
### DWebBrowserEvents2 ###
DocumentComplete has been modified to include an extra parameter, IsTopLevel which indicates whether we have the top level document.

  * DocumentComplete
  * BeforeNavigate2
  * ClientToHostWindow
  * CommandStateChange
  * DownloadBegin
  * DownloadComplete
  * FileDownload
  * NavigateComplete2
  * NavigateError
  * NewWindow2
  * NewWindow3
  * PrintTemplateInstantiation
  * PrintTemplateTeardown
  * PrivacyImpactedStateChange
  * ProgressChange
  * PropertyChange
  * SetSecureLockIcon
  * StatusTextChange
  * TitleChange
  * WindowClosing
  * WindowSetHeight
  * WindowSetLeft
  * WindowSetResizable
  * WindowSetTop
  * WindowSetWidth
  * UpdatePageStatus
### Drag Drop ###
To use internal drag drop functionality, RegisterForInternalDragDrop must be set to true (default)

  * WBDragEnter
  * WBDragLeave
  * WBDragOver
  * WBDragDrop
### Extended ###
FileDownloadExXXX events are activated by setting UseInternalDownloadManager property to true (default)

  * WBKeyDown - Rather than just firing when accelerator keys are used, I have decided to intercept key down and up which I find to be more useful
  * WBKeyUp
  * WBContextMenu - Handle context menus
  * WBGetOptionKeyPath - Allows the client to set up their own registry settings for Webbrowser control to use
  * WBDocHostShowUIShowMessage - Allows interception of messageboxes
  * DocumentCompleteEX - Setting SendSourceOnDocumentCompleteWBEx property will cause this event to fire instead of DocumentComplete, passing an extra parameter which contains the source of the document
  * WBAuthenticate - Fires for basic and NTLM authentications. For NTLM, client needs to pass credentials as, Username = Domain\username
  * WBSecurityProblem - Fires when WinInet encounters a security problem
  * WBEvaluteNewWindow - XPsp2, replaces NewWindowx events
  * RefreshBegin
  * RefreshEnd
  * ScriptError - Fires for script errors. Contains all details in regard to script error
  * ProcessUrlAction - Policy based URL processing
  * HTMLEvent - Only event handler for HTMLDocument and HTMLwindow events
  * FileDownloadExStart - If UseInternalDownloadManager true, notifies client of a request to start a file download. Stop download at any point using a unique id, save file in the background, ... Overrides webbrowser default file download mechanism
  * FileDownloadExEnd - If UseInternalDownloadManager true, notifies client of end of a file download
  * FileDownloadExProgress - If UseInternalDownloadManager true, notifies client of status of a file download
  * FileDownloadExAuthenticate - If UseInternalDownloadManager true, notifies client of a request from server for authentication
  * FileDownloadExError - If UseInternalDownloadManager true, notifies client of an error during a file download
  * ProtocolHandlerOnBeginTransaction Enables the client to view all the HTTP and HTTPS request headers of webbrowser control
  * ProtocolHandlerOnResponse Enables the client to view all HTTP and HTTPS the response headers of webbrowser control
  * AllowFocusChange - IE7 Vista - notify client when focus is being changed via implementation of IProtectFocus interface
  * HTMLOMWindowServices\_moveTo - IHTMLOMWindowServices implementation - Moves the screen position of the upper-left corner of the application window to the specified coordinates
  * HTMLOMWindowServices\_moveBy - IHTMLOMWindowServices implementation - Moves the screen position of the application window by the specified offset values
  * HTMLOMWindowServices\_resizeTo - IHTMLOMWindowServices implementation - Changes the current size of the application window by the specified offset values.
  * HTMLOMWindowServices\_resizeBy - IHTMLOMWindowServices implementation - Sets the size of the application window to the specified values