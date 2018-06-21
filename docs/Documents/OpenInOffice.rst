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

