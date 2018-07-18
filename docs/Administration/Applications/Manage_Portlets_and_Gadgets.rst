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


