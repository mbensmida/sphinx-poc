.. _Document-viewer:

===============
Document Viewer
===============

.. _Viewable-types:

The viewable document types
-----------------------------

The Documents application allows users to build custom content types and
provides some built-in content types. It also provides a viewer for
common file types so users can read Office documents, view images or
play videos directly from the activity stream.

When a document has a preview, a part of it is displayed, if not a
thumbnail icon is displayed:

|image11|

When clicking to preview, here is what we got in the two cases:

|image12|

The following types are viewable i.e has a preview:

-  Printable files: *pdf*, *doc* (and other Office files) or any other
   type of files :ref:`JODConverter <#PLFAdminGuide.Configuration.JODConverter>`
   supports. See the full list of types at :ref:`JODConverter, Administrator
   Guide <#PLFAdminGuide.Configuration.JODConverter>`.

-  Images: *png, jpg, jpeg, gif*.

-  Audios/Videos: *mp3, mp4*.

-  ECMS content, either custom or built-in templates, such as a *web
   content* template.

For these viewable types, when you click a document preview thumbnail in
the Activity Stream or select the *View Document* menu from Documents in
the left navigation pane, the **Document Viewer** opens. The viewer
provides a large viewing area and some functions, such as Search,
Download and Print.

.. tip:: To exit the Viewer, hit *Esc* key or click **X** icon at the top right corner.


.. note::The Comment pane, where you can comment on or like a post, is only available when you view a document in the Activity Stream.
		 If the document is an unknown type, you must download it to your local machine and open it with another application.

.. _Office-PDF-files:

Office documents and pdf files
-------------------------------

You can always view pdf files, whereas Office documents require
:ref:`JODConverter <#PLFAdminGuide.Configuration.JODConverter>` to be
installed on the server. If you cannot view an MS Word file, for
example, contact your administrators.

For these file types, the Document Viewer provides maximized reading
estate and all the functions listed.

|image13|

-  **Page Navigator**

Although you can simply scroll to go to another page, the Page Navigator
provides many page selectors (e.g. previous, next, first and last page
links, page number selector). You can also show/hide the Page Thumbnail
pane by clicking the leftmost icon in the toolbar. Click it again to
close it.

|image14|

-  **Search**: Click the Search icon |image15| to open the Search bar and
   click it again to exit.

|image16|

-  **Download**: Click the Donwload icon |image17| to download the file.

-  **Full screen mode**: Click the *Switch to Presentation Mode* icon
   |image18| to read in full screen. Hit *Esc* key to exit this mode.

-  **Print**: Click the *Tools* icon |image19| then select *Print*.

-  **Comment**: You will see the Comment area on the right side when you
   open the viewer. If it is hidden, you can bring it back by clicking
   the rightmost arrow icon.

|image20|

-  **Like**: In the Comment area, click the *Like* icon |image21| to
   like the post. Click it again to unlike.

.. _Images-audio-videos:

Images, Audios and Videos
--------------------------

For viewable media types, the available functions are Download, Comment
and Like.

|image22|


.. note::Audio/Video playback may require appropriate browser plugins. A
			message like "*Video format or MIME type is not supported*\ "
			indicates that you may need to install or enable some plugins for that media type.

.. _ECMS-content:

ECMS Content
-------------

If the document is ECMS Content, it is viewable. The following
screenshot shows *illustrated web content*, which is one of the built-in
templates.

|image23|


