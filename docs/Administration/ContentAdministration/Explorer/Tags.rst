Tags
-----

The **Tagging** function enables you to manage tag styles.

In Explorer, select Tags to open the Tags panel:

|image81|

The style of tag which is applied depends on the number of documents
using the tag. For example, if one tag is used twice, its style will be
``font-size: 12px; font-weight: bold; color: #6b6b6b; font-family: verdana; text-decoration:none;``.

Editing/Deleting a tag style
`````````````````````````````

**Editing a tag**

The Tag Manager tab enables you to edit the existing tags.

1. Click |image82| corresponding to the tag name which you want to edit 
   in the Action column to edit the tag style configuration. The Edit 
   Tag Style Configuration form appears which is similar to that of 
   adding a tag style.

2. Change values in the fields, including Number of Occurrences and HTML
   Style, except Style Name.

3. Click Update to save new changes.

**Deleting a tag**

To delete one tag style, simply click |image83| in the Action column,
then select **OK** in the confirmation message.

Adding a tag style
````````````````````

1. Click Add Style at the bottom to open the Edit Tag Style 
   Configuration form.

|image82|

**In which:**

+--------------------+--------------------------------------------------------+
| Field              | Description                                            |
+====================+========================================================+
| **Style Name**     | The tag name which cannot be edited after you have     |
|                    | added.                                                 |
+--------------------+--------------------------------------------------------+
| **Number of        | The number of documents assigned to a tag.             |
| Occurrences**      |                                                        |
+--------------------+--------------------------------------------------------+
| **HTML Style**     | Includes font-size, font-weight, color, font-family,   |
|                    | and text-decoration.                                   |
+--------------------+--------------------------------------------------------+
| **Asterisk (\*)**  | Indicates the fields are mandatory.                    |
+--------------------+--------------------------------------------------------+

2. Input values in the fields: Style Name, Number of Occurrences, and 
   HTML Style.

3. Click Update to accept adding a new tag style.

.. note:: The format of valid range must be: a..b where 'a', 'b' are positive integers. You can use \* instead of 'b' to indicate it is unlimited. For example, 0..2 (means 0-2 documents assigned to a tag), 10..\* (means at least 10 documents assigned to a tag).
		  The HTML Style textbox cannot be empty. You can change values of font size, font weight, color, font family, and text decoration later.

Setting permissions on public tags
````````````````````````````````````

The Tag Permission Manager tab helps you set permissions regarding to
editing and deleting public tags.

|image83|

**Setting permission to tag management**

Here, you can click |image84| or |image85| or |image86| to add 
permissions to the users, memberships or anyone respectively. Then, 
click Add to add your selected permissions to the User or Group table.

.. note:: -  If you set the \* membership for a group, all users of the group will be able to manage tags, regardless of their membership role.

**Deleting a permission**

In the User or Group table, simply click |image87|, then select **OK** in
the confirmation message.

