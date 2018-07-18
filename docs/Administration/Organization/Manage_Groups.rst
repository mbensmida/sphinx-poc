.. _ManagingYourOrganization.ManagingGroups:

Managing groups
~~~~~~~~~~~~~~~~

Select the Groups tab which is used to add, edit or delete a group. You
can also add or delete a user to/from a group and edit the user
membership in the group.

|image166|

By default, all existing groups will be displayed on the left panel. The
right panel shows information of the selected group and of its members
with the Add Member form.

.. _AddNewGroup:

Adding a new group
------------------

1. Select the path to create a new group by clicking the group from the
   left panel or by clicking |image167| if you want to create a group at a
   higher level. The selected path is displayed in the breadcrumb bar.

2. Click |image168| in the left panel.


The Add New Group form will be displayed in the right panel.

|image169|

**Details:**

+--------------------+--------------------------------------------------------+
| Field              | Description                                            |
+====================+========================================================+
| Group Name         | Name of the group that is required and unique within   |
|                    | the portal with its length from 3 to 30 characters.    |
|                    | Only letters, numbers, dash and underscore characters  |
|                    | are allowed for the Group Name field.                  |
+--------------------+--------------------------------------------------------+
| Label              | The display name of the group with any length from 3   |
|                    | to 50 characters.                                      |
+--------------------+--------------------------------------------------------+
| Description        | Description of the group with any length from 0 to 255 |
|                    | characters.                                            |
+--------------------+--------------------------------------------------------+

3. Fill in the required fields. Once being saved, the Group Name cannot 
   be edited.

4. Click Save to accept creating the new group.

.. note:: The creator will automatically become the manager of that group. The creator's username will be added to the created group with the "manager" membership.

.. _EditDeleteGroup:

Editing/Deleting a group
------------------------

Editing a group
````````````````

1. Select the group you want to edit in the left panel.

2. Click |image170| in the left panel to show the Edit Current Group 
   form of the selected group.

|image171|

3. Make changes on the fields, except Group Name.

4. Click Save to commit your changes.

Deleting a group
`````````````````

Simply select the group you want to delete in the left panel. Next,
click |image172| and select **OK** in the confirmation message.

.. note:: After being deleted, all information related to that group, such as users and navigation, is also deleted. You cannot delete the mandatory groups, including *Platform, Platform/Administration, Platform/Guests, Platform/Users.*

.. _AddingUserToGroup:

Adding a user to a group
------------------------

1. Select the group to which you want to add a new user in the left 
   panel. The Group Info panel with the Add member form will be opened.

|image173|

2. Enter the exact Username of the user that you want to add to the
   selected group (you can add many usernames separated by commas); or
   click |image174| to select your desired users from the Select User 
   form.

3. Select the membership for the users from the Membership drop-down 
   menu. You can click |image175| to update the memberships list in case 
   of any changes. See more information of membership types :ref:`here <ManagingYourOrganization.ManagingMemberships>`.

.. note:: -  Under the Spaces group, if you select the \* membership for a user in any space group, the user will have the right to access the corresponding :ref:`Space Settings <Manage-Space-Settings>`.
		     Besides, this user will be listed as a manager in the :ref:`Members <ManagingMembers>` tab as well as an administrator in the :ref:`member list <MembersListOfSpace>` of the space.

4. Click Save to accept adding the selected users to the specific group
   with the specified membership type.

.. note:: By default, the "manager" membership has the highest right in a group. A user can have several membership types in a group. 
          To do that, you have to use the Add Member form for each membership type. The user's membership information is hereafter updated. 
          You can check it by opening the Users form and editing the user you just added.

.. _EditUserMembershipInGroup:

Editing a user membership in a group
------------------------------------

1. Click |image176| in the Action column in the Group Info form. 
   The Edit Membership form will open.

   |image177|

2. Change the membership of the selected user by selecting another value
   from the Membership drop-down menu.

3. Click Save to complete your changes.


