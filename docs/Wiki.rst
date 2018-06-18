.. _Wiki:

####################
Working With Wikis
####################


    The **Wiki** application provides the content productivity to portal
    users as a tool to forge the unstructured knowledge. With **Wiki**,
    you can create and edit pages by using a simplified markup language
    or a WYSIWYG editor. Also, your company can use **Wiki** as an
    internal reference, such as work policy or a public wiki for
    comprehensive product information. **Wiki** along with **Forums**
    will complete the ideal combination that helps users enhance their
    experiences on collaboration activities and build valuable knowledge
    center for clients.

    This chapter covers the following topics:

:ref:`Managing your content <Managing-Content>`

       Steps to perform common actions on a Wiki page (for example,
       creating, editing, using the editor, managing drafts, adding a
       related page, and attaching files); information about spreading
       your content; how to manage page changes (by comparing between 2
       versions or by watching); and ways to organize your content.

:ref:`Advanced settings <AdvancedSettings>`

       Steps specified for administrators to change space settings,
       manage permissions and author content via WebDAV.

.. _Wiki-layout:

**Wiki layout**


After opening Wiki, you should see the Wiki homepage as below:

|image7|

**In which**:

-  |image0|: The **Breadcrumb** which shows the page hierarchy.

-  |image1|: The Wiki administration area which allows administrators
   only to configure the Wiki settings.

-  |image2|: The **Search** box.

-  |image3|: The pages tree view.

-  |image4|: The **Page Control** area which helps users take actions
   with the current page.

-  |image5|: The page content.

-  |image6|: The page information. Click **number of attachment(s)** to
   open the **Attachments** details panel at the bottom of the page.
   Click **Public** or **Restricted** to update the permissions of the
   page.

.. _Navigate-across-spaces:

**Navigating across spaces**


The breadcrumb in Wiki shows the :ref:`page hierarchy <Page-hierarchy-wiki>` to
help you know where you are staying. Additionally, you can navigate to
another space right in the breadcrumb of the current Wiki navigation. To
quickly switch to another space, simply click the currently browsed
space name:

Type your desired space name in the search box to filter the space and
click your space name from the search results. Then you will be
redirected to the Wiki home of the selected space. The "**My Wiki**\ "
and "**Intranet**\ " are displayed by default, which will direct you to
the homepage of your personal Wiki and Intranet Wiki accordingly.


.. note::Only spaces where you are their member are displayed in the search result.

.. _Page-hierarchy-wiki:

**Page hierarchy in Wiki**


The **Wiki** content is organized as a page tree in which each page may
contain many sub-pages. The hierarchy is reflected on UI by the
**Breadcrumb** and the page tree in the left pane. When a page is added,
it is always defined as a sub-page to the current one. You can have
wikis for portals, wikis for groups or users.

.. _Wiki-spaces:

**Wiki Spaces**

Space is a set of pages, so the spaces partitioning means that spaces
are independent trees. This separation enables **Wiki** to provide
knowledge spaces for different groups.

There are 3 space types:

-  **Intranet wiki**: The global wiki of the Social Intranet.

An Intranet wiki is published for every user who can access that portal.

-  **Group wiki**: The wiki of a space.

A group wiki can be understood as a space wiki. The wiki application of
a space works as a group wiki for that space. The group wiki can be
accessed by members of that group.

For example:

-  **User wiki**: The wiki of an individual user.

Every user has his own Wiki. You can switch to **My Wiki** from the
Select Location drop-down menu or from the drop-down menu of the display
name. See :ref:`Working with your wiki <Working-Wiki>` for more details.

.. note:: In this document, Spaces are referred as wikis, particularly portal
			wikis, group wikis and user wikis.
			Any space which has an implicit root page is named Wiki Home.

.. _Managing-Content:

======================
Managing your content
======================

The section consists of the following topics:

:ref:`Adding and editing pages <Adding-Editing-Wiki-Page>`

   Instructions on how to add and edit a Wiki page.

:ref:`Spreading your content <Spreading-Content>`

   Instructions on how to share your content with others by publishing
   your content on the Activity Stream, sharing a link or exporting a
   page as PDF.

:ref:`Managing page changes <ManagingContentChanges>`

   Instructions on how to manage versions of a Wiki page and watch a Wiki page.

:ref: `Organizing your content <Organizing-Content>`

   Instructions on how to move/delete a Wiki page.
   
.. _Adding-Editing-Wiki-Page:

Adding and editing pages
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section shows you how to work with Wiki pages via the following
topics:

:ref:`Creating a page <Creating-New-Page>`

:ref:`Editing a page <Editing-Page>`

:ref:`Using WYSIWYG editor (Rich Texteditor) <Editors>`

:ref:`Managing drafts <Managing-Page-Drafts>`

:ref:`Adding a related page <Adding-Related-Page>`

:ref:`Working with attachments <Working-With-Attachments>`

.. _Creating-New-Page:

Creating a page
------------------

**Creating a blank page**

1. Go to a Wiki space in which you want to create a page.

2. Click Add Page, then select Blank Page.

|image9|

3. Enter the title for your page. The page title must be unique.

4. Enter the content of your page by using **`Wiki Markup <#PLFUserGuide.WorkingWithWikis.ManagingContent.AddingAndEditingPages.UsingTheRichTextEditor.UsingSourceEditor.SyntaxHelp>`**
or the
**`WYSIWYG <#PLFUserGuide.WorkingWithWikis.WorkingWithWikis.ManagingContent.AddingAndEditingPages.UsingTheRichTextEditor.UsingWYSIWYGEditor>`**
editor.

5. Click Preview if you want to see how your page looks like.

6. Click Save to finish.

**Creating a page from template**

1. Go to a Wiki space in which you want to create a page.

2. Click Add Page, then select From Template....

A list of available templates will appear.

|image10|

You can:

**i.** Click |image8| corresponding to the template you want to see. The
template preview appears.

|image11|

**ii.** Tick the checkbox corresponding to the template you want to select for your new page and click Select. The selected template appears.

3. Enter the title for your page. The page title must be unique.

4. Enter the content of your page by using **`Wiki
Markup <#PLFUserGuide.WorkingWithWikis.ManagingContent.AddingAndEditingPages.UsingTheRichTextEditor.UsingSourceEditor.SyntaxHelp>`**
or the
**`WYSIWYG <#PLFUserGuide.WorkingWithWikis.WorkingWithWikis.ManagingContent.AddingAndEditingPages.UsingTheRichTextEditor.UsingWYSIWYGEditor>`**
editor.

5. Click Preview if you want to see how your page looks like.

6. Click Save to finish.

.. note:: These templates can be created, edited and deleted by administrator.
			See the `Managing a page template <#PLFUserGuide.WorkingWithWikis.AdvancedSettings.ManagingPageTemplate>` section for more details.

**Adding an undefined link for creating a page later**

In the **Wiki** application of eXo Platform, you can add a link pointing to a
page which you are going to create later. Such links are called
undefined links which are often used to remind other **Wiki** users to
create the page. You must use the `Source
editor <#PLFUserGuide.WorkingWithWikis.ManagingContent.AddingAndEditingPages.UsingTheRichTextEditor.UsingSourceEditor>`
to create the undefined links.

1. Add a link by typing the page title between square brackets '[[...]]'
into your page body.

For example:

+----------------------+----------------+
| What you type        | What you get   |
+======================+================+
| [[eXo User Guide]]   |                |
+----------------------+----------------+

2. Click Save to save the page containing the link. The undefined link is
underlined.

3. Click this link to open the Add Page form.

4. Follow the steps stated `above <#PLFUserGuide.BuildWiki.WorkWithWikiPages.ManagingContent.AddingAndEditingPages.CreatingPage.FirstWay>`
to enter the page title, content and save the page.

.. _Editing-Page:

Editing a page
----------------

You can edit a page at any time if you have the **Edit** permission on
that page.

**Editing the whole page content**

To edit the whole page content, click Edit in the Page Control area.
Your page will be switched to the **Edit** mode which allows you to
rename the page and edit the page content.

|image13|

The toolbar in the **Edit** mode will be changed to activate the following actions.

|image14|

**Details:**

+--------------------+--------------------------------------------------------+
| Item               | Description                                            |
+====================+========================================================+
||image15|           | Switches to the **Rich Text (WYSIWYG)** editor.        |
+--------------------+--------------------------------------------------------+
|                    | Displays the preview mode of the currently edited      |
||image16|           | content. Previewing a page helps you verify the result |
|                    | of rendering the markup you just entered without       |
|                    | saving.                                                |
+--------------------+--------------------------------------------------------+
||image17|           | Opens the Wiki syntax help panel.                      |
+--------------------+--------------------------------------------------------+
||image18|           | Shows more syntax help.                                |
+--------------------+--------------------------------------------------------+
||image19|           | Ticks the Publish Activity checkbox to publish your    |
|                    | content modification on Activity Stream after saving   |
|                    | your changes                                           |
+--------------------+--------------------------------------------------------+
||image20|           | Inputs the edit reason if necessary.                   |
+--------------------+--------------------------------------------------------+
|                    | Saves the current page and go back to the view mode.   |
|                    | Changes will be sent to watchers via mail              |
||image21|           | notification.                                          |
+--------------------+--------------------------------------------------------+
|                    | Discards the current changes and go back to the        |
||image22|           | **View** mode.                                         |
+--------------------+--------------------------------------------------------+

**Editing a page section**

To edit only a section in the whole page content, hover your cursor over
the title of the section you want to edit, then click |image12|.

|image23|

The selected section will be switched to the **Edit** mode.


.. tip::    In the **View** mode, you can quickly edit the page title by double-clicking it, then press **Enter** when finishing.





.. |image0| image:: images/common/1.png
.. |image1| image:: images/common/2.png
.. |image2| image:: images/common/3.png
.. |image3| image:: images/common/4.png
.. |image4| image:: images/common/5.png
.. |image5| image:: images/common/6.png
.. |image6| image:: images/common/7.png
.. |image7| image:: images/wiki/overview.png
.. |image8| image:: images/wiki/preview_template_icon.png
.. |image9| image:: images/wiki/add_page.png
.. |image10| image:: images/wiki/template.png
.. |image11| image:: images/wiki/template_preview.png
.. |image12| image:: images/common/edit_icon.png
.. |image13| image:: images/wiki/page_control.png
.. |image14| image:: images/wiki/page_edit.png
.. |image15| image:: images/common/1.png
.. |image16| image:: images/common/2.png
.. |image17| image:: images/common/3.png
.. |image18| image:: images/common/4.png
.. |image19| image:: images/common/5.png
.. |image20| image:: images/common/6.png
.. |image21| image:: images/common/7.png
.. |image22| image:: images/common/8.png
.. |image23| image:: images/wiki/edit_section.png
