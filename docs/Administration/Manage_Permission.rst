.. _ManagingPermissions:

====================
Managing permissions
====================

Permissions play an important role in accessing and performing actions
in eXo Platform. Depending on the permissions assigned by administrators,
users can gain the Access and/or Edit permissions to sites, pages and
various components of the sites.

In eXo Platform, **permission types** define what a user can do within a
site, including:

-  **Access permission** enables users to access sites, pages or
   applications and content in the site pages. This permission can be
   set for multiple member groups.

-  **Edit permission** enables users to make changes on sites, pages or
   applications and content in the site pages. This permission is set
   for only one group at one time.

-  **Move Apps permission** enables users to add, delete or move
   applications on sites and pages via drag and drop. This permission
   can be set for multiple member groups.

-  **Move Containers permission** enables users to add, delete or move
   containers on sites and pages via drag and drop. This permission can
   be set for multiple member groups.

And, **permission levels** specify where the users' permission types can
be applied in the site.

-  **Site**: The permission at the site level defines actions permitted
   on the site. Users with the access permission can view (but not edit)
   the site. Meanwhile, users with the edit permission at the site level
   can modify the site.

-  **Page**: The permission at the page level restricts users to several
   particular pages. Users are only able to see and/or edit pages they
   have been granted, depending on the permission type assigned to them.

-  **Application**: The permission at the application level defines who
   can access the application.

-  **Container**: An application, page, or site may be put into one or
   more containers. The permission at the container level restricts the
   Access permission to content inside it.

With these permission types and levels, administrators can effectively
control who can access and which actions users can perform within the
site. For this reason, you, as an administrator, need to clarify the
layered architecture of a site to grant appropriate permissions to
groups. The simplest way to understand is that:

-  A site consists of one or more pages. These pages may be put into one
   or more containers.

-  Each page normally contains content and/or application(s). These
   content and applications may be put into one or more containers.

If you want members under a group (**platform/guests**, for example) to
be accessible to one application on a site page, grant the Access
permission to that group at the following layers:

-  The application and its containers

-  The page and its container where the application is stored.

-  The page site and its containers.

In the case you only grant the Access permission to the
**platform/guests** group at the site and page layers, this group will
see the page, but not see the applications and content restricted in
that page. To be clearer, see the below example.

**Making guests accessible to the Register form of Intranet**


.. tip:: To make handy for checking permissions at all levels, it is recommended you use the root account to have the highest rights.

For the Intranet site, the Register form is already featured by the
Register application and put into the Register page (node) (by selecting
|image208| --> Portal --> Sites Edit Navigation next to **intranet**).

|image209|

By default, the Register node is already linked to the Register page and
this page already contains the Register application.

You can use the URL format to access pages existing on a site:
`http://mycompany.com:port/portal/{site\_name}/{node\_name} <http://mycompany.com:port/portal/{site_name}/{node_name}>`__.
Remember that {site\_name} and {node\_name} are **case-sensitive**.

In this scenario, log out and use the URL:
`http://mycompany.com:port/portal/intranet/Register <http://mycompany.com:port/portal/intranet/Register>`__.
Now, as a guest, you will be redirected to the Login form, not Register
form. This may be because the Access permission is not granted to the
**platform/guests** group (or is not made public) at the Register
application itself or its outer layers. To make it accessible to the
**platform/guests** group, do as follows:

1. Log in as root, then use
   `http://mycompany.com:port/portal/intranet/Register <http://mycompany.com:port/portal/intranet/Register>`__
   to go to the Register page.

2. Check the Access permission at the Register page level by clicking
   |image210| --> Page --> Edit Layout.

|image211|

-  i. At the application, the Access permission is already granted to
   the **/platform/guests** group by default.

-  ii. At the container (by selecting Containers tab in **Page
   Editor**), the Access permission is already granted to the
   **platform/guests** group. Repeat this step for each container.

 .. note:: Setting the \* membership for a group means that all its users are granted permissions to view the container block, regardless of their membership role.

-  iii. At the page (by selecting View Page properties at the **Page
   Editor** bottom), the Access permission is already granted to the
   **platform/guests** group.

.. note:: Remember to click |image212| to make your changes affect, if any.

3. Go to
   `http://mycompany.com:port/portal/intranet <http://mycompany.com:port/portal/intranet>`__
    to be at the site level, then select |image213| --> Site --> Layout.
    
    |image214|

-  i. At the site container(s) containing the Register page, the Access
   permission is made public by default, meaning that all (including
   guests) can access at the site container.

-  ii. At the outermost layer of the Intranet site (by clicking Site's
   Config at the bottom of **Edit Inline Composer**), the Access
   permission is already assigned to the **platform/users** group only.
   This is the reason why guests cannot access the Register form. So, in
   the **Access tab**, you need to select Add PermissionPlatformGuests
   in the group pane, and **\*** in the membership pane. Alternatively,
   tick the Everyone checkbox.

.. note:: Remember to click |image214| to make your changes affect, if any.

4. Log out, then try using the
   `http://mycompany.com:port/portal/intranet/Register <http://mycompany.com:port/portal/intranet/Register>`__
   link. Now, as a guest, you still can view the Register form, not the
   Login form.

5. Optionally, if you want guests to be redirected to the Register form
   when they only enter
   `http://mycompany.com:port/portal/intranet <http://mycompany.com:port/portal/intranet>`__,
   simply move gradually the Register node to the top in the Navigation
   Management (by right-clicking **Register** and selecting Move Up - 
   you need to repeat this step until the Register node is at the top).

|image215|

Log out, then use the link:
`http://mycompany.com:port/portal/intranet <http://mycompany.com:port/portal/intranet>`__.
Now, you will be redirected to the Register form without entering the
exact URL of the Register page.

|image216|

.. note:: -  In this section, some examples and screenshots use :ref:`default groups and memberships <#PLFAdminGuide.Configuration.PredefinedUserGroupMembership>`
             that are ready-made by configuration. To create groups and memberships as you want, see :ref:`Managing your organization <ManagingYourOrganization>`.

		  -  Do not misunderstand that labels of predefined membership types, such as "manager" or "publisher", represent their permissions.
             This means, those labels do not define any permissions. If you create a page, you are the person who decides if a "manager" has access to your page or not.

Permissions in this section are divided into:

-  :ref:`Setting permissions on a site <ManagingPermissions.SettingPortalPermissions>`

-  `Setting permissions on a page <ManagingPermissions.SettingPagePermissions>`

-  `Setting permissions on a container <ManagingPermissions.SettingContainerPermissions>`

-  `Access permission on a category <ManagingPermissions.SettingAccessPermissionOnCategory>`

-  `Access permission on a portlet <ManagingPermissions.SettingAccessPermissionOnPortlet>`


.. _ManagingPermissions.SettingPortalPermissions:

Setting permissions on a site
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can set the site permissions (**Access, Edit, Move Apps** and **Move
Containers**) for a specific group via the Permissions tab if your user
account belongs to the */platform/administrators* group.

The Permissions tab can be opened in some various ways, depending on the
following approaches.

1. Click |image217| Portal Sites on the top navigation bar.

The **Manage Sites** page appears.

|image218|

2. **For new sites:**

   -  Select Add New Site to open the Create New Portal form.

   -  Click the Permissions tab.

   **For existing portals:**

   -  Select Edit Site Configuration Permissions tab:

   |image219|

.. _SettingPortalPermissions.AccessPermission:

Access permission
------------------

.. note:: To access a site, you must belong to one of the groups that have the *Access* permission to that site.

Select the Access sub-tab to set the Access permission on the site.

|image220|

-  If you want to assign the *Access* permission to users in the public
   mode (without signing in), simply select the Everyone checkbox.

-  If you do not want everyone to access the portal, first deselect the
   Everyone checkbox, and do the followings: 
   
   1. Click |image221| to open the Select Permission form. 
   
   |image222|
   
   2. Select one group in the left panel, and one membership type in the 
      right panel. 
   
   
 .. note:: In the list of membership types, if you select the asterisk (\*), all users of the selected group will have the right to access this site, regardless of their membership role. 
   
   3. Click Save to finish your settings.

-  After you have selected a membership type, the selected permission is
   displayed in the *Access* permission list.

-  You can only select one group with one membership type at each time.
   If you want to add more, click |image223| and select again.

.. _SettingPortalPermissions.EditPermission:

Edit permission
----------------

1. Select the Edit sub-tab of the Permissions tab to set the Edit
   permission on a site and do the followings:

|image224|

2. Click Select Permission to open the Permission Selector form.

|image225|

3. Select one group in the left pane and one membership type in the right
   pane.

.. note:: In the list of membership types, if you select the asterisk (\*), all users of the selected group will have the right to edit this site, regardless of their membership role.

4. Click Save to finish your settings.

.. _SettingPortalPermissions.MoveAppsPermission:

Move Apps permission
----------------------

1. Select the Move Apps sub-tab of the Permissions tab to set the **Move
   Apps permission** on a site and do the followings:

|image226|

2. Click on Add Permission to select groups and add their membership 
   types.
   You can add several memberships to a group as in :ref:`adding Access permission <SettingPortalPermissions.AccessPermission>`.

.. note:: Unless a more restrictive permission is defined for a container (See :ref:`Setting Permissions on a Container <ManagingPermissions.SettingContainerPermissions>`), users who are granted the **Move Apps** permission on a site are able to do the followings when 
          :ref:`editing the site layout <EditingLayout>`:

			-  Add new applications from the **Edit Inline Composer** to the site layout via drag and drop.

			-  Move applications contained in the site layout via drag and drop.

		  Users who are not granted the **Move Apps** permission on a site are unable to see the *Remove Portlet* icon on applications as well as drag or drop these applications on the site layout.

.. _SettingPortalPermissions.MoveContainersPermission:

Move Containers permission
----------------------------

1. Select the Move Containers sub-tab of the Permissions tab to set the
   **Move Containers permission** on a site and do the followings:

|image227|

2. Click on Add Permission to select groups and add their membership 
   types.
   You can add several memberships to a group as in :ref:`adding Access permission <SettingPortalPermissions.AccessPermission>`.

.. note:: Unless a more restrictive permission is defined for a container (See :ref:`Setting Permissions on a Container <ManagingPermissions.SettingContainerPermissions>`),
		  users who are granted the **Move Containers** permission on a site are able to do the followings when :ref:`editing the site layout <EditingLayout>`:

			-  Add new containers from the **Edit Inline Composer** to the site layout via drag and drop.

			-  Move containers contained in the site layout via drag and drop.

		  Users who are not granted the **Move Containers** permission on a site are unable to see the *Delete Container* icon on containers as well as drag or drop these containers on the site layout.

.. note:: If you do not specify which groups or users for the **Move Containers** or **Move Apps** permissions, those who are granted the :ref:`Edit permission <SettingPortalPermissions.EditPermission>` will have these permissions.

.. _ManagingPermissions.SettingPagePermissions:

Setting permissions on a page
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If your user account belongs to the */platform/administrators* group,
you are able to set permissions on a page. You first need to go to the
Permissions tab via one of two following ways:

.. _ViaEditPage:

Via Edit Page:
---------------

1. Open the page which you want to set permissions.

2. Click Edit --> Page --> Edit Layout.

|image228|

You will be directed to the Page Editor window.

3. Click View Page Properties in the Page Editor window.

4. Select the Permissions tab.

.. _AccessingPagesManagementPage:

Via Pages Management:
----------------------

1. Select |image229| --> Portal --> Pages on the top navigation bar to 
   open the Pages Management page.

2. Locate the page you want to edit using the Page Id column, then click
  |image230| corresponding to the page in the Action column. You will be
   directed to the Page Editor window.

3. Click View Page Properties in the Page Editor window.

4. Select the Permissions tab.

|image231|

.. _SettingPagePermissions.AccessPermission

Access permission
------------------

.. note:: To be able to access a page, you have to be in one of the groups that have the *Access* permission to that page.

To assign the *Access* permission on a page, simply follow steps as
stated in the :ref:`Access permission <SettingPortalPermissions.AccessPermission>`
section.

.. _SettingPagePermissions.EditPermission:

Edit permission
----------------

.. note:: Only users under the page's editors group can edit it. The Access permission can be set for several groups but the *Edit* permission only can be set for one group.

To give users the *Edit* permission, you must add them to the editors
group of that page via **Permission Setting** and follow steps as stated
in the :ref:`Edit
permission <SettingPortalPermissions.EditPermission>` section.

.. _SettingPagePermissions.MoveAppsPermission:

Move Apps permission
---------------------

To assign the *Move Apps* permission on a page, simply follow steps as
stated in :ref:`this section <SettingPortalPermissions.MoveAppsPermission>`.

.. note:: Unless a more restrictive permission is defined for a container (see :ref:`Setting Permissions on a Container <ManagingPermissions.SettingContainerPermissions>`),
          users who are granted the **Move Apps** permission on a page are able to do the followings via Edit Page Edit Layout:

			-  Add new applications from the **Page Editor** to the page layoutvia drag and drop.

			-  Move applications contained in the page layout via drag and drop.

		  Users who are not granted the **Move Apps** permission on a page are unable to see the *Delete Portlet* icon on applications as well as drop these applications on the page layout.

.. _.. _SettingPagePermissions.MoveContainersPermission:

Move Containers permission
---------------------------

To assign the *Move Containers* permission on a page, simply follow
steps as stated in :ref:`this section <SettingPortalPermissions.MoveContainersPermission>`.

.. note:: Unless a more restrictive permission is defined for a container (see :ref:`Setting Permissions on a Container <ManagingPermissions.SettingContainerPermissions>`),
		  users who are granted the **Move Containers** permission on a page are able to do the followings via Edit Page Edit Layout:

			-  Add new containers from the **Page Editor** to the page layout via drag and drop.

			-  Move containers contained in the page layout via drag and drop.

		  Users who are not granted the **Move Containers** permission on a page are unable to see the *Delete Container* icon on containers laid directly on the page layout.



.. note:: If you choose the \* membership for the selected group when setting Access, Edit, Move Apps and Move Containers permissions, all users of the group regardless of their membership role will be granted the *Access, Edit, Move Apps* and *Move Containers* permissions respectively.

.. _ManagingPermissions.SettingContainerPermissions:

Setting permissions on a container
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If your user account belongs to the */platform/administrators* group,
you can set the *Access, Move Apps* and *Move Containers* permissions on
a specific container of a page (via Edit --> Page --> Edit Layout --> 
Page Editor) or a site (via Edit --> Site --> Layout --> Edit Inline 
Composer).

1. Select the **Containers** tab, then hover your cursor over the 
   container that you want to edit and click on |image232|.

2. Select the **Permissions** tab.

|image233|

3. Click on the Add Permission button in the *Access, Move Apps* and 
   *Move Containers* tabs to add the corresponding permissions to 
   specific groups.

.. note:: 	-  Users who are not granted the *Move Apps* permission on a container do not see the *Delete Portlet* icon laid directly on applications contained in the container in edit mode.

			-  Users who are not granted the *Move Containers* permission on a container do not see the *Delete Container* icon in edit mode.

			-  Users who are granted the *Move Apps* or *Move Containers* permissions on a container can add new applications or containers from the composer to this container via drag and drop. Besides, they can move the applications or containers contained in this container via drag and drop.

.. _ManagingPermissions.SettingAccessPermissionOnCategory:

Setting Access permission on a category
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _AccessingManageApplicationsPage:

Setting the *Access* permission on categories allows these categories to
be listed when a page is edited to add portlets or widgets.

1. Click |image234| Applications on the top navigation bar to open the
   **Manage Applications** page.

|image235|

2. Select one category from the list of available categories in the left
   panel, then click |image236|.

3. Select the Permission Setting tab.

4. Set the *Access* permission on a category that is similar to the 
   :ref:`Access permission <SettingPortalPermissions.AccessPermission>`
   section.


.. note:: If you set the \* membership for a group, all users of the group will have the right to view this category when :ref:`editing layout <EditingLayout>`.

.. _ManagingPermissions.SettingAccessPermissionOnPortlet:

Setting Access permission on a portlet
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. :ref:`Go to the Manage Applications page <AccessingManageApplicationsPage>`.

2. Select the category containing the portlet you want to set the 
   *Access* permission, then click the relevant portlet under your 
   selected category.

   The selected portlet will be highlighted in grey in the left panel 
   with its detailed information in the right pane.

3. Follow steps stated in the :ref:`Access permission <SettingPortalPermissions.AccessPermission>`
   section to assign the Access permission on your selected portlet in 
   the Default Permission Settings form.

.. note:: If you set the \* membership for a group, all users of the group will have the right to view this application when :ref:`editing layout <EditingLayout>`.


