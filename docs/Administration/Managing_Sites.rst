.. _ManagingSites:

==============
Managing sites
==============

Managing sites include the following actions:

-  :ref:`Creating a newsite <CreatingNewSite>`

-  :ref:`Editing asite <ManagingSites.EditingSite>`

-  :ref:`Selecting the site's skin <ManagingSites.SelectSkin>`

-  :ref:`Deleting a site <ManagingSites.DeletingSite>`

.. _CreatingNewSite:

Creating a new site
~~~~~~~~~~~~~~~~~~~~

.. note:: You can perform this action only when you are a member of the ``/platform/administrators`` group.

1. Click |image181| Portal Sites on the top navigation bar, then click 
   Add New Site in the Manage Sites page;

   Or, click EditSiteAdd Site.

By default, the window to create a new site, which contains the Portal
Settings tab, will open.

|image182|

2. Fill in the Portal Name field. The field is required, unique and must
   start with a letter. Only alphabetical, numerical, dash and 
   underscore characters are allowed for this field with the length from
   3 to 30 characters.

3. Select the default display language for the site from the Locale 
   field.

4. Click the Properties tab to set the properties of a site.

|image183|

**Details:**

+--------------------+--------------------------------------------------------+
| Field              | Description                                            |
+====================+========================================================+
| Keep session alive | Keeps the working session for a long time to avoid the |
|                    | time-out. There are 3 options:                         |
|                    | Never: The session will time out if the logged-in user |
|                    | does not do any action after a given period. In this   |
|                    | case, there will be a message which asks the user to   |
|                    | log in again.                                          |
|                    |                                                        |
|                    | On Demand: The session will time out to the            |
|                    | application's requirement. If there is no request from |
|                    | the application, the session will time out after the   |
|                    | given period that is similar to that of **Never.**     |
|                    |                                                        |
|                    | Always: The session will never time out even if the    |
|                    | logged-in user does not do any action after a long     |
|                    | time.                                                  |
+--------------------+--------------------------------------------------------+
| Show info bar by   | Ticks the checkbox to show the info bar of the portlet |
| default            | by default when the portlet is used in a page of the   |
|                    | site.                                                  |
|                    | The "Show info bar by default" option only takes       |
|                    | effect on new portlets as from the time you select the |
|                    | checkbox rather than all portlets of the site. In      |
|                    | particular, after creating your new site with the      |
|                    | "Show info bar by default" option checked, newly       |
|                    | created portlets of the site will be displayed with    |
|                    | the info bar by default. However, if you deselect this |
|                    | option when editing the site's configuration, the      |
|                    | former portlets with the shown info bar are remained;  |
|                    | meanwhile new portlets, which are created after this   |
|                    | option is deselected, will be shown without the info   |
|                    | bar.                                                   |
+--------------------+--------------------------------------------------------+

5. Click the Permissions tab to set permissions on the site.

The list of *Access* permissions for the portal is empty by default. You
have to select at least one or tick the Everyone checkbox to assign the
*Access* permission to everyone.

.. note:: For more details on how to grant permissions on the site, see :ref:`Setting permissions on a site <ManagingPermissions.SettingPortalPermissions>`.

6. Click the Portal Templates tab to select the template for your site.

7. Click Save to accept creating your new site.

.. note:: After creating a new site, you can access it via the URL format: ``http://{domain-name}/portal/[name-site]``. For example, accessing the Agital site: ``http://mycompany.com:8080/portal/Agital``.

.. _ManagingSites.EditingSite:

Editing a site
~~~~~~~~~~~~~~~~

.. note:: The function allows you to edit layouts, navigations and properties of a site. To do this, you must have the *Edit* permission on sites by contacting your administrator.

**When you have the *Edit* permission, access the relevant form that
allows you to do actions related to editing a portal.**

1. :ref:`Access the Manage Sites panel <CreatingNewSite>`.

2. Specify your desired site, and do the following actions:

-  :ref:`Editing the site's layout <EditingLayout>` by clicking Edit 
    Layout.

-  :ref:`Changing the site's navigation <EditingNavigation>` by clicking
    Edit Navigation.

-  :ref:`Editing the site's configurations <EditingConfigurations>` by 
   clicking Edit Site Configuration.

.. _EditingLayout:

Editing layout
--------------

1. Click Edit Layout corresponding to your desired site on the Manage 
   Sites panel;

   Or, click EditSiteLayout on the top navigation bar.

   The Edit Layout form will display.

|image184|

2. To add a new application/container to the site, drag and drop it from
   the Edit Inline Composer window to the main site body.

   To rearrange elements in the site body, drag and drop them into your
   desired positions.

   To edit or remove any element, hover your cursor over it, then select
   |image185| or |image186| respectively.

.. note:: For more details on how to edit elements, see the :ref:`Editing a specific portlet <EditingSpecificPortlet>` section.

.. _EditingNavigation:

Editing navigation
-------------------

Click Edit Navigation corresponding to your desired site on Manage Sites
form;

Or, click EditSiteNavigation on the top navigation bar.

The Navigation Management form appears.

|image187|

.. note:: For more information about actions, which can be done in the Navigation Management form, see the `Managing navigations <ManagingNavigations>` section.

.. _EditingConfigurations:

Editing configurations
------------------------

The configurations of a site include settings, properties and
permissions that can be set by clicking Edit Site Configuration in the
Manage Sites panel.

The Edit window with the **Portal Settings** tab appears.

|image188|

In this window, you can make changes on fields in the various tabs,
except the Portal Name field in the Portal Settings tab.

.. note:: For more details on these fields, refer to the `Creating a new site <CreatingNewSite>` section.

.. _ManagingSites.SelectSkin:

Selecting the site's skin
~~~~~~~~~~~~~~~~~~~~~~~~~~~


With eXo Platform 5.0 a new ready skin is available as an add-on for
enterprise packages.

You can install it by using this command in a 5.0 eXo Platform
package versions: ::

    addon install exo-enterprise-skin

Having the add-on installed in your package and being an administrator,
you can apply it easily by following these steps:

1. Click |image189| Portal Sites on the top navigation bar.

2. Click on the button Edit Site Configuration, a pop up appears to
   configure the site.

3. Select the skin: either the default one or the Enterprise one

|image190|

and then click on save button.

Going back to the site's homepage, the selected skin is applied:

|image191|

.. _ManagingSites.DeletingSite:

Deleting a site
~~~~~~~~~~~~~~~~

.. note:: To delete a site, you must be in the group that has the **Edit Permission** on that portal.

1. `Access the Manage Sites panel <CreatingNewSite>`.

2. Click |image192| corresponding to the site you want to delete.

3. Click **OK** in the confirmation message.

.. note:: You cannot delete the Intranet site.


