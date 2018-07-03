.. _Administrator.AdministrativeTasks:

Administrative tasks
~~~~~~~~~~~~~~~~~~~~~

All of administrative tasks can be reached via the menu that appears
after clicking |image169| on the Forums Administration bar. You can select
a desired action from the following drop-down menu.

|image170|

The administrative tasks include the following actions:

- :ref:`Configuring Sort Settings <Sort-settings>`

- :ref:`Defining censored keywords <Administrating-Censor>`

- :ref:`Customizing an email notificationtemplate <Customize-email-notifs>`

- :ref:`Customizing BBCodes <Customize-BBCodes>`

- :ref:`Setting up auto-pruningauto-pruning>`

- :ref:`Banning IPs <AdministrativeTasks.BanningIPs>`

- :ref:`Backing up a category/forum <BackingupCategoryForum>`

.. _Sort-settings:

Configuring Sort Settings
-------------------------

Click |image171| on the Forums Administration bar, then click Sort
Settings from the drop-down menu. The Sort Settings form opens. Now, you
can set properties for how forums and topics are sorted in **Forums**.

|image172|

-  Sort Forums by: Sort forums by several criteria: name, order, lock
   status, creation date, modification date, topic count and post count.

-  Direction: Sort forums in the Ascending or Descending order.

-  Sort Topics by: Sort topics by name, lock status, creation date,
   modification date, date of last post, post count, view count,
   attachments count.

-  Direction: Sort topics in the Ascending or Descending order.

.. _Administrating-Censor:

Defining censored keywords
--------------------------

Censored keywords are those which are specified as inappropriate in the
**Forums** application. If any topics or posts contain censored
keywords, they will be hidden until being verified by Administrators or
Moderators. The Censor Keyword form will be displayed.

1. Click |image173| on the Forums Administration bar, then click Censor
Keywords from the drop-down menu. The Censor Keyword form appears: 

|image174|

2. Entercensored keywords in the Censored Keywords field. 
The keywords are separated by commas. 

3. Click Save to complete defining the censored keywords.

.. _Customize-email-notifs:

Customizing an email notification template
------------------------------------------

If there are new posts in the category, forum or topic that a user has
watched, the user will receive the email notification like this.

|image175|

This section will describe how to create and edit the email templates
that can be used to send email notifications to users.

Click |image176| on the Forums Administration bar and click Notifications
from the drop-down menu to open the Notifications form.

|image177|

The Notifications form consists of two tabs:

-  New Posts Notification: Customizes the template of the email
   notification when there is a new post/topic in
   categories/forums/topics that users are watching.

-  Moved Notification: Customizes the template of the email notification
   when a category/forum/topic/post which is being watched is moved to
   another location.

**Details:**

-  Subject: The notification subject.

-  Add a prefix to notifications: Ticks the checkbox to add a prefix to
   the email notification.

-  Content Notification: The template content of the email notification
   of new topics/posts that can be modified with the built-in Editor.

The followings are variables which can be used in the template:

**The common variables for both tabs:**

-  VIEWPOST\_LINK: Will be replaced by the public link referring to the
   new topic/post.

-  $VIEWPOST\_PRIVATE\_LINK: Will be replaced by the private link
   referring to the new topic/post.

-  $REPLYPOST\_LINK: Will be replaced by the private link referring to
   the topic and a form to reply will be automatically opened.

**The variables used in the New Post Notification tab:**

-  $OBJECT\_WATCH\_TYPE: Will be replaced by the watched object type
   (category/forum/topic).

-  $OBJECT\_NAME: Will be replaced by the name of the watched object
   (category/forum/topic).

-  $ADD\_TYPE: Will be replaced by the newly added object type
   (topic/post).

-  $ADD\_NAME: Will be replaced by the newly added object name (topic
   name/post name).

-  $POSTER: Will be replaced by the topic/post owner.

-  $POST\_CONTENT: Will be replaced by the topic/post content.

-  $TIME: Will be replaced by the time when the topic/post was added.

-  $DATE: Will be replaced by the date when the topic/post was added.

-  $CATEGORY: Will be replaced by the category name.

-  $FORUM: Will be replaced by the forum name.

-  $TOPIC: Will be replaced by the topic name.

**The variables used in the Moved Notification tab:**

-  $OBJECT\_PARENT\_NAME: Will be replaced by the forum name (if moving
   topics) or the topic name (if moving posts).

-  $OBJECT\_PARENT\_TYPE: Will be replaced by the type of the moved
   parent object, such as forum (if moving topics) or topic (if moving
   posts).

-  $OBJECT\_NAME: Will be replaced by the name of the moved object
   (topic name/post name).

-  $OBJECT\_TYPE: Will be replaced by the type of the moved object
   (topic/post).

These variables are used to load the content dynamically. Thus, you
should not edit them. In case the template is changed unexpectedly, you
can go back to the default template by clicking |image178| . You can use
the text editor to format the template as you wish.

.. _Customize-BBCodes:

Customizing BBCodes
-------------------

By default, there are some default BBCode tags that are initialized via
plugins: "[B]", "[I]", "[U]", "[FONT]", "[HIGHLIGHT]", "[IMG]", "[CSS]",
"[URL]", "[GOTO]", "[QUOTE]", "[LEFT]", "[RIGHT]", "[CENTER]",
"[JUSTIFY]", "[SIZE]", "[COLOR]", "[CSS]", "[EMAIL]", "[CODE]",
"[LIST]", "[WIKI], "[SLIDESHARE]". You can add, edit or delete the
BBCode tags.

Click |image179| on the Forums Administration bar, then select BBCodes
from the drop-down menu to open the BBCode Manager form.

|image180|

Here, you can do the following actions:

-  :ref:`Adding a new BBCode <CustomizingBBcodes.AddingNewBBCode>`

-  :ref:`Editing/Deleting a BBCode <CustomizingBBcodes.EditingDeletingBBCode>`

-  :ref:`Activating/Deactivating a BBCode <CustomizingBBcodes.ActivatingDeactivatingBBCode>`

.. _CustomizingBBcodes.AddingNewBBCode:

Adding a new BBCode
````````````````````

1. Click Add BBCode in the BBCode Manager form to open the Add BBCode form.

2. Input values into the Add BBCode form.

|image181|

**Details:**

|image182| **Tag**: This is the text for BBCode, which goes inside the
square bracket.

|image183| **Replacement**: The HTML codes that replace the user-entered
BBCode.

|image184| **Description**: The brief description about this BBCode tag.

|image185| **Example**: The sample of the BBCode in use.

|image186| **Use {option}**: Allows BBCode tag to have option or not.

|image187|: Clicks this icon to preview your rendered BBCode.

|image188|: Clicks this icon to see descriptions of each field.

3. Click Save to finish or Reset to clear all input fields.

.. _CustomizingBBcodes.EditingDeletingBBCode:

Editing/Deleting a BBCode
``````````````````````````

**Editing a BBCode**

1. Click |image189| corresponding to the relevant BBCode tag in the 
BBCode Manager form.

|image190|

2. Make changes on the BBCode tag.

2. Click Save to finish your changes.

**Deleting a BBCode**

Simply click |image191| corresponding to the BBCode you want to delete in
the BBCode Manager form, then select **OK** in the confirmation message
to accept your deletion.

.. _CustomizingBBcodes.ActivatingDeactivatingBBCode:

Activating/Deactivating a BBCode
`````````````````````````````````

Any BBCode can be activated/deactivated.

|image192|

-  To activate an existing BBCode tag, tick the relevant checkbox.

-  To deactivate an existing BBCode tag, simply deselect the relevant
   checkbox. The entered BBCode will be displayed as the plain text.

.. _auto-pruning:

Setting up auto-pruning
-----------------------

The pruning allows you to clean a large amount of obsolete and inactive
topics based on criteria.

1. Click |image193| on the Forums Administration bar and click Pruning from
the drop-down menu to open the Auto Prune form.

|image194|

2. Click |image195| corresponding to the forum you want to set the prune
settings.

|image196|

3. Specify the criteria.

4. Click |image197| to check how many topics will be pruned.

5. Click Save to accept settings.

After setting the prune successfully, the auto-prune will be run
automatically on the forum that has been set to check for the inactivate
topics.

.. _AdministrativeTasks.BanningIPs:

Banning IPs
-----------

Administrators can ban IP addresses used by users who abuse the forum
functions or violate the forum rules and policies. All banned IPs cannot
be used to add posts to all forums in the **Forums** application. Any
users who use banned IPs to add post, will be recognized as the banned
user. As the result, the banned user can only view in **Forums**.

Click |image198| on the Forums Administration bar, then click Banned IPs
from the drop-down menu. The Banned IPs form appears.

|image199|

-  To ban an IP, simply enter the IP address into the IP textboxes and
   click Add. All banned IPs will be listed in the banned IPs table. You
   can view all posts which are posted from the specific banned IP or
   delete them from the banned IPs list.

-  To view all posts submitted from a specific IP, click |image200| of
   the respective IP. These posts can be viewed and deleted by the
   administrator.

-  To remove banned IPs from the banned IPs list, click |image201| of 
   the respective IP.

Besides, you can also filter the banned IPs if there are so many banned
IPs.

To filter banned IPs, enter a part of the IPs address into filter
textbox, all IPs matching with the filter term will be displayed.

.. _BackingupCategoryForum:

Backing up a category & forum
-----------------------------

The **Export** function is a best way to back up data in the **Forums**
application. This function allows you to export categories and forums in
the **Forums** application into the .zip or .xml file. When a
category/forum is exported, all of its forum, topics, posts and
properties are also exported. This exported file can be used to import
into the **Forums** application.

Backing up a category & forum includes the following actions:

-  :ref:`Exporting a category <Export-category>`

-  :ref:`Exporting a forum <Export-forum>`

-  :ref:`Importing a category <Import-category>`

-  :ref:`Importing a forum <Importing-a-forum>`

.. _Export-category:

Exporting a category
`````````````````````

1. Click |image202| on the Forums Administration bar.

2. Click Export from the drop-down menu to open the Export Categories 
form.

|image203|

*Details:*

+---------------------+------------------------------------------------------+
| Field               | Description                                          |
+=====================+======================================================+
| File Name           | Name of the exported file.                           |
+---------------------+------------------------------------------------------+
| Export All          | Checks this option to export all data in **Forums**, |
|                     | such as all categories, user profiles and forum      |
|                     | statistics.                                          |
+---------------------+------------------------------------------------------+
| Only Categories     | Checks this option to export the selected categories |
|                     | only.                                                |
+---------------------+------------------------------------------------------+

3. Select categories and enter the file name into the File Name field.

4. Click Save.

.. _Export-forum:

Exporting a forum
`````````````````````

This function is used to export forums and all topics inside the
**Forums** application into the .xml or .zip file.

**The first way**

1. Go into a forum you want to export and click |image206| on the Action
bar.

2. Click Export Forum from the drop-down menu to open the Export Forums
form.

|image204|

3. Input the file name.

4. Tick the Compress checkbox to export the file into the .zip file or
leave it blank to export into .xml file.

5. Click Save to get and store the exported file in your local device.

**The second way**

1. Go into a category containing the forum you want to export.

2. Click |image205| on the Action bar, then click Export Forum from the
drop-down menu.

3. Select a forum you want to export by ticking the relevant checkbox. 
The Compress checkbox is checked by default that means the file is 
exported in the .zip format.

4. Click Save to get and store the exported file in your local device.

.. _Import-category:

Importing a category
`````````````````````

1. Click |image207| on the Forums Administration bar, then click Import 
from the drop-down menu to open the Import Category form.

|image208|

2. Click Select File to browse and select the file to import.

3. Click Save.

.. _Importing-a-forum:

Importing a forum
``````````````````

1. Go into one category, then click |image209| on the Action bar.

2. Click Import Forum from the drop-down menu.

3. Browse and upload the selected file in the Import Forum form.

4. Click Save to accept importing.

After being imported successfully, the forum and topic data will be
displayed properly in the **Forums** homepage.


