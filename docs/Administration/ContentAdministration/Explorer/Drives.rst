.. _WorkingWithExplorer.Drives:

Drives
-------

Drive is a shortcut to a specific location in the content repository
that enables administrators to limit visibility of each workspace for
groups of users. It is also a simple way to hide the complexity of the
content storage by showing only the structure that is helpful for
business users.

Currently, eXo Platform presets 6 drive types. However, the number of drives
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

|image39|

Here, you can do certain actions on the drives as follows:

- :ref:`Editing a drive <Drives.EditingDrive>`
   |image40|

- :ref:`Deleting a drive <Drives.DeletingDrive>`
   |image41|

- :ref:`Adding a new drive <Drives.AddingNewDrive>`
   |image42|

.. _Drives.EditingDrive:

Editing a drive
``````````````````


1. Click |image43| corresponding to your desired drive in the Action column.

The Edit Drive form appears.

|image44|

2. Edit the properties as required.

3. Click Save to commit your changes.


.. note:: The drive name cannot be edited in this form.

.. _Drives.DeletingDrive:

Deleting a drive
`````````````````

Simply click |image45| that corresponds to the drive you want to delete,
then select **OK** in the confirmation message.

.. _Drives.AddingNewDrive:

Adding a new drive
```````````````````

1. Click Add Drive at the bottom to open the Add Drive form.

|image46|

2. Input a name for the new drive in the Name field that is required.

3. Select a workspace for the drive from the drop-down menu by clicking 
   the Workspace entry.

|image47|

4. Select the home path for the drive by clicking |image48|.

5. Browse an icon for the workspace by clicking |image49|.

6. Select permissions for groups that have access rights to this drive 
   by clicking |image50|.

.. note:: Setting the \* membership for a group will allow all users of the group to access this drive (via DocumentsShow Drives), regardless of their membership role.

7. Select or deselect the various checkboxes to hide or show the drive
   elements respectively.

|image51|

8. Select the document type that will be created in this drive.

9. Limit the node types shown in the left tree by clicking |image52| 
   next to the Allowance nodetype on left tree field.

-  If you do not select the value for this field, this means all node
   types are shown in the left tree. The "empty" value is converted into
   **\*** once you have clicked Save.

-  If you define specific node types in this field, only these node
   types are shown in the left tree.

10. Select the Apply Views tab and select the view types you want to be
    available in the drive.

|image53|

11. Click Save to complete creating the new drive, or Refresh to clear 
    the form.


