.. _WorkingWithRepository:

Working with Repository
~~~~~~~~~~~~~~~~~~~~~~~~~~

From the Manage ECM Main Functions panel, select Repository.

|image90|

Here you can manage:

-  :ref:`Namespaces <WorkingWithRepository.Namespaces>`

-  :ref:`Node types <WorkingWithRepository.NodeTypes>`

-  :ref:`Locks <WorkingWithRepository.Locks>`

.. _WorkingWithRepository.Namespaces:

Namespaces
------------

The namespace is a prefix in the node type name. It enables you to
create node types without fearing any conflict with existing node types.

In Repository, select Namespaces to open the Namespaces panel.

|image91|

**Registering a namespace**

1. Click Register at the bottom of the Namespaces form open the Register
   New Namespace form.

|image92|

2. Enter the value for the Namespace Prefix field that is required.

3. Enter the value for the URI field which must be unique and required.

.. note:: The namespace must not contain special characters, such as ``!,#,$,&,\*,(,)``.

.. _WorkingWithRepository.NodeTypes:

Node types
-----------

This function is used to control all node types in eXo Platform.

In Repository, select Node Types to open the Node Types panel.

|image93|

**Viewing node types**

1. Click |image94| corresponding to the node you want to view. The View 
   Node Type Information form will appear.

|image95|

2. Click Close at the bottom of the form to exit.

**Adding a node type**

1. Click Add at the bottom of the **Node Types** page to open the 
   Add/Edit Node Type Definitions form.

|image96|

2. Select a namespace for the node.

3. Enter a name in the Node Type Name field. This field is mandatory and
   its value must be unique.

.. note:: The name must not contain special characters, such as ``!,#,$,&,\*,(,)``.

4. Select a value for the Is Mixin Type field.

-  True: This node is Mixin type.

-  False: This node is not Mixin type.

5. Select a value for the Orderable Child Nodes field.

-  True: Child nodes are ordered.

-  False: Child nodes are not ordered.

6. Enter a value for the Primary Item Name field.

7. Enter a value for the Super Types field. Clicking |image97| will 
   direct you to the Super Types tab for you to search for available 
   super types.

   -  Property Definitions: Lists all definition names of the Property 
      tab.

   -  Child Node Definitions: Lists all definition names of the Child Node
      tab.

8. Click Save to accept adding a new node type, or Save as Draft to save
   this node type as draft.

**Importing node types**

1. Click Import at the bottom of the **Node Types** page to open the 
   Import Node Type From XML File form.

|image98|

2. Click Select File to upload a file.

.. note:: You must upload an XML or ZIP file. This file is in the node type's format.

3. Click the Upload button.

.. note:: If you want to upload another file, click |image99| to delete the file which has just been uploaded, then upload other files.

4. Tick the checkboxes corresponding to the nodes that you want to 
   import.

5. Click Import to complete importing a node type.

**Exporting node types**

1. Click Export at the bottom of the **Node Types** page to open the 
   Export Node Types form.

|image100|

2. Click Uncheck all if you do not want to export all node types. After
   clicking Uncheck all, this button becomes the Check all button.

3. Select nodes that you want to export by ticking the corresponding
   checkboxes.

4. Click Export in this form.

5. Select the location in your device to save the exported node.

.. note:: You must select at least 1 node type to be exported. If you do not want to export the node, click Cancel to quit this pop-up.


.. _WorkingWithRepository.Locks:

Locks
------

In Repository, select Locks to open the Locks panel. The locked nodes
will be listed in the right panel.

|image101|

**Unlocking a node**

Simply click |image102| corresponding to nodes which need to be unlocked
in the Locked Node tab. The unlocked nodes will disappear from the
locked nodes list.

**Managing locks**

Administrators can manage and add the unlock permission for another
group and users in the Manage Lock tab.

Select the group on the Select Group panel and the corresponding
membership on the Select Membership panel. The selected group will be
listed in the Groups Or Users column.

-  Click |image103| corresponding to the group which you want to remove
   from the "Unlock" permission list, except the
   ``*:/platform/administrator`` group.

.. note:: If you set the \* membership for a group, all users of the group will be able to manage locks, regardless of their membership role.


