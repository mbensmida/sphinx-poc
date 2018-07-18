.. _ManagingApplications:

=====================
Managing applications
=====================


To manage categories, portlets and gadgets in a portal, you first need
to go to the **Manage Applications** page by clicking |image247| on the
top navigation bar, and select Applications. The **Manage Applications**
page will appear.

|image248|

**In which:**

-  |image249| **Tab bar** consists of two items, including Portlet and
   Gadget.

-  |image250| **Action bar** consists of actions related to adding a
   category and importing applications.

-  |image251| **Left pane** lists all categories and portlets/gadgets of
   each category.

-  |image252| **Breadcrumb bar** is the path from a specific category to a
   specific portlet/gadget in that category.

-  |image253| **Right pane** provides the detailed information of a
   specific portlet/gadget.

Portlets and gadgets are organized into different categories. Each
category contains one or several portlets or gadgets. You can also mix
portlets and gadgets into one category. By default, all gadgets are
placed in the Gadgets category.


.. _ManagingApplications.ManageCategory:

Managing categories
~~~~~~~~~~~~~~~~~~~~

Managing categories includes the following actions:

-  :ref:`Adding a new category <ManagingCategories.AddingNewCategory>`

-  :ref:`Editing/Deleting a category <ManagingCategories.EditingDeletingCategory>`

-  :ref:`Adding Portlets/Gadgets to a category <ManagingCategories.AddingPorletGadgets>`

.. _ManagingCategories.AddingNewCategory:

Adding a new category
---------------------

1. Click |image254| on the Action bar to open the form below.

|image255|

**In which:**

In the Category Setting tab:

Category name
    The field is required, unique and must start with a letter. Only
    alphabetical, numerical, dash and underscore characters are allowed
    for this field with the length between 3 and 30 characters.

Display name
    The display name of the category and its length must be between 3
    and 30 characters.

Description
    A brief description of the category. Any length from 0 to 255
    characters is allowed.

2. Enter values in the Category Setting tab.

3. Select the Permission Setting tab to set the *Access* permission for
   your category. It is required. Accordingly, other users can only view
   and use portlets in your category to which they have access.

For example, set the *Access* permission for all the members of the
/platform/web-contributors group:

|image256|

For more details about how to set the *Access* permission, refer to
:ref:`Access Permission <SettingPortalPermissions.AccessPermission>`.

4. Click Save to accept adding a new category to the categories list in 
   the left pane.

.. _ManagingCategories.EditDeleteCategory:

Editing/Deleting a category
---------------------------

**Editing a category**

1. Click your desired category, then click |image257| on the title bar.

2. Update the category information.

2. Click Save to apply changes.

.. note:: You cannot change the category name.

**Deleting a category**

1. Select your desired category and click |image258| on the title bar.

2. Click **OK** in the confirmation message.

.. _ManagingCategories.AddPortletToCategory:

Adding a portlet/gadget to a category
-------------------------------------

This function helps you add a portlet/gadget to a specific category
easily as follows:

1. Click |image259| located on the title bar of the category to which 
   you want to add portlets/gadgets.

  |image260|

Display name
    The display name of a portlet/gadget.

Application Type
    Either Portlet or Gadget.

2. Enter the display name and select an application type.

3. Select a portlet/gadget by checking the radio button.

4. Click Add to accept adding the selected portlet/gadget to the 
   category.

.. _ManagingApplications.ManagingPortletsAndGadgets:

Managing portlets and gadgets
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Managing portlets and gadgets includes the following actions:

-  :ref:`Adding a portlet/gadget to the Application list <ManagingPortletsAndGadgets.AddingPortletGadgetToApplicationList>`

-  :ref:`Activating the Import Applications function <ManagingPortletsAndGadgets.ActivatingImportApplicationsFunction>`

-  :ref:`Viewing/Editing detailed information of a portlet/gadget <ManagingPortletsAndGadgets.ViewingEditingDetailedInformation>`

-  :ref:`Editing a specific portlet <EditingSpecificPortlet>`

-  :ref:`Adding a gadget <ManagingPortletsAndGadgets.AddingGadget>`

-  :ref:`Editing a gadget <ManagingPortletsAndGadgets.EditingGadget>`


.. _ManagingPortletsAndGadgets.AddingPortletGadgetToApplicationList:

Adding a portlet/gadget to the Applications list
------------------------------------------------

This section shows you how to add a portlet/gadget to the Applications
list on the left panel of the Manage Applications page.

1. Click Portlet/Gadget on the Tab bar to open a list of portlets/gadgets  
   respectively.

|image261|

**Details**:

-  Left panel |image262|: The list of portlets/gadget.

-  Right panel |image263|: The information of the portlet/gadget.

-  Breadcrumb bar |image264|: The path of the portlet/gadget.

2. Click the portlet/gadget which you want to add to the Applications 
   list.

The information of the portlet/gadget is displayed.

3. Click the Click here to add into categories link to open a form which
   allows you to select categories for the portlet.

|image265|

4. Select your desired categories and click Save to accept adding the
   portlet/gadget to the Applications list.

Then, you will see the list of categories to which the portlet/gadget is
added.

|image266|

.. note:: In case the portlet/gadget was already added to the Applications list, there is no the Click here to add into categories link.

.. _ManagingPortletsAndGadgets.ActivatingImportApplicationsFunction:

Activating the Import Applications function
-------------------------------------------

The Import Applications function allows you to import all applications
available in the system to the categories on the left panel. However, to
avoid importing unnecessary applications, this function is hidden on the
action bar by default. To show it on the action bar, do as follows:

1. Go to the :ref:`Manage Applications page <GoToManageApplicationsPage>`
--> Edit --> Page --> Edit Layout on the Administration bar.

2. Hover your cursor over the Application Registry portlet, then click
   |image267| at the upper left corner of that portlet.

The Edit Mode will be displayed.

|image268|

3. Tick the Show "Import Applications" button checkbox, then click Save 
   to accept the changes.

4. Click Close to close the Edit Mode form, then click |image269| to quit 
   the Page Editor page.

The Import Applications button is now shown on the Manage Applications
page.

**Importing portlets and gadgets**

Now you can import default portlets and gadgets into different
categories as follows:

1. Click |image270| at the right corner on the Action bar.

2. Click **OK** in the confirmation message to accept importing portlets
   and gadgets automatically.

All portlets and gadgets of all categories will be imported and listed
on the left panel.

Viewing/Editing detailed information of a portlet/gadget
--------------------------------------------------------

**Viewing a portlet**

To view details of a portlet/gadget, simply select one portlet/gadget in
the left panel. The details of that portlet/gadget will be shown on the
right panel.

|image271|

**Left panel** |image272|
    All portlets and gadgets grouped by categories.

**Breadcrumb bar** |image273|
    The path of the portlet/gadget.

**Right panel** |image274|
    Details of the portlet: Name, Display Name, Description, and
    information on the Access permission.

Editing a portlet
``````````````````

1. Click |image275| on the top corner of the right panel.

The Edit Application Information form will appear.

|image276|

2. Make changes on the fields in the form, except Application Name.

3. Click Save to commit your changes.

.. _EditingSpecificPortlet:

Editing a specific portlet
--------------------------

This section tells you how to access the Edit mode of a portlet and edit
it.

1. Define your desired portlet to check if this portlet has been existing
   in the portal or page. If not, drag and drop it from **Edit Inline
   Composer** to the main portal body while :ref:`editing the portal's layout <EditingLayout>`
   or :ref:`editing a page. <ManagingPages.EditingPage>`

2. Hover your cursor over your desired portlet, then click |image277| 
   at the upper left corner of that portlet.

   The Edit form will be displayed.
   
   |image278|

Normally, a portlet has four tabs: Portlet Setting, Select Icon,
Decoration Themes and Access Permission. However, some portlets may also
have Edit Mode and Preferences tabs. For example, IFrame and Dashboard
portlets have the Edit Mode tab where administrators can define the
interface details.

4. Make changes on fields in the various tabs.

-  The Portlet Setting tab allows you to change values related to
   settings of your selected portlet.

   **In which:**

   +-----------------------+----------------------------------------------------+
   | Field                 | Description                                        |
   +=======================+====================================================+
   | Display Name          | The display name of portlet which cannot be        |
   |                       | changed.                                           |
   +-----------------------+----------------------------------------------------+
   | Portlet Title         | The portlet title with the length between 3 and 60 |
   |                       | characters.                                        |
   +-----------------------+----------------------------------------------------+
   | Width                 | The portlet's vertical size. The value of this     |
   |                       | field must be in numeric format.                   |
   +-----------------------+----------------------------------------------------+
   | Height                | The portlet's horizontal size. The value of this   |
   |                       | field must be in numeric format.                   |
   +-----------------------+----------------------------------------------------+
   | Show Info Bar         | The option enables the information bar to be shown |
   |                       | or hidden. If the Show Info Bar checkbox is not    |
   |                       | selected, Portlet Mode and Window State will not   |
   |                       | be displayed in that portlet.                      |
   +-----------------------+----------------------------------------------------+
   | Show Portlet Mode     | The option enables the portlet mode to be shown or |
   |                       | hidden.                                            |
   +-----------------------+----------------------------------------------------+
   | Show Window State     | The option enables the portlet's window state to   |
   |                       | be shown or not.                                   |
   +-----------------------+----------------------------------------------------+
   | Description           | The brief information of the portlet. The length   |
   |                       | must be between 0 and 255 characters.              |
   +-----------------------+----------------------------------------------------+

-  The Select Icon tab allows you to select an icon for the portlet. By
   clicking Get Default, you do not have to select any icon from the
   list, the suitable icon will be got automatically.

-  The Decoration Themes tab allows you to select a theme for the
   portlet from the themes list. By clicking Get Default, you do not
   have to choose any theme, it will be automatically set.

-  The Access Permission tab allows you to set the access permission on
   the portlet. The portlet can be made public to everyone or restricted
   to specific groups.

.. note:: If you set the \* permission to a group, all users of that group will have the right to view this portlet, regardless of their membership role. 
	      See the :REF:`Setting Access permission on a portlet <ManagingPermissions.SettingAccessPermissionOnPortlet>` section for details on how to assign the access permission on a portlet.

4. Click Save And Close to accept your changes, then click |image279| to
   quit the Edit Inline Composer/ Page Editor page.

.. _ManagingPortletsAndGadgets.AddingGadget:

Adding a gadget
---------------

To add a gadget, you first need to access the **Gadget** page by
selecting Gadget on the **Tab** bar of the **Manage Applications** page.

|image280|

You can add a remote gadget using its URL or create a new gadget into
the list.

Adding a remote gadget
```````````````````````

1. Click the Add a remote gadget link.

2. Enter the link of your desired gadget which is in the *.xml* format 
   in the URL field.

|image281|

3. Click Add to accept your inputted URL.

The selected gadget will be added to the gadgets list in the left panel
with its details in the right panel.

Creating a new gadget
``````````````````````

1. Click the Create a new gadget link.

2. Enter values in the form.

For example:

|image282|

3. Click Save to accept creating your new gadget.

.. note:: To add the newly added remote gadget to a specific category, simply click the "Click here to add into categories" link at the bottom of the right panel. The table listing all categories will appear and allow you to select your desired category.

		  To update information of the added gadget, simply click |image283| to refresh information.

-  You can delete a local gadget using |image284| corresponding to each
   gadget in the left gadgets list.

Adding a new gadget from Dashboard
``````````````````````````````````

See the :ref:`Adding more external gadgets from Dashboard <add-more-external-gadgets>`
section for instructions on how to add new gadgets from the dashboard.

.. _ManagingPortletsAndGadgets.EditingGadget:

Editing a gadget
----------------

1. Select your desired gadget in the left panel, for example Group
   Navigations, then click |image285| located at the header of the 
   **Gadget Details** page to display the following window.

|image286|

2. Makes changes in the XML Source Code.

3. Click Save to commit your changes.

.. note:: You cannot change the Name field.


.. _ManagingApplications.ManagemenentAndMonitoringGadgets:

Management and Monitoring Gadgets
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The **Management** and **Monitoring** gadgets include gadgets designed
for providing the overall vision of the system. These gadgets monitor
the system and provide the current system performance statistics which
are especially useful for the system administrators and developers.

.. _MonitoringGadgets:

Monitoring gadgets
-------------------

eXo Platform provides 3 types of the Monitoring gadget:

-  Memory

-  Caches level

-  Application Statistics

You can use these gadgets from the Dashboard Workspace. However, you can
quickly use them via the Monitoring page by clicking Administration -->
Administration --> Monitoring on the top navigation bar.

|image287|

Memory
```````

The Memory gadget provides the statistics of heap and non-heap memory
via charts which show the part of used memory and remaining memory
during runtime.

|image288|

In the table next to the chart, you can see:

-  Used: The total used memory.

-  Free: The total free memory.

-  Total: The total memory.

Caches level
`````````````

The Caches level gadget displays the eXo cache levels and settings.
Based on these statistics, the administrators can configure the cache
settings properly to get better performance:

-  If the cache is full but the hit ratio is low (or missed ratio is
   high), it means the cache is full of unnecessary data. It should be
   cleared and/or its size is increased, or its lifetime is decreased.

-  If the cache is full and the hit ratio is high, this is good. It
   means most of data are retrieved from the cache, but not from the
   database, so the system gets better performances.

-  If the cache is empty, it should be configured differently, for
   example, increasing its lifetime.
   
   |image289|

-  The Consumption tab shows the overall cache consumption in the
   system.

-  The Hit ratio tab shows the ratio between requested data fetched from
   cache and data fetched from database.
   
   |image290|

The Details tab shows the cache level and the current cache settings.

|image291|

In which:

-  Max size: The maximum size of the cache.

-  Time to live: The lifetime (in seconds) of cache entries before being
   cleared.

-  Hit/Missed: The percentage of data fetched from cache versus the
   percentage of data fetched from database.

Application Statistics
```````````````````````

The Application Statistics gadget lists all information related to the
execution time of all applications in the portal, therefore
administrators and developers will know how fast applications are and
which ones should be optimized.

|image292|

The gadget consists of two tabs:

-  10 Slowest: Lists 10 slowest applications in the portal.

-  All: Shows the total number of applications and a list of the
   applications in the portal.

Each application provides you with the following information:

-  The execution phase next to the application name (if any). For
   example: AllSpacesPortlet/ACTION\_PHASE

-  The full path of the application when you hover your cursor over its
   name.

-  The average execution time (in ms) highlighted next to the
   application name.

   -  The time will be highlighted with the yellow color if it is more
      than 1000 ms and less than 5000 ms.

   -  The time will be highlighted with the red color if it is more than
      5000 ms.

-  exec: The number of executions of the application.

-  min: The minimum execution time of the application.

-  max: The maximum execution time of the application.


.. _ServiceManagement:

Service Management
-------------------

The Service Management gadget provides an interface to interact with
manageable services via REST management API.

You can use these gadgets from the Dashboard Workspace. However, you can
quickly use them via the Service Management page by clicking
Administration --> Administration --> Management on the top navigation 
bar.

The Service Management page is displayed.

|image293|

-  Select the service from the **Services** drop-down list. For each
   selected service, its respective methods and properties are shown.

   To invoke a method of the selected service, click Run corresponding
   to it. After invoking it successfully, you will see the result
   returned if any.






