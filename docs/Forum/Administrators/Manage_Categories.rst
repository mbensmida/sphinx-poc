.. _Administrator.ManagingCategories:

Managing categories
~~~~~~~~~~~~~~~~~~~~

Only administrators can do categories-related management tasks. To
manage forums better, the administrators usually build a good forum
structure using categories. So, a category is a set of forums containing
all discussions about the same subject. See the following diagram to
learn about the typical structure of a forum.

|image139|

.. _Add-category:

Adding a new category
---------------------

Only when you are assigned as an **administrator**, you can do this
function. Normally, one category is created as public and it allows
everyone to access without any restrictions. Meanwhile, one 
:ref:`restricted category <AddingRestrictedCategories>`
only allows specific users/groups/memberships to access. Also, you can
assign moderators to your category and specify a set of permissions for
members in the category.

1. Click |image140| on the Forums Administration bar. 
The Category form will be displayed.

2. Enter the category title into the Title field which is required. Its
length must be between 1 and 100 characters (Special characters and
spaces are accepted).

In the Category tab, optionally you can also:

-  Enter the order of category in the numeric format into the Order
   field.

-  Give a brief description for your category into the Description
   field.
   
.. _AddingRestrictedCategories:

-  Create a category restricted which allows specific users/roles/groups
   only to have access via one of the following ways:

   -  **The first way**

      Enter names of users/groups/memberships into the Restricted
      Audience textbox. The different values are separated by commas.

   -  **The second way**

      Use selectors next to the Restricted Audience textbox.

      **Selecting a specific user**: Click |image141| to open the Select
      User form, then check your desired users and click Add to accept
      your selection.

      **Selecting all users with a specific role in a group**:

      **i.** Click |image142| to open the Select Role form.

      **ii.** Select a group on the left panel and a specific role on
      the right panel.

 ..note:: If you select \* on the right panel, it means that all members of the group are selected.

      **Selecting a group of users**:

      **i.** Click |image143| to open the Select Group form.

      **ii.** Select a group on the left panel and its sub-group on the
      right panel.

      If the group on the left panel does not have any sub-groups and
      you want to select it, click the Select this Group link.

.. note:: The Restricted Audience field is empty, it means any users can access the category.
       
.. _SettingCategoryPermission:       

3. Optionally, set category permissions.

By default, all users have rights to start topics, add and view posts in
forums of a category. However, you can set these permissions and assign
the **moderator** role to specific users/roles/groups.

-  Select the Permissions tab.

   |image144|

-  Do the same as setting the :ref:`Restricted audiences <AddingRestrictedCategories>`
   of a category.

-  Click Add to add selected users/roles/groups to the permissions list.

-  Tick the checkboxes corresponding to the rights you want to grant to
   the users/roles/groups.

To remove permissions of the users/roles/groups from the list, click the
corresponding |image145| icon.

.. note:: - When granting the **moderator** to a specific user/role/group, to allow other users to start topics, add/view posts, you should uncheck these rights of the moderator. The moderator of a category can manage all forums in the category.

          -  When granting any permissions above, if you set the \* membership for the selected group, this permission will be granted to all users of that group, regardless of their membership role.

4. Click Save to finish.

.. note:: In eXo Platform, each space forum belongs to a category named "spaces" and there is only one forum per space. You cannot therefore create new categories within each space forum.

.. _Edit category:

Editing a category
------------------

1. Select a category to edit from the **Forums** homepage, then click
|image146| on the Action bar when you are in the categories list.

2. Click Edit from the drop-down menu.

3. Make changes on the category properties.

4. Click Save to save your changes.

.. _Delete-category:

Deleting a category
-------------------

1. Select a category that you want to delete from the **Forums** 
homepage, then click |image147| on the Action bar.

2. Click Delete from the drop-down menu.

3. Click **OK** in the confirmation message to accept your deletion.

.. note:: When a category is removed, all its forums are also removed.


