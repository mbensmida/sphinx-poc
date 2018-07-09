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


