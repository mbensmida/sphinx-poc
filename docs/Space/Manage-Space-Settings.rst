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

      |image0|

-  **The second way**

   -  `Go to the Spaces  page <note-access-spaces-page>`, then select the All Spaces or My Spaces tab.

   -  Click Edit under the space name which you want to edit.

      |image1|

.. _ChangingInfoVisibility:

Changing space information/visibility
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Changing space information
---------------------------

This function allows you to edit the basic information of a space.

1. Select the Settings tab in the **Space Settings** page.

|image2|

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

|image25|

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

      1. Click |image3| to open the Select Users form.

      |image4|

      2. Select your desired users by ticking their corresponding checkboxes, and click Add.

      You can also search for your desired members in eXo Platform, do as follows:

      -  **i.** Enter a search term into the Search box.

      -  **ii.** Select a criterion you want to find in the combo box next to the Search box.

      -  **iii.** Click |image5| or press **Enter** to perform searching.

      3. Click Invite to invite your selected users.

   -  **The third way**

      |image6|

      1. |image7| Go to Members application of the space.

      2. |image8| Enter the username of the person you wish to invite to
      the space. You can just type in the first letters and a list of
      suggestions should appear. This list contains persons having those
      letters in their username, First name or Last name. Press Enter on
      keyboard to confirm the user selection.

      If you entered a wrong username (i.e it doesn't exist), it gets underlined in red:
      
      |image26|

      3. |image9| Choose one or more persons to invite from the list. You
      can remove some persons by just clicking on |image10| in front of
      the displayed named.

      4. |image11| Click on Invite to send invitations to the chosen
      persons.

      If you press on Enter to confirm a wrong username and then click
      on Invite, an error pop up appears indicating that the selected
      username is not valid.
      
      |image27|

   -  **Inviting users from a group**

      1. Click |image12| to open the Select a Group form.

      2. Select a group on the left pane, then select its sub-group on the right pane.

      3. Click Invite to invite your selected group.

After that, you will see the list of invited users. The invitees will
see your invitations in the :ref:`Invitations application <InvitationsApp>` at the right panel of their homepage.

Revoking your invitations
---------------------------

If the invited users have not accepted your requests yet, you can revoke
your invitations by clicking |image13| corresponding to the users' name.
The users will be removed from the Invited list.

Validating/Declining request
-----------------------------

As a manager or creator of a space, you can validate other users'
requests for joining your space.

-  To accept a user's request for joining your space, click |image14| in
   the Action column.

-  To decline a user's request for joining your space, click |image15|
   in the Action column.

Promoting/Demoting a member
----------------------------

-  To promote a member to the manager position, click |image16| in the
   Manager column. The user will be automatically promoted as a manager
   in the current space.

-  To demote a member, click |image17|.

.. note:: Be careful not to remove the rights for yourself; otherwise, you
			will not be able to change your space's settings anymore. Besides,
			there should be at least one manager in a space, so the last manager
			of the space is not permitted to be demoted.

Removing a member
------------------

Click |image18| corresponding to the member you want to delete in the
**Members** list. In case this member is the only manager of the space,
there will be a warning like this:

|image19|

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

|image20|

2. Click a category on the left panel to show its applications on the right
panel, then select the application you want to add by clicking Add
corresponding to it.

If there is no available application, ask your system administrator to
gain the access right.

Deleting an application
--------------------------

To remove an application, click |image21| corresponding to the
application name.

 .. note::You cannot delete the Space Settings application because it is configured as a mandatory space application.

.. _Manage-space-navbar:

Managing space navigation bar
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Each space is featured with some "pages" on the space navigation bar.
These pages may contain applications or any content. By clicking on each
page, you will be redirected to it.

|image22|

Also, you can easily manage these pages on the space navigation bar
through actions on the relevant navigation nodes. To do so, in Space
Settings, select the Navigations bar, then right-click the relevant
navigation node. See `Managing navigation
nodes <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations>`__
for more details.

|image23|

Creating a space page
-----------------------

To create a page that is accessible on the space navigation bar, simply
add a navigation node that links to your desired page in the Page
Selector tab. See `Adding a new
node <#PLFUserGuide.AdministeringeXoPlatform.ManagingNavigations.AddingNewNode>`__
for more details.

|image24|

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

.. |image0| image:: images/social/space_settings_on_navigation_bar.png
.. |image1| image:: images/social/edit_space.png
.. |image2| image:: images/social/space_configuration_settings_tab.png
.. |image3| image:: images/common/select_users_icon.png
.. |image4| image:: images/platform/select_users_form.png
.. |image5| image:: images/common/search_icon.png
.. |image6| image:: images/social/invite_members_app.png
.. |image7| image:: images/common/1.png
.. |image8| image:: images/common/2.png
.. |image9| image:: images/common/3.png
.. |image10| image:: images/common/remove_icon.png
.. |image11| image:: images/common/4.png
.. |image12| image:: images/common/select_everyone_icon.png
.. |image13| image:: images/common/delete_icon.png
.. |image14| image:: images/social/validate_icon.png
.. |image15| image:: images/social/decline_icon.png
.. |image16| image:: images/social/promote_space_manager_button.png
.. |image17| image:: images/social/demote_space_manager_button.png
.. |image18| image:: images/common/delete_icon.png
.. |image19| image:: images/social/remove_space_manager_warning.png
.. |image20| image:: images/social/space_application_installer_form.png
.. |image21| image:: images/common/remove_icon.png
.. |image22| image:: images/social/space_navigation_bar.png
.. |image23| image:: images/social/space_configuration_navigations_tab.png
.. |image24| image:: images/social/space_page_creation.png
.. |image25| image:: images/social/member_tab_space.png
.. |image26| image:: images/social/wrong_name.png
.. |image27| image:: images/social/wrong_username-popup.png
