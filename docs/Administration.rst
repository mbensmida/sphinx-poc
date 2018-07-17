.. _Administration:


############################
Administering eXo Platform
############################

    This chapter is for administrators only who have the highest right
    to administer eXo Platform via the following topics:

    -  :ref:`Branding eXo Platform <BrandingeXoPlatform>`
       Instructions on how to change your company logo and the color of
       the top navigation bar in the portal.

    -  :ref:`Notification administration <NotificationAdministration>`
       Instructions on how to enable/disable notification plugins.

    -  :ref:`Customizing the look and feel of eXo Platform <CustomizingLookAndFeel>`
       Instructions on how to create and apply a global stylesheet into
       a site.

    -  :ref:`Editing eXo Platform <Editing>`
       Instructions on how to edit certain aspects of eXo Platform, including
       website content, pages and sites.

    -  :ref:`Content Administration <ContentAdministration>`
       The way to access the Content Administration page where you can
       manage workspaces, drives, node types, metadata, templates, and
       queries.

    -  :ref:`WebDAV <WebDAV>`
       Definition of WebDAV and its advantages, how to access a
       workspace using various WebDAV clients (on a web browser or in an
       OS window), and WebDAV restrictions.

    -  :ref:`Managing your organization <ManagingYourOrganization>`
       Instructions on how to manage users, groups and memberships in
       eXo Platform.

    -  :ref:`Managing sites <ManagingSites>`
       In-depth instructions on how to create, edit and delete sites.

    -  :ref:`Managing pages <ManagingPages>`
       Steps to add/delete a new page, and edit its properties and
       layout.

    -  :ref:`Managing permissions <ManagingPermissions>`
       Introduction to permission levels in eXo Platform, and how to set
       permissions at various levels.

    -  :ref:`Managing navigations <ManagingNavigations>`
       Introduction to navigation levels eXo Platform, and in-depth
       instructions on how to perform various actions on navigation
       nodes.

    -  :ref:`Managing applications <ManagingApplications>`
       How to manage categories, portlets and gadgets, and introduction
       to management and monitoring gadgets in eXo Platform.

    -  :ref:`Building an online community <BuildingOnlineCommunity>`
       How to enable users to register themselves, publish some
       resources for anonymous access

.. _BrandingeXoPlatform:

======================
Branding eXo Platform
======================

eXo Platform allows you to easily brand eXo Platform by changing your company logo
and the color of the top navigation bar in the portal.

1. Click |image0| --> Portal --> Branding on the top navigation bar.

The Branding page will be displayed:

|image1|

**Details**:

-  The Select Logo pane: Uploads your company logo that must be in the
   ``.png`` format.

-  The Select Navigation Bar Style pane: Selects the navigation bar
   style suitable to your logo. There are two styles available on the
   portal, consisting of Dark which is default, and Light.

-  The Preview pane: Displays the preview of the top navigation bar with
   the currently defined logo and navigation bar style.

2. Click Upload to browse and upload the logo from your local device;

Or, drag the logo from your local device and drag it into the current
logo preview in the Select Logo pane. This way is just done if your
browser supports the HTML 5 and the Drag and Drop function.

|image2|

3. Click the box in the Select Navigation Bar Style pane and select one
   style from the drop-down.

Your style selection will also make the color of fonts on the top
navigation bar change.

.. tip:: If your logo is light and colorful, you should select the Dark style. If it is darker, you should select the Light style.

4. Click Save to accept your changes.

.. _NotificationAdministration:

===========================
Notification administration
===========================

eXo Platform allows administrators to enable/disable notification 
plugins in the administrative interface.

To do so, simply select |image3| --> Portal --> Notifications on the top
administration bar.

The Activity Notification Administration page will be displayed as
below:

|image4|

-  Notification types: Enables or disables notification types globally.

   -  Notification: Name and categories of the notifications.

   -  Title: Title of the notification that will be shown in the email.

   -  Enable: Enables or disables sending the email notifications for
      each corresponding notification type.

-  Name: Defines the display name of the email sender in the **From**
   field.

-  Address: Defines the email address of the sender in the **From**
   field. It must be in the correct form, such as username@abc.com.

.. note::	 -  Once a notification type is disabled, it will disappear from the Notification Settings page of all users, and no new notification of this type is sent anymore.
			 -  The **My Tasks** settings are available only if the :ref:`Task Management <ManageTasks>` add-on is  installed.

.. _CustomizingLookAndFeel:

==============================================
Customizing the look and feel of eXo Platform
==============================================

As a web-contributor or an administrator, you can easily customize the
look and feel of eXo Platform by editing the existing
``Globalstylesheet.css`` file or creating a new global stylesheet and
applying it into the portal.

Global stylesheet is a shared one which is applied into your entire
site. Global stylesheets of eXo Platform are put into the css folder to
manage the stylesheet of your desired site. This section aims at showing
you how to create and apply your own global stylesheet through **Sites
Explorer**.

This section covers the following topics:

-  :ref:`Creating a global stylesheet <CreatingGlobalStylesheet>`
   Detailed instructions on how to create, edit and rename a global
   stylesheet.

-  :ref:`Checking the display <CheckingDisplayOfGlobalStylesheet>`
   Steps to activate a global stylesheet and check its display.

.. _CreatingGlobalStylesheet:

Creating a global stylesheet
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Click |image5| Content Sites Explorer on the top navigation bar.

2. Select the Sites Management drive in the drives list.

3. Select a site in the Sites Management panel, for example, ``agital``, 
   then select the css folder.

4. Click |image6| to open the CSS File form which allows creating a new
   global stylesheet.

|image7|

5. Enter the name of global stylesheet into the Name field, for example,
   ``GlobalStylesheet\_Orange``.

6. Set the value as "True" in the Active field to activate your global
   stylesheet for your site. "True" is set by default when a new global
   stylesheet is created. If you select "False", your newly created 
   global style will be disabled.

7. Input one positive integer into the Priority field, for example "10".

8. Define your styles in the ``CSS Data`` field. Here, you can directly
   enter your CSS rules, or copy and paste them from your favorite text
   editor.

   For example, you can define your styles with the following 
   information:

|image8|

Click Save or Save & Close to save your newly created global stylesheet.
You will see your global stylesheet in the Sites Management panel.

|image9|

.. note:: -  The values in both of the Active and Priority fields decide if your newly created global stylesheet is applied into your site 
             successfully or not. If the Active field is set to "True" in many global stylesheets, the system will automatically merge all 
             the global stylesheets into the ``${site-name}/Default/Stylesheet-min-lt.css`` file of the css folder in the ascending order 
             and get the stylesheet with the highest priority. Thus, after selecting "True", to make sure that your stylesheet is applied, 
             you need to pay attention to the priority level so that the selected priority of your stylesheet is higher than those of other 
             global stylesheets in the css folder.

		  -  The default global stylesheet will be automatically created in the css folder when you create a new site. However, this global
             stylesheet can be overwritten by either setting "False" for its Active field or setting the higher priority for other global
             stylesheet than that of the default global stylesheet.

		  -  When you want to create a common stylesheet to share for all sites in the portal, you should create one in the 
		     Sites Management/shared/css folder. This stylesheet will be rendered and applied into your desired site when you switch to it.

.. _EditGlobalStylesheet:

Editing a global stylesheet
----------------------------

Simply select your desired global stylesheet and click Edit on the
action bar, or right-click the file and select Edit from the drop-down
menu to open the CSS File form.

.. _RenameGlobalStylesheet:

Renaming a global stylesheet
-------------------------------

Simply right-click your desired global stylesheet in the Sites
Management panel, then select Rename.

.. _CheckingDisplayOfGlobalStylesheet:

Checking the display
~~~~~~~~~~~~~~~~~~~~~

You can have several global stylesheets in one site. To see differences
when applying various global stylesheets, for example,
``GlobalStylesheet_Blue`` and ``GlobalStylesheet_Orange``, do as
follows:

1. Activate the ``GlobalStylesheet_Blue`` and ``GlobalStylesheet_Orange``
   files by turns.

2. Open your desired site by entering its URL in the address bar, for
   example, opening the intranet site: ``http://{domain-name}/portal/intranet``.

.. note:: The two GlobalStylesheet\_Blue and GlobalStylesheet\_Orange should been added to ``/intranet/css`` folder.


-  If you activate ``GlobalStylesheet_Blue``, your site is as below:

   |image10|

-  If you activate ``GlobalStylesheet_Orange``, your site is as below:

   |image11|

.. _Editing:

=====================
Editing eXo Platform
=====================

If you belong to members of editor or administrator groups, you will see
|image12| on the top navigation bar. By clicking this button, you will
see a drop-down menu that allows you to edit content, pages and site
quickly.

|image13|

.. _EditWebsiteContent:

Editing a website's content
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. note:: You can do this function only when the ACME add-on is already installed by your administrator. See :ref:`here <#PLFAdminGuide.AddonsManagement.Installing>` for how-to.

Simply click Content from the drop-down menu. The Edit mode will be
turned on. For more details, see :ref:`Edit mode <EditMode>`.

.. _EditingPage:

Editing a page
~~~~~~~~~~~~~~~

Hover your cursor over Page, then click:

-  Edit Layout if you want to edit the page's layout as stated in
   :ref:`Arranging the page layout <RearrangingPageLayout>`.

-  SEO if you want to manage SEO. See :ref:`Managing SEO <ManagingSEO>`
   for details.

-  Add Page if you want to add a new page. See :ref:`Using Page Creation Wizard <PageCreationWizard>`
   for details.

.. _EditingSite:

Editing a site
~~~~~~~~~~~~~~

Hover your cursor over Site, then click:

-  Layout to edit the site's layout. See :ref:`Editing layout <EditingLayout>`
   for details.

-  Click Navigation to manage navigation. See :ref:`Managing navigations <ManagingNavigations>`
   for details.

-  Click Add Site to add a new site. See :ref:`Creating a new site <CreatingNewSite>`
   for details.

.. _ContentAdministration:

======================
Content Administration
======================

This section covers the following topics:

-  :ref:`Working with Templates <WorkingWithTemplates>`
   Instructions on how to view, edit and delete the predefined templates
   or add a new template.

-  :ref:`Working with Explorer <WorkingWithExplorer>`
   Instructions on how to manage drives, views, and tags.

-  :ref:`Working with Repository <WorkingWithRepository>`
   Instructions on how to manage namespaces, node types and locks.

-  :ref:`Working with Advanced configuration <WorkingWithAdvancedConfiguration>`
   Instructions on how to manage with categories, queries, scripts, and
   actions.

Only administrators and web contributors can access the Content
Administration page to manage all workspaces, drives, node types,
metadata, templates, queries, and more.

To access the **Content Administration** page, click |image14| on the 
top navigation bar, then select ContentContent Administration from the
drop-down menu.

The Content Administration page will appear.

|image15|

From this page, you can access:

-  **Templates** |image16|: Manage templates of documents, CLV and
   metadata.

-  **Explorer** |image17|: Manage views, drives and tags.

-  **Repository** |image18|: Manage namespaces, node types and locks.

-  **Advanced** |image19|: Manage categories, queries, scripts and
   actions.

.. _WorkingWithTemplates:

Working with Templates
~~~~~~~~~~~~~~~~~~~~~~~

When creating content in eXo Platform, you must set its properties. 
Thus, each content needs to have a form to enter data for its properties
(called the **Dialog** template), and display the existing values
(called the **View** template). In the templates management, you are
able to view, edit and delete the predefined templates or to add a new
template.

From the Manage ECM Main Functions panel, select Templates.

|image20|

eXo Platform provides 3 available template types, including:

- :ref:`Documents <WorkingWithTemplates.DocumentTemplates>`: Manages 
  view, dialog and CSS templates of document types.

- :ref:`List <WorkingWithTemplates.ListTemplates>`: Manages Content List
   Viewer templates.

- :ref:`Metadata <WorkingWithTemplates.MetadataTemplates>`: Manages view
   and dialog templates of metadata node types.

.. _WorkingWithTemplates.DocumentTemplates:

Document templates
-------------------

In Templates, select Documents to open the Documents panel.

|image21|

The Documents templates are categorized into 3 sub-tabs that makes ease
for management. You can use default templates provided by PRODUCT in
each sub-type or define a new template.

-  The Documents tab includes **Contact Us**, **Product**, **Accessible
   Media**, **Announcement**, **CSS File**, **HTML File**, **Javascript
   File**, **Web Link**, **Illustrated Web Content**, **Web Content**,
   **File**, **Accessible Breadcrumb**, **Accessible Navigation**, and
   **Accessible Site Search Box**.

-  The Actions tab includes **Add Metadata Action**, **Automatic
   Versioning**, **Enable Versioning**, **Populate to Menu**, and **Add
   Category Action**.

-  The Others tab includes **Comments**, **Votes**, and **File
   Content**.

.. note:: -  **Contact Us** and **Product** are for the ACME site, so these templates only appear when the ACME site is enabled.
		  -  **Accessible Breadcrumb**, **Accessible Navigation** and  **Accessible Site Search Box** are for the WAI site, so these templates only appear when the WAI site is enabled.
		  -  **Populate to Menu** only appears in the list of Action templates when the ACME site is enabled.

Editing/Deleting a Document template
``````````````````````````````````````

**Editing a Document template**

1. Select the template type tab (Documents, Actions or Others).

2. Click |image22| corresponding to your desired template in the Action
   column.

The View & Edit Template form appears.

|image23|

3. Make changes on the values of each tab, including:

-  In the Template tab, you can edit the label of the template. The is
   Document Template checkbox is selected by default when you select the
   Documents tab. However, this checkbox is disabled by default when you
   select the Actions or Others tab.

-  In the Dialog tab, you can add a dialog, edit or delete an existing
   dialog. Besides, you can set permission to use the dialog form for a
   specific group and membership. Setting the \* membership will allow
   all users of the group to have this permission. For more details, see
   `Dialogs <../../../reference/html/PLFRefGuide.PLFDevelopment.TemplateConfiguration.Content.ContentTypes.Dialogs.html>`__.

-  In the View tab, you can add a view, edit or delete an existing view.
   Besides, you can set permission to view the template for a specific
   group and membership. Setting the \* membership will allow all users
   of the group to have this permission. For more details, see
   `Views <../../../reference/html/PLFRefGuide.PLFDevelopment.TemplateConfiguration.Content.ContentTypes.View.html>`__.

-  In the CSS tab, you can add a new stylesheet, edit or delete an
   existing stylesheet.

.. note:: -  You cannot delete the default dialog/view.
		  -  You cannot change the dialog/view/CSS name.
		  -  If you click Enable Versioning or Versioning activated checkbox, the edited dialog/view/CSS automatically increments one version after you have clicked **Save**. It is displayed at the Version column.
		  -  After the dialog/view/CSS has been enabled versioning, you will see the Versions field and the Restore button at the bottom of the form. You can use Restore to roll back to a selected version.

**Deleting a Document template**

Simply click |image24| corresponding to the template you want to remove,
then select **OK** in the confirmation message.

Adding a new document template
```````````````````````````````

1. Select the template type tab (Documents, Actions or Others).

2. Click Add Template at the bottom to open the Template Form window.

|image25|

.. note:: The is Document Template checkbox is selected by default when you select the Documents tab. However, this checkbox is disabled by default when you select the Actions or Others tab.

3. Select the template type from the Name drop-down menu.

4. Specify a name for the template in the Label field.

5. Click |image26| next to the Permission field to open the Select
   Permission dialog.

6. Optionally, select the Dialog tab, View, and/or CSS and enter the 
   value in the input-text box.

7. Click Save to create the template.

.. _WorkingWithTemplates.ListTemplates:

List templates
---------------

In Templates, select List to open the List panel. There are 3 types of
List (also called CLV) templates: Content, Navigation and Paginator.

|image27|

Editing/Deleting a List template
`````````````````````````````````

**Editing a List template**

1. Click |image28| corresponding to your desired template in the Action
   column.

The Edit List Template form appears.

|image29|

2. Make any changes on fields: Content, Name, or change the template 
   type from the Template Type drop-down menu.

.. note:: You cannot change the Template Name field.

**Deleting a List template**

Simply click |image30| corresponding to the template you want to remove,
then select **OK** in the confirmation message.

Adding a new List template
```````````````````````````

1. Click Add Template at the bottom to open the Add List Template window.

|image31|

2. Add values to the Content, Name, Template Name fields and select the
   template type from the Template Type drop-down menu.

.. note:: After creating your new List template, you cannot edit the Template Name field.

3. Click Save to finish adding your new list template, or Reset to clear
   your entered values.

.. _WorkingWithTemplates.MetadataTemplates:

Metadata templates
-------------------

Metadata are information which describes, or supplements the central
data. When data are provided to end-users, the metadata allow users to
understand about information in details.

In Templates, select Metadata to open the Metadata panel.

|image32|

**Viewing a Metadata template**

Simply click |image33| corresponding to the metadata you want to view.

The Metadata Information form will open.

|image34|

**Editing a Metadata template**

1. Click |image35| corresponding to your desired template in the Action
   column.

The Edit Metadata's Template form appears.

|image36|

2. Change the required properties of the metadata.

.. note:: You cannot edit the metadata name.

3. Click Apply to save all metadata changes.

**Deleting a Metadata template**

Simply click |image37| corresponding to the template you want to remove,
then select **OK** in the confirmation message.
   
   
.. _WorkingWithExplorer:

Working with Explorer
~~~~~~~~~~~~~~~~~~~~~~

From the Manage ECM Main Functions panel, select Explorer.

|image38|

Here you can manage:

- :ref:`Views <WorkingWithExplorer.Views>`

- :ref:`Drives <WorkingWithExplorer.Drives>`

- :ref:`Tags <WorkingWithExplorer.Tags>`



.. _WorkingWithExplorer.Views:

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
    

.. _WorkingWithExplorer.Tags:    
    
Tags
-----

The **Tagging** function enables you to manage tag styles.

In Explorer, select Tags to open the Tags panel:

|image81|

The style of tag which is applied depends on the number of documents
using the tag. For example, if one tag is used twice, its style will be
``font-size: 12px; font-weight: bold; color: #6b6b6b; font-family: verdana; text-decoration:none;``.

Editing/Deleting a tag style
`````````````````````````````

**Editing a tag**

The Tag Manager tab enables you to edit the existing tags.

1. Click |image82| corresponding to the tag name which you want to edit 
   in the Action column to edit the tag style configuration. The Edit 
   Tag Style Configuration form appears which is similar to that of 
   adding a tag style.

2. Change values in the fields, including Number of Occurrences and HTML
   Style, except Style Name.

3. Click Update to save new changes.

**Deleting a tag**

To delete one tag style, simply click |image83| in the Action column,
then select **OK** in the confirmation message.

Adding a tag style
````````````````````

1. Click Add Style at the bottom to open the Edit Tag Style 
   Configuration form.

|image84|

**In which:**

+--------------------+--------------------------------------------------------+
| Field              | Description                                            |
+====================+========================================================+
| **Style Name**     | The tag name which cannot be edited after you have     |
|                    | added.                                                 |
+--------------------+--------------------------------------------------------+
| **Number of        | The number of documents assigned to a tag.             |
| Occurrences**      |                                                        |
+--------------------+--------------------------------------------------------+
| **HTML Style**     | Includes font-size, font-weight, color, font-family,   |
|                    | and text-decoration.                                   |
+--------------------+--------------------------------------------------------+
| **Asterisk (\*)**  | Indicates the fields are mandatory.                    |
+--------------------+--------------------------------------------------------+

2. Input values in the fields: Style Name, Number of Occurrences, and 
   HTML Style.

3. Click Update to accept adding a new tag style.

.. note:: The format of valid range must be: a..b where 'a', 'b' are positive integers. You can use \* instead of 'b' to indicate it is unlimited. For example, 0..2 (means 0-2 documents assigned to a tag), 10..\* (means at least 10 documents assigned to a tag).
		  The HTML Style textbox cannot be empty. You can change values of font size, font weight, color, font family, and text decoration later.

Setting permissions on public tags
````````````````````````````````````

The Tag Permission Manager tab helps you set permissions regarding to
editing and deleting public tags.

|image85|

**Setting permission to tag management**

Here, you can click |image86| or |image87| or |image88| to add 
permissions to the users, memberships or anyone respectively. Then, 
click Add to add your selected permissions to the User or Group table.

.. note:: -  If you set the \* membership for a group, all users of the group will be able to manage tags, regardless of their membership role.

**Deleting a permission**

In the User or Group table, simply click |image89|, then select **OK** in
the confirmation message.


.. _WorkingWithRepository:

Working with Repository
~~~~~~~~~~~~~~~~~~~~~~~~~~

From the Manage ECM Main Functions panel, select Repository.

|image90|

Here you can manage:

-  :ref:`Namespaces <WorkingWithRepository.Namespaces>`

-  :ref:`Node types <WorkingWithRepository.NodeTypes>`

-  :ref:`Locks <WorkingWithRepository.Locks>`

.. _WorkingWithRepository.Namespaces:

Namespaces
------------

The namespace is a prefix in the node type name. It enables you to
create node types without fearing any conflict with existing node types.

In Repository, select Namespaces to open the Namespaces panel.

|image91|

**Registering a namespace**

1. Click Register at the bottom of the Namespaces form open the Register
   New Namespace form.

|image92|

2. Enter the value for the Namespace Prefix field that is required.

3. Enter the value for the URI field which must be unique and required.

.. note:: The namespace must not contain special characters, such as ``!,#,$,&,\*,(,)``.

.. _WorkingWithRepository.NodeTypes:

Node types
-----------

This function is used to control all node types in eXo Platform.

In Repository, select Node Types to open the Node Types panel.

|image93|

**Viewing node types**

1. Click |image94| corresponding to the node you want to view. The View 
   Node Type Information form will appear.

|image95|

2. Click Close at the bottom of the form to exit.

**Adding a node type**

1. Click Add at the bottom of the **Node Types** page to open the 
   Add/Edit Node Type Definitions form.

|image96|

2. Select a namespace for the node.

3. Enter a name in the Node Type Name field. This field is mandatory and
   its value must be unique.

.. note:: The name must not contain special characters, such as ``!,#,$,&,\*,(,)``.

4. Select a value for the Is Mixin Type field.

-  True: This node is Mixin type.

-  False: This node is not Mixin type.

5. Select a value for the Orderable Child Nodes field.

-  True: Child nodes are ordered.

-  False: Child nodes are not ordered.

6. Enter a value for the Primary Item Name field.

7. Enter a value for the Super Types field. Clicking |image97| will 
   direct you to the Super Types tab for you to search for available 
   super types.

   -  Property Definitions: Lists all definition names of the Property 
      tab.

   -  Child Node Definitions: Lists all definition names of the Child Node
      tab.

8. Click Save to accept adding a new node type, or Save as Draft to save
   this node type as draft.

**Importing node types**

1. Click Import at the bottom of the **Node Types** page to open the 
   Import Node Type From XML File form.

|image98|

2. Click Select File to upload a file.

.. note:: You must upload an XML or ZIP file. This file is in the node type's format.

3. Click the Upload button.

.. note:: If you want to upload another file, click |image99| to delete the file which has just been uploaded, then upload other files.

4. Tick the checkboxes corresponding to the nodes that you want to 
   import.

5. Click Import to complete importing a node type.

**Exporting node types**

1. Click Export at the bottom of the **Node Types** page to open the 
   Export Node Types form.

|image100|

2. Click Uncheck all if you do not want to export all node types. After
   clicking Uncheck all, this button becomes the Check all button.

3. Select nodes that you want to export by ticking the corresponding
   checkboxes.

4. Click Export in this form.

5. Select the location in your device to save the exported node.

.. note:: You must select at least 1 node type to be exported. If you do not want to export the node, click Cancel to quit this pop-up.


.. _WorkingWithRepository.Locks:

Locks
------

In Repository, select Locks to open the Locks panel. The locked nodes
will be listed in the right panel.

|image101|

**Unlocking a node**

Simply click |image102| corresponding to nodes which need to be unlocked
in the Locked Node tab. The unlocked nodes will disappear from the
locked nodes list.

**Managing locks**

Administrators can manage and add the unlock permission for another
group and users in the Manage Lock tab.

Select the group on the Select Group panel and the corresponding
membership on the Select Membership panel. The selected group will be
listed in the Groups Or Users column.

-  Click |image103| corresponding to the group which you want to remove
   from the "Unlock" permission list, except the
   ``*:/platform/administrator`` group.

.. note:: If you set the \* membership for a group, all users of the group will be able to manage locks, regardless of their membership role.


.. _WorkingWithAdvancedConfiguration:

Working with Advanced configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

From the Manage ECM Main Functions panel, select Advanced.

|image104|

Here you can manage:

-  :ref:`Categories <WorkingWithAdvancedConfiguration.Categories>`

-  :ref:`Queries <WorkingWithAdvancedConfiguration.Queries>`

-  :ref:`Scripts <WorkingWithAdvancedConfiguration.Scripts>`

-  :ref:`Actions <WorkingWithAdvancedConfiguration.Actions>`


.. _WorkingWithAdvancedConfiguration.Categories:

Categories
-----------

A category can be understood as a classification practice and science.
It is used to sort documents, aiming at facilitating searches. The
category management includes adding, editing and deleting a category
tree.

In Advanced, select Categories. You will be directed to the
**Categories** panel as below:

|image105|

Here, you can do the following actions:

-  :ref:`Editing a category tree <Categories.EditingCategoryTree>`
   |image106|

-  :ref:`Deleting a category tree <Categories.DeletingCategoryTree>`
   |image107|

-  :ref:`Adding a category tree <Categories.AddingCategoryTree>`
   |image108|
   
.. _Categories.EditingCategoryTree:   

Editing/Deleting a category tree
`````````````````````````````````

**Editing a category tree**

1. Click |image109| in the Action column to open the Edit Category Tree 
   form.

|image110|

2. Click |image111| in the Add column to add more category trees. The 
   mini Edit Category Tree form will appear.

|image112|

3. Enter a category name in the Category Name field which is required.

.. note:: The category name must not contain more than 150 characters.

4. Click Save to save the category name.

5. Click Previous to return to the previous steps.

6. Click Save to save all changes, or Previous or Next if you want to 
   edit more.

.. _Categories.DeletingCategoryTree:

**Deleting a category tree**

Simply click |image113| in the Action column, then select **OK** in the
confirmation message.

.. _Categories.AddingCategoryTree:

Adding a category tree
````````````````````````

1. Click Add Category Tree to open the Add Category Tree form.

|image114|

2. Enter the category tree name in the Name field which is required.

3. Select the workspace you want to work with.

4. Select the home path by clicking |image115|. The Select Home Path 
   form will appear.

|image116|

-  Click |image117| next to Root Path if you want to select the root path
   or;

-  Click the arrow icon to go to the up level path and click the plus
   sign to expand the folder in the left pane.

   Click |image118| corresponding to the path that you want to select as
   a home path.

5. Click Next to select permissions for the category tree.

|image119|

-  **i.** Click |image120| or |image121| or |image122| to set 
   permissions for user, membership or everyone respectively. Your 
   selected user or membership will be displayed in the User or Group 
   column.

.. note:: When ticking any permissions above (Read, Add Node or Remove), if you set the \* membership for a group, this permission will be granted to all users of the group, regardless of their membership role.

-  **ii.** Check the right options for the selected user to membership:

.. note:: Ticking only Add Node Right or Remove Right means that Read Right is selected automatically.

6. Click Save to save all values, or Reset to change values that have 
   just been set. After clicking Save, click Next to go to the next step.

|image123|

7. Enter the name for an action of the category tree in the Name field
   which is required.

8. Select values for Lifecycle, Node Types, Target Workspace, Target Path,
   Affected Node Types which are required.

9. Click Save to commit all values.

.. note:: -  Do not input some special characters into the Name field, such as: ``!,#,$,&,\*,(,)``.

		  -  Do not add a category which has the same name and level with existing taxonomies in a node.


.. _WorkingWithAdvancedConfiguration.Queries:

Queries
---------

In Advanced, select Queries. You will be directed to the **Queries**
panel as below:

|image124|

Here, you can do certain actions on the queries as follows:

-  :ref:`Editing a query <Queries.EditingQuery>` |image125|

-  :ref:`Deleting a query <Queries.DeletingQuery>` |image126|

-  :ref:`Adding a new query <Queries.AddingNewQuery>` |image127|

.. _Queries.EditingQuery:

Editing a query
`````````````````

1. Click |image128| in the Action column to open the Edit Query form.

|image129|

2. Edit the properties of the selected query.

.. note:: In the *Permissions* field, if you set the \* membership for a group, all users of the group will be able to access this saved query, regardless of their membership role.

3 .Click Save to accept all changes.

.. _Queries.DeletingQuery:

Deleting a query
``````````````````

Simply click |image130| in the Action column, then select **OK** in the
confirmation message.

Adding a new query
`````````````````````

1. Click Add Query to open the Add Query form.

|image131|

2. Enter a query name into the Query Name field that is required.

3. Select the query type from the Query Type drop-down menu.

-  xPath (XML Path Language) is a language for selecting nodes. For
   example, ``/jcr:root/Documents/Live``.

-  SQL (Structured Query Language) is a database computer language.

4. Enter the statement for the query that must be unique.

5. Check or uncheck the Enable Cache Results option. If you tick this
   checkbox, for the first time you use this query to search, the result
   will be cached. For the second time you search using this query, it 
   will show the cached results. After 10 minutes, the cache will be 
   removed.

   For example, you have the **Test** query with the **//element (\*,
   nt:file)**. In Sites Explorer, you have a ``nt:file`` document named
   ``File1``. When you execute the query ``Test``, only the ``File1``
   document is shown. After that, create a ``nt:file`` document named
   ``File2`` and execute the query ``Test``, only the ``File1`` document 
   is listed. After 45 minutes, the cache will be removed. When you 
   execute the query ``Test``, ``File1`` and ``File2`` will be listed.

6. Select permissions for a group that can use this query by clicking
   |image132|.

.. note:: In the *Permissions* field, if you set the \* membership for a group, all users of the group will be able to access this saved query, regardless of their membership role.

7. Click Save to finish adding a new query.


.. _WorkingWithAdvancedConfiguration.Scripts:

Scripts
--------

In Advanced, select Scripts. You will be directed to the **Scripts**
panel as below:

|image133|

The Scripts panel has 3 tabs:

-  Actions which is for action scripts.

-  Interceptors which is for dialog interceptors.

-  Widgets which is for widget scripts.

Here, you can do certain actions on the scripts as follows:

-  :ref:`Editing a script <Scripts.EditingScript>` |image134|

-  :ref:`Deleting a script <Scripts.DeletingScript>` |image135|

-  :ref:`Adding a new script <Scripts.AddingNewScript>` |image136|

.. _Scripts.EditingScript:

Editing a script
`````````````````

**Editing a script**

1. Click |image137| in the Action column to open the Add/Edit Script 
   form.

|image138|

2. Edit the properties in this form.

3. Click Save to save all changes.

.. _Scripts.DeletingScript:

Deleting a script
``````````````````

Simply click |image139| in the Action column, then click **OK** in the
confirmation message.

.. _Scripts.AddingNewScript:

Adding a new script
````````````````````

1. Click Add Script to open the Add/Edit Script form.

2. Enter values for the Content, Name and Script fields.

.. note:: The value for the Script field must be unique and not contain special characters, such as ``!,#,$,&,\*,(,)``.

3. Click Save to accept adding your new script.

.. _WorkingWithAdvancedConfiguration.Actions:

Actions
--------

This function allows you to manage all action nodes in eXo Platform. In
Advanced, select Actions to open the **Actions** panel.

|image140|

Here, you can do certain actions as follows:

-  :ref:Editing an action <Actions.EditingAction>` |image141|

-  :ref:Deleting an action <Actions.DeletingAction>` |image142|

-  :ref:Adding an action type <Actions.AddingActionType>` |image143|

Editing an action
```````````````````

1. Click |image144| in the Action column to open the Add Action Type 
   form.

2. Edit the properties in this form.

3. Click Save to save all changes.

Deleting an action
```````````````````

Simply click |image145| in the Action column, then select **OK** in the
confirmation message.

Adding an action type
``````````````````````

1. Click Add Action Type to open the Add Action Type form.

|image146|

2. Input a name for the action.

3. Select the script type.

4. Enter the value for the Variables field.

-  Click |image147| to add more values for the action.

-  Click |image148| to delete one value.

5. Click Save to accept adding a new action type.




.. |image0| image:: images/common/administration_navigation.png
.. |image1| image:: images/platform/branding_page.png
.. |image2| image:: images/platform/current_logo_preview.png
.. |image3| image:: images/common/administration_navigation.png
.. |image4| image:: images/social/notification_administration.png
.. |image5| image:: images/common/administration_navigation.png
.. |image6| image:: images/ecms/new_content_button.png
.. |image7| image:: images/ecms/css_file_form.png
.. |image8| image:: images/ecms/globalstylesheet_orange_css.png
.. |image9| image:: images/ecms/new_css_file.png
.. |image10| image:: images/ecms/globalstylesheet_blue.png
.. |image11| image:: images/ecms/globalstylesheet_orange.png
.. |image12| image:: images/common/edit_navigation.png
.. |image13| image:: images/platform/edit_menu.png
.. |image14| image:: images/common/administration_navigation.png
.. |image15| image:: images/ecms/content_administration_page.png
.. |image16| image:: images/common/1.png
.. |image17| image:: images/common/2.png
.. |image18| image:: images/common/3.png
.. |image19| image:: images/common/4.png
.. |image20| image:: images/ecms/template_types.png
.. |image21| image:: images/ecms/documents_template_panel.png
.. |image22| image:: images/common/edit_icon.png
.. |image23| image:: images/ecms/view_edit_template_form.png
.. |image24| image:: images/common/delete_icon.png
.. |image25| image:: images/ecms/add_new_template.png
.. |image26| image:: images/common/plus_icon.png
.. |image27| image:: images/ecms/list_templates_panel.png
.. |image28| image:: images/common/edit_icon.png
.. |image29| image:: images/ecms/edit_list_template.png
.. |image30| image:: images/common/delete_icon.png
.. |image31| image:: images/ecms/add_list_template.png
.. |image32| image:: images/ecms/metadata_panel.png
.. |image33| image:: images/common/view_icon.png
.. |image34| image:: images/ecms/metadata_information_form.png
.. |image35| image:: images/common/edit_icon.png
.. |image36| image:: images/ecms/edit_metadata_template.png
.. |image37| image:: images/common/delete_icon.png
.. |image38| image:: images/ecms/explorer_types.png
.. |image39| image:: images/ecms/drives_management.png
.. |image40| image:: images/common/1.png
.. |image41| image:: images/common/2.png
.. |image42| image:: images/common/3.png
.. |image43| image:: images/common/edit_icon.png
.. |image44| image:: images/ecms/edit_drive_form.png
.. |image45| image:: images/common/delete_icon.png
.. |image46| image:: images/ecms/add_drive_form.png
.. |image47| image:: images/ecms/workspaces.png
.. |image48| image:: images/common/plus_icon.png
.. |image49| image:: images/common/plus_icon.png
.. |image50| image:: images/common/plus_icon.png
.. |image51| image:: images/common/show_elements.png
.. |image52| image:: images/common/plus_icon.png
.. |image53| image:: images/ecms/apply_views_tab.png
.. |image54| image:: images/ecms/views_form.png
.. |image55| image:: images/ecms/admin_view.png
.. |image56| image:: images/ecms/icons_view.png
.. |image57| image:: images/ecms/list_view.png
.. |image58| image:: images/ecms/categories_view.png
.. |image59| image:: images/ecms/web_view.png
.. |image60| image:: images/common/view_icon.png
.. |image61| image:: images/ecms/preview_view_form.png
.. |image62| image:: images/common/edit_icon.png
.. |image63| image:: images/ecms/edit_view_form.png
.. |image64| image:: images/ecms/edit_view_restore_field.png
.. |image65| image:: images/common/edit_icon.png
.. |image66| image:: images/common/delete_icon.png
.. |image67| image:: images/ecms/content_administration.png
.. |image68| image:: images/ecms/Manage_ECM_functions.png
.. |image69| image:: images/common/edit_portlet_icon.png
.. |image70| image:: images/common/edit_portlet_icon.png
.. |image71| image:: images/ecms/action_tab.png
.. |image72| image:: images/ecms/check_uncheck_actions_view.png
.. |image73| image:: images/common/delete_icon.png
.. |image74| image:: images/ecms/add_view_form.png
.. |image75| image:: images/ecms/add_edit_tab_form.png
.. |image76| image:: images/ecms/tab_added_form.png
.. |image77| image:: images/ecms/explorer_templates.png
.. |image78| image:: images/common/edit_icon.png
.. |image79| image:: images/common/delete_icon.png
.. |image80| image:: images/ecms/add_explorer_template_form.png
.. |image81| image:: images/ecms/tags_view.png
.. |image82| image:: images/common/edit_icon.png
.. |image83| image:: images/common/delete_icon.png
.. |image84| image:: images/ecms/edit_style.png
.. |image85| image:: images/ecms/tag_permission_manager.png
.. |image86| image:: images/common/select_user_icon.png
.. |image87| image:: images/common/select_membership_icon.png
.. |image88| image:: images/common/select_everyone_icon.png
.. |image89| image:: images/common/delete_icon.png
.. |image90| image:: images/ecms/repository_types.png
.. |image91| image:: images/ecms/namespaces_panel.png
.. |image92| image:: images/ecms/register_namespace_form.png
.. |image93| image:: images/ecms/node_types_panel.png
.. |image94| image:: images/common/view_icon.png
.. |image95| image:: images/ecms/view_node_type_information_form.png
.. |image96| image:: images/ecms/add_edit_node_type_definitions.png
.. |image97| image:: images/common/search_icon.png
.. |image98| image:: images/ecms/import_nodetype.png
.. |image99| image:: images/common/delete_icon.png
.. |image100| image:: images/ecms/export_node_types.png
.. |image101| image:: images/ecms/locks_panel.png
.. |image102| image:: images/common/lock_icon.png
.. |image103| image:: images/common/delete_icon.png
.. |image104| image:: images/ecms/advanced_types.png
.. |image105| image:: images/ecms/categories_panel.png
.. |image106| image:: images/common/1.png
.. |image107| image:: images/common/2.png
.. |image108| image:: images/common/3.png
.. |image109| image:: images/common/edit_icon.png
.. |image110| image:: images/ecms/edit_category_tree_form.png
.. |image111| image:: images/common/plus_icon.png
.. |image112| image:: images/ecms/mini_edit_category_tree_form.png
.. |image113| image:: images/common/delete_icon.png
.. |image114| image:: images/ecms/add_category_tree.png
.. |image115| image:: images/common/plus_icon.png
.. |image116| image:: images/ecms/select_homepage_form.png
.. |image117| image:: images/common/select_icon.png
.. |image118| image:: images/common/select_icon.png
.. |image119| image:: images/ecms/set_permissions_category_tree.png
.. |image120| image:: images/common/select_user_icon.png
.. |image121| image:: images/common/select_membership_icon.png
.. |image122| image:: images/common/select_everyone_icon.png
.. |image123| image:: images/ecms/add_category_tree_fullform.png
.. |image124| image:: images/ecms/queries_panel.png
.. |image125| image:: images/common/1.png
.. |image126| image:: images/common/2.png
.. |image127| image:: images/common/3.png
.. |image128| image:: images/common/edit_icon.png
.. |image129| image:: images/ecms/edit_query_form.png
.. |image130| image:: images/common/delete_icon.png
.. |image131| image:: images/ecms/add_query_form.png
.. |image132| image:: images/common/plus_icon.png
.. |image133| image:: images/ecms/scripts_panel.png
.. |image134| image:: images/common/1.png
.. |image135| image:: images/common/2.png
.. |image136| image:: images/common/3.png
.. |image137| image:: images/common/edit_icon.png
.. |image138| image:: images/ecms/add_edit_script_form.png
.. |image139| image:: images/common/delete_icon.png
.. |image140| image:: images/ecms/actions_panel.png
.. |image141| image:: images/common/1.png
.. |image142| image:: images/common/2.png
.. |image143| image:: images/common/3.png
.. |image144| image:: images/common/edit_icon.png
.. |image145| image:: images/common/delete_icon.png
.. |image146| image:: images/ecms/add_action_type.png
.. |image147| image:: images/common/plus_icon.png
.. |image148| image:: images/common/delete_icon.png
