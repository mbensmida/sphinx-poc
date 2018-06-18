.. _Manage-view:

==============
Managing views
==============

eXo Platform supports two views which are:

* :ref:`List view <list-View>`
* :ref:`Board view <Board-View>`


.. _list-View:

list View
~~~~~~~~~~

By default, when you access any item on the left pane, the corresponding
tasks in the central pane will be displayed in a simple list like this:

|image73|

In which:

-  The **!** symbol in red indicates overdue tasks that have not been
   completed on time.

-  The **!** symbol in blue indicates tasks that need to be done today.

In this view, you can do the followings:

Marking a task as completed:
-----------------------------

Hover cursor over the task that you want to mark it as completed and
click the tick icon that appears:

|image74|

The task will disappear from the List view unless
:ref:`Filter <Filtering>` is set to show completed tasks.

.. _sort-tasks-list-view:

Sorting/Grouping tasks
-----------------------

At the top right corner of the central pane, there are two options under
the top filter that help you to sort and group tasks in categories.

|image75|

You can arrange these tasks by the following options:

-  *Created Date*: sorts by the created date of tasks, with the most
   recent tasks on top.

-  *Due Date*: sorts by the due date of tasks, with the oldest tasks on
   top.

-  *Title*: sorts by the task titles in alphabetical order.

-  *Priority*: sorts by the task priority, with the highest on top.

-  *Rank*: sorts by the task rank.

In addition to sorting tasks by the above options, you can also group
the tasks by:

-  *Assignee*: groups by the tasks' assignee.

-  *Label*: groups by the tasks' label.

-  *Due Date*: groups by the tasks' due date.

-  *Project*: groups by projects.

-  *Status*: groups by the tasks's status in a project.

-  *None*: ungroups tasks.

.. note:: Depending on the view you select from the left pane, such as Task
			filters, Projects or Labels views, some of the options above may be disabled.


.. _Board-View:

Board view
~~~~~~~~~~~~~~

This view is designed only for projects, therefore you need to go to a
specific project to see this view. In this view, you can manage tasks as
well as the project workflow:

|image76|

In which:

-  Each column corresponds to a status of the project workflow.

-  The color of a task card depends on its priority: *High* - Light Red,
   *Medium/Normal* - Light Orange, *Low* - Light Green, None priority -
   Light Gray.

-  The number of tasks in a column is displayed next to the status name.

Creating new tasks:
----------------------

In addition to creating new tasks by :ref:`this way <CreateTask>`, you can quickly do this via the Board view as follows:

1. Hover cursor over the last task of a column (or grouping), an editable
field will appear:

|image77|

2. Type the task title in this field, then press Enter key. Your new task
will be created immediately in the corresponding column.

Sorting/Grouping tasks:
------------------------

|image78|

You can sort these tasks by the *Due Date, Priority* and *Rank* options
as well as group them by the *Assignee, Label* and *None* options as in
:ref:`this view <sort-tasks-list-view>`.

Moving tasks
-------------

You can drag/drop tasks back and forth between assignees, labels and
statuses.

-  Between statuses:

   |image79|

-  Between assignees:

   |image80|

-  Between labels:

   |image81|

Managing project workflow
--------------------------

By default, your project will have a workflow with four statuses
including *To Do - In Progress - Waiting On - Done* and you can change
it on your own.

-  To modify a status, double-click the status name in the Board view,
   and type the new name in the editable field that appears:

   |image82|

   Press Enter key to finish updating.

-  To delete a status, hover cursor over the status name in the Board
   view, and select the delete icon that appears:

   |image83|


.. note:: -  All tasks assigned to the deleted status are affected to the
			previous status (the column on the left in the Board view).
		  -  If the status is the first of the list (the first column in
          the Board view), the tasks will be assigned to the next status
          (the next column on the right in the Board view).
		  -  The last status cannot be deleted.


