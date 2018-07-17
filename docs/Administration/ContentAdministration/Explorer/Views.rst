Views
------

eXo Platform provides various drives for you to store and manage your content
efficiently. Each drive has some views that enable you to view data in
the drive in a particular way. Each view has some action tabs and each
action tab contains some functions.

eXo Platform supports you some ways to view nodes in a specific folder and
show actions of corresponding tab on the Action bar.

The number of view types depends on which drive you are browsing. In
Explorer, select Views to open the Views panel.

|image54|

.. _ViewsIneXo:

Views in eXo Platform
``````````````````````

All eXo Platform views are in the Views tab. Here, you can view, edit,
delete, and add new views.

**Admin**

|image55|

**Icons**

|image56|

**List**

|image57|

**Categories**

|image58|

**Web**

|image59|

To learn about differences between these views, see the following table:

+------------+--------------------------------+------------+----------------------+
| View names | Default actions                | Default    | Default permissions  |
|            |                                | templates  |                      |
+============+================================+============+======================+
| **Admin**  | Add Folder, Edit Document,     | List       | ``*:/platform/admini |
|            | View Permissions, Manage       |            | strators``           |
|            | Actions, Manage Auditing,      |            |                      |
|            | Manage Relations, Show JCR     |            |                      |
|            | Structure, Upload, View        |            |                      |
|            | Metadata, View Properties      |            |                      |
+------------+--------------------------------+------------+----------------------+
| **Icons**  | Add Folder, Edit Document,     | Thumbnails | ``*:/platform/users` |
|            | Manage Versions, Tag Document, |            | `                    |
|            | Upload, View Metadata, View    |            |                      |
|            | Permissions, Vote, Comment,    |            |                      |
|            | Watch Document, Overload       |            |                      |
|            | Thumbnail                      |            |                      |
+------------+--------------------------------+------------+----------------------+
| **List**   | Add Folder, Edit Document,     | List       | ``*:/platform/users` |
|            | Manage Versions, View          |            | `                    |
|            | Permissions, Tag Document,     |            |                      |
|            | Upload, View Metadata, Vote,   |            |                      |
|            | Comment, Watch Document        |            |                      |
+------------+--------------------------------+------------+----------------------+
| **Categori | Add Category, Add Document,    | Content    | ``*:/platform/web-co |
| es**       | Edit Document, View            |            | ntributors``         |
|            | Permissions, Manage            |            |                      |
|            | Categories, Manage             |            |                      |
|            | Publication, Approve Content,  |            |                      |
|            | Publish, Request Approval,     |            |                      |
|            | Upload, Tag Document, Vote,    |            |                      |
|            | Comment, Watch Document        |            |                      |
+------------+--------------------------------+------------+----------------------+
| **Web**    | Add Category, Add Document,    | Content    | ``*:/platform/web-co |
|            | Add Folder, Edit Document,     |            | ntributors``         |
|            | Manage Categories, Manage      |            |                      |
|            | Publication, Approve Content,  |            |                      |
|            | Publish, Request Approval,     |            |                      |
|            | Upload, View Permissions Tag   |            |                      |
|            | Document, Vote, Comment, Watch |            |                      |
|            | Document, Add Translation      |            |                      |
+------------+--------------------------------+------------+----------------------+

Viewing/Editing/Deleting a view
````````````````````````````````

**Viewing**

Simply click |image60| corresponding to your desired view in the Action
column.

The View form will open.

|image61|

**Editing a view**

1. Click |image62| in the Action column.

The Edit View form appears.

|image63|

2. Edit the view properties.

-  You cannot change the view name.

-  If you select the Enable Version checkbox, this view automatically
   increases to one version after you have clicked Save. It is displayed
   at the Base Version column in the Views tab. Moreover, the View tab
   in the Edit View form will have the Restore Version field which
   allows rolling back a given version.

   |image64|

.. _HidingExplorerPanelInSidebar:

-  By default, the Hide explorer panel in side bar checkbox is only
   selected for the **Admin** and **List** views. This means you can use
   the Explorer tree to browse content from the side bar in the
   **Icons**, **Categories**, and **Web** views by default. However, in
   the **Admin** and **List** views, you need to deselect these
   checkboxes first.

3. Optionally, select the Action tab to do the following actions on the
   tab.

-  i. Click |image65| to edit one existing tab. You can add or remove
   functions on the selected tab by selecting/deselecting the
   corresponding checkboxes. Note that you cannot change the tab name.

-  ii. Click |image66| to delete an existing tab.

-  iii. Click Add to add a new tab to the view.

4. Optionally, select the Permission tab to delete the existing 
   permissions or to add new permissions.

.. note:: Setting the \* membership for a group will allow all users of the group to use this view when :ref:`exploring documents <DocumentsInterface>`.

5. Click Save to apply all changes in the View tab.

**Adding/deleting an action in a view**

In the previous part :ref:`Views in eXo Platform <ViewsIneXo>`, we 
described different views in eXo Platform with their defaut actions.

It is possible to edit the action bar of a view by following these
steps:

1. Log in to eXo Platform as an administrator.

2. Go to Administration Content Content Administration.

|image67|

3. In **Manage ECM Main Functions** panel click on **Explorer** tab and 
   then click on Views item.

|image68|

4. In the right panel, click on edit button |image69| of the view you 
   want to change, List view for example.

5. In the **Edit form**, select **Action** tab then click on |image70|.

|image71|

6. A new popup appears, you can check to add or uncheck to delete 
   actions on the view.

|image72|

7. Click Save to apply actions check/uncheck then save in the 
   **Edit View** form.

**Deleting a view**

Click |image73| corresponding to the view you want to delete, then click
**OK** in the confirmation message.

.. note:: You cannot delete a view which is in use.

Adding a view
```````````````

1. Click Add View located at the bottom to open the Add View form.

|image74|

2. Specify the view name in the Name field that must be unique, and only
   contains standard alphanumeric characters. This field is required.

3. Select one template from the Template drop-down menu.

.. note:: Tick the Enable Version checkbox if you want to activate versioning for your view.

4. Select the Action tab, then click Add to create a functional tab on 
   this view. This step is required.

The Add/Edit Tab form appears.

|image75|

-  **i.** Enter the name for the tab in the Tab Name field.

-  **ii.** Tick checkboxes corresponding to the actions you want to add
   to the tab.

-  **iii.** Click Save to finish creating a tab.

   The newly created tab is displayed in the Tab column.

   |image76|

5. Select the Permission tab, then click Add to add permissions for the
   view. It is required.

6. Click Save to finish adding your view.

Explorer templates in eXo Platform
````````````````````````````````````

In the Views form, click the Explorer Templates tab to see a list of
Explorer templates. Currently, there are 3 Explorer templates which can
be used for views in eXo Platform, including: Content, List and 
Thumbnails.

|image77|

Here, you can edit information, delete or add a new Explorer template.

Editing/Deleting an Explorer template
```````````````````````````````````````

**Editing an Explorer template**

1. Click |image78| next to the template you want to edit.

2. Change the current template's properties.

.. note:: -  You cannot edit the template name.
		  -  If you tick the Enabled Version checkbox, this template will automatically increase to one version after you have clicked Save. Then, the Edit Explorer Template form has more the Select Version field.
		  -  If the template has at least two versions, the Edit Explorer Template form displays Restore at the form bottom that allows restoring to a selected version.

3. Click Save to accept all changes.

**Deleting an Explorer template**

Click |image79| corresponding to the template you want to delete, then
select **OK** in the confirmation message.

Adding an Explorer template
```````````````````````````````

1. Click Add to open the Add Explorer Template form.

|image80|

2. Input content of the template in the Content field.

3. Input a name for the template in the Name field.

4. Select a type for the template in the Template Type field.

5. Click Save to accept adding this new template.




