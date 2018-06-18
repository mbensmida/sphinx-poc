.. _Manage-Space-Settings:

=======================
Managing space settings
=======================

If you are the creator or have the **Manage** permission on a space, you
can manage its initial settings in Space Settings, including:

-  :ref:`Space information/visibility <ChangingInfoVisibility>`

-  :ref:`Space members <ManagingMembers>`

-  :ref:`Space applications <ManagingSpaceApplication>`

-  :ref:`Space navigation bar <Manage-space-navbar>`

To edit a space, access the Space Settings page first by following one
of 2 ways:

-  **The first way**

   -  :ref:`Access your desired space <Access-Space>`, then select Space Settings on the space navigation bar.

      |image33|

-  **The second way**

   -  `Go to the Spaces  page <note-access-spaces-page>`, then select the All Spaces or My Spaces tab.

   -  Click Edit under the space name which you want to edit.

      |image34|

.. _ChangingInfoVisibility:

Changing space information/visibility
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Changing space information
---------------------------

This function allows you to edit the basic information of a space.

1. Select the Settings tab in the **Space Settings** page.

|image35|

2. Change information in the Name, Description fields and the space avatar.

-  To change the space avatar, click Change Picture below the avatar to
   open the Upload an Image form. See :ref:`Uploading your avatar <Change-your-avatar>` for more details.

3. Click Save to accept your changes.

Changing visibility
--------------------

1. Select the Access & Edit tab in the **Space Settings** page.

2. Change values of Visibility and Registration if you want. For more details, see :ref:`here <access-level-step>`.

3. Click Save to accept your changes.

.. _ManagingMembers:

Managing members
~~~~~~~~~~~~~~~~~

Select the Members tab in **Space Settings** page.

|image58|

Here, you can do many actions on members as follows:

Inviting new members
---------------------

You can invite other users to join your spaces as follows:

-  **Inviting users**

   -  **The first way**

      If you know the username of a person, simply enter his/her
      username in the textbox, then click Invite.

      To invite multiple people, use commas to separate your multiple
      entered usernames.

   -  **The second way**

      1. Click |image36| to open the Select Users form.

      |image37|

      2. Select your desired users by ticking their corresponding checkboxes, and click Add.

      You can also search for your desired members in eXo Platform, do as follows:

      -  **i.** Enter a search term into the Search box.

      -  **ii.** Select a criterion you want to find in the combo box next to the Search box.

      -  **iii.** Click |image38| or press **Enter** to perform searching.

      3. Click Invite to invite your selected users.

   -  **The third way**

      |image39|

      1. |image40| Go to Members application of the space.

      2. |image41| Enter the username of the person you wish to invite to
      the space. You can just type in the first letters and a list of
      suggestions should appear. This list contains persons having those
      letters in their username, First name or Last name. Press Enter on
      keyboard to confirm the user selection.

      If you entered a wrong username (i.e it doesn't exist), it gets underlined in red:
      
      |image42|

      3. |image43| Choose one or more persons to invite from the list. You
      can remove some persons by just clicking on |image10| in front of
      the displayed named.

      4. |image44| Click on Invite to send invitations to the chosen
      persons.

      If you press on Enter to confirm a wrong username and then click
      on Invite, an error pop up appears indicating that the selected
      username is not valid.
      
      |image60|

   -  **Inviting users from a group**

      1. Click |image45| to open the Select a Group form.

      2. Select a group on the left pane, then select its sub-group on the right pane.

      3. Click Invite to invite your selected group.

After that, you will see the list of invited users. The invitees will
see your invitations in the :ref:`Invitations application <InvitationsApp>` at the right panel of their homepage.

Revoking your invitations
---------------------------

If the invited users have not accepted your requests yet, you can revoke
your invitations by clicking |image46| corresponding to the users' name.
The users will be removed from the Invited list.

Validating/Declining request
-----------------------------

As a manager or creator of a space, you can validate other users'
requests for joining your space.

-  To accept a user's request for joining your space, click |image47| in
   the Action column.

-  To decline a user's request for joining your space, click |image48|
   in the Action column.

Promoting/Demoting a member
----------------------------

-  To promote a member to the manager position, click |image49| in the
   Manager column. The user will be automatically promoted as a manager
   in the current space.

-  To demote a member, click |image50|.

.. note:: Be careful not to remove the rights for yourself; otherwise, you
			will not be able to change your space's settings anymore. Besides,
			there should be at least one manager in a space, so the last manager
			of the space is not permitted to be demoted.

Removing a member
------------------

Click |image51| corresponding to the member you want to delete in the
**Members** list. In case this member is the only manager of the space,
there will be a warning like this:

|image52|

That is, you should promote another member to the manager position
before you can delete that member.

 .. note::You cannot invite, promote, demote or remove users who are `suspended by an administrator <#PLFUserGuide.AdministeringeXoPlatform.ManagingYourOrganization.ManagingUsers.DisablingUser>`__.
    
.. _ManagingSpaceApplication:    

Managing space applications
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Select the Applications tab to go the **Applications** page which allows
you to manage space applications.

Here, you can:

Adding a new space application
-------------------------------

1. Click Add Application to open the Space Application Installer form.

|image53|

2. Click a category on the left panel to show its applications on the right
panel, then select the application you want to add by clicking Add
corresponding to it.

If there is no available application, ask your system administrator to
gain the access right.

Deleting an application
--------------------------

To remove an application, click |image54| corresponding to the
application name.

 .. note::You cannot delete the Space Settings application because it is configured as a mandatory space application.

.. _Manage-space-navbar:

Managing space navigation bar
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Each space is featured with some "pages" on the space navigation bar.
These pages may contain applications or any content. By clicking on each
page, you will be redirected to it.

|image55|

Also, you can easily manage these pages on the space navigation bar
through actions on the relevant navigation nodes. To do so, in Space
Settings, select the Navigations bar, then right-click the relevant
navigation node. See `Managing navigation
nodes <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations>`__
for more details.

|image56|

Creating a space page
-----------------------

To create a page that is accessible on the space navigation bar, simply
add a navigation node that links to your desired page in the Page
Selector tab. See `Adding a new
node <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations.AddingNewNode>`__
for more details.

|image57|

Also, you can create a space page using:

-  `Page Creation
   Wizard <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.AddingNewPage.PageCreationWizard>`__;
   Or

-  `Pages
   Management <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.AddingNewPage.PagesManagement>`__.
   In this case, Owner Type should be **group**, and Owner Id should be
   **/spaces/[space\_node\_name]**. For example, if you want to add a
   page to the space named PLF team, the Owner Id should be
   **/spaces/plf\_team**. Remember that in this way, you only create the
   space page that is still not accessible. To make this page
   accessible, create a node that links to this page (in the Page
   Selector tab).

Editing a space page
---------------------

To edit this space page, simply right-click the navigation node
containing the page and select Edit Node's Page from the context menu.
The **Edit Page** window will be displayed in the Page Properties view.
See `Editing a
page <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.EditingPage>`__
for more details.

Removing a space page
----------------------

If you right-click the node containing the page and select Delete Node
from the context menu, only the navigation node linking to the page will
be removed from the space navigation bar, but its page still exists. To
actually delete this page, see `Deleting a
page <#PLFUserGuide.AdministeringeXoPlatform.ManagingPages.DeletingPage>`__.


