.. _Calendar:

########################
Managing Your Calendars
########################

    This chapter introduces you to the **Calendar** application and its
    actions that allow you to schedule appointments and meetings,
    establish recurring activities, create multiple calendars and share
    calendars with others. With **Calendar**, it is easy to keep track
    of all important events/tasks and collaborate with other people, all
    in one place. This chapter is divided into the following topics:

    - :ref:`Calendar interface <Interface>`

       Introduction to the Calendar interface and its main components.

    - :ref:`Creating a calendar <CreatingCalendar>`

       How to create a personal calendar, group calendar or remote
       calendars.

    - :ref:`Editing a calendar <EditingCalendar>`

       Steps to edit details and properties of a calendar, to set the
       calendar color, and to delete a calendar.

    - :ref:`Exporting/Importing a calendar <ExportingImportingCalendar>`

       How to import calendars or export calendars to a calendar
       application that supports the iCalendar format.

    - :ref:`Sharing a personal calendar <SharingPersonalCalendar>`

       Information about setting permissions on your shared calendar and
       how to share your personal calendar with other users so that they
       can participate in all activities of the calendar.

    - :ref:`Scheduling an event <SchedulingEvent>`

       How to to perform common actions with events in Calendar:
       creating, editing, deleting, importing and exporting events.

    - :ref:`Editing Calendar settings <EditingCalendarSettings>`

       Steps to change the Calendar preferences.

    - :ref:`Generating RSS <GeneratingRSS>`

       Steps to publish your calendar as an RSS feed.

    - :ref:`Managing categories <ManagingCategories>`

       Steps to add, edit and delete categories which are used to
       classify events and tasks.

.. _Interface:

==================
Calendar interface
==================

The Calendar interface has 5 basic components.

In which:

-  |image0|: The **Toolbar** contains most of actions in Calendar, such
   as adding an event, switching between view modes and more.

-  |image1|: The **Search Pane** where you can perform quick and
   advanced searches.

-  |image2|: The **Mini calendar** where you can go backward/forward
   months by clicking |image3|/ |image4|. Also, you can jump to your
   desired date by directly clicking that date.

-  |image5|: The **Calendar View pane** where you can create events
   quickly and view your own events.

-  |image6|: The **Calendars pane** which includes 3 groups:

   -  Personal Calendars: Your private calendars.

   -  Group Calendars: Calendars of groups in which you are a member.

   -  Shared Calendars: Calendars which others share with you.

.. note:: If the :ref:`Task Management application <Manage-Task>` is installed by your administrator, you will see another Calendar group named "*Task Calendars*\ " below your *Group Calendars*. Each project from this application will have an individual calendar here but for view purpose only. Under the group, there will be also a *Tasks* calendar that displays all tasks assigned to you.

.. _CreatingCalendar:

===================
Creating a calendar
===================

You may create a :ref:`personal calendar <PersonalCalendar>`
or :ref:`group calendar <GroupCalendar>`
that can be shared with specific users or groups to your desires. You
can also create a calendar which is synchronized with a 
:ref:`remote calendar <RemoteCalendar>`.

.. _PersonalCalendar:

Creating a personal calendar
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. note:: All personal calendars will be put in the **Personal Calendars** pane.

1. Click |image7|, then select Add Calendar from the drop-down menu.

2. Fill in fields of the Details tab.

|image8|

*Details:*

+-----------------------+----------------------------------------------------+
| Field                 | Description                                        |
+=======================+====================================================+
| Display Name          | The calendar name which is displayed.              |
+-----------------------+----------------------------------------------------+
| Description           | The brief description of the calendar.             |
+-----------------------+----------------------------------------------------+
| Time Zone             | The display time zone for the calendar activities  |
|                       | which cannot be edited. However, you can change    |
|                       | the time zone in your :ref:`calendar               |
|                       | settings <TimeZone>`.                              |
+-----------------------+----------------------------------------------------+
| Color                 | The display color of the calendar activities that  |
|                       | can be personalized.                               |
+-----------------------+----------------------------------------------------+

.. note:: If you select the :ref:`Show in Groups <ShowInGroupsForm>` tab, then click |image9| to define specific groups and click |image10|, the calendar will be put in the **Group Calendars** category, not in the **Personal Calendars** category.

3. Click Save to finish your creation.

.. _GroupCalendar:

Creating a group calendar
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. note:: All group calendars will be put in the **Group Calendars** pane.

1. Follow steps as stated in :ref:`Creating a personal calendar <PersonalCalendar>`
to give details for your new calendar.

.. _ShowInGroupsForm:

2. Select the Show in Groups tab.

|image11|

3. Select groups that contain your created calendar. The users of the
selected groups can only view this calendar.

**i.** Click |image12| to open the Group Selector form. This form will
help you select a group that you want to share.

|image13|

**ii.** Click your desired group, then select |image14| to add the
defined group.

**iii.** Click |image15| or |image16| to grant permissions to specific
users or memberships respectively from the selected group.

.. note:: - If you set the \* membership in the User able to edit calendar column, all users of the selected group will be able to edit this calendar, regardless of their membership role.

		  -  You can select more users/memberships by repeating the above steps. The selected users/memberships will be updated in corresponding textboxes.

		  -  You can delete your selected users/memberships manually in the textboxes or click |image17| to remove the permissions.

4. Click Save to finish creating your new group calendar.

.. _RemoteCalendar:

Creating a remote calendar
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. note:: To create a remote calendar in the **Calendar** application successfully, you need to learn about the calendar settings of the relevant provider. For more information about types of remote calendars, see :ref:`here <MoreAboutiCalCalDAV>`.

1. Click |image18|, then select Remote Calendar from the drop-down menu. 
The Subscribe Calendar form appears.

|image19|

2. Select the type of the remote calendar: iCalendar or CalDAV.

3. Enter the URL linking to your calendar server in the URL field.

4. Click Next to go to the Remote Calendar form.

|image20|

5. Fill in the fields. The asterisk (\*) indicates the field is mandatory.

6. Tick the Use Authentication checkbox, then enter the username and
password of your remote calendar server if the remote server requires
verification.

7. Click Save to accept your creation.

.. note:: After creating a remote calendar, you can ONLY VIEW all events and tasks which are created in the remote calendar server right in the **Calendar** application by clicking it. To get the updates, hover your cursor over the remote calendar, then click |image21| to select Refresh from the drop-down menu.

.. _MoreAboutiCalCalDAV:

More information about types of remote calendars
--------------------------------------------------

-  **iCalendar**:

iCalendar provides a link to an online .ics file from another calendar
servers, such as Google Calendar, Yahoo Calendar, or eXo Calendar
(including public URL or private URL).

An example of a Google Calendar URL (in iCal format):

`https://calendar.google.com/calendar/ical/en.tn%23holiday%40group.v.calendar.google.com/public/basic.ics <http://calendar.google.com/calendar/ical/en.tn%23holiday%40group.v.calendar.google.com/public/basic.ics>`__

-  **CalDAV**:

CalDAV is an open protocol that allows you to access calendars via
WebDAV. With CalDAV, you can publish and subscribe to calendars, share
them collaboratively, synchronize among multiple users or devices.

**Google**: https://apidata.googleusercontent.com/caldav/v2/calid/events
where ``calid`` is the calendar id to be accessed.

**Yahoo**:
https://caldav.calendar.yahoo.com/dav/your_yahoo_account@yahoo.com/Calendar/calendar_name/

.. _ImportGoogleCalendar:

How to import a Google calendar?
----------------------------------

Below an example of how to import a Google calendar to eXo Platform:

1. Go to your Google calender interface and select the calendar you 
wish to import to eXo Platform.

2. Click on options button |image22| of the chosen calendar and then 
select *Settings and sharing*.

|image23|

3. An interface Settings appears, scroll down to the section Integrate
calendar and copy your calendar's public link in iCal format.

|image24|

4. Go to the calendar interface in eXo Platform and click on the 
|image25| then on Remote calendar.

5. Paste the iCal link to the field URL.

6. Click on Next to move to the form in calendar settings. Fill in the
needed fields.

.. note:: If the imported remote calendar is not public, you should input your google account credentials in the "Authentication" section to enable the import procedure.

.. _EditingCalendar:

==================
Editing a calendar
==================

.. note:: -  You can ONLY edit personal calendars and group calendars that you created.

		  -  For group calendars which are created by another users, you can ONLY edit them if you are granted the **Edit** permission. Meanwhile, for shared calendars, you cannot edit them. If you are granted the **Edit** permission on them by the calendar creators, you can ONLY have the right on their tasks or events (for example, adding/modifying/deleting, exporting/importing).

1. Hover your cursor over the calendar which you want to edit, then 
click |image26| that appears.

2. Click Edit from the drop-down menu. The form to edit the calendar 
will be different, depending on your selected calendar type. 
For example, if you select a personal calendar, the form only contains 
the Details tab.

3. Make changes on the calendar, then click Save to accept your changes.

.. _CalendarColor:

Setting the calendar color
---------------------------

The **Calendar** application allows you to select different colors for
all types of calendars to recognize them easily.

1. Hover your cursor over the calendar which you want to set the color,
then click |image27| that appears.

2. Select one color from the available 24-color palette.

|image28|

.. _DeleteCalendar:

Deleting a calendar
----------------------

This function allows you to remove any calendars and all their events.

.. note:: You cannot delete group calendars created by another users if you are not granted the **Edit** permission.

1. Hover your cursor over the calendar which you want to delete, then 
click |image29| that appears.

2. Select Remove from the drop-down menu.

3. Click Yes in the confirmation message.






.. |image0| image:: images/common/1.png
.. |image1| image:: images/common/2.png
.. |image2| image:: images/common/3.png
.. |image3| image:: images/calendar/left_arrow_icon.png
.. |image4| image:: images/calendar/right_arrow_icon.png
.. |image5| image:: images/common/4.png
.. |image6| image:: images/common/5.png
.. |image7| image:: images/calendar/add_icon_calendar.png
.. |image8| image:: images/calendar/calendar_form.png
.. |image9| image:: images/common/select_everyone_icon.png
.. |image10| image:: images/calendar/add_button.png
.. |image11| image:: images/calendar/show_in_groups_tab.png
.. |image12| image:: images/common/select_group_icon.png
.. |image13| image:: images/calendar/group_selector.png
.. |image14| image:: images/calendar/add_button.png
.. |image15| image:: images/common/select_user_icon.png
.. |image16| image:: images/common/select_role_icon.png
.. |image17| image:: images/common/delete_icon.png
.. |image18| image:: images/calendar/add_icon_calendar.png
.. |image19| image:: images/calendar/subscribe_calendar.png
.. |image20| image:: images/calendar/remote_calendar_form.png
.. |image21| image:: images/calendar/calendar_setting_icon.png
.. |image22| image:: images/calendar/options_button.png
.. |image23| image:: images/calendar/settings_sharing_option.png
.. |image24| image:: images/calendar/public_address_ical.png
.. |image25| image:: images/calendar/add_icon_calendar.png
.. |image26| image:: images/calendar/calendar_setting_icon.png
.. |image27| image:: images/calendar/calendar_setting_icon.png
.. |image28| image:: images/calendar/calendar-color.png
.. |image29| image:: images/calendar/calendar_setting_icon.png
