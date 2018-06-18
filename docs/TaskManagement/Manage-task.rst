.. _Manage-task:

Managing tasks
==============

This part introduces you how to:

* :ref:`Create a task <CreateTask>`
* :ref:`Edit a task <EditTask>`
* :ref:`Schedule a task <ScheduleTask>`
* :ref:`Get permalink of a task <GetPermalink>`
* :ref:`Clone a task <CloneTask>`
* :ref:`Delete a task <DeleteTask>`
* :ref:`Filtering tasks <Filtering>`


.. _CreateTask:

Creating a task
~~~~~~~~~~~~~~~~~~~

Creating a task in eXo Platform is designed as an effortless operation, so
you just need to follow one of the following ways.

Via Tasks management overview
--------------------------------------

1. Click any items (except *Overdue*) under the **Tasks**, **Projects** or **Labels** sections.

2. Enter the task title into the single line text box under the New Task button:

|image2|

3. Hit **Enter** key to create this task.

    .. note:: -  If you choose to create the task in a filter, it will be put into
				that filter and automatically assigned to the currently logged-in
				user. Note that for the *Upcoming* filter, the due date will be
				the next seven days, while for the *Today* and *Tomorrow*
				filters, the due date will be today and tomorrow respectively.

				-  If you choose to create the task in a project or label, it will
				belong to that project or labelled to that label. Besides, by
				default it will not be assigned to anyone.

Via Activity stream
----------------------

You can even create a task outside the BRAND\_TASK\_MANAGEMENT
application by using the following syntaxes on the Activity stream:

-  Creating a task: ++\ *task\_title*.

-  Setting priority: !\ *task\_priority*. Recognized priorities include
   *High, Medium* and *Low*.

-  Assigning: @\ *task\_assignee* @\ *task\_coworker\_1*
   @\ *task\_coworker\_2*

-  Setting due date: ^\ *due\_date*. Recognized syntaxes include *Today,
   Tomorrow, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday,
   Sunday, Next Week, Next Month* and *dd-mon* (e.g *12-apr* for 12th
   April).

-  Tag: #\ *tag*. The tag will be created if it does not exist.

See this example:

|image3|

Or via comment:
-------------------

|image4|

You will see that there are two new tasks created as below:

|image5|

    .. note:: - Anyone that has access permission to a task can do anything on the task.
			  -  By default, tasks inherit permissions from the project they are
				in. Therefore, all members and managers of the project are able
				to access these tasks. In case they are not assigned to any
				project, only the creator, assignee and coworkers are granted the
				access permission.


.. _EditTask:

Editing a task
~~~~~~~~~~~~~~~~~~~~~

After creating a task, the right pane will be opened for you to edit the
task directly (if you create the new task via the overview interface) or
you can choose any other task from the central pane. The details of a
task are as follows:

|image6|

In which:

-  |image7|: the name of the project that the task belongs to. In case
   the task is not assigned to any project, this field says "*No
   Project*\ ".

       .. note:: -  To select a project for a task, you must have permission on
          that project. Besides, a task should belong to only one
          project, so you should remove the existing project from the
          task before adding a new one.

       -  If you move a task to another project, its status will be set
          to the same one in the new project workflow (statuses must
          match alphabetically to be considered the same). If no status
          matches in the new project workflow, the status is set to the
          first one in the new project workflow.

-  |image8|: the labels that are assigned to the task.

-  |image9|: the title of the task which should be from 1 to 250
   characters.

-  |image10|: the due date of the task. You can choose among 4 options,
   including *None, Today, Tomorrow* and *Next Week* or specify any
   other due date.

-  |image11|: the assignee and co-workers that are assigned to the task.
   Only one assignee is accepted, while you can add multiple co-workers.

-  |image12|: the status of the task in the project workflow. Note that
   this information is available only for the tasks that are assigned to
   a specific project.

-  |image13|: the task description.

-  |image14|: the schedule of the task. If no schedule is specified,
   this field says "*Unscheduled*\ ". To remove the current schedule,
   hover cursor over it and select the deletion icon that appears.

-  |image15|: the task priority. You can choose between 4 values,
   including *High, Normal, Low* and *None*.

-  |image16|: the **Comments** tab allows people to discuss about the
   task, while the **Changes** tab shows all changes history of the
   task.

   |image17|

-  |image18|: the *Mark as completed* feature, clicking this icon will
   mark the task as completed and it will disappear from the List and
   Board views unless
   `Filter <#PLFUserGuide.WorkingWithTasks.ManageTask.Filtering>`__ is
   set to show completed tasks.

    .. note:: A formatting toolbar appears once you click in the comment composer.
				It allows you to change the formatting of your message, attaching
				images and links and preview how it will look once posted. (like
				what we have for :ref:`the activity stream composer <posting-status-updates>`)

To edit the task:

1. Hover cursor over any information and click it that you want to edit.

2. Make changes on the task, then hit **Enter** key or just click out the edited field.

.. _ScheduleTask:

Scheduling a task
~~~~~~~~~~~~~~~~~~~~

After creating a task or being assigned one, you can schedule it by
following these steps:

|image19|

-  |image20|: Select the list of tasks by clicking on All Tasks.

-  |image21|: Select one of the assigned/created tasks.

-  |image22|: Click on Unscheduled.

Two calendars appear to select From and To dates.

|image23|

After saving the selected dates, a message is displayed under the task's
description indicating the time interval chosen with a note about the
schedule:

-  If the To date is chosen after the due date, a message appears to
   warn that you may miss the deadline because you planned the work too
   late.

   |image24|

-  If the To date is chosen before the due date, the message that
   appears indicates that the work is planned between the chosen dates.

   |image245|

    .. note:: -  When the today's date is the task's due date, a blue exclamation
				mark |image26| precedes the task's name in the list/board view.
				-  When the task's due date has already expired, i.e. today's date
				is after the due date and the task is not yet finished, it is
				preceded with a red exclamation mark: |image27|
				|image28|
    
.. _GetPermalink:

Getting permalink of a task
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Click the link icon at the top right corner of the task pane:

|image29|

You will get the permalink to share the task.


.. _CloneTask:

Cloning a task
~~~~~~~~~~~~~~~

1. Click the down arrow at the top right corner of the task pane, a
drop-down menu will appear as follows:

|image30|

2. Select Clone to clone the task. The cloned task will have the same name
with the original task and be prefixed by "*Copy of*\ ".


.. _DeleteTask:

Deleting a task
~~~~~~~~~~~~~~~~~~~~

1. Select Delete from the dropdown menu:

|image31|

2. Click OK in the confirmation message to delete the task.

|image32|

    .. note:: This action is available to the task creator and the project manager only.


.. _Filtering:

Filtering tasks
~~~~~~~~~~~~~~~~~~~~

The central pane by default will list all the tasks depending on which
task filter, project or label is selected. This could be difficult for
you if there are too many tasks available. The Tasks management
application offers you a useful tool to narrow these tasks by specific
information.

|image33|

1. |image34| Click the filter icon |image35| at the top right corner of
the central pane.

2. |image36| The Filter form will be shown on the right pane.

In which:

-  *Contains*: filters tasks that have the title or description matching
   the input text.

-  *Labels*: filters tasks that contain the input labels.

-  *Due*: filters tasks by due date.

-  *Priority*: filters tasks that have the selected priority.

-  *Show completed tasks*: filters tasks that are completed. Unchecking
   this box will show uncompleted tasks.

    .. note:: Depending on the view you select from the left pane such as :ref:`Task filters <Tasks-filters>`,
				Projects or Labels views, some of the options above may be disabled.

2. Change any information above. The central panel will reflect instantly
to list only the matched tasks.

3. A Close icon |image37| on top-right corner of the filter panel closes
it. But the values are remembered and filter remains active.

The filter icon has two statuses:

-  It turns blue |image38| when it is activated which means that the
   central panel is filtered.

-  It is grey |image39| when it is inactive which means that the central
   panel is not filtered.

