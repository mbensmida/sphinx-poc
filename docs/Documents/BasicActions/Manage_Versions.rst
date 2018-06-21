.. _ActivatingDocumentVersion:

Versioning
==========

A versioned document is one which can be recovered at any given time.
You need to clarify the following points:

-  Once "Version" is activated for a document, this is called a
   "versioned" document.

-  The saved state of a document is called "version".

-  Versions created for a document behave as parts of the versions
   history.

-  The version on which you are currently working is called the "base"
   version.

Versioning is an optional feature, so you need to activate this for
either an independent file or a whole folder.

    **Note**

    This feature only applies to documents, not to web contents.
    Besides, if you wish to enable versioning for a drive so that its
    new documents will be automatically versioned, you need to contact
    the administrator. See `Document versioning
    configuration <#PLFAdminGuide.Configuration.DocumentVersioning>`__
    for more details.

**Enabling versioning for a file**

Open the document you want to enable versioning.

Click |image0| on the Action bar.

The following message will appear.

|image1|

Click Activate to enable versioning for the document.

**Enabling versioning for a folder**

You can enable versioning for an entire folder instead of doing it on
every child document of the folder.

For example, here are steps to enable versioning of the folder
``collaboration:/sites/test``.

In Sites Explorer, open the drive *Collaboration*, then select the
folder.

Switch to *Admin* view, and click Actions on the Action bar.

Select the Add Action tab. On the dialog that appears, input:

-  Create Action of Type: *exo:autoVersioning*.

-  Name: *Auto Versioning*.

-  Lifecycle: *Content Addition*.

-  Is Deep: *checked*.

|image2|

Click the Search icon in the row **Affected Node Types**. Then check
*Select All Document Types*, and click Save.

Click Save, then Close to finish.

Whenever you update a document in the folder, a version will be created.

Adding a version to document
----------------------------

Versioning files is done automatically whenever a user overwrites a
file. There are many ways in which PRODUCT will help you to create a new
document version.

**Via Documents application**

In the **Documents** application, there are two ways to create a version
for a document. You can go to the folder that you want to create a new
document version and try one of the following ways.

**The first way**

Upload a file (or multiple files) to this folder by using the **Upload**
button on the Action bar or dragging/dropping this file directly from
your computer.

-  If this is a totally new document and the versioning is enabled for
   the folder or the drive that contains this folder, the first version
   will be created as below:

   |image3|

   If the versioning is not enabled, no version is created.

-  If there is an existing versioned document with the same name as the
   uploaded file, a popup with the following suggestions is shown:

   |image4|

   In which:

   -  **Keep both**: no version of the existing document is created, but
      a new document is created with the same name (as a sibling
      document).

   -  **Upload new version**: a new version of the file is created with
      other information, such as title or description of the old
      document kept on the new version.

   -  **Cancel**: the upload is cancelled.

**The second way**

Copy and paste a document (or multiple documents) to a folder which
contains a document with the same name.

-  If the document is versioned, there will be a confirmation popup like
   this:

   |image5|

   In which, the options **Keep Both, Save as new version** and
   **Cancel** are exactly the same as the **Keep Both, Upload a new
   version** and **Cancel** options respectively in `the first
   way <#PLFUserGuide.ManagingYourDocuments.WorkingWithBasicActions.ActivatingVersion.AddingVersion.ViaDocumentApp.Upload.Versioned>`__.
   Besides, if you upload multiple files, ticking the checkbox
   "*Remember my choice for all others versioned documents*\ " will
   apply the selected option for the remaining versioned files.

-  If the document is not versioned, the options will be the same as
   `those <#PLFUserGuide.ManagingYourDocuments.WorkingWithBasicActions.ActivatingVersion.AddingVersion.ViaDocumentApp.Upload.NonVersionned>`__
   in the first way:

   |image6|

   Ticking the checkbox "*Remember my choice for all other versioned
   documents*\ " will apply the selected option for the remaining not
   versioned files.

**Via File Upload**

There is also an another case in which you probably need to create a
document version.

Click |image7| in CKEditor of web content or illustrated web content
file template.

Upload a file to a folder that contains a document with the same name:

-  If the document is versioned, there will be an alert like this:

   |image8|

   In which, the options **Keep Both, Create a new version** and
   **Cancel** are exactly the same as the **Keep Both, Upload new
   version** and **Cancel** options respectively in `this
   case <#PLFUserGuide.ManagingYourDocuments.WorkingWithBasicActions.ActivatingVersion.AddingVersion.ViaDocumentApp.Upload.Versioned>`__.

-  If the document is not versioned, the options will be the same.

       **Note**

       If none of these actions is chosen, the new version of the
       document is not used and the upload is cancelled.

**Via the Action bar**

**The first way**

Open a versioned document that you want to create a new version in the
Preview Mode.

Click the **Upload a new version** button on the Action bar.

Select a file to upload. Notice that the uploaded file does not need to
have the same name as the versioned document, but it should be the same
file type.

Once the file is selected, a new version with the same name as the
current document is automatically created. One success message will be
displayed.

**The second way**

Right-click the versioned document that you want to create a new
version.

Select the **Create a new version** button from the popup menu.

This will automatically create a new version of the document based on
the current version so that you can change the document properties on
this version while its content is still kept.

**Via WebDAV**

It is pretty simple to create a version for a document via WebDAV. You
just need to access WebDAV and upload a file to a folder. Several cases
will happen as below:

-  If this is a totally new document and versioning is enabled for the
   folder or the drive that contains the folder, its first version is
   created.

-  If there is an existing not versioned document with the same name,
   the new document will replace the existing one.

-  If there is an existing versioned document with the same name, a new
   version will be created.

Managing versions
-----------------

You can manage your versions by comparing with the current version,
adding/removing labels, viewing/deleting versions or restoring to a
specific version. All such management actions will be done in the
Version History window.

|image9|

**Comparing two versions**

|image10|

Check two versions among the versions list of the document/content.

Click on Compare selected versions buttons.

A page appears to highlight changes done between the two selected
versions. If the update contains an addition, it is highlighted in
green. If the update contains a deletion, it is highlighted in red.

|image11|

**Adding a summary**

You can give a summary to each document version. For that purpose,
simply double click on the label Click here to add a summary, fill in
the text field then save by clicking on |image12|

You can abondon the summary addition by clicking on |image13|.

**Restoring a version**

Define the version that you want to restore as the base version by
checking it among the version list.

Click |image14| from the column **Action** that is in the version's line
to make the selected version become the base one.

**Viewing a version**

Simply click |image15| to view the document at the selected version.

**Deleting a version**

Click |image16| corresponding to the version you want to delete.

Click **OK** in the confirmation message to accept your deletion.

    **Note**

    You cannot delete the base version.

.. |image0| image:: images/ecms/versions_button.png
.. |image1| image:: images/ecms/versioning/activate_version_message.png
.. |image2| image:: images/ecms/versioning/auto_versioning.png
.. |image3| image:: images/ecms/versioning/first_version.png
.. |image4| image:: images/ecms/versioning/upload_versioned_file.png
.. |image5| image:: images/ecms/versioning/paste_versioned_file.png
.. |image6| image:: images/ecms/versioning/paste_nonversioned_file.png
.. |image7| image:: images/ecms/insert_content.png
.. |image8| image:: images/ecms/versioning/file_upload_versioned_ck.png
.. |image9| image:: images/ecms/versioning/manage_versions.png
.. |image10| image:: images/ecms/versioning/compare_versions.png
.. |image11| image:: images/ecms/versioning/comparison.png
.. |image12| image:: images/ecms/versioning/save_summary_icon.png
.. |image13| image:: images/ecms/versioning/close_icon.png
.. |image14| image:: images/common/restore_icon.png
.. |image15| image:: images/common/view_icon.png
.. |image16| image:: images/common/delete_icon.png
