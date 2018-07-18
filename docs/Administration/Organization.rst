.. _ManagingYourOrganization:

===========================
Managing your organization
===========================

This section covers the following topics:

-  :ref:`Adding a user <ManagingYourOrganization.AddingUser>`
   How to add a new user to your organization.

-  :ref:`Managing users <ManagingYourOrganization.ManagingUsers>`
   Actions related to managing users in your organization, including
   searching for users, editing information of users, or deleting users.

-  :ref:`Managing groups <ManagingYourOrganization.ManagingGroups>`
   How to add, edit, delete groups and members in groups.

-  :ref:`Managing memberships <ManagingYourOrganization.ManagingMemberships>`
   How to add, edit and delete membership types.

-  :ref:`Sending mail about users registration <ManagingYourOrganization.SendingMailUserCreation>`
   How to configure the platform to send emails to the administrator
   about new users registration.


.. _ManagingYourOrganization.AddingUser:

Adding a user
~~~~~~~~~~~~~~

1. Click |image157| on the top navigation bar, then select Community Add
   Users from the drop-down menu.

A window with the Account Setting and User Profile tabs will open.

|image158|

.. _CreateNewAccountFormDetails:

**Details:**

+-----------------------+----------------------------------------------------+
| Field                 | Description                                        |
+=======================+====================================================+
| Asterisk (\*)         | This mark indicates that the field is mandatory.   |
+-----------------------+----------------------------------------------------+
| User Name             | The name used to log in. The username must be:     |
|                       |                                                    |
|                       | -  Lowercase (a - z), digit (0 - 9), underscore    |
|                       |    (\_), and dot (.) characters, but dash (-) are  |
|                       |    not allowed.                                    |
|                       |                                                    |
|                       | -  From 3 to 30 characters in length.              |
|                       |                                                    |
|                       | -  Lowercase for its first character.              |
|                       |                                                    |
|                       | -  Lowercase or digit for its last character.      |
|                       |                                                    |                                                                          
+-----------------------+----------------------------------------------------+
| Password              | The authentication string which must be between 6  |
|                       | and 30 characters, including spaces.               |
+-----------------------+----------------------------------------------------+
| Confirm Password      | Retypes the password above. The values in both     |
|                       | Password and Confirm Password fields must be the   |
|                       | same.                                              |
+-----------------------+----------------------------------------------------+
| First Name            | The user's first name which must start with a      |
|                       | character. Its length must be between 1 and 45     |
|                       | characters.                                        |
+-----------------------+----------------------------------------------------+
| Last Name             | The user's last name which must start with a       |
|                       | character. Its length must be between 1 and 45     |
|                       | characters.                                        |
+-----------------------+----------------------------------------------------+
| Display Name          | This field is not required. Its length must be     |
|                       | between 0 and 90 characters.                       |
+-----------------------+----------------------------------------------------+
| Email Address         | The user's email address that must be in the       |
|                       | correct form, such as username@abc.com.            |
|                       |                                                    |
|                       | There are 2 parts in the email address, called     |
|                       | local part and domain (for example,                |
|                       | local\_part@domain):                               |
|                       |                                                    |
|                       | -  Local part: Only lowercase (a - z), digit (0 -  |
|                       |    9), underscore (\_), dash (-) and dot (.)       |
|                       |    characters are allowed, and the first and last  |
|                       |    characters of this part must be lowercase or    |
|                       |    digit ones.                                     |
|                       |                                                    |
|                       | -  Domain: Only lowercase (a - z), digit (0 - 9),  |
|                       |    dash (-) and dot (.) characters are allowed,    |
|                       |    and the first and last characters of this part  |
|                       |    must be lowercase or digit ones. Note that the  |
|                       |    dot (.) character is required.                  |
|                       |                                                    |                                                                          
+-----------------------+----------------------------------------------------+

2. Fill all fields in the Account Setting tab which must be completed.

   Further information about the user, such as nickname, or birthday, 
   can be added in the User Profile tab that is not required.

3. Click Save to accept your new account. If you want to refresh the 
   input information, simply click Reset.


.. _ManagingYourOrganization.ManagingUsers:

Managing users
~~~~~~~~~~~~~~~


Click |image159| on the top navigation bar, then select Community --> 
Manage Community from the drop-down menu.

You will be redirected to the Users tab. By default, all active users
will be shown in this tab.

|image160|

Editing user information
--------------------------

1. Locate the user you want to edit his information.

2. Click |image161| corresponding to the user with the information you 
   wantto edit.

3. Select the Account Info tab to edit main information of the user,
   including First Name, Last Name, Display Name, or Email Address.

|image162|

*User Name*
    The User Name cannot be changed.

*Change Password*
    The Change Password option allows an administrator to set a new
    password for the selected user. When the Change Password option is
    unchecked, New Password and Confirm Password are hidden. Passwords
    must contain at least 6 characters, including letters, numbers and
    punctuation marks.

For more details on these fields, see :ref:`here <CreateNewAccountFormDetails>`.

4. Select the User Profile tab to edit personal information of the 
   selected user, including Profile, Home Info, Business Info, and 
   Social Networks Info (if :ref:`OAuth authentication <#PLFAdminGuide.OAuthAuthentication>`
   is configured by your administrator).

   -  In Social Networks Info, when clicking the Save button:

      -  If the field of social network username was cleared, the current
      eXo account is unlinked to the new social network username.

      -  If the field of social network username was changed, it should be
      unlinked to the previous social network username and linked to the
      a new (changed) social network username. If the field was left
      blank, it should only be unlinked.

   -  You may also switch the default display language for that user by
   selecting another language from the Language field.

5. Select the User Membership tab to see the group membership 
   information of the user.

The User Membership tab displays which groups the selected user belongs
to.

To remove a membership type of the use, simply click |image163|.

6. Click Save to accept your changes.

Removing a user
----------------

In the Users tab, simply click |image164| in the Action column, then 
click **OK** in the confirmation message.

Activating/Suspending a user
----------------------------

As of eXo Platform 4.3, the administrator is provided with a new feature 
for activating or suspending a user.

1. To see all suspended users, select All or Suspended from the Status
   drop-down menu and click on Search button:

|image165|

For users after being suspended, here are changes on their account that
should be noticed:

**Activity Stream**

-  Their activity stream will not receive any new activity until their
   account is re-activated.

-  The suspended users obviously will not be able to post, so people in
   their Connections list will no longer receive activities from these
   users in their :ref:`All Activities <Managing-Activities>` or
   :ref:`Connections <ConnectionsFilter>` streams.

-  Their past activities, comments and likes will be remained.

-  Their account will not be listed in the suggestions list when someone
   :ref:`mentions <Mentioning-People>`.

**People**

-  Their account will be neither listed nor searchable in applications,
   including :ref:`My Connections, Everyone <MyConnectionPage.Tabs>`,
   :ref:`Suggestions <SuggestionsApp>` and :ref:`Invitations <InvitationsApp>`
   applications as usual.

-  They cannot log in, but their profile is still accessible to others,
   so it is possible to :ref:`connect <Send-Connection-Request>`,
   :ref:`disconnect <Disconnect-Contact>` or
   :ref:`revoke <Revoke-Connection-Request>` an invitation.

**Wiki**

-  Their account will not be listed in the :ref:`Wiki permissions <AddingWikiPermissions>`
   or :ref:`Page permissions <PagePermissions>`.

-  They will not receive emails from the :ref:`Watching a page <WatchingPage>`
   feature in Wiki application.

**Calendar**

-  Their account will not be listed when someone :ref:`shares their personal calendars <SharePersonalCalendar>`
   or :ref:`grants group calendar permissions <GroupCalendar>`.

-  Their account will not be listed when someone :ref:`adds participants in an event <AddingParticipantsToEvent>`
   , or :ref:`views the availability time of participants in an event <ViewingTimeAvailability>`, 
   or :ref:`sends a reminder email for an event/task <CreatingEventReminder>`.

-  In case they have been involved in tasks/events, once being
   suspended, they will not receive:

   -  Invitation emails from Calendar (after someone modified an event
      where the suspended user was participant already).

   -  Event/Task reminder emails from the Calendar application.

-  Calendars shared by suspended users remain to be available to the
   shared people.

**Documents**

-  Their account will not be listed when someone :ref:`adds permissions on content <ManagingPermissions>`,
   sets permissions on :ref:`public tags <SettingPermissionsOnPublicTags>`
   or :ref:`category trees <Categories.AddingCategoryTree>`,
   or :ref:`adds or edits <ViewsIneXoPlatform.AddingView>` a view <ViewsIneXo>`.

-  They will no longer receive any email from the :ref:`Document Watch feature <WatchingUnwatchingDocument>`.

-  Their documents in the :ref:`Personal Document drive <WorkingWithExplorer.Drives>`
   will be remained.

**Forum**

-  Their account will not be listed when someone sets :ref:`topic permissions <CreatingTopics.SettingTopicPermissions>`/
   `forum permissions <SettingForumPermissions>`, :ref:`adds restricted audience <AddingRestrictedCategories>`
   or :ref:`grants permissions <SettingCategoryPermission>` in forum 
   categories.

-  They will not receive any email from the :ref:`Watching
   feature <Regularusers-Watching>`, :ref:`private message <Regularusers-PrivateMessages>`
   or :ref:`my subscriptions <Edit-subscription>`.

**Spaces**

-  Their account will not be listed when someone :ref:`invites members <InvitingMembers>`
   to join a space.

-  Their account is still available in Space SettingsMembers, but
   impossible to be :ref:`promoted/demoted <PromotingDemotingMember>`
   or :ref:`removed <RemovingMember>`.

-  Their account will not be listed or searchable in SpaceMembers.

**Notifications**

-  The suspended users will no longer receive any email or on-site
   notifications.

**Answers**

.. note:: Answers is provided as an add-on, so you need to install it first. See :ref:`here <#eXoAddonsGuide.Answers>` for details.

-  Their account will not be listed when someone sets the :ref:`category permissions <#eXoAddonsGuide.Answers.Moderator.ManagingCategories.AddingCategory>`.

-  They will no longer receive emails from the :ref:`Watching feature <#eXoAddonsGuide.Answers.RegularUser.WatchingCategory>` 
   of Answers.

2. To suspend a user, switch **Active ?** button corresponding to this 
   user to Yes.

.. note:: -  Users/groups permitted to access this application can suspend users. By default, this permission is granted to the *platform/administrator* group.

		  -  A user cannot suspend himself, one warning appears if he attempts to do this.

		  -  The superuser *root* cannot be suspended.

3. To re-activate a user, simply switch Active ? button corresponding to
   this user to No.


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

.. _ManagingYourOrganization.ManagingMemberships:

Managing memberships
~~~~~~~~~~~~~~~~~~~~~

Select the Memberships tab. Here, you can manage user roles in a
specific group.

By default, 9 membership types are available in PRODUCT including
Member, Author, Editor, Manager, Redactor, Validator, Webdesigner,
Publisher and \*.

|image178|

.. note:: The \* membership is identical to any other type, so choosing this type means adding all available membership types.

.. _AddNewMembership:

Adding a new membership type
-----------------------------

1. Enter values into the fields of the Add/Edit Membership form. The
   Membership name field is required, and only letters, digits, dots,
   dashes and underscores are allowed without ANY SPACES.

2. Click Save to accept adding a new membership, or Reset to clear 
   entered values.

.. _EditMembership:

Editing a membership type
--------------------------

1. Click |image179| corresponding to the membership type you want to 
   edit in the Action column.

2. Make your desired changes on the Description field. You cannot change
   the Membership name.

3. Click Save to accept your changes.

.. _DeleteMembership:

Deleting a membership type
---------------------------

Simply click |image180| in the Action column, then click **OK** in the
confirmation message.

.. note:: The \* membership type is not allowed to be deleted or edited.

.. _ManagingYourOrganization.SendingMailUserCreation:

Sending mail about users registration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In eXo Platform registration page is by default disabled. An 
administrator can enable it by following this `guide <ManagingPermissions>` 
to make it accessible to guests so they can register to eXo Platform by
themselves.

To be notified about new users registration, an administrator can
configure eXo Platform to send him emails by following these steps:

1. Configure your SMTP server by following the :ref:`Outgoing mail service <#PLFAdminGuide.Configuration.OutgoingMailService>` guide.

2. Configure the service used for sending emails in ``portal.war/WEB-INF/conf/admin/admin-configuration.xml``. 
   This file contains descriptions for each available parameter, 
   including:

   -  Two mandatory parameters:

      -  ``sendMailAfterRegistration``: Set this parameter to "true" to
      enable email sending after a user registration.

      -  ``mailTo``: Add your email address in which you wish to receive
      notifications about new registrations.

   -  Optional configurations of mail content:

      -  ``mailFrom``: This will be used as from header in the mail.

      -  ``mailSubject``: The Subject of the mail.

      -  ``mailMessage``: The content of the mail.

.. tip:: Use the **${user.userName}** token for **mailSubject** and**mailMessage** to be then replaced by the real username that have been registred.

To check if your configuration takes effect, restart the server and
register a new user. An email that notifies of newly registered user
should be sent to you.




