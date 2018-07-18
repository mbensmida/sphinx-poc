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


