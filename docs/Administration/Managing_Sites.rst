.. _ManagingSites:

==============
Managing sites
==============

Managing sites include the following actions:

-  `Creating a new
   site <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.CreatingNewSite>`__

-  `Editing a
   site <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.EditingSite>`__

-  `Selecting the site's
   skin <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.SelectSkin>`__

-  `Deleting a
   site <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.DeletingSite>`__

.. _CreatingNewSite:

Creating a new site
-------------------

    **Note**

    You can perform this action only when you are a member of the
    */platform/administrators* group.

Click |image0| Portal Sites on the top navigation bar, then click Add
New Site in the Manage Sites page;

Or, click EditSiteAdd Site.

By default, the window to create a new site, which contains the Portal
Settings tab, will open.

Fill in the Portal Name field. The field is required, unique and must
start with a letter. Only alphabetical, numerical, dash and underscore
characters are allowed for this field with the length from 3 to 30
characters.

Select the default display language for the site from the Locale field.

Click the Properties tab to set the properties of a site.

|image1|

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

Click the Permissions tab to set permissions on the site.

The list of *Access* permissions for the portal is empty by default. You
have to select at least one or tick the Everyone checkbox to assign the
*Access* permission to everyone.

    **Note**

    For more details on how to grant permissions on the site, see
    `Setting permissions on a
    site <#PLFUserGuide.AdministeringeXoPlatform.ManagingPermissions.SettingPortalPermissions>`__.

Click the Portal Templates tab to select the template for your site.

Click Save to accept creating your new site.

    **Note**

    After creating a new site, you can access it via the URL format:
    ``http://{domain-name}/portal/[name-site]``. For example, accessing
    the ACME site: ``http://mycompany.com:8080/portal/acme``.

Editing a site
--------------

    **Note**

    The function allows you to edit layouts, navigations and properties
    of a site. To do this, you must have the *Edit* permission on sites
    by contacting your administrator.

**When you have the *Edit* permission, access the relevant form that
allows you to do actions related to editing a portal.**

`Access the Manage Sites panel <#OpeningSitesManagementPage>`__.

Specify your desired site, and do the following actions:

-  `Editing the site's
   layout <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.EditingSite.EditingLayout>`__
   by clicking Edit Layout.

-  `Changing the site's
   navigation <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.EditingSite.EditingNavigation>`__
   by clicking Edit Navigation.

-  `Editing the site's
   configurations <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.EditingSite.EditingConfigurations>`__
   by clicking Edit Site Configuration.

.. _EditingLayout:

**Editing layout**

Click Edit Layout corresponding to your desired site on the Manage Sites
panel;

Or, click EditSiteLayout on the top navigation bar.

The Edit Layout form will display.

|image2|

To add a new application/container to the site, drag and drop it from
the Edit Inline Composer window to the main site body.

To rearrange elements in the site body, drag and drop them into your
desired positions.

To edit or remove any element, hover your cursor over it, then select
|image3| or |image4| respectively.

    **Note**

    For more details on how to edit elements, see the `Editing a
    specific
    portlet <#PLFUserGuide.AdministeringeXoPlatform.ManagingApplications.ManagingPortletsAndGadgets.EditingSpecificPortlet>`__
    section.

**Editing navigation**

Click Edit Navigation corresponding to your desired site on Manage Sites
form;

Or, click EditSiteNavigation on the top navigation bar.

The Navigation Management form appears.

|image5|

    **Note**

    For more information about actions, which can be done in the
    Navigation Management form, see the `Managing
    navigations <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations>`__
    section.

**Editing configurations**

The configurations of a site include settings, properties and
permissions that can be set by clicking Edit Site Configuration in the
Manage Sites panel.

The Edit window with the **Portal Settings** tab appears.

|image6|

In this window, you can make changes on fields in the various tabs,
except the Portal Name field in the Portal Settings tab.

    **Note**

    For more details on these fields, refer to the `Creating a new
    site <#PLFUserGuide.AdministeringeXoPlatform.ManagingSites.CreatingNewSite>`__
    section.

Selecting the site's skin
-------------------------

    **Warning**

    This section is written while the enterprise skin add-on is still in
    an unstable version. Some datas and information may change later.

With PRODUCT PLF\_VERSION a new ready skin is available as an add-on for
enterprise packages.

You can install it by using this command in a PLF\_VERSION PRODUCT
package versions:

::

    addon install exo-enterprise-skin

Having the add-on installed in your package and being an administrator,
you can apply it easily by following these steps:

Click |image7| Portal Sites on the top navigation bar.

Click on the button Edit Site Configuration, a pop up appears to
configure the site.

Select the skin: either the default one or the Enterprise one

|image8|

and then click on save.

Going back to the site's homepage, the selected skin is applied:

|image9|

In the previous screenshot, the enterprise skin is selected.

Deleting a site
---------------

    **Note**

    To delete a site, you must be in the group that has the **Edit
    Permission** on that portal.

`Access the Manage Sites panel <#OpeningSitesManagementPage>`__.

Click |image10| corresponding to the site you want to delete.

Click **OK** in the confirmation message.

    **Note**

    You cannot delete the Intranet site.

.. |image0| image:: images/common/administration_navigation.png
.. |image1| image:: images/gatein/properties_tab.png
.. |image2| image:: images/gatein/edit_layout_form.png
.. |image3| image:: images/common/edit_portlet_icon.png
.. |image4| image:: images/common/delete_icon.png
.. |image5| image:: images/gatein/navigation_management_form.png
.. |image6| image:: images/gatein/portal_settings_tab.png
.. |image7| image:: images/common/administration_navigation.png
.. |image8| image:: images/platform/select-skin.png
.. |image9| image:: images/platform/skin-enterprise.png
.. |image10| image:: images/common/delete_icon.png
