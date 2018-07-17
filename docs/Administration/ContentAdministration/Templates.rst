.. _WorkingWithTemplates:

Working with Templates
~~~~~~~~~~~~~~~~~~~~~~~

When creating content in eXo Platform, you must set its properties. 
Thus, each content needs to have a form to enter data for its properties
(called the **Dialog** template), and display the existing values
(called the **View** template). In the templates management, you are
able to view, edit and delete the predefined templates or to add a new
template.

From the Manage ECM Main Functions panel, select Templates.

|image20|

eXo Platform provides 3 available template types, including:

- :ref:`Documents <WorkingWithTemplates.DocumentTemplates>`: Manages 
  view, dialog and CSS templates of document types.

- :ref:`List <WorkingWithTemplates.ListTemplates>`: Manages Content List
   Viewer templates.

- :ref:`Metadata <WorkingWithTemplates.MetadataTemplates>`: Manages view
   and dialog templates of metadata node types.

.. _WorkingWithTemplates.DocumentTemplates:

Document templates
-------------------

In Templates, select Documents to open the Documents panel.

|image21|

The Documents templates are categorized into 3 sub-tabs that makes ease
for management. You can use default templates provided by PRODUCT in
each sub-type or define a new template.

-  The Documents tab includes **Contact Us**, **Product**, **Accessible
   Media**, **Announcement**, **CSS File**, **HTML File**, **Javascript
   File**, **Web Link**, **Illustrated Web Content**, **Web Content**,
   **File**, **Accessible Breadcrumb**, **Accessible Navigation**, and
   **Accessible Site Search Box**.

-  The Actions tab includes **Add Metadata Action**, **Automatic
   Versioning**, **Enable Versioning**, **Populate to Menu**, and **Add
   Category Action**.

-  The Others tab includes **Comments**, **Votes**, and **File
   Content**.

.. note:: -  **Contact Us** and **Product** are for the ACME site, so these templates only appear when the ACME site is enabled.
		  -  **Accessible Breadcrumb**, **Accessible Navigation** and  **Accessible Site Search Box** are for the WAI site, so these templates only appear when the WAI site is enabled.
		  -  **Populate to Menu** only appears in the list of Action templates when the ACME site is enabled.

Editing/Deleting a Document template
``````````````````````````````````````

**Editing a Document template**

1. Select the template type tab (Documents, Actions or Others).

2. Click |image22| corresponding to your desired template in the Action
   column.

The View & Edit Template form appears.

|image23|

3. Make changes on the values of each tab, including:

-  In the Template tab, you can edit the label of the template. The is
   Document Template checkbox is selected by default when you select the
   Documents tab. However, this checkbox is disabled by default when you
   select the Actions or Others tab.

-  In the Dialog tab, you can add a dialog, edit or delete an existing
   dialog. Besides, you can set permission to use the dialog form for a
   specific group and membership. Setting the \* membership will allow
   all users of the group to have this permission. For more details, see
   `Dialogs <../../../reference/html/PLFRefGuide.PLFDevelopment.TemplateConfiguration.Content.ContentTypes.Dialogs.html>`__.

-  In the View tab, you can add a view, edit or delete an existing view.
   Besides, you can set permission to view the template for a specific
   group and membership. Setting the \* membership will allow all users
   of the group to have this permission. For more details, see
   `Views <../../../reference/html/PLFRefGuide.PLFDevelopment.TemplateConfiguration.Content.ContentTypes.View.html>`__.

-  In the CSS tab, you can add a new stylesheet, edit or delete an
   existing stylesheet.

.. note:: -  You cannot delete the default dialog/view.
		  -  You cannot change the dialog/view/CSS name.
		  -  If you click Enable Versioning or Versioning activated checkbox, the edited dialog/view/CSS automatically increments one version after you have clicked **Save**. It is displayed at the Version column.
		  -  After the dialog/view/CSS has been enabled versioning, you will see the Versions field and the Restore button at the bottom of the form. You can use Restore to roll back to a selected version.

**Deleting a Document template**

Simply click |image24| corresponding to the template you want to remove,
then select **OK** in the confirmation message.

Adding a new document template
```````````````````````````````

1. Select the template type tab (Documents, Actions or Others).

2. Click Add Template at the bottom to open the Template Form window.

|image25|

.. note:: The is Document Template checkbox is selected by default when you select the Documents tab. However, this checkbox is disabled by default when you select the Actions or Others tab.

3. Select the template type from the Name drop-down menu.

4. Specify a name for the template in the Label field.

5. Click |image26| next to the Permission field to open the Select
   Permission dialog.

6. Optionally, select the Dialog tab, View, and/or CSS and enter the 
   value in the input-text box.

7. Click Save to create the template.

.. _WorkingWithTemplates.ListTemplates:

List templates
---------------

In Templates, select List to open the List panel. There are 3 types of
List (also called CLV) templates: Content, Navigation and Paginator.

|image27|

Editing/Deleting a List template
`````````````````````````````````

**Editing a List template**

1. Click |image28| corresponding to your desired template in the Action
   column.

The Edit List Template form appears.

|image29|

2. Make any changes on fields: Content, Name, or change the template 
   type from the Template Type drop-down menu.

.. note:: You cannot change the Template Name field.

**Deleting a List template**

Simply click |image30| corresponding to the template you want to remove,
then select **OK** in the confirmation message.

Adding a new List template
```````````````````````````

1. Click Add Template at the bottom to open the Add List Template window.

|image31|

2. Add values to the Content, Name, Template Name fields and select the
   template type from the Template Type drop-down menu.

.. note:: After creating your new List template, you cannot edit the Template Name field.

3. Click Save to finish adding your new list template, or Reset to clear
   your entered values.

.. _WorkingWithTemplates.MetadataTemplates:

Metadata templates
-------------------

Metadata are information which describes, or supplements the central
data. When data are provided to end-users, the metadata allow users to
understand about information in details.

In Templates, select Metadata to open the Metadata panel.

|image32|

**Viewing a Metadata template**

Simply click |image33| corresponding to the metadata you want to view.

The Metadata Information form will open.

|image34|

**Editing a Metadata template**

1. Click |image35| corresponding to your desired template in the Action
   column.

The Edit Metadata's Template form appears.

|image36|

2. Change the required properties of the metadata.

.. note:: You cannot edit the metadata name.

3. Click Apply to save all metadata changes.

**Deleting a Metadata template**

Simply click |image37| corresponding to the template you want to remove,
then select **OK** in the confirmation message.






