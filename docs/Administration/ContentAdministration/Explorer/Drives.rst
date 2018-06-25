.. _Drives:

Drives
======

Drive is a shortcut to a specific location in the content repository
that enables administrators to limit visibility of each workspace for
groups of users. It is also a simple way to hide the complexity of the
content storage by showing only the structure that is helpful for
business users.

Currently, PRODUCT presets 6 drive types. However, the number of drives
you can access depend on your user role. Also, these drives use the
various views. See the following table to make distinction between
drives:

+------------------+--------------+---------------------------+------------------+
| Drives           | Workspace    | Permissions               | Views            |
+==================+==============+===========================+==================+
| **Personal       | collaboratio | ``*:/platform/users``     | List, Icons,     |
| Documents**      | n            |                           | Admin            |
+------------------+--------------+---------------------------+------------------+
| **Collaboration* | collaboratio | ``*:/platform/administrat | Wed, Admin       |
| *                | n            | ors, *:/platform/web-cont |                  |
|                  |              | ributors``                |                  |
+------------------+--------------+---------------------------+------------------+
| **Groups**       | collaboratio | ``*:${groupId}``          | List, Icons      |
|                  | n            |                           |                  |
+------------------+--------------+---------------------------+------------------+
| **Managed        | collaboratio | ``*:/platform/administrat | Web              |
| Sites**          | n            | ors, *:/platform/web-cont |                  |
|                  |              | ributors``                |                  |
+------------------+--------------+---------------------------+------------------+
| **Powers**       | collaboratio | ``* :/platform/web-contri | Categories       |
|                  | n            | butors``                  |                  |
+------------------+--------------+---------------------------+------------------+
| **Trash**        | collaboratio | ``*:/platform/administrat | Admin            |
|                  | n            | ors``                     |                  |
+------------------+--------------+---------------------------+------------------+

In Explorer, select Drives.

|image0|

Here, you can do certain actions on the drives as follows:

-  `Editing a
   drive <#PLFUserGuide.AdministeringeXoPlatform.ContentAdministration.WorkingWithExplorer.Drives.EditingDrive>`__
   |image1|

-  `Deleting a
   drive <#PLFUserGuide.AdministeringeXoPlatform.ContentAdministration.WorkingWithExplorer.Drives.DeletingDrive>`__
   |image2|

-  `Adding a new
   drive <#PLFUserGuide.AdministeringeXoPlatform.ContentAdministration.WorkingWithExplorer.Drives.AddingNewDrive>`__
   |image3|

Editing/Deleting a drive
------------------------

**Editing a drive**

Click |image4| corresponding to your desired drive in the Action column.

The Edit Drive form appears.

|image5|

Edit the properties as required.

Click Save to commit your changes.


.. note:: The drive name cannot be edited in this form.

**Deleting a drive**

Simply click |image6| that corresponds to the drive you want to delete,
then select **OK** in the confirmation message.

Adding a new drive
------------------

Click Add Drive at the bottom to open the Add Drive form.

|image7|

Input a name for the new drive in the Name field that is required.

Select a workspace for the drive from the drop-down menu by clicking the
Workspace entry.

|image8|

Select the home path for the drive by clicking |image9|.

Browse an icon for the workspace by clicking |image10|.

Select permissions for groups that have access rights to this drive by
clicking |image11|.

    **Note**

    Setting the \* membership for a group will allow all users of the
    group to access this drive (via DocumentsShow Drives), regardless of
    their membership role.

Select or deselect the various checkboxes to hide or show the drive
elements respectively.

Show Referenced Document
    Allows viewing referenced documents.

Show Non-document Nodes
    Allows viewing non-documents.

Show Sidebar
    Allows showing the sidebar.

Show Hidden Nodes
    Allows showing the hidden nodes.

Select the document type that will be created in this drive.

Limit the node types shown in the left tree by clicking |image12| next
to the Allowance nodetype on left tree field.

-  If you do not select the value for this field, this means all node
   types are shown in the left tree. The "empty" value is converted into
   **\*** once you have clicked Save.

-  If you define specific node types in this field, only these node
   types are shown in the left tree.

Select the Apply Views tab and select the view types you want to be
available in the drive.

|image13|

Click Save to complete creating the new drive, or Refresh to clear the
form.

.. |image0| image:: images/ecms/drives_management.png
.. |image1| image:: images/common/1.png
.. |image2| image:: images/common/2.png
.. |image3| image:: images/common/3.png
.. |image4| image:: images/common/edit_icon.png
.. |image5| image:: images/ecms/edit_drive_form.png
.. |image6| image:: images/common/delete_icon.png
.. |image7| image:: images/ecms/add_drive_form.png
.. |image8| image:: images/ecms/workspaces.png
.. |image9| image:: images/common/plus_icon.png
.. |image10| image:: images/common/plus_icon.png
.. |image11| image:: images/common/plus_icon.png
.. |image12| image:: images/common/plus_icon.png
.. |image13| image:: images/ecms/apply_views_tab.png
