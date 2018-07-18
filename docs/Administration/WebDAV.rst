.. _WebDAV:

======
WebDAV
======

WebDAV enables you to use the third party tools to communicate with
hierarchical content servers via HTTP. It is possible to add and remove
documents or a set of documents from a path on the server.

.. note:: If you add some documents (by uploading) via WebDAV, you should check carefully its version history. See :ref:`Document Versioning <via-webdav>` for more details.

**What is WebDAV?**

**WebDAV** is an abbreviation of **Web-based Distributed Authoring** and
**Versioning**. It is used to publish and manage files and directories
on a remote server. It also enables users to perform these functions on
a website.

WebDAV provides the following features:

*Locking*
    This feature prevents two or more collaborators from overwriting
    shared content.

*Site Manipulation*
    WebDAV supports the "copy" and "move" actions and the creation of
    *collections* (file system directories).

*Name Space Management*
    This function enables copying and moving webpages within a server's
    namespace.

**Why uses WebDAV?**

With WebDAV, you can manage content efficiently with the following
actions:

-  Copying/pasting content on your device and have those changes
   reflected in a host-based site.

-  Manipulating actions on a content easily, quickly and flexibly
   without accessing it directly via web browsers. Content can be
   accessed from anywhere and is stored in local directories.

-  Easily and quickly uploading content to eXo Platform simply by copying it
   into the appropriate directory.
   
.. _ConnectToWebDav:   

Connecting to WebDAV
~~~~~~~~~~~~~~~~~~~~~~

In eXo Platform, there are 2 modes of WebDAV:

-  **Public**: Login is not required, and users can view all the public
   items. The URL to access will be:
   `http://mycompany.com:port/rest/jcr/{RepositoryName}/{WorkspaceName}/{Path} <http://mycompany.com:port/rest/jcr/{RepositoryName}/{WorkspaceName}/{Path}>`__
   or
   `dav://mycompany.com:port/rest/jcr/{RepositoryName}/{WorkspaceName}/{Path} <dav://mycompany.com:port/rest/jcr/{RepositoryName}/{WorkspaceName}/{Path}>`__.

-  **Private**: Login is required, and users can view all the items
   which they had access right. The URL to access will be:
   `http://mycompany.com:port/rest/private/jcr/{RepositoryName}/{WorkspaceName}/{Path} <http://mycompany.com:port/rest/private/jcr/{RepositoryName}/{WorkspaceName}/{Path}>`__
   or
   `dav://mycompany.com:port/rest/private/jcr/{RepositoryName}/{WorkspaceName}/{Path} <dav://mycompany.com:port/rest/private/jcr/{RepositoryName}/{WorkspaceName}/{Path}>`__.

In which:

-  **mycompany.com:port**: The URL of your site.

-  **RepositoryName**: The repository name.

-  **WorkspaceName**: The workspace name.

-  **path**: The path of the content.

The access to your workspace via various WebDAV clients is not the same.
This part will give instructions about using WebDAV over a web browser
and common WebDAV clients. It is assumed that you want to access the
Wiki Home of the "Support Team" space, do as follows:

**Over a web browser:**

Simply enter
`http://mycompany.com:port/rest/private/jcr/repository/collaboration/Groups/spaces/support\_team/ApplicationData/eXoWiki/WikiHome <http://mycompany.com:port/rest/private/jcr/repository/collaboration/Groups/spaces/support_team/ApplicationData/eXoWiki/WikiHome>`__
into the address bar of your browser. The selected content will be shown
in WebDAV as below:

|image149|

**Nautilus (Linux):**

1. Open Nautilus - the file manager (GNOME Files), then open the address
   bar (by using the hot key: Ctrl + L).

2. Enter
   ``dav://mycompany.com:8080/rest/private/jcr/repository/collaboration/Groups/spaces/support_team/ApplicationData/eXoWiki/WikiHome``
   into the address bar.

3. Enter your username and password in the login form.

|image150|

4. Click **Connect**. You will be redirected to the Wiki Home window as
   below:

|image151|

**Windows Explorer (Windows 7):**

1. Open the Computer window, then click **Map network drive**.

|image152|

2. Select any available letter for the drive in the Drive list.

3. Enter
   ``http://mycompany.com:8080/rest/private/jcr/repository/collaboration/Groups/spaces/support_team/ApplicationData/eXoWiki/WikiHome``
   into the **Folder** field.

|image153|

Select the Reconnect at logon checkbox to connect every time you log
onto your computer.

4. Click **Finish**, then enter your username and password into the
   **Windows Security** pop-up, and click **OK** to connect. You will be
   redirected to the Wiki Home window.

.. note:: If you still do not connect successfully, check if you have followed instructions in :ref:`WebDAV restrictions <WebDAV.Restrictions>`.

**Windows Explorer (Windows 8):**

The procedure to set up a web folder by "mapping a network drive"
through My Computer in Windows 8 is quite similar to that in Windows 7.
Note that you need to point to the down pointer at the upper-right
corner of the Computer windows to show **Map network drive**.

.. note:: If you still do not connect successfully, check if you have followed instructions in :ref:`WebDAV restrictions <WebDAV.Restrictions>`.

**Windows Explorer (Windows XP):**

1. Navigate to the **My Network Places**.

2. Click the Add a network place link on the left to open the 
   **Add Network Place Wizard**.

|image154|

3. Click **Next** to select a network location.

4. Select Choose another network location to create a shortcut, then 
   click **Next**.

|image155|

5. Enter `http://mycompany.com:8080/rest/private/jcr/repository/collaboration/Groups/spaces/support_team/ApplicationData/eXoWiki/WikiHome <http://mycompany.com:8080/rest/private/jcr/repository/collaboration/Groups/spaces/support_team/ApplicationData/eXoWiki/WikiHome>`__
   into the Internet or network address field, then click **Next**.

6. Enter your usename and password into the login form.

7. Type name for your network place, then click Next.

8. Select the Open this network place when I click Finish option, then
   click Finish.

9. Enter your usename and password again to access your selected folder.
   You will be redirected to the selected folder as below:

|image156|

**"net use" command**

In addition, for Windows, you can use the "net use" command to connect a
drive in your computer with the shared resource of eXo Platform. The command
format will be:
``net use X: http://mycompany.com:port/rest/private/jcr/{RepositoryName}/{WorkspaceName}/{Path}``
where X: is the drive letter you want to assign to the shared resource.

1. Open the cmd screen.

2. Type the "net use" command, for example:

``net use E: http://mycompany.com:port/rest/private/jcr/repository/collaboration/Groups/spaces/support_team/ApplicationData/eXoWiki/WikiHome``,
   
   then hit Enter.

3. Enter username and password as requested in the screen. If your
connection is successful, you will get a message like: "The command
completed successfully". If not successful, check if you have followed
steps in :ref:`WebDAV Restrictions <WebDAV.Restrictions>`.

4. Open the Computer window, then select the **E:** drive. Here you will
   see the Wiki content of the Support Team space.

.. note:: If you still do not connect successfully, check if you have followed instructions in :ref:`WebDAV restrictions <WebDAV.Restrictions>`.

.. _WebDAV.Restrictions:

WebDAV restrictions
~~~~~~~~~~~~~~~~~~~~~

There are some restrictions for WebDAV in different OSs.

**Windows 7/Windows 8**

When you try to set up a web folder by "adding a network location" or
"mapping a network drive" through My Computer, you can get an error
message saying that either "The folder you entered does not appear to be
valid. Please choose another" or "Windows cannot access... Check the
spelling of the name. Otherwise, there might be ...". These errors may
appear when you are using SSL or non-SSL. To fix this problem, do as
follows:

**Windows 7**

1. Click Start, type **regedit** in the Start Search box, then hit Enter 
   to open the Windows Registry Editor.

2. Find the key:
``HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlset\services\WebClient\Parameters``.

3. Select ``BasicAuthLevel`` and change its value to 2. If this does not
   exist, create it as a ``REG_DWORD`` key.

4. Reboot your OS.

**Windows 8**

1. Go to Windows Registry Editor, then find the key:
``HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlset\services\WebClient\Parameters``.

2. Select ``UseBasicAuth`` and change its value to 1. If this does not
   exist, create it as a ``REG_DWORD`` key.

3. Select ``BasicAuthLevel`` and change its value to 2. If this does not
   exist, create it as a ``REG_DWORD`` key.

4. Reboot your OS.

**Microsoft Office 2010**

If you have Microsoft Office 2010 or Microsoft Office 2007 applications
installed on a client computer, try to access an Office file that is
stored on a web server that is configured for Basic authentication from
the client computer. The connection between your computer and the web
server does not use Secure Sockets Layer (SSL). When you try to open or
to download the file, you may see the following problems:

-  The Office file is not opened or downloaded.

-  You do not receive a Basic authentication password prompt when you
   try to open or to download the file.

-  You do not receive an error message when you try to open the file.
   The Office application will start, but the selected file is not
   opened.

To fix these errors, enable the Basic authentication on the client
computer as follows:

1. Click Start, type **regedit** in the Start Search box, then hit Enter.

2. Locate and then click the following registry subkey:
``HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Common\Internet``.

3. On the Edit menu, point to **New**, then click **DWORD Value**.

4. Type ``BasicAuthLevel``, then hit Enter.

5. Right-click ``BasicAuthLevel``, then click **Modify**.

6. In the Value data box, type **2**, then click **OK**.

7. Reboot your OS.


