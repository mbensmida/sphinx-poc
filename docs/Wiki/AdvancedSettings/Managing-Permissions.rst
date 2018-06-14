.. _Managing-Permissions:

====================
Managing permissions
====================

**Wiki** lets you decide the restrictions to apply on a wiki or a page
and to specific users, groups or memberships. So, there are two levels
of permissions in **Wiki**:

-  `Page
   Permissions <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPermissions.PagePermissions>`__

-  `Wiki
   Permissions <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPermissions.WikiPermissions>`__

**Page permissions**

The **Page Permissions** allows you to set the View and Edit permissions
for a specific Wiki page.

Open a Wiki page that you want to set the permissions.

Click More and select Page Permissions from the drop-down menu.

The Page Permissions form appears.

Pages are viewable/editable according to the Wiki permission. On each
page, a user with the **Admin Pages** permission will be able to
override the view and edit permissions on a specific page.

A **Page Permissions** action appears in the page action menu when the
user has the **Admin Pages** permission.

You can add and delete the **View Pages Permission** or the **Edit Pages
Permission** for the page. Do the same as `Adding Wiki
permissions <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPermissions.AddingWikiPermissions>`__
and `Deleting Wiki
permissions <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPermissions.DeletingWikiPermissions>`__.

    **Note**

    -  When ticking any permissions above, if you select a group with
       the \* membership, this permission will be grated to all users of
       that group, regardless of their membership role.

    -  All **Page Permissions** are restricted to a specific page,
       therefore any changes made on the page's permissions will not
       affect both its children and parents.

**Wiki permissions**

Wiki permissions determine which actions a user can perform. A
permission can be assigned to any users, groups or memberships.

To change the Wiki permissions, click Browse and select Wiki Settings
from the drop-down list. Select the Permission tab in the Wiki Settings
page.

There are some permissions on a Wiki as follows:

+----------------------+-----------------------------------------------------+
| Permission           | Description                                         |
+======================+=====================================================+
| View Pages           | Specifies who can view and watch pages of this      |
|                      | Wiki, its attachments and history.                  |
+----------------------+-----------------------------------------------------+
| Edit Pages           | Specifies who can edit pages of this Wiki.          |
+----------------------+-----------------------------------------------------+
| Admin Pages          | Specifies who have the administration rights on     |
|                      | pages of this Wiki.                                 |
+----------------------+-----------------------------------------------------+
| Admin Wiki           | Specifies who can administrate the Wiki permissions |
|                      | and settings.                                       |
+----------------------+-----------------------------------------------------+

In the Permission tab, you can:

-  `Adding Wiki permissions of the users, groups and
   memberships <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPermissions.AddingWikiPermissions>`__.

-  `Deleting Wiki permissions of the users, groups and
   memberships <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPermissions.DeletingWikiPermissions>`__.

**Adding Wiki permissions**

You can add permissions for individual users, groups of users or
memberships.

Click |image0| to assign permissions to a user, a membership or a group
respectively.

The form to select the user, the membership and the group appears.

Select a user, a membership or a group, then click Add.

    **Note**

    When ticking any permissions above, if you select a group with the
    \* membership, this permission will be granted to all users of that
    group, regardless of their membership role.

Click Add to add the selectors to the User or Group column in the
Permission form.

Tick the checkboxes corresponding to each permission you want to assign
to the selectors.

Click Save to commit.

    **Note**

    View and Edit permissions are applied by default to any Wiki pages
    unless specific page permissions are set. The super user has all
    permissions implicitly.

**Deleting Wiki permissions**

To delete the permissions of a user, group or membership, just click
|image1| corresponding to a user or group or membership in the
Permissions form.

.. |image0| image:: images/common/select_permission_icon.png
.. |image1| image:: images/common/delete_icon.png
