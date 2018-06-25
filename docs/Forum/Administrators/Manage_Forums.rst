Managing forums
===============

Forums management can be performed through the following actions:

.. _Adding-forum:

**Adding a new forum**

Open the Forum form by following either of two ways below:

**The first way**

-  Click |image0| on the Forums Administration bar.

**The second way**

-  Go into the category to which you want to add a new forum.

-  Click |image1| on the Forums Administration bar;

   Or, click |image2| on the Action bar and select Add Forum.

   |image3|

The Forum form will be displayed:

|image4|

Enter the forum title which is required. Its length must be less than 50
characters, including spaces.

Optionally, you can:

-  Select the category to which you want to add your forum by clicking
   Add Forum to Category and selecting one from the categories list.

       **Note**

       If you follow `this way <#ManageCategorymenu>`__, you cannot
       change the pre-selected category.

-  Enter the order for your forum that must be in the positive integer
   format.

-  Select the forum state.

-  Select the forum status.

-  Give brief description for your forum.

Click Save to finish.

The administrators and moderators of a forum may want to get updated of
what is new in forums under their management. This can be done when
creating a new forum.

**Configuring the moderation settings**

When creating a forum, you can set moderation-related options.

Select the Moderation Options tab in the Forum form.

Do actions in the relevant fields.

**Details:**

+-------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Field                                                 | Description                                                                                                                                                                                  |
+=======================================================+==============================================================================================================================================================================================+
| Auto-fill the moderator's email                       | Checks this option if you want the moderator's email is auto-filled. The email address will be taken from the moderator profile.                                                             |
+-------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Email addresses to notify when there is a new post    | Enters the list of email addresses which will get the notification if any new post is created. This field will be filled automatically if the Auto-fill the moderator's email is checked.    |
+-------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Email addresses to notify when there is a new topic   | Enters the list of email addresses which will get the notification if any new topic is created. This field will be filled automatically if the Auto-fill the moderator's email is checked.   |
+-------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Moderate Topics                                       | By default, new topics must be always approved and visible to everyone. If this option is selected, new topics will be pending for approval before being viewable.                           |
+-------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Setting forum permissions**

While creating a new forum, you can assign the **moderator** role or
rights to start topics, add and view posts in the forum to specific
users/roles/groups. To do this, select the Permissions tab in the Forum
form and follow `this
step <#PLFUserGuide.BuildingYourForum.Administrator.ManagingCategories.AddingCategories.SettingCategoryPermission>`__.

    **Note**

    -  When granting the "moderator" role to a specific user/role/group,
       to allow other users to start topics, add/view posts, you should
       uncheck these rights. The moderator of a forum only has right to
       manage the forum.

    -  If you do not set the starting topics, posting, and viewing posts
       permissions for any users/roles/groups, and the category which
       includes the forum is not `set
       permissions <#PLFUserGuide.BuildingYourForum.Administrator.ManagingCategories.AddingCategories.SettingCategoryPermission>`__,
       it means all users can do these actions.

    -  When granting any permissions above (moderate, start topics, post
       or only view posts in a forum), if you set the \* membership for
       the selected group, this permission will be granted to all users
       of that group, regardless of their membership role.

.. _Delete-forum:

**Deleting a forum**

Only administrators can perform this action. When a forum is removed,
all of its topics will then be deleted.

Go into the forum you want to remove.

Click |image5| on the Action bar, then select Delete from the drop-down
menu.

Click **OK** in the confirmation message to accept your deletion.

.. _Move-forum:

**Moving a forum**

You can move a forum to another category as follows:

Go into the forum you want to move.

Click |image6| on the Action bar, then select Move from the drop-down
menu.

A list of existing categories will appear. Select a destination category
to which your selected forum will be moved.

.. |image0| image:: images/forum/add_forum_btn.png
.. |image1| image:: images/forum/add_forum_btn.png
.. |image2| image:: images/forum/manage_category_btn.png
.. |image3| image:: images/forum/admin_add_forum.png
.. |image4| image:: images/forum/admin_add_forum_tab.png
.. |image5| image:: images/forum/more_actions_button.png
.. |image6| image:: images/forum/more_actions_button.png
