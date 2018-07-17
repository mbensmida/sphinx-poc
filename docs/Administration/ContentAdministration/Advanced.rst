.. _WorkingWithAdvancedConfiguration:

Working with Advanced configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

From the Manage ECM Main Functions panel, select Advanced.

|image104|

Here you can manage:

-  :ref:`Categories <WorkingWithAdvancedConfiguration.Categories>`

-  :ref:`Queries <WorkingWithAdvancedConfiguration.Queries>`

-  :ref:`Scripts <WorkingWithAdvancedConfiguration.Scripts>`

-  :ref:`Actions <WorkingWithAdvancedConfiguration.Actions>`


.. _WorkingWithAdvancedConfiguration.Categories:

Categories
-----------

A category can be understood as a classification practice and science.
It is used to sort documents, aiming at facilitating searches. The
category management includes adding, editing and deleting a category
tree.

In Advanced, select Categories. You will be directed to the
**Categories** panel as below:

|image105|

Here, you can do the following actions:

-  :ref:`Editing a category tree <Categories.EditingCategoryTree>`
   |image106|

-  :ref:`Deleting a category tree <Categories.DeletingCategoryTree>`
   |image107|

-  :ref:`Adding a category tree <Categories.AddingCategoryTree>`
   |image108|
   
.. _Categories.EditingCategoryTree:   

Editing/Deleting a category tree
`````````````````````````````````

**Editing a category tree**

1. Click |image109| in the Action column to open the Edit Category Tree 
   form.

|image110|

2. Click |image111| in the Add column to add more category trees. The 
   mini Edit Category Tree form will appear.

|image112|

3. Enter a category name in the Category Name field which is required.

.. note:: The category name must not contain more than 150 characters.

4. Click Save to save the category name.

5. Click Previous to return to the previous steps.

6. Click Save to save all changes, or Previous or Next if you want to 
   edit more.

.. _Categories.DeletingCategoryTree:

**Deleting a category tree**

Simply click |image113| in the Action column, then select **OK** in the
confirmation message.

.. _Categories.AddingCategoryTree:

Adding a category tree
````````````````````````

1. Click Add Category Tree to open the Add Category Tree form.

|image114|

2. Enter the category tree name in the Name field which is required.

3. Select the workspace you want to work with.

4. Select the home path by clicking |image115|. The Select Home Path 
   form will appear.

|image116|

-  Click |image117| next to Root Path if you want to select the root path
   or;

-  Click the arrow icon to go to the up level path and click the plus
   sign to expand the folder in the left pane.

   Click |image118| corresponding to the path that you want to select as
   a home path.

5. Click Next to select permissions for the category tree.

|image119|

-  **i.** Click |image120| or |image121| or |image122| to set 
   permissions for user, membership or everyone respectively. Your 
   selected user or membership will be displayed in the User or Group 
   column.

.. note:: When ticking any permissions above (Read, Add Node or Remove), if you set the \* membership for a group, this permission will be granted to all users of the group, regardless of their membership role.

-  **ii.** Check the right options for the selected user to membership:

.. note:: Ticking only Add Node Right or Remove Right means that Read Right is selected automatically.

6. Click Save to save all values, or Reset to change values that have 
   just been set. After clicking Save, click Next to go to the next step.

|image123|

7. Enter the name for an action of the category tree in the Name field
   which is required.

8. Select values for Lifecycle, Node Types, Target Workspace, Target Path,
   Affected Node Types which are required.

9. Click Save to commit all values.

.. note:: -  Do not input some special characters into the Name field, such as: ``!,#,$,&,\*,(,)``.

		  -  Do not add a category which has the same name and level with existing taxonomies in a node.


.. _WorkingWithAdvancedConfiguration.Queries:

Queries
---------

In Advanced, select Queries. You will be directed to the **Queries**
panel as below:

|image124|

Here, you can do certain actions on the queries as follows:

-  :ref:`Editing a query <Queries.EditingQuery>` |image125|

-  :ref:`Deleting a query <Queries.DeletingQuery>` |image126|

-  :ref:`Adding a new query <Queries.AddingNewQuery>` |image127|

.. _Queries.EditingQuery:

Editing a query
`````````````````

1. Click |image128| in the Action column to open the Edit Query form.

|image129|

2. Edit the properties of the selected query.

.. note:: In the *Permissions* field, if you set the \* membership for a group, all users of the group will be able to access this saved query, regardless of their membership role.

3 .Click Save to accept all changes.

.. _Queries.DeletingQuery:

Deleting a query
``````````````````

Simply click |image130| in the Action column, then select **OK** in the
confirmation message.

Adding a new query
`````````````````````

1. Click Add Query to open the Add Query form.

|image131|

2. Enter a query name into the Query Name field that is required.

3. Select the query type from the Query Type drop-down menu.

-  xPath (XML Path Language) is a language for selecting nodes. For
   example, ``/jcr:root/Documents/Live``.

-  SQL (Structured Query Language) is a database computer language.

4. Enter the statement for the query that must be unique.

5. Check or uncheck the Enable Cache Results option. If you tick this
   checkbox, for the first time you use this query to search, the result
   will be cached. For the second time you search using this query, it 
   will show the cached results. After 10 minutes, the cache will be 
   removed.

   For example, you have the **Test** query with the **//element (\*,
   nt:file)**. In Sites Explorer, you have a ``nt:file`` document named
   ``File1``. When you execute the query ``Test``, only the ``File1``
   document is shown. After that, create a ``nt:file`` document named
   ``File2`` and execute the query ``Test``, only the ``File1`` document 
   is listed. After 45 minutes, the cache will be removed. When you 
   execute the query ``Test``, ``File1`` and ``File2`` will be listed.

6. Select permissions for a group that can use this query by clicking
   |image132|.

.. note:: In the *Permissions* field, if you set the \* membership for a group, all users of the group will be able to access this saved query, regardless of their membership role.

7. Click Save to finish adding a new query.


.. _WorkingWithAdvancedConfiguration.Scripts:

Scripts
--------

In Advanced, select Scripts. You will be directed to the **Scripts**
panel as below:

|image133|

The Scripts panel has 3 tabs:

-  Actions which is for action scripts.

-  Interceptors which is for dialog interceptors.

-  Widgets which is for widget scripts.

Here, you can do certain actions on the scripts as follows:

-  :ref:`Editing a script <Scripts.EditingScript>` |image134|

-  :ref:`Deleting a script <Scripts.DeletingScript>` |image135|

-  :ref:`Adding a new script <Scripts.AddingNewScript>` |image136|

.. _Scripts.EditingScript:

Editing a script
`````````````````

**Editing a script**

1. Click |image137| in the Action column to open the Add/Edit Script 
   form.

|image138|

2. Edit the properties in this form.

3. Click Save to save all changes.

.. _Scripts.DeletingScript:

Deleting a script
``````````````````

Simply click |image139| in the Action column, then click **OK** in the
confirmation message.

.. _Scripts.AddingNewScript:

Adding a new script
````````````````````

1. Click Add Script to open the Add/Edit Script form.

2. Enter values for the Content, Name and Script fields.

.. note:: The value for the Script field must be unique and not contain special characters, such as ``!,#,$,&,\*,(,)``.

3. Click Save to accept adding your new script.

.. _WorkingWithAdvancedConfiguration.Actions:

Actions
--------

This function allows you to manage all action nodes in eXo Platform. In
Advanced, select Actions to open the **Actions** panel.

|image140|

Here, you can do certain actions as follows:

-  :ref:Editing an action <Actions.EditingAction>` |image141|

-  :ref:Deleting an action <Actions.DeletingAction>` |image142|

-  :ref:Adding an action type <Actions.AddingActionType>` |image143|

Editing an action
```````````````````

1. Click |image144| in the Action column to open the Add Action Type 
   form.

2. Edit the properties in this form.

3. Click Save to save all changes.

Deleting an action
```````````````````

Simply click |image145| in the Action column, then select **OK** in the
confirmation message.

Adding an action type
``````````````````````

1. Click Add Action Type to open the Add Action Type form.

|image146|

2. Input a name for the action.

3. Select the script type.

4. Enter the value for the Variables field.

-  Click |image147| to add more values for the action.

-  Click |image148| to delete one value.

5. Click Save to accept adding a new action type.





