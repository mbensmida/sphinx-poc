.. _Forum:

#####################
Building Your Forum
#####################


    The **Forums** application is designed for the group discussion and
    user-generated content in which participants with common interests
    can exchange their opinions on a subject.

    The chapter provides you a guide to use all **Forums** features or
    to make **Forums** work in your desired manner.

    -  **`Regular
       user <#PLFUserGuide.BuildingYourForum.RegularUser>`__**

       Detailed instructions on how to do common actions that are for
       regular users, such as creating topics and posts, subscribing,
       using BBCode, or changing user settings.

    -  **`Moderator <#PLFUserGuide.BuildingYourForum.Moderator>`__**

       Introduction to the Moderation tasks that are for moderators, and
       steps to perform them, including: moderating forums/topics/posts,
       viewing all pending moderation tasks, or banning IPs.

    -  **`Administrator <#PLFUserGuide.BuildingYourForum.Administrator>`__**

       Details about advanced tasks that are for administrators only,
       including setting up the Forum portlet, managing
       categories/forums/users and other administrative tasks.

In **Forums**, the role of each user group is clear and very important.
Each role has a set of tasks that they can execute. Administrators and
moderators are responsible for setting up and maintaining **Forums**.
With the highest rights, the administrators are in charge of the entire
management tasks, including form configurations, users management,
permissions, categories, forums, topics and messages. With sub-sets of
administrative permissions, the moderators will manage the respective
sub-sets of the forum.

The user interface will indicate which features are available to you,
based on your role.

-  As a regular user, you will have the User bar and Action bar with the basic actions.

|image0|

-  As a moderator, you will have the User bar and Action bar with a sub-set of certain capabilities.

|image1|

-  As an administrator, you will have the Administration bar which is
   basically the User bar with more administrative actions. You also see
   the Action bar with the advanced actions on forums and categories.
   Most of management tasks are shown via these bars.
   
|image2|   

To have an overall look of actions which users of each role can do in
the **Forums** application, see the following table:

====================================================== =========================================================================================================================  =============  ========== ============ =========
 Features                                            	Description   																											  Administrator   Moderator Regular user  Guest   
             	   				                      																														 
+===================================================== =========================================================================================================================  =============  ========== ============ =========
:ref:Subscribing to RSS feeds <SubscribingRSSFeeds>     Gets a link to a forum for easy sharing.																					   |OK|         |OK|	     |OK|       |OK|  

:ref:Attaching a file <AttachingFiles>                  Uploads an attachment to a topic/post, previews and downloads it. 														       |OK|         |OK|	     |OK|       |OK|

:ref:Bookmarks <Bookmarks>                              Bookmarks a category, forum, topic.																						       |OK|         |OK|	     |OK|       |NOK|

:ref:Creating a post <Posts>                            Posts a reply, quote, private post, quick reply.																			   |OK|         |OK|	     |OK|       |NOK|

:ref:Editing your post <Edit-delete-post>               Edits a post, quote and private post.																					       |OK|         |OK|	     |OK|       |NOK|

:ref:Deleting your post <Edit-delete-post>              Deletes a post inside a specific topic. 																					   |OK|         |OK|	     |OK|       |NOK|

:ref:Creating a topic <Create-topic>                    Starts a new topic.																										       |OK|         |OK|	     |OK|       |NOK|

:ref:Editing a topic <Editing-topic>                    Edits a topic in a specific forum.																						       |OK|         |OK|	     |OK|       |NOK|

:ref:Deleting a topic <Deleting-topic>                  Deletes a topic inside a specific forum.																					   |OK|         |OK|	     |OK|       |NOK|

:ref:Locking/Unlocking a topic <Lock-unlock-topics>     Locks/Unlocks a topic inside a specific forum.																			       |OK|         |OK|	     |NOK|      |NOK|  

:ref:Adding a poll <Create-poll>                        Adds a poll to a topic.																									       |OK|         |OK|	     |OK|       |NOK| 

:ref:Rating a topic <Rate-topics>                       Evaluates a topic by rating stars.																						       |OK|         |OK|	     |OK|       |NOK| 
 
:ref:Adding a tag <Tagging-topic>                       Creates a new tag and tags a topic.																						       |OK|         |OK|	     |OK|       |NOK|

:ref:Sending private messages <Send-Private-message>    Sends or receives private messages.																						       |OK|         |OK|	     |OK|       |NOK|

:ref:Watching <Watch>                                   Subscribes to a category, forum, topic to receive email notifications of new posts or topics.							       |OK|         |OK|	     |OK|       |NOK|

:ref:User settings <User-settings>                      Changes profile settings, personal forum settings.																		       |OK|         |OK|	     |OK|       |NOK|

:ref:Sticking/Unsticking a topic <Stick-unstick>        Sticks/Unsticks a topic inside a specific forum.																			   |OK|         |OK|	     |OK|       |NOK|

:ref:Locking/Unlocking a topic <Lock-unlock-topics>     Closes/Opens a topic inside a specific forum																				   |OK|         |OK|	     |NOK|      |NOK|

:ref:Splitting a topic <Split-topic>                    Divides one topic into two separate topics.																				       |OK|         |OK|	     |NOK|      |NOK| 

:ref:Merging topics <Merge-topics>                      Combines two or more topics into one.																					       |OK|         |OK|	     |NOK|      |NOK| 

:ref:Managing a poll <Create-poll>                      Creates, edits, deletes, closes and reopens a poll.																		       |OK|         |OK|	     |NOK|      |NOK| 

:ref:Moving a topic/post <Moving-topic>                 Moves one topic/post from a forum/topic to the other forum/topic.														       |OK|         |OK|	     |NOK|      |NOK|

:ref:Approving a topic/post <Approve-topic>             Changes a new topic/post from pending status to normal status so that guests and normal users can view.					       |OK|         |OK|	     |NOK|      |NOK| 

:ref:Uncensoring a post <Uncensor-post>                 Allows a topic which has censored content to be displayed.																       |OK|         |OK|	     |NOK|      |NOK|

:ref:Showing/ Hiding a post <Show-hide-post>            Allows a post to be shown/hidden.																						       |OK|         |OK|	     |NOK|      |NOK| 
 
:ref:Managing pending tasks <Manage-pending-tasks>      Manages all topics/posts waiting for moderation in one place.															       |OK|         |OK|	     |NOK|      |NOK|

:ref:Managing a watch <Edit-subscription>               Manages the subscription (watch), edits and deletes a subscribed email.													       |OK|         |OK|	     |NOK|      |NOK| 

:ref:Banning users <Banning-users>                      Bans users from accessing specific forums or categories.																	   |OK|         |NOK|        |NOK|      |NOK| 

:ref:Adding a forum <Adding-forum>                      Adds a new forum to a specific category.																					   |OK|         |NOK|        |NOK|      |NOK| 

:ref:Editing a forum <Edit-forum>                       Changes the title, description, moderator, permissions of a forum. However, moderators cannot set moderators for a forum.      |OK|         |OK|	     |NOK|      |NOK|

:ref:Deleting a forum <Delete-forum>                    Deletes a forum from a specific category.																				       |OK|         |NOK|        |NOK|      |NOK|
	
:ref:Locking/Unlocking a forum <Lock-unlock-forum>      Locks a forum so that it can be viewed only.																				   |OK|         |OK|	     |NOK|      |NOK|

:ref:Closing/Opening a forum <Close-open-forum>         Closes/Opens a forum. The closed forums are still manageable by administrators and moderators.							       |OK|         |OK|	     |NOK|      |NOK|

:ref:Moving a forum <Move-forum>                        Moves a forum from one category to the other.																			       |OK|         |NOK|        |NOK|      |NOK|

:ref:Exporting a forum <Export-forum>                   Exports a forum in the format of a ``.zip`` or ``.xml`` file.															       |OK|         |NOK|        |NOK|      |NOK|

:ref:Importing a forum <Import-forum>                   Imports a forum from a ``.zip``/``.xml`` file into the Forums application.												       |OK|         |NOK|        |NOK|      |NOK|

:ref:Adding a category <Add-category>                   Adds a new category. 																									       |OK|         |NOK|        |NOK|      |NOK|

:ref:Editing a category <Edit category>                 Edits a category and changes its properties.																				   |OK|         |NOK|        |NOK|      |NOK|

:ref:Exporting a category <Export-category>             Exports categories in the format of a ``.zip`` or ``.xml`` file.															   |OK|         |NOK|        |NOK|      |NOK|

:ref:Importing a category <Import-category>             Imports a category from a ``.zip``/``.xml`` file into the Forums application.											       |OK|         |NOK|        |NOK|      |NOK|

:ref:Deleting a category <Delete-category>              Deletes a category and all forums, topics, posts inside it.																       |OK|         |NOK|        |NOK|      |NOK|

:ref:Administrating Sorting <Sort-settings>             Sorts forums, topics according to specific conditions.																	       |OK|         |NOK|        |NOK|      |NOK|

:ref:Administrating Censor <Administrating-Censor>      Defines keywords that will be censored in a forum.																		       |OK|         |NOK|        |NOK|      |NOK|

:ref:Customizing an email notification template         Defines content of the email notifications.																				       |OK|         |NOK|        |NOK|      |NOK|
<Customize-email-notifs>                             																															 	

:ref:Customizing BBCodes <Customize-BBCodes>            Adds, edits and deletes the BBCode tags used in writing posts/topics.													       |OK|         |NOK|        |NOK|      |NOK|

:ref:Setting up auto-pruning <auto-pruning>             Sets up auto-pruning to clean a large amount of obsolete and inactive topics based on criteria.							       |OK|         |NOK|        |NOK|      |NOK|

:ref:Banning IPs <Banning-IPs>                          Bans IPs in the whole Forums application (only administrators) and in specific forums only(administrators and moderators).     |OK|         |OK|	     |NOK|      |NOK|

:ref:Managing users <Manage-users>                      Manages user's profile, promotes users, bans users, views a topic and post of a specific user.                                 |OK|         |NOK|        |NOK|      |NOK|


.. note:: **(\*):** Regular users can only edit/delete their own posts/topics.


.. |image0| image:: images/forum/forum_user_actions.png
.. |image1| image:: images/forum/mod_action_bar.png
.. |image2| image:: images/forum/forum_home.png
