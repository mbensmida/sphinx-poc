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

+--------------+-------------------+------------+------------+------------+------------+
| Features     | Description       | Administra | Moderator  | Regular    | Guest      |
|              |                   | tor        |            | user       |            |
+==============+===================+============+============+============+============+
| `Subscribing | Gets a link to a  |            |            |            |            |
| to RSS       | forum for easy    |            |            |            |            |
| feeds <#PLFU | sharing.          |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.RegularUs |                   |            |            |            |            |
| er.Subscribi |                   |            |            |            |            |
| ngRSSFeeds>` |                   |            |            |            |            |
| __           |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Attaching a | Uploads an        |            |            |            |            |
| file <#PLFUs | attachment to a   |            |            |            |            |
| erGuide.Buil | topic/post,       |            |            |            |            |
| dingYourForu | previews and      |            |            |            |            |
| m.RegularUse | downloads it.     |            |            |            |            |
| r.Topics.Cre |                   |            |            |            |            |
| atingTopic.A |                   |            |            |            |            |
| ttachingFile |                   |            |            |            |            |
| s>`__        |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Bookmarks < | Bookmarks a       |            |            |            |            |
| #PLFUserGuid | category, forum,  |            |            |            |            |
| e.BuildingYo | topic.            |            |            |            |            |
| urForum.Regu |                   |            |            |            |            |
| larUser.Book |                   |            |            |            |            |
| marks>`__    |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Creating a  | Posts a reply,    |            |            |            |            |
| post <#PLFUs | quote, private    |            |            |            |            |
| erGuide.Buil | post, quick       |            |            |            |            |
| dingYourForu | reply.            |            |            |            |            |
| m.RegularUse |                   |            |            |            |            |
| r.Posts>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Editing     | Edits a post,     |            |            |            |            |
| your         | quote and private |            |            |            |            |
| post <#PLFUs | post.             |            |            |            |            |
| erGuide.Buil |                   |            |            |            |            |
| dingYourForu |                   |            |            |            |            |
| m.RegularUse |                   |            |            |            |            |
| r.Post.Editi |                   |            |            |            |            |
| ngPost>`__   |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Deleting    | Deletes a post    |            |            |            |            |
| your         | inside a specific |            |            |            |            |
| post <#PLFUs | topic.            |            |            |            |            |
| erGuide.Buil |                   |            |            |            |            |
| dingYourForu |                   |            |            |            |            |
| m.RegularUse |                   |            |            |            |            |
| r.Post.Delet |                   |            |            |            |            |
| ingPost>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Creating a  | Starts a new      |            |            |            |            |
| topic <#PLFU | topic.            |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.RegularUs |                   |            |            |            |            |
| er.Topics.Cr |                   |            |            |            |            |
| eatingTopic> |                   |            |            |            |            |
| `__          |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Editing a   | Edits a topic in  |            |            |            |            |
| topic <#PLFU | a specific forum. |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.RegularUs |                   |            |            |            |            |
| er.Topics.Ed |                   |            |            |            |            |
| itingTopic>` |                   |            |            |            |            |
| __           |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Deleting a  | Deletes a topic   |            |            |            |            |
| topic <#PLFU | inside a specific |            |            |            |            |
| serGuide.Bui | forum.            |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingT |                   |            |            |            |            |
| opics.Deleti |                   |            |            |            |            |
| ngTopic>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Locking/Unl | Locks/Unlocks a   |            |            |            |            |
| ocking       | topic inside a    |            |            |            |            |
| a            | specific forum.   |            |            |            |            |
| topic <#PLFU |                   |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingT |                   |            |            |            |            |
| opics.Lockin |                   |            |            |            |            |
| gUnlockingTo |                   |            |            |            |            |
| pic>`__      |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Adding a    | Adds a poll to a  |            |            |            |            |
| poll <#PLFUs | topic.            |            |            |            |            |
| erGuide.Buil |                   |            |            |            |            |
| dingYourForu |                   |            |            |            |            |
| m.RegularUse |                   |            |            |            |            |
| r.Topics.Cre |                   |            |            |            |            |
| atingPoll>`_ |                   |            |            |            |            |
| _            |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Rating a    | Evaluates a topic |            |            |            |            |
| topic <#PLFU | by rating stars.  |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.RegularUs |                   |            |            |            |            |
| er.Topics.Ra |                   |            |            |            |            |
| tingTopic>`_ |                   |            |            |            |            |
| _            |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Adding a    | Creates a new tag |            |            |            |            |
| tag <#PLFUse | and tags a topic. |            |            |            |            |
| rGuide.Build |                   |            |            |            |            |
| ingYourForum |                   |            |            |            |            |
| .RegularUser |                   |            |            |            |            |
| .Topics.Tagg |                   |            |            |            |            |
| ingUntagging |                   |            |            |            |            |
| Topic>`__    |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Sending     | Sends or receives |            |            |            |            |
| private      | private messages. |            |            |            |            |
| messages <#P |                   |            |            |            |            |
| LFUserGuide. |                   |            |            |            |            |
| BuildingYour |                   |            |            |            |            |
| Forum.Regula |                   |            |            |            |            |
| rUser.Privat |                   |            |            |            |            |
| eMessage.Sen |                   |            |            |            |            |
| dingPrivateM |                   |            |            |            |            |
| essage>`__   |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Watching <# | Subscribes to a   |            |            |            |            |
| PLFUserGuide | category, forum,  |            |            |            |            |
| .BuildingYou | topic to receive  |            |            |            |            |
| rForum.Regul | email             |            |            |            |            |
| arUser.Watch | notifications of  |            |            |            |            |
| ing>`__      | new posts or      |            |            |            |            |
|              | topics.           |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `User        | Changes profile   |            |            |            |            |
| settings <#P | settings,         |            |            |            |            |
| LFUserGuide. | personal forum    |            |            |            |            |
| BuildingYour | settings.         |            |            |            |            |
| Forum.Regula |                   |            |            |            |            |
| rUser.UserSe |                   |            |            |            |            |
| ttings>`__   |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Sticking/Un | Sticks/Unsticks a |            |            |            |            |
| sticking     | topic inside a    |            |            |            |            |
| a            | specific forum.   |            |            |            |            |
| topic <#PLFU |                   |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingT |                   |            |            |            |            |
| opics.Sticki |                   |            |            |            |            |
| ngUnsticking |                   |            |            |            |            |
| Topic>`__    |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Locking/Unl | Closes/Opens a    |            |            |            |            |
| ocking       | topic inside a    |            |            |            |            |
| a            | specific forum.   |            |            |            |            |
| topic <#PLFU |                   |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingT |                   |            |            |            |            |
| opics.Lockin |                   |            |            |            |            |
| gUnlockingTo |                   |            |            |            |            |
| pic>`__      |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Splitting a | Divides one topic |            |            |            |            |
| topic <#PLFU | into two separate |            |            |            |            |
| serGuide.Bui | topics.           |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingT |                   |            |            |            |            |
| opics.Splitt |                   |            |            |            |            |
| ingTopic>`__ |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Merging     | Combines two or   |            |            |            |            |
| topics <#PLF | more topics into  |            |            |            |            |
| UserGuide.Bu | one.              |            |            |            |            |
| ildingYourFo |                   |            |            |            |            |
| rum.Moderato |                   |            |            |            |            |
| r.Moderating |                   |            |            |            |            |
| Topics.Mergi |                   |            |            |            |            |
| ngTopics>`__ |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Managing a  | Creates, edits,   |            |            |            |            |
| poll <#PLFUs | deletes, closes   |            |            |            |            |
| erGuide.Buil | and reopens a     |            |            |            |            |
| dingYourForu | poll.             |            |            |            |            |
| m.RegularUse |                   |            |            |            |            |
| r.Topics.Cre |                   |            |            |            |            |
| atingPoll>`_ |                   |            |            |            |            |
| _            |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Moving a    | Moves one         |            |            |            |            |
| topic <#PLFU | topic/post from a |            |            |            |            |
| serGuide.Bui | forum/topic to    |            |            |            |            |
| ldingYourFor | the other         |            |            |            |            |
| um.Moderator | forum/topic.      |            |            |            |            |
| .ModeratingT |                   |            |            |            |            |
| opics.Moving |                   |            |            |            |            |
| Topic>`__/`p |                   |            |            |            |            |
| ost <#PLFUse |                   |            |            |            |            |
| rGuide.Build |                   |            |            |            |            |
| ingYourForum |                   |            |            |            |            |
| .Moderator.M |                   |            |            |            |            |
| oderatingPos |                   |            |            |            |            |
| ts.MovingPos |                   |            |            |            |            |
| t>`__        |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Approving a | Changes a new     |            |            |            |            |
| topic <#PLFU | topic/post from   |            |            |            |            |
| serGuide.Bui | pending status to |            |            |            |            |
| ldingYourFor | normal status so  |            |            |            |            |
| um.Moderator | that guests and   |            |            |            |            |
| .ModeratingT | normal users can  |            |            |            |            |
| opics.Approv | view.             |            |            |            |            |
| ingTopic>`__ |                   |            |            |            |            |
| /`post <#PLF |                   |            |            |            |            |
| UserGuide.Bu |                   |            |            |            |            |
| ildingYourFo |                   |            |            |            |            |
| rum.Moderato |                   |            |            |            |            |
| r.Moderating |                   |            |            |            |            |
| Posts.Approv |                   |            |            |            |            |
| ingPost>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Uncensoring | Allows a topic    |            |            |            |            |
| a            | which has         |            |            |            |            |
| post <#PLFUs | censored content  |            |            |            |            |
| erGuide.Buil | to be displayed.  |            |            |            |            |
| dingYourForu |                   |            |            |            |            |
| m.Moderator. |                   |            |            |            |            |
| ModeratingPo |                   |            |            |            |            |
| sts.Uncensor |                   |            |            |            |            |
| ingPost>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Showing <#P | Allows a post to  |            |            |            |            |
| LFUserGuide. | be shown/hidden.  |            |            |            |            |
| BuildingYour |                   |            |            |            |            |
| Forum.Modera |                   |            |            |            |            |
| tor.Moderati |                   |            |            |            |            |
| ngPosts.Show |                   |            |            |            |            |
| ingPost>`__/ |                   |            |            |            |            |
| `Hiding a    |                   |            |            |            |            |
| post <#PLFUs |                   |            |            |            |            |
| erGuide.Buil |                   |            |            |            |            |
| dingYourForu |                   |            |            |            |            |
| m.Moderator. |                   |            |            |            |            |
| ModeratingPo |                   |            |            |            |            |
| sts.HidingPo |                   |            |            |            |            |
| st>`__       |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Managing    | Manages all       |            |            |            |            |
| pending      | topics/posts      |            |            |            |            |
| tasks <#PLFU | waiting for       |            |            |            |            |
| serGuide.Bui | moderation in one |            |            |            |            |
| ldingYourFor | place.            |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ViewPending |                   |            |            |            |            |
| Tasks>`__    |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Managing a  | Manages the       |            |            |            |            |
| watch <#PLFU | subscription      |            |            |            |            |
| serGuide.Bui | (watch), edits    |            |            |            |            |
| ldingYourFor | and deletes a     |            |            |            |            |
| um.RegularUs | subscribed email. |            |            |            |            |
| er.UserSetti |                   |            |            |            |            |
| ngs.EditingS |                   |            |            |            |            |
| ubscriptions |                   |            |            |            |            |
| >`__         |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Banning     | Bans users from   |            |            |            |            |
| users <#PLFU | accessing         |            |            |            |            |
| serGuide.Bui | specific forums   |            |            |            |            |
| ldingYourFor | or categories.    |            |            |            |            |
| um.Administr |                   |            |            |            |            |
| ator.Managin |                   |            |            |            |            |
| gUsers.Banni |                   |            |            |            |            |
| ngUsers>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Adding a    | Adds a new forum  |            |            |            |            |
| forum <#PLFU | to a specific     |            |            |            |            |
| serGuide.Bui | category.         |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Administr |                   |            |            |            |            |
| ator.Managin |                   |            |            |            |            |
| gForums.Addi |                   |            |            |            |            |
| ngForum>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Editing a   | Changes the       |            |            |            |            |
| forum <#PLFU | title,            |            |            |            |            |
| serGuide.Bui | description,      |            |            |            |            |
| ldingYourFor | moderator,        |            |            |            |            |
| um.Moderator | permissions of a  |            |            |            |            |
| .ModeratingF | forum. However,   |            |            |            |            |
| orums.Editin | moderators cannot |            |            |            |            |
| gForum>`__   | set moderators    |            |            |            |            |
|              | for a forum.      |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Deleting a  | Deletes a forum   |            |            |            |            |
| forum <#PLFU | from a specific   |            |            |            |            |
| serGuide.Bui | category.         |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Administr |                   |            |            |            |            |
| ator.Managin |                   |            |            |            |            |
| gForums.Dele |                   |            |            |            |            |
| tingForum>`_ |                   |            |            |            |            |
| _            |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Locking/Unl | Locks a forum so  |            |            |            |            |
| ocking       | that it can be    |            |            |            |            |
| a            | viewed only.      |            |            |            |            |
| forum <#PLFU |                   |            |            |            |            |
| serGuide.Bui |                   |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingF |                   |            |            |            |            |
| orums.Lockin |                   |            |            |            |            |
| gUnlockingFo |                   |            |            |            |            |
| rum>`__      |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Closing/Ope | Closes/Opens a    |            |            |            |            |
| ning         | forum. The closed |            |            |            |            |
| a            | forums are still  |            |            |            |            |
| forum <#PLFU | manageable by     |            |            |            |            |
| serGuide.Bui | administrators    |            |            |            |            |
| ldingYourFor | and moderators.   |            |            |            |            |
| um.Moderator |                   |            |            |            |            |
| .ModeratingF |                   |            |            |            |            |
| orums.Closin |                   |            |            |            |            |
| gOpeningForu |                   |            |            |            |            |
| m>`__        |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Moving a    | Moves a forum     |            |            |            |            |
| forum <#PLFU | from one category |            |            |            |            |
| serGuide.Bui | to the other.     |            |            |            |            |
| ldingYourFor |                   |            |            |            |            |
| um.Administr |                   |            |            |            |            |
| ator.Managin |                   |            |            |            |            |
| gForums.Movi |                   |            |            |            |            |
| ngForum>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Exporting a | Exports a forum   |            |            |            |            |
| forum <#PLFU | in the format of  |            |            |            |            |
| serGuide.Bui | a ``.zip`` or     |            |            |            |            |
| ldingYourFor | ``.xml`` file.    |            |            |            |            |
| um.Administr |                   |            |            |            |            |
| ator.Adminis |                   |            |            |            |            |
| trativeTasks |                   |            |            |            |            |
| .BackingupCa |                   |            |            |            |            |
| tegoryForum. |                   |            |            |            |            |
| ExportingFor |                   |            |            |            |            |
| um>`__       |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Importing a | Imports a forum   |            |            |            |            |
| forum <#PLFU | from a            |            |            |            |            |
| serGuide.Bui | ``.zip``/``.xml`` |            |            |            |            |
| ldingYourFor | file into the     |            |            |            |            |
| um.Administr | **Forums**        |            |            |            |            |
| ator.Adminis | application.      |            |            |            |            |
| trativeTasks |                   |            |            |            |            |
| .BackingupCa |                   |            |            |            |            |
| tegoryForum. |                   |            |            |            |            |
| ImportingFor |                   |            |            |            |            |
| um>`__       |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Adding a    | Adds a new        |            |            |            |            |
| category <#P | category.         |            |            |            |            |
| LFUserGuide. |                   |            |            |            |            |
| BuildingYour |                   |            |            |            |            |
| Forum.Admini |                   |            |            |            |            |
| strator.Mana |                   |            |            |            |            |
| gingCategori |                   |            |            |            |            |
| es.AddingCat |                   |            |            |            |            |
| egory>`__    |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Editing a   | Edits a category  |            |            |            |            |
| category <#P | and changes its   |            |            |            |            |
| LFUserGuide. | properties.       |            |            |            |            |
| BuildingYour |                   |            |            |            |            |
| Forum.Admini |                   |            |            |            |            |
| strator.Mana |                   |            |            |            |            |
| gingCategori |                   |            |            |            |            |
| es.EditingCa |                   |            |            |            |            |
| tegory>`__   |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Exporting a | Exports           |            |            |            |            |
| category <#P | categories in the |            |            |            |            |
| LFUserGuide. | format of a       |            |            |            |            |
| BuildingYour | ``.zip`` or       |            |            |            |            |
| Forum.Admini | ``.xml`` file.    |            |            |            |            |
| strator.Admi |                   |            |            |            |            |
| nistrativeTa |                   |            |            |            |            |
| sks.Backingu |                   |            |            |            |            |
| pCategoryFor |                   |            |            |            |            |
| um.Exporting |                   |            |            |            |            |
| Category>`__ |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Importing a | Imports a         |            |            |            |            |
| category <#P | category from a   |            |            |            |            |
| LFUserGuide. | ``.zip``/``.xml`` |            |            |            |            |
| BuildingYour | file into the     |            |            |            |            |
| Forum.Admini | **Forums**        |            |            |            |            |
| strator.Admi | application.      |            |            |            |            |
| nistrativeTa |                   |            |            |            |            |
| sks.Backingu |                   |            |            |            |            |
| pCategoryFor |                   |            |            |            |            |
| um.Importing |                   |            |            |            |            |
| Category>`__ |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Deleting a  | Deletes a         |            |            |            |            |
| category <#P | category and all  |            |            |            |            |
| LFUserGuide. | forums, topics,   |            |            |            |            |
| BuildingYour | posts inside it.  |            |            |            |            |
| Forum.Admini |                   |            |            |            |            |
| strator.Mana |                   |            |            |            |            |
| gingCategori |                   |            |            |            |            |
| es.DeletingC |                   |            |            |            |            |
| ategory>`__  |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Administrat | Sorts forums,     |            |            |            |            |
| ing          | topics according  |            |            |            |            |
| Sorting <#PL | to specific       |            |            |            |            |
| FUserGuide.B | conditions.       |            |            |            |            |
| uildingYourF |                   |            |            |            |            |
| orum.Adminis |                   |            |            |            |            |
| trator.Admin |                   |            |            |            |            |
| istrativeTas |                   |            |            |            |            |
| ks.Configuri |                   |            |            |            |            |
| ngSortSettin |                   |            |            |            |            |
| gs>`__       |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Administrat | Defines keywords  |            |            |            |            |
| ing          | that will be      |            |            |            |            |
| Censor <#PLF | censored in a     |            |            |            |            |
| UserGuide.Bu | forum.            |            |            |            |            |
| ildingYourFo |                   |            |            |            |            |
| rum.Administ |                   |            |            |            |            |
| rator.Admini |                   |            |            |            |            |
| strativeTask |                   |            |            |            |            |
| s.DefiningCe |                   |            |            |            |            |
| nsoredKeywor |                   |            |            |            |            |
| ds>`__       |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Customizing | Defines content   |            |            |            |            |
| an email     | of the email      |            |            |            |            |
| notification | notifications.    |            |            |            |            |
| template <#P |                   |            |            |            |            |
| LFUserGuide. |                   |            |            |            |            |
| BuildingYour |                   |            |            |            |            |
| Forum.Admini |                   |            |            |            |            |
| strator.Admi |                   |            |            |            |            |
| nistrativeTa |                   |            |            |            |            |
| sks.Customiz |                   |            |            |            |            |
| ingEmailTemp |                   |            |            |            |            |
| late>`__     |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Customizing | Adds, edits and   |            |            |            |            |
| BBCodes <#PL | deletes the       |            |            |            |            |
| FUserGuide.B | BBCode tags used  |            |            |            |            |
| uildingYourF | in writing        |            |            |            |            |
| orum.Adminis | posts/topics.     |            |            |            |            |
| trator.Admin |                   |            |            |            |            |
| istrativeTas |                   |            |            |            |            |
| ks.Customizi |                   |            |            |            |            |
| ngBBcodes>`_ |                   |            |            |            |            |
| _            |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Setting up  | Sets up           |            |            |            |            |
| auto-pruning | auto-pruning to   |            |            |            |            |
|  <#PLFUserGu | clean a large     |            |            |            |            |
| ide.Building | amount of         |            |            |            |            |
| YourForum.Ad | obsolete and      |            |            |            |            |
| ministrator. | inactive topics   |            |            |            |            |
| Administrati | based on          |            |            |            |            |
| veTasks.Sett | criteria.         |            |            |            |            |
| ingupAutoPru |                   |            |            |            |            |
| ne>`__       |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Banning     | Bans IPs in the   |            |            |            |            |
| IPs <#PLFUse | whole **Forums**  |            |            |            |            |
| rGuide.Build | application (only |            |            |            |            |
| ingYourForum | administrators)   |            |            |            |            |
| .Moderator.B | and in specific   |            |            |            |            |
| anningIPs>`_ | forums only       |            |            |            |            |
| _            | (administrators   |            |            |            |            |
|              | and moderators).  |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+
| `Managing    | Manages user's    |            |            |            |            |
| users <#PLFU | profile, promotes |            |            |            |            |
| serGuide.Bui | users, bans       |            |            |            |            |
| ldingYourFor | users, views a    |            |            |            |            |
| um.Administr | topic and post of |            |            |            |            |
| ator.Managin | a specific user.  |            |            |            |            |
| gUsers>`__   |                   |            |            |            |            |
+--------------+-------------------+------------+------------+------------+------------+


.. note:: **(\*):** Regular users can only edit/delete their own posts/topics.


.. |image0| image:: images/forum/forum_user_actions.png
.. |image1| image:: images/forum/mod_action_bar.png
.. |image2| images/forum/forum_home.png
