.. _Manage-Documents:

###########################
Managing Your Documents
###########################

    This chapter gives you a tutorial of the **Documents** application
    and step-by-step instructions on how to use basic actions via the
    following main topics:

    -  :ref:`Documents Interface <DocumentsInterface>`
       Overall introduction to the **Documents** interface, and common views which can be switched in the **Documents** application.

    -  :ref:`Navigating through Documents <NavigatingThroughDocuments>`
       Ways to browse your documents in the **Documents** application, both in the **Icons** and **List** views.

    -  :ref:`Document Viewer <DocumentViewer>`
       Introduction to the document types and how the Document Viewer enhances the readability and the collaboration.

    -  :ref:`Open in Office <OpenInOffice>`
       Introduction to this feature, as well as compatibility and client
       requirements that you need to know.

    -  :ref:`Working with basic actions <WorkingWithBasicActions>`
       Step-by-step instructions on how to do basic actions on your documents and folders.

    -  :ref:`Organizing your  content <OrganizingYourContent>`
       Instructions on various ways for you to arrange your documents efficiently.

    -  :ref:`Sharing your documents <SharingYourDocuments>`
       Information about the Share and Auto-share features which are integrated into the **Documents** application.

    -  :ref:`Extending your actions <ExtendingYourActions>`
       Detailed instructions on how to extend some useful actions which are not set by default in the **Documents** application.

The content management is one of key strategies in the organizational
process of each enterprise. A good content management allows you to:

-  Store, share and work on the same content efficiently.

-  Trace changes of content intuitively and instantly.

-  Simplify the way to manage your content.

The Enterprise Content Management system delivered by eXo Platform not only
satisfies basic demands (for example, uploading, previewing and
sharing/editing), but also makes useful capabilities available
(versioning, metadata, advanced searches, and more). These new
management solutions featured in the **Documents** application are built
on existing content management capabilities in a flexible and practical
way.


.. note::    -  The "document" denotes a file, script, image or piece of information.

			 -  The "folder" denotes a directory which contains a set of documents and even sub-folders.

			 -  The "content" is used for denoting both document and folder.


.. _DocumentsInterface:

===================
Documents Interface
===================

After logging into the :ref:`Social Intranet homepage <PLFHomepage>`
successfully, you simply click **Documents** on the left panel to be
redirected to the **Documents** interface. As a normal user, you can
switch between **Icons** and **List** views by clicking |image0| or
|image1| respectively.

|image2|

If you are an administrator, you can see **Documents** in the **Admin**
view.

|image3|

.. note::Refer to :ref:`Views <#PLFUserGuide.AdministeringeXoPlatform.ContentAdministration.WorkingWithExplorer.Views>`
			to learn about differences between views.

The way to do actions on content is different between **Icons** and
**List** views as follows:

-  In the **Icons** view, you can do actions via the Right-click action
   or directly on the **Action** bar.

-  In the **List** view, the Right-click action is disabled.

Depending on your various purposes, you are free to switch between the
**Icons** and **List** views just in one click. That is, if you want to
see your content as images, it is recommended you use the **Icons**
view.

|image4|

But in case you want to see more details directly in the view, the
**List** view is an optimal choice.

|image5|

Here's what you can do in the **List** view:

-  Seeing important details of your content, including name,
   created/updated dates, creator, file size, directly in the view.
   Other information (such as extension, version number) is also present
   here, if any.

-  Showing/Hiding children of content without going inside it. Thus, you
   can have multiple folders opened in the view.

-  Changing the current context for a specific content simply clicking
   its name.

-  Doing basic actions on your content.


.. _Navigate-through-document:

============================
Navigating through Documents
============================

In the **Documents** application, you can store your content in both
drives and folders. However, to make ease for browsing your content, you
are advised to keep them in relevant folders. You can browse your
content in various ways, for example:

-  In the **Icons** view, double-click the content to open it.

-  In the **List** view, click |image6| to expand a specific folder that
   allows you to see its children without going into the folder. To hide
   its children, simple click |image7| to collapse this view.

-  Enter the path of the relevant content directly into the address bar.

   |image8|

   You can come back to the previous content by clicking |image9|.

-  Browse your content from the left sidebar in the **Icons** view. In
   the **List** and **Admin** views, the sidebar is disabled by default.
   To browse in this way, refer to `Hide explorer panel in
   sidebar <#HidingExplorerPanelInSidebar>`__.

-  Switch to another drive by clicking |image10| on the Action bar. A
   list of drives which are accessible to you will be shown.

.. note:: Depending on your role and permission, you will see various drives. See
			:ref:`Drives <#PLFUserGuide.AdministeringeXoPlatform.ContentAdministration.WorkingWithExplorer.Drives>` for more details.


.. _Document-viewer:

===============
Document Viewer
===============

.. _Viewable-types:

The viewable document types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Documents application allows users to build custom content types and
provides some built-in content types. It also provides a viewer for
common file types so users can read Office documents, view images or
play videos directly from the activity stream.

When a document has a preview, a part of it is displayed, if not a
thumbnail icon is displayed:

|image11|

When clicking to preview, here is what we got in the two cases:

|image12|

The following types are viewable i.e has a preview:

-  Printable files: *pdf*, *doc* (and other Office files) or any other
   type of files :ref:`JODConverter <#PLFAdminGuide.Configuration.JODConverter>`
   supports. See the full list of types at :ref:`JODConverter, Administrator
   Guide <#PLFAdminGuide.Configuration.JODConverter>`.

-  Images: *png, jpg, jpeg, gif*.

-  Audios/Videos: *mp3, mp4*.

-  ECMS content, either custom or built-in templates, such as a *web
   content* template.

For these viewable types, when you click a document preview thumbnail in
the Activity Stream or select the *View Document* menu from Documents in
the left navigation pane, the **Document Viewer** opens. The viewer
provides a large viewing area and some functions, such as Search,
Download and Print.

.. tip:: To exit the Viewer, hit *Esc* key or click **X** icon at the top right corner.


.. note::The Comment pane, where you can comment on or like a post, is only available when you view a document in the Activity Stream.
		 If the document is an unknown type, you must download it to your local machine and open it with another application.

.. _Office-PDF-files:

Office documents and pdf files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can always view pdf files, whereas Office documents require
:ref:`JODConverter <#PLFAdminGuide.Configuration.JODConverter>` to be
installed on the server. If you cannot view an MS Word file, for
example, contact your administrators.

For these file types, the Document Viewer provides maximized reading
estate and all the functions listed.

|image13|

-  **Page Navigator**

Although you can simply scroll to go to another page, the Page Navigator
provides many page selectors (e.g. previous, next, first and last page
links, page number selector). You can also show/hide the Page Thumbnail
pane by clicking the leftmost icon in the toolbar. Click it again to
close it.

|image14|

-  **Search**: Click the Search icon |image15| to open the Search bar and
   click it again to exit.

|image16|

-  **Download**: Click the Donwload icon |image17| to download the file.

-  **Full screen mode**: Click the *Switch to Presentation Mode* icon
   |image18| to read in full screen. Hit *Esc* key to exit this mode.

-  **Print**: Click the *Tools* icon |image19| then select *Print*.

-  **Comment**: You will see the Comment area on the right side when you
   open the viewer. If it is hidden, you can bring it back by clicking
   the rightmost arrow icon.

|image20|

-  **Like**: In the Comment area, click the *Like* icon |image21| to
   like the post. Click it again to unlike.

.. _Images-audio-videos:

Images, Audios and Videos
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For viewable media types, the available functions are Download, Comment
and Like.

|image22|


.. note::Audio/Video playback may require appropriate browser plugins. A
			message like "*Video format or MIME type is not supported*\ "
			indicates that you may need to install or enable some plugins for that media type.

.. _ECMS-content:

ECMS Content
~~~~~~~~~~~~~~

If the document is ECMS Content, it is viewable. The following
screenshot shows *illustrated web content*, which is one of the built-in
templates.

|image23|

.. _Open-in-office:

==============
Open in Office
==============

With the Open in Office feature, you are able to easily edit documents,
spreadsheets and presentations in the native applications installed on
your client, without keeping a local copy.

In fact, this feature already existed before, but since PRODUCT 4.2,
more operating systems and browsers will be supported. You will be able
to open not only Office formats, but also virtually any file format as
long as an application is associated with it in your client.

Depending on the file type, a new contextual action appears as below:

-  **Open in Word** for file types: ``.docx``, ``.doc``, ``.docm``,
   ``.dot``, ``.dotm``, ``.dotx``.

   |image24|

-  **Open in Excel** for file types: ``.xltx``, ``.xltm``, ``.xlt``,
   ``.xlsx``, ``.xlsm``, ``.xlsb``, ``.xls``, ``.xll``, ``.xlam``,
   ``.xla``.

   |image25|

-  **Open in Powerpoint** for file types: ``.pptx``, ``.pptm``,
   ``.ppt``, ``.ppsx``, ``.ppsm``, ``.pps``, ``.ppam``, ``.ppa``,
   ``.potx``, ``.potm``, ``.pot``.

   |image26|

-  **Open on Desktop** for Non-MS Office files that are different from
   Word, Excel or Powerpoint files.

   |image27|


.. note:: The labels used for these buttons can be set by an administrator.
		  See :ref:`how-to <#PLFAdminGuide.Configuration.OpenInOfficeConfiguration>` in Administrator Guide.

This feature can be used not only in the Activity Stream (like above),
but also in many places:

-  Admin and List views (directly on the Action bar):

   |image28|

-  Categories, Icons and Web views (on the right-click menu)

   |image29|

-  File Preview

   By default, in some views (including Admin, Icons and List view),
   these buttons will be displayed as an action on the Actions bar.
   These buttons can be configured in any views (Categories, Web) like
   any other actions by your administrator 
   (Administration --> Content -->Content Administration --> Explorer --> View--> |image30| --> Action tab --> |image31| --> Remote Edit checkbox).


.. note:: These buttons will not be displayed in case multiple files are selected.

**How to use?**

By clicking either of these buttons, you can open and edit that document
in one native application that is registered on your client. A new
version of the document will be automatically created when it is saved
within the Office application.

-  When one document is currently opened by one user, the Lock icon will
   appear next to that file: |image32|. If you still want to open this
   file, one message saying that you can open it in the Read-only format will appear.

   |image33|

-  In case there is no application registered for one file type, one
   message appears, saying that you have no application registered to
   open that file.


.. note:: To make this feature work well, you need to learn about :ref:`Compatibility <Compatibility>`
			as well as :ref:`Client requirements <ClientRequirements>`.

.. _Compatibility:

Compatibility
~~~~~~~~~~~~~~

.. _Basic-compatibility:

Basic compatibility
---------------------

eXo Platform core has a basic compatibility for Microsoft environments. So,
if you are using Windows (7, 8 or 10) with Microsoft Office 2016
installed, you can work with Word, Excel and Powerpoint files in many
browsers: IE11, Firefox, Google Chrome and Edge.

.. note::To make Open in Office work well on IE11, you need to enable ActiveX
			by selecting Internet OptionsSecurity tabCustom levelInitialize and
			script ActiveX controls not marked as safe for scripting, and
			ticking the **Enable (not secure)** checkbox.

.. _Enhanced-compatibility:

Enhanced compatibility
-----------------------

For editing more file types and in various platforms, it is required
your administrator install the Remote Edit add-on on eXo Platform server
(by the command: ``addon install exo-remote-edit``). With this
installation, you can start using Open in Office in more various
environments. Here are the client environments that are currently
supported in eXo Platform:

+--------------------+----------------------------+----------------------------+
| OS                 | Browsers                   | Office suites              |
+====================+============================+============================+
| Windows 7, Windows | IE11, Firefox, Chrome,     | Microsoft Office 2016      |
| 8, Windows 10      | Edge                       | (Recommended), Microsoft   |
|                    |                            | Office 2010 and 2013       |
|                    |                            | (Supported)                |
+--------------------+----------------------------+----------------------------+
| MAC OS 10.9+       | Firefox, Safari            | Microsoft Office for Mac   |
|                    |                            | 2016 (Recommended),        |
|                    |                            | Microsoft Office for Mac   |
|                    |                            | 2011 (Compatible)          |
+--------------------+----------------------------+----------------------------+
| Ubuntu 17.04       | Firefox                    | LibreOffice 5.4            |
|                    |                            | (Supported), OpenOffice    |
|                    |                            | 4.1 (Compatible)           |
+--------------------+----------------------------+----------------------------+


.. note::	-  It is recommended to use the latest versions of Firefox and Chrome.

			-  Google chrome browser is incompatible for Ubuntu OS.

			-  For Chrome in Windows and MAC OS, you need to enable NPAPI, as said `here <https://java.com/en/download/faq/chrome.xml#npapichrome>`__.

.. _ClientRequirements:

Client requirements
~~~~~~~~~~~~~~~~~~~~~~~~~

In client side, you need to pay attention to the following environment
requirements before using this feature.


.. note:: For all OSs/browsers, it is recommended you install and make sure
			Java Applet enabled. This is required for opening Non-MS Office
			files. You can visit http://javatester.org/ to make sure Java Plugin
			already installed on your browser.

.. _Windows:

Windows
---------

**Note 1. Allowing to open and edit MS Office file types.**

1. Configure WebDAV Redirector on the client.

-  On Windows 7, click **Start**, type *regedit* in the Start Search
   box, and then press Enter. If you are in Windows 8, hold the Windows
   key (WINKEY) + F, highlight **Apps** in the Menu bar, type *regedit*
   in the Search box, and press Enter.

-  Locate to the following:
   ``HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WebClient\Parameters``.

-  On the Edit menu, point to **New**, and then click **DWORD Value**.

-  Type *BasicAuthLevel*, and then press Enter.

-  Right-click *BasicAuthLevel*, and then click **Modify**.

-  In the Value data box, type *2*, and click OK.

2. Update the Registry on the client.

-  Locate to the following:
   ``HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Common\Internet``
   (for MS Office 2010) or
   ``HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Common\Internet``
   (for MS Office 2013).

-  On the Edit menu, create *BasicAuthLevel* with the same value as in
   `Configure WebDAV Redirector on the
   client <#ConfiguringWebDAVRedirector>`__.

3. Exit **Registry Editor**, and restart your client.

**Note 2. On Chrome browser**

If you install both Microsoft Office and OpenOffice, you need to choose
Microsoft Office as default application for office files.

**Note 3. For Non-MS Office files**

When you open/edit a Non-MS Office file, one NPE exception is thrown on
eXo Platform server and even when the file is opened successfully, the
client gets very slow. See `here <http://stackoverflow.com/questions/27416798/it-hit-webdav-open-non-office-files>`__
for understanding the problem.

.. _Linux:

Linux
-------

On Firefox, to open/edit one file, you need to install **davfs2** that
allows mounting a WebDav server as a disk drive:

   $ sudo apt-get install davfs2

To open a document using untrusted SSL, you should export your server
certification and then register and trust it on davfs2 by following
these steps:

1. To export the server certification, use this command:

   $ openssl s_client -connect ${REMHOST}:${REMPORT} | sed -ne '/-BEGIN CERTIFICATE-/,/-END CERTIFICATE-/p' > myserver.pem

2. Register the certification on davfs by copiying it to ``davfs2/certs/``:


   $ sudo cp myserver.pem /etc/davfs2/certs/

3. Trust the certication on davfs2 by editing the file ``/etc/davfs2/davfs2.conf`` and adding this content:


   $ trust_server_cert /etc/davfs2/certs/myserver.pem

.. _MAC:

MAC
----

-  Enable **BasicAuth None SSL** with the command:

   $ defaults -currentHost write com.microsoft.registrationDB hkey_current_user\\hkey_local_machine\\software\\microsoft\\office\\14.0\\common\\internet\\basicauthlevel -int 2

-  In case you cannot open Microsoft Office files, you should close or
   force closing Microsoft Office Application, then re-open it.

-  In MAC OS 10.9, to edit a text file, it is recommended you use
   TextWrangler (not default TextEditor) to edit it.

.. _Basic-actions:

==========================
Working with basic actions
==========================

eXo Platfoem features some ways for you to do actions on your content
flexibly, regardless of in which view you are using.

Before doing any actions on your content, it is recommended that you
clarify the following points:

-  In the **Icons** view, you can right-click the content that shows a
   drop-down menu.

   |image34|

-  In the **List** view, you cannot right-click the content. Instead,
   click anywhere under a specific area of the content (marked with the
   ticked checkbox). You will see a list of actions on the Action bar
   that are similar to those from the Right-click menu.

   |image35|


.. note:: Depending on the display width of your device, some actions (for
			example, Download And Allow Edition and Copy URL To Clipboard)
			may be grouped in the More drop-down menu.

-  The available actions shown in the Action bar when you double-click
   the content in the **Icons** view are quite similar to those when you
   click directly the content title in the **List** view. The difference
   is that the Overload Thumbnail function is only featured in the
   **Icons** view.

-  See the comparison table as below to have an overview of actions:

   +----------------------------------------------------------------------+-----------------------------+--------------------------------------+
   | **Actions**                                                          |       **Icons view**   		|           **List view**      		   |
   |                               										  |                             |                                      |
   |																	  |	Right click | double click	| Tick checkbox | Click title directly |		
   +======================================================================+=============+===============+===============+======================+
   | :ref:`Adding to favorites <AddingToFavorites>`                       |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Copying/Cutting & Pasting <CopyingCuttingPasting>`             |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Editing a document <EditingDocument>`                          |    |yes|    |     |yes|     |    |yes|      |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Deleting <DeletingContent>`                                    |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Locking/Unlocking <LockingUnlocking>`                          |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Renaming <Renaming>`                                           |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Creating a symlink <CreatingSymlink>`                          |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Viewing document information <ViewingDocumentInformation>`     |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Viewing a document <ViewingDocument>`                          |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Viewing WebDAV <ViewingWebDAV>`                                |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Copying URL to clipboard <CopyingURLToClipboard>`              |    |yes|    |     |no|      |    |yes|      |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Tagging a document <TaggingDocument>`                          |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Voting for a document <VotingDocument>`                        |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Viewing document metadata <ViewDocMetadata>`                   |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Managing permissions <ManagingPermissions>`                    |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Overloading a thumbnail <OverloadingThumbnail>`                |    |no|     |     |yes|     |    |no|       |        |no|          |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Watching/Unwatching a document <WatchingUnwatchingDocument>`   |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Versioning <ActivatingDocumentVersion>`                        |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+
   | :ref:`Commenting on a document <CommentingDocument>`                 |    |no|     |     |yes|     |    |no|       |        |yes|         |
   +----------------------------------------------------------------------+-------------+---------------+---------------+----------------------+






.. |image0| image:: images/ecms/icons_view_icon.png
.. |image1| image:: images/ecms/list_view_icon.png
.. |image2| image:: images/ecms/documents_interface.png
.. |image3| image:: images/ecms/admin_view.png
.. |image4| image:: images/ecms/icons_view.png
.. |image5| image:: images/ecms/list_view.png
.. |image6| image:: images/common/right_arrow_icon.png
.. |image7| image:: images/common/down_arrow_icon.png
.. |image8| image:: images/ecms/address_bar.png
.. |image9| image:: images/common/back_icon.png
.. |image10| image:: images/ecms/personal_documents_button.png
.. |image11| image:: images/ecms/preview_thumbnail.png
.. |image12| image:: images/ecms/preview_mode.png
.. |image13| image:: images/ecms/doc_viewer_demo_pdf.png
.. |image14| image:: images/ecms/doc_viewer_page_selectors.png
.. |image15| image:: images/common/search_icon.png
.. |image16| image:: images/ecms/doc_viewer_search.png
.. |image17| image:: images/ecms/doc_viewer_download_icon.png
.. |image18| image:: images/ecms/doc_viewer_full_screen_icon.png
.. |image19| image:: images/ecms/doc_viewer_tools_icon.png
.. |image20| image:: images/ecms/doc_viewer_comment_area.png
.. |image21| image:: images/common/like_icon.png
.. |image22| image:: images/ecms/doc_viewer_demo_img.png
.. |image23| image:: images/ecms/doc_viewer_demo_ecms_content.png
.. |image24| image:: images/ecms/OpenInOffice/openinword.png
.. |image25| image:: images/ecms/OpenInOffice/openinexcel.png
.. |image26| image:: images/ecms/OpenInOffice/openinpowerpoint.png
.. |image27| image:: images/ecms/OpenInOffice/openondesktop.png
.. |image28| image:: images/ecms/OpenInOffice/admin_view_openinoffice.png
.. |image29| image:: images/ecms/OpenInOffice/icon_view_openinoffice.png
.. |image30| image:: images/ecms/edit_portlet_icon.png
.. |image31| image:: images/ecms/edit_portlet_icon.png
.. |image32| image:: images/ecms/OpenInOffice/lock_file.png
.. |image33| image:: images/ecms/OpenInOffice/open_read_only.png
.. |image34| image:: images/ecms/right_click_actions.png
.. |image35| image:: images/ecms/checkbox_actions.png
.. |yes| image:: images/common/yes.png
.. |no| image:: images/common/no.png
