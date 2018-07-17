.. _ManagingPages:

==============
Managing pages
==============

Managing pages includes the following actions:

-  `Adding a new
   page. <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.AddingNewPage>`__

-  `Editing the page properties and
   layout. <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.EditingPage>`__

-  `Deleting a
   page. <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.DeletingPage>`__

``
      
    ``

-  `Managing
   permissions <#PLFUserGuide.AdministeringeXoPlatform.ManagingPermissions>`__

-  `Managing
   sites <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites>`__

-  `Managing
   navigations <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations>`__

-  `Managing
   applications <#PLFUserGuide.AdministeringeXoPlatform.ManagingApplications>`__

Adding a new page
-----------------

Before diving into how to add a new page, you need to clarify the
relationship between navigation node and page. Node and page are two
entities that are totally different and a node can be referenced to a
page. A page can only be accessed by users via a node.

.. _PageCreationWizard:

**Using Page Creation Wizard**

The **Page Creation Wizard** is available to the portal's administrators
and facilitates them to create and publish portal pages quickly and
easily. In this way, you are creating a navigation node and its page
together.

The whole process to create a new page can be divided into **3**
specific steps:

**Step 1: Selecting a navigation node and creating the page**

In the first step, you have to set Node Name and Display Name of your
page. You are also able to decide the pages visibility and the
publication period of the page.

Open the site to which you want to add a new page. You will be switched
to your selected site only after a few seconds.

Click |image0| on the top navigation bar, then select Page Add Page from
the drop-down menu to open the Page Creation Wizard form.

The wizard is divided into two sections.

-  The left panel contains existing pages/nodes displayed in the tree
   hierarchy. Here, you can navigate up and down the node/page
   structure.

-  The right panel displays Page Editor where you can make changes on
   the selected navigation node. You can input parameters for your new
   page in this panel.

**In which:**

+--------------------------+--------------------------------------------------+
| Field                    | Description                                      |
+==========================+==================================================+
| Selected Page Node       | The path of the selected node to add a new       |
|                          | sub-page.                                        |
+--------------------------+--------------------------------------------------+
| Node Name                | The node name of the added page. This field is   |
|                          | required, unique and must start with a letter.   |
|                          | Only alphabetical, numerical, dash and           |
|                          | underscore characters are allowed for this field |
|                          | with the length between 3 and 30 characters.     |
+--------------------------+--------------------------------------------------+
| Extended label mode      | Ticks the checkbox to show the Language field    |
|                          | for you to select another language for your      |
|                          | created node's display name. It means that if    |
|                          | this checkbox is deselected, the Language field  |
|                          | will be deactivated.                             |
+--------------------------+--------------------------------------------------+
| Language                 | Selects your desired language for the node's     |
|                          | display name from the drop-down menu.            |
+--------------------------+--------------------------------------------------+
| Display Name             | The display name of the node which contains the  |
|                          | added page and its length must be between 3 and  |
|                          | 120 characters.                                  |
+--------------------------+--------------------------------------------------+
| Visible                  | Toggles the global visibility of this page.      |
|                          |                                                  |
|                          | If this option is checked, the page or the page  |
|                          | node appears on the navigation bar, the page     |
|                          | navigation and the sitemap. If "Visible" is      |
|                          | checked, the visibility also depends on the      |
|                          | Publication Date & Time option.                  |
|                          |                                                  |
|                          | If not being unchecked, the page is hidden under |
|                          | any circumstances, even if the publication       |
|                          | period is valid.                                 |
+--------------------------+--------------------------------------------------+
| Publication date & time  | Allows the page to be published for a given      |
|                          | period. If this option is checked, Start         |
|                          | Publication Date and End Publication Date will   |
|                          | be shown.                                        |
+--------------------------+--------------------------------------------------+
| Start Publication Date   | The start date and time to publish the page.     |
+--------------------------+--------------------------------------------------+
| End Publication Date     | The end date and time to publish the page.       |
+--------------------------+--------------------------------------------------+

    **Note**

    If a node is not visible (the "Visible" option is unchecked or the
    current time is not within publication period), it does not appear
    in any navigation or site map, but is still accessible via its URL.

Click Next or number '2' of the wizard steps to go to `Step
2. <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.PageCreationWizard.SelectingPageLayoutTemplate>`__

**Step 2: Selecting a page layout template**

|image1|

Select Empty Layout or click the down-arrow icon in the left panel to
see more templates and select one.

Click Next or number '3' of the wizard steps to go to the `last
step. <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.PageCreationWizard.RearrangingPageLayout>`__

.. _RearrangingPageLayout:

**Step 3: Arranging the page layout**

In this step, you can arrange the page's layout by:

-  Adding your desired applications, containers or gadgets by dragging
   and dropping them from Page Editor to the main page body.

   |image2|

   **In which:**

   +----------------------+-----------------------------------------------------+
   | Tab                  | Description                                         |
   +======================+=====================================================+
   | Applications         | This tab lists all existing categories and their    |
   |                      | portlets that you easily can drag and drop into the |
   |                      | container.                                          |
   +----------------------+-----------------------------------------------------+
   | Containers           | This tab contains all existing containers to build  |
   |                      | your page layout. You can add a container to your   |
   |                      | page area by dragging and dropping available        |
   |                      | containers from Page Editor to the main page body.  |
   |                      |                                                     |
   |                      | -  There are various layouts available, including   |
   |                      |    Rows Layout, Columns Layout, Autofit Columns     |
   |                      |    Layout, Tabs Layout and Mixed Layout.            |
   |                      |                                                     |
   |                      |    For Tabs Layout, you can add more tabs to the    |
   |                      |    layout, and reorder the position of the tabs.    |
   |                      |                                                     |
   |                      | -  For each layout, you can edit different layers,  |
   |                      |    from the parent container to its child           |
   |                      |    containers. The parent container holds its child |
   |                      |    containers and the child containers can hold     |
   |                      |    applications. You can also drag a container to   |
   |                      |    another one that helps you create various        |
   |                      |    layouts to your desires.                         |
   |                      |                                                     |
   |                      | -  Remember that you can also drag and drop the     |
   |                      |    container to another one that helps you create   |
   |                      |    your own various layouts to your desires.        |
   |                      |                                                     |
   |                      | -  For any container layout, you can edit the       |
   |                      |    parent container or its child containers         |
   |                      |    separately. Deleting the parent container means  |
   |                      |    that its child containers are removed as well.   |
   |                      |                                                     |
   |                      | -  You cannot drag and drop a child container to    |
   |                      |    change its location, but can drag it outside its |
   |                      |    parent container.                                |
   |                      |                                                     |
                                                                               
   +----------------------+-----------------------------------------------------+

-  Rearranging elements in the page body by dragging and dropping them
   into your desired positions. Also, you can edit or remove any element
   by hovering your cursor over it and selecting |image3| , or |image4|
   respectively.

-  Viewing page properties by clicking View Page Properties at the
   bottom of the Page Editor window.

-  Previewing your changes by clicking Switch View Mode.

    **Note**

    Click |image5| in the Page Editor window to save all changes, or
    |image6| to close without saving your changes.

**Using Pages Management**

In this way, the page only will be created. Thus, to make this page
accessible, you need to create a node that links to this page (in the
Page Selector tab). See `Adding a new
node <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations.AddingNewNode>`__
for more details.

`Access the Pages Management page <#AccessingPagesManagementPage>`__.

Select Add New Page at the bottom. The form with the Page Settings tab
opened will display as below.

|image7|

**In which:**

+------------------------+---------------------------------------------------+
| Field                  | Description                                       |
+========================+===================================================+
| Page Id                | The page's identification string which will be    |
|                        | automatically generated when the page is created. |
+------------------------+---------------------------------------------------+
| Owner Type             | -  If Owner Type is "*portal*\ ", the page is     |
|                        |    created for a portal. Therefore, only users    |
|                        |    who have the *Edit* permission on the portal   |
|                        |    can create this page type.                     |
|                        |                                                   |
|                        | -  If Owner Type is "*group*\ ", the page is      |
|                        |    created for a group. Therefore, only users who |
|                        |    are the *manager* of that group can create     |
|                        |    this page type.                                |
|                        |                                                   |
                                                                            
+------------------------+---------------------------------------------------+
| Owner Id               | The identification name of the page's owner which |
|                        | will be automatically created after you have      |
|                        | selected Owner Type.                              |
|                        |                                                   |
|                        | -  When the owner type is set to "group", a list  |
|                        |    of groups will allow you to select one user as |
|                        |    the 'owner'.                                   |
|                        |                                                   |
|                        | -  The name of the current portal is              |
|                        |    automatically selected for Owner Id, ensuring  |
|                        |    the *Edit* permission is assigned to users who |
|                        |    can edit the current portal.                   |
|                        |                                                   |
                                                                            
+------------------------+---------------------------------------------------+
| Page Name              | The page name which is required, unique and       |
|                        | starts with a letter. Only alphabetical,          |
|                        | numerical, dash and underscore characters are     |
|                        | allowed with its length from 3 to 30 characters.  |
+------------------------+---------------------------------------------------+
| Page Title             | The page title which is optional with its length  |
|                        | from 3 to 30 characters.                          |
+------------------------+---------------------------------------------------+
| Show Max Window        | The option enables the page to be shown at the    |
|                        | maximum size or not.                              |
+------------------------+---------------------------------------------------+

Define the page layout in the Page Layout tab.

Define permissions in the Permissions tab. This tab consists of four
sub-tabs named Access, Edit, Move Apps and Move Containers.

-  The Access tab shows all users who can access the page:

   -  If the value of the Owner Type field is "*Portal*\ ", the name of
      the current portal is automatically selected for the Owner Id
      field, so that the *Access* permission is assigned to all users
      who can access the current portal.

   -  If the value of the Owner Type field is "*Group*\ ", the *Access*
      permission is assigned to all users who are the members of the
      group that is selected in the Owner Id field of the Page Settings
      tab.

   To reassign the *Access* permission for the page, see details in the
   `Access
   permission <#PLFUserGuide.AdministeringeXoPlatform.ManagingPermissions.SettingPortalPermissions.AccessPermission>`__
   section.

-  The Edit shows all users who have the *Edit* permission on the page.

   -  If the value of the Owner Type field is "*Portal*\ ", the *Edit*
      permission is assigned to users who can edit the current portal.

   -  If the value of the Owner Type field is "*Group*\ ", the *Edit*
      permission is assigned to all users who are the members of the
      group that is selected in the Owner Id field of the Page Settings
      tab.

   To reassign the *Edit* permission for the page, see details in the
   `Edit
   Permission <#PLFUserGuide.AdministeringeXoPlatform.ManagingPermissions.SettingPortalPermissions.EditPermission>`__
   section.

Click Save to accept creating a new page.

Editing a page
--------------

Open the **Page Properties** page by following one of the two ways:

**The first way**

**i.** Open the Navigation Management form by doing the steps in the
`Editing
navigation <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.EditingSite.EditingNavigation>`__
section.

**ii.** Right-click your desired node and select Edit Node's Page from
the drop-down menu.

**The second way**

**i.** `Access the Pages Management
page <#AccessingPagesManagementPage>`__.

**ii.** Click |image8| corresponding to the page you want to edit.

The Edit Page form will be displayed in the Page Properties window.

|image9|

Click View Page Properties in the Page Editor window to edit the page
properties.

|image10|

**i.** In the Page Settings tab, you cannot change values in Page Id,
Owner Type, Owner Id and Page Name.

**ii.** In the Permissions tab, you can change or add more *Access*,
*Edit*, *Move Apps* and *Move Containers* permissions. This form is only
supported for pages of a *group* or a *portal.* Because the user's page
is private, no one can access or edit it, except the creator.

    **Note**

    For more details on how to assign permissions on a page, refer to
    the `Setting permissions on a
    page <#PLFUserGuide.AdministeringeXoPlatform.ManagingPermissions.SettingPagePermissions>`__
    section.

Click Save, then select |image11| in Page Editor for all changes to take
effect, or |image12| to abort.

Deleting a page
---------------

`Access the Pages Management page <#AccessingPagesManagementPage>`__.

You will see a list of all existing pages.

Click |image13| in the row of the page you want to delete.

Click **OK** in the confirmation message.

.. |image0| image:: images/common/edit_navigation.png
.. |image1| image:: images/gatein/wizard_page_layout.png
.. |image2| image:: images/gatein/wizard_arrange_page.png
.. |image3| image:: images/common/edit_portlet_icon.png
.. |image4| image:: images/common/delete_portlet_icon.png
.. |image5| image:: images/common/save_icon.png
.. |image6| image:: images/common/discharge_icon.png
.. |image7| image:: images/gatein/page_settings_tab.png
.. |image8| image:: images/common/edit_icon.png 
.. |image9| image:: images/gatein/view_page_properties.png
.. |image10| image:: images/gatein/page_settings_tab_edit_page_form.png
.. |image11| image:: images/common/save_icon.png
.. |image12| image:: images/common/remove_icon.png
.. |image13| image:: images/common/delete_icon.png
