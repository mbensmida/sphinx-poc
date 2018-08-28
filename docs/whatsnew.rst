.. _whatsnew:

#################################
What's new in eXo Platform 5.1?
#################################


.. _FunctionalNovelties:

==================================
New features in eXo Platform 5.1?
==================================

Many great enhancements come up in eXo Platform 5.0. Thanks to eXo teams 
and Community members who participated by contributing ideas, discussing 
and voting for the new features.

**Enterprise skin**

A new skin is introduced in the 5.0 version, the ``Enterprise skin``.
The new skin is a full redesign more modern, enhances usability, reduces 
eye fatigue and highlights user content for a more engaging user 
experience.

|image0|

**Revamped navigation experience**

*Left navigation menu*

The left navigation was revamped into a collapsible panel to make the 
best use of any screen size.

|image1|

*Space navigation*

The space navigation has been improved by adding a customizable banner 
to easily recognize in which space you are.
Space avatar, call and chat buttons were moved into the navigation bar.
Space navigation now floats on top and shrinks down to facilitate 
navigating between apps and to preserve screen space and switch easily
between apps.
The banner is also available for users profiles.

|image2|

**Share multiple documents in activity stream**

You can now attach multiple documents to a post in the activity stream. 
You can drag and drop them or select them from your computer or even 
from your eXo drives.
An elegant mosaic of preview thumbnails is displayed in the activity 
stream and the full page viewer now lets you navigate between the 
attached documents.

|image3|

**Likes on comments**

In addition to activities, it is now possible to like an individual 
comment.

|image4|

**Replying to comments**

In addition to liking the comments, you can also reply to them.

|image5|

**Inserting image in posts and comments**

You can now enhance your posts with images coming from your computer or 
your eXo drives and have more control on their size and alignment.

|image6|

**Web conferencing**

You can now make video calls directly from the user interface via Call 
buttons. 
No browser plugin is required thanks to WebRTC. 
Call buttons can be extended by external third party services connectors 
(e.g Skype, etc.) if needed.

|image7|

|image8|

**eXo Engagement analytics by Lecko**

Measure user engagement and communities' collaboration maturity thanks 
to this integration with Lecko Analytics.

|image9|

.. _TechnicalNovelties:

========================================
Technical novelties in eXo Platform 5.1
========================================

**Upgrades**

In the version 5.0, many tools/applications used by eXo Platform were 
upgraded to newer  versions in order to benefit from their latest 
updates and improvements: 

- Tomcat 8.5

- JBoss EAP 7.0

- Elasticseach 5.6 

- Infinispan 8

- Groovy 2.4

- JQuery 3.2 

- Shindig 2.5

**Performances and scalability**

In eXo Platform 5.0, we insisted on improving the performance and the 
scalability by changing some strategies, configurations and data 
storage.  

- Cache strategy and configuration

- New cache on organization service

- Files indexing in Elasticsearch

- Storage of all spaces members in Social database tables

**Migrations**

With eXo Platform 5.0, some data were migrated from JCR to database to 
improve performance and scalability:

- Notifications and settings in JPA dataset

- ECMS files are indexed in Elasticsearch

- Space members stored in Social database tables 

Many other improvements and refinements were also done in :

- Customizing skin: No more need to duplicate the whole project 
  platform-ui.

- Extending the IM list of user profile is now doable through UI.

- When indexing JCR workspace, old indexes are always existing until the 
  end of indexation.

- An Mbean is added to reload Javascript.

- A new minify attribute allowing to enable/disable the minification.

- Compilation of Javascript scripts by Google Closure Compiler to ES5.

- Improve the Upgrade plugin framework: Add configuration to define the 
  target version.

- Add the possibility to define a group of users able to manage all 
  spaces.

- eXo Platform 5.0 could be ran with Java9.

- Improvements on Elasticsearch mappings.

- Copying URL feature does not use Flash anymore but it relies on 
  Javascript clipboard feature.

- Javascript errors are no more logged into WebUI popups but in console.
    


.. |image0| image:: images/enterprise_skin.png
.. |image1| image:: images/hamburger_menu.gif
.. |image2| image:: images/space_banner.png
.. |image3| image:: images/multi_upload.png
.. |image4| image:: images/like_comments.png
.. |image5| image:: images/reply_comment.png
.. |image6| image:: images/resize_image.pn
.. |image7| image:: images/web_conf1.png
.. |image8| image:: images/web_conf2.png
.. |image9| image:: images/Lecko_analytics.png
