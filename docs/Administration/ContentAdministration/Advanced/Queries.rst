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


