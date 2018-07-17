.. _CustomizingLookAndFeel:

==============================================
Customizing the look and feel of eXo Platform
==============================================

As a web-contributor or an administrator, you can easily customize the
look and feel of eXo Platform by editing the existing
``Globalstylesheet.css`` file or creating a new global stylesheet and
applying it into the portal.

Global stylesheet is a shared one which is applied into your entire
site. Global stylesheets of eXo Platform are put into the css folder to
manage the stylesheet of your desired site. This section aims at showing
you how to create and apply your own global stylesheet through **Sites
Explorer**.

This section covers the following topics:

-  :ref:`Creating a global stylesheet <CreatingGlobalStylesheet>`
   Detailed instructions on how to create, edit and rename a global
   stylesheet.

-  :ref:`Checking the display <CheckingDisplayOfGlobalStylesheet>`
   Steps to activate a global stylesheet and check its display.

.. _CreatingGlobalStylesheet:

Creating a global stylesheet
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Click |image5| Content Sites Explorer on the top navigation bar.

2. Select the Sites Management drive in the drives list.

3. Select a site in the Sites Management panel, for example, ``agital``, 
   then select the css folder.

4. Click |image6| to open the CSS File form which allows creating a new
   global stylesheet.

|image7|

5. Enter the name of global stylesheet into the Name field, for example,
   ``GlobalStylesheet\_Orange``.

6. Set the value as "True" in the Active field to activate your global
   stylesheet for your site. "True" is set by default when a new global
   stylesheet is created. If you select "False", your newly created 
   global style will be disabled.

7. Input one positive integer into the Priority field, for example "10".

8. Define your styles in the ``CSS Data`` field. Here, you can directly
   enter your CSS rules, or copy and paste them from your favorite text
   editor.

   For example, you can define your styles with the following 
   information:

|image8|

Click Save or Save & Close to save your newly created global stylesheet.
You will see your global stylesheet in the Sites Management panel.

|image9|

.. note:: -  The values in both of the Active and Priority fields decide if your newly created global stylesheet is applied into your site 
             successfully or not. If the Active field is set to "True" in many global stylesheets, the system will automatically merge all 
             the global stylesheets into the ``${site-name}/Default/Stylesheet-min-lt.css`` file of the css folder in the ascending order 
             and get the stylesheet with the highest priority. Thus, after selecting "True", to make sure that your stylesheet is applied, 
             you need to pay attention to the priority level so that the selected priority of your stylesheet is higher than those of other 
             global stylesheets in the css folder.

		  -  The default global stylesheet will be automatically created in the css folder when you create a new site. However, this global
             stylesheet can be overwritten by either setting "False" for its Active field or setting the higher priority for other global
             stylesheet than that of the default global stylesheet.

		  -  When you want to create a common stylesheet to share for all sites in the portal, you should create one in the 
		     Sites Management/shared/css folder. This stylesheet will be rendered and applied into your desired site when you switch to it.

.. _EditGlobalStylesheet:

Editing a global stylesheet
----------------------------

Simply select your desired global stylesheet and click Edit on the
action bar, or right-click the file and select Edit from the drop-down
menu to open the CSS File form.

.. _RenameGlobalStylesheet:

Renaming a global stylesheet
-------------------------------

Simply right-click your desired global stylesheet in the Sites
Management panel, then select Rename.

.. _CheckingDisplayOfGlobalStylesheet:

Checking the display
~~~~~~~~~~~~~~~~~~~~~

You can have several global stylesheets in one site. To see differences
when applying various global stylesheets, for example,
``GlobalStylesheet_Blue`` and ``GlobalStylesheet_Orange``, do as
follows:

1. Activate the ``GlobalStylesheet_Blue`` and ``GlobalStylesheet_Orange``
   files by turns.

2. Open your desired site by entering its URL in the address bar, for
   example, opening the intranet site: ``http://{domain-name}/portal/intranet``.

.. note:: The two GlobalStylesheet\_Blue and GlobalStylesheet\_Orange should been added to ``/intranet/css`` folder.


-  If you activate ``GlobalStylesheet_Blue``, your site is as below:

   |image10|

-  If you activate ``GlobalStylesheet_Orange``, your site is as below:

   |image11|


