.. _Configuration:

#############
Configuration
#############

    This chapter covers the following topics:

    -  :ref:`Configuration overview <Configuration.ConfigurationOverview>`
       How to change default configurations via ``exo.properties``.

    -  :ref:`eXo Platform configuration <Configuration.eXoConfiguration>`
       Explanation of eXo Platform configuration, its directory and some
       parts of eXo Platform internals.

    -  :ref:`Properties reference <Configuration.PropertiesReference>`
       A reference to eXo configuration properties.

    -  :ref:`Configure username case sensitive <Configuration.CaseSensitiveUsername>`
       How to make eXo Platform usernames case sensitive/insensitive.
       
    -  :ref:`User inactivity delay configuration <Configuration.UserInactivityDelay>`
       How to define the user inactivity delay.

    -  :ref:`Data directory configuration <Configuration.DataDirectory>`
       Explanations of several paths in the local file system.

    -  :ref:`Assets version parameter <Configuration.AssetsVersionConf>`
       eXo Platform assets version parameter.

    -  :ref:`Quartz Scheduler configuration <Configuration.QuartzScheduler>`
       Quartz Scheduler configuration.

    -  :ref:`Configure documents multiupload in the activity stream functionnality <Configuration.CustomizeMultiupload>`
       Parameters to configure the number of files and size per activity.

    -  :ref:`Transaction service <Configuration.JCRTransactionService>`
       Information about the default timeout value of JCR transaction,
       and the value when your application runs longer transactions.

    -  :ref:`Server base URL <Configuration.ServerBaseURL>`
       The server base URL is used to generate links (in emails for
       example). It is necessary to configure it to make the links
       right.

    -  :ref:`Wiki application base URI <Configuration.WikiBaseURI>`
       The base URI for the wiki application.

    -  :ref:`Account setup <Configuration.AccountSetup>`
       How to skip the Account Setup and Greetings! screens in eXo Platform.

    -  :ref:`Custom data validators configuration <Configuration.ValidatorsConfiguration>`
       How to configure custom data validators.

    -  :ref:`Outgoing mail service <OutgoingMailService>`
       The SMTP configurations required for sending emails.

    -  :ref:`Changing sender information of email notification <Configuration.ChangingSenderInformationOfEmailNotifications>`
       Configuration about sender from which all email notifications are
       sent.

    -  :ref:`Subscribing to notifications of document changes <Configuration.EmailNotificationOfDocumentChanges>`
       The email configuration for watching a document.

    -  :ref:`WebDAV configuration <Configuration.WebDAV>`
       Configuration of the WebDAV service.

    -  :ref:`Open in Office configuration <Configuration.OpenInOfficeConfiguration>`
       How to configure the file types associated with the application
       and to set a new label.

    -  :ref:`JODConverter configuration <Configuration.JODConverter>`
       How to enable and configure document preview feature that allows
       users to read online many document types like MS Word.

    -  :ref:`Limiting the size of uploaded files <Configuration.FileSizeLimit>`
       Instructions to configure the maximum allowed size of uploaded
       files.

    -  :ref:`Limiting public access to the upload service <Configuration.UploadHandler>`
       How to configure the upload handler for preventing
       unauthenticated users to use the upload service.

    -  :ref:`Customizing site data <Configuration.CustomizeSiteData>`
       Instructions to configure the import mode for ACME and Intranet
       sites.

    -  :ref:`Enabling/Disabling auto-creating a taxonomy tree <Configuration.AutocreatingTaxonomyTree>`
       Instructions on how to enable/disable auto-creating a taxonomy
       tree during a new site creation.

    -  :ref:`Enabling/Disabling Activity type <Configuration.ActivityType>`
       Instructions on how to enable/disable an activity type from
       posting on streams.

    -  :ref:`Configure spaces administration group <Configuration.SpacesAdministration>`
       How to define spaces administrators groups.

    -  :ref:`Logs <Configuration.Logs>`
       Introduction to the logs of eXo Platform, and where to configure this
       function.

    -  :ref:`JCR Configuration <Configuration.JCR>`
       Details of the set of properties which control the JCR behavior.

    -  :ref:`Cache configuration <Configuration.CacheConfiguration>`
       Overall introduction to the Cache configuration of eXo Platform,
       including: **Portal**, **Social**, and **ECMS**.

    -  :ref:`Predefined users, groups and memberships <Configuration.PredefinedUserGroupMembership>`
       The configurations for users, groups and memberships
       initialization.

    -  :ref:`Gadget configuration <Configuration.GadgetConfiguration>`
       Information about the OAuth key that will be used in case the
       OAuth gadgets do not indicate a key, and how to disable the
       Shindig default online features.

    -  :ref:`Groovy templates statistics <Configuration.statisticsParameter>`
       Parameter for enabling/disabling Groovy Templates statistics.

    -  :ref:`Search connector configuration <Configuration.SearchConnector>`
       Configuration for activating/de-activating a Search connector.

    -  :ref:`Unified Search configuration <Configuration.UnifiedSearch>`
       Configuration for enabling/disabling Fuzzy search and adjusting
       the similarity criterion.

    -  :ref:`Elasticsearch Configuration <Configuration.ElasticSearch>`
       Configuration of Elasticsearch parameters.

    -  :ref:`CometD <Configuration.CometDConfig>`
       CometD introduction and how to configure it.

    -  :ref:`Youtube integration <Configuration.YoutubeIntegration>`
       Instruction to enable the Youtube integration using a YouTube V3
       API Key.

    -  :ref:`Notification <Configuration.Notification>`
       Configuration related to the Email/On-site Notification feature.

    -  :ref:`Document Versioning <Configuration.DocumentVersioning>`
       Instruction to enable the Document versioning and control the
       generated versions.

    -  :ref:`Document Viewer <Configuration.DocumentViewer>`
       Configuration related to the Document Viewer component.

    -  :ref:`Forgot Password <Configuration.ForgotPassword>`
       Configuration related to the Forgot Password feature.

    -  :ref:`Password Encryption <Configuration.PasswordEncryption>`
       Users who upgrade from a previous version older than 4.3 will
       need to beware of the new default encryption algorithm.

    -  :ref:`Task Management <Configuration.TaskManagement>`
       Configuration related to the project workflow in the Task
       Management application.

    -  :ref:`Chat Configuration <Configuration.ChatConfiguration>`
       Configuration needed for eXo Chat.

    -  :ref:`Update of last login time <Configuration.lastlogintime>`
       Parameter for enabling/disabling the update of user's last login
       time.

.. _Configuration.ConfigurationOverview:

======================
Configuration overview
======================

In eXo Platform, a lot of configuration options are customizable via
properties. If you want to change the default configurations of eXo Platform,
simply do as follows:

1. Create your own ``.properties`` file that must be named
   ``exo.properties``. This file contains all configurations to be
   customized.

   -  ``$PLATFORM_TOMCAT_HOME/gatein/conf/exo.properties`` (Tomcat).

   -  ``$PLATFORM_JBOSS_HOME/standalone/configuration/gatein/exo.properties``
   (JBoss).

A ``.properties`` file has no header, so you do not need to preserve the
header. You can refer to ``exo-sample.properties`` that is provided by
default but has no effect on the eXo Platform configuration. This default
file exposes all properties you can override or extend, but in comments
(#). Instead of creating new, you can rename ``exo-sample.properties``
into ``exo.properties``, then make changes on your needed properties and
remove their comments.

2. Add configurations to be customized in ``exo.properties``. Pay attention
   to the followings:

   -  Each property is defined on one line that conforms to the syntax:
      *property\_name=property\_value*.

   -  Order of the property lines does not take any effect, but it is
      important that you use the exact key of each property in
      ``exo.properties`` that is already exposed in
      ``exo-sample.properties`` or listed in this chapter. The usage of
      properties and their keys are detailed in the later sections.

   -  The text before the equal sign is the key that you should not change
      and the text after the equal sign is the property's value that you
      can edit.

3. Save and restart the eXo Platform server for your changes to take 
   effect.

Besides the capability of customizing configurations in
``exo.properties``, you can follow in another way by adding a system
property, either in ``bin/setenv-customize.sample.(sh|bat)`` or
``bin/standalone-customize.sample.conf(.bat)``, or in any your custom
scripts. See :ref:`Customizing environment variables <CustomizingEnvironmentVariables>`
for detailed instructions.

.. note:: There are some configuration properties that will not be
		  configurable by the system property but in ``exo.properties`` only,
		  including:

			-  ``exo.jcr.cluster.jgroups.config``

			-  ``exo.idm.cluster.jgroups.config``

			-  ``exo.jcr.cache.config``

			-  ``exo.jcr.cache.config.workspace.portal-system``

			-  ``exo.jcr.lock.cache.config``

			-  ``exo.jcr.index.cache.config``

			-  ``exo.cache.config.template``

			-  ``exo.idm.api.store.config``

.. _Configuration.eXoConfiguration:

============================
eXo Platform configuration
============================

In eXo Platform, almost all configurations are performed in a folder that is
controlled by a system property named **exo.conf.dir**. This property is
set by ``setenv.*`` scripts (Tomcat) or ``standalone-exo-*.xml`` files
(JBoss).

The default value of **exo.conf.dir** is:

-  ``$PLATFORM_TOMCAT_HOME/gatein/conf`` (Tomcat).

-  ``$PLATFORM_JBOSS_HOME/standalone/configuration/gatein`` (JBoss).

That folder contains the following main files that you need to take
care: ``exo.properties`` (if you need to override the eXo Platform
configurations); ``configuration.xml`` and
``portal/${PORTAL_NAME}/configuration.xml`` (if having the
${PORTAL\_NAME} portal container).

.. note:: The xml configuration is mainly done during the development phase,
		  whereas the configuration in ``exo.properties`` targets the
		  deployment phase. So configurations that you want to customize
		  should be done in the ``exo.properties`` file.

To understand more clearly the role of those files, let's begin with the
portal container concept.

The eXo Platform Kernel collects runtime components in the portal containers.
A portal container holds all components to run a portal instance. It
serves pages under the servlet context for its name.

The default portal container in eXo Platform is called "portal". This
explains why the default URL of the samples is
*http://localhost:8080/portal*. The default portal container can be
configured directly inside **exo.conf.dir**.

eXo Platform is capable of running several portal instances simultaneously on
the same server. Each instance can be configured and customized
independently via files located at: ``portal/${PORTAL_NAME}`` (under
**exo.conf.dir**), where **${PORTAL\_NAME}** is the name of the portal
container.

.. note:: The name of the configuration file can be altered. Please refer to
		  the `PortalContainer <#PortalContainer>`__ section in the Kernel
		  reference for more details on portal containers and other options to
		  modify the location of the properties.

Services that run inside a portal container are declared via the xml
configuration files like ``configuration.xml``. Such files exist in
jars, wars and below **exo.conf.dir**.

The ``.xml`` configuration files also serve as the main way to customize
the portal via the multiple plugins offered by the eXo Platform components.

Additionally, the ``.xml`` files may contain variables that are
populated via properties defined in ``exo.properties``. Hence, the
``exo.properties`` file serves as exposing some selected variables that
are necessary to configure eXo Platform in a server environment.

exo.properties
~~~~~~~~~~~~~~~

This file can be added to easily override or extend configurations of
eXo Platform. The important variables that can be overridden are exposed in a
sample properties file named ``exo-sample.properties``, but in comments.
See :ref:`Configuration overview <Configuration.ConfigurationOverview>`
for more details.

configuration.xml
~~~~~~~~~~~~~~~~~~

This file contains the built-in configuration for the "portal" portal
container.

-  In most cases, you should not change this file.

-  In case you do not want to use "portal" as the default portal for
   your project, this file can be used to import another
   PortalContainerDefinition into the root container.

.. note:: To learn more about how to configure a new portal container, please
		  refer to `eXo Kernel <../../reference/html/chapter-Kernel.html>`__.

portal/${PORTAL\_NAME}/configuration.xml
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The extra configuration for the ${PORTAL\_NAME} portal container if any.
This is where further customizations (for ${PORTAL\_NAME} portal
container) can be placed. Generally, custom configurations are provided
by extension wars. However, this file is the last loaded by Kernel. It
has a higher priority over any other configuration files, including
extensions. So, you can override any internal component configuration.

This may turn handy services or configurations that are not exposed in
``exo.properties``.

.. _Configuration.PropertiesReference:

====================
Properties reference
====================

This page is a reference to configurations exposed via
``exo.properties``.

 .. note:: This is not an exhaustive list. Some properties are not documented
		   in this chapter, because they are extremely rarely used by
		   administrators. If the property you are searching for is not here,
		   search it in the whole documentation and raise a question in
		   `Community Forum <http://community.exoplatform.com/portal/intranet/forum>`__,
		   if necessary.
		   
.. _PlatformProperties:

Platform
~~~~~~~~~ 

+----------------------------+------------------+-------------------------+
| Name                       | Description      | Default                 |
+============================+==================+=========================+
| exo.base.url    	     | Generates links. | http://localhost:8080   |
+----------------------------+------------------+-------------------------+
| exo.accountsetup.skip      | Skips "account   | false                   |
| 			     | setup" screen or |                         |
|            		     | not?             |                         |
+----------------------------+------------------+-------------------------+
| exo.super.user 	     | The predefined   | root                    |
| 		             | super user's     |                         |
| 			     | name.            |                         |
+----------------------------+------------------+-------------------------+               
| exo.portal.resetpassword.ex| The expiration   | 24 (hours)              |
| piretime   		     | time of a reset  |                         |
| 			     | password link.   |                         |
+----------------------------+------------------+-------------------------+                                         

.. _SMTP:

SMTP
~~~~~

+----------------------------+------------------+-------------------------+
| Name                       | Description      | Default                 |
+============================+==================+=========================+
| :ref:`exo.email.smtp.from  | The "From" field | noreply@exoplatform.com |
| <OutgoingMailService>`     | in outgoing      |                         |
|       		     | emails.          |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.host  | The external     | localhost               |
|  <OutgoingMailService>`    | mail server.     |                         |
|       		     | emails.          |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.port  | The external     | 25                      |
| <OutgoingMailService>`     | mail server      |                         |
|                            | port.            |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.start | Enable TLS or    | false                   |
| tls.enable 		     | not?             |                         |
| <OutgoingMailService>`     |			|			  |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.auth  | Enable SMTP      | false                   |
| <OutgoingMailService>`     | authentication   |                         |
|                            | or not?          |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.usern | Username to get  |                         |
| ame <OutgoingMailService>` | authenticated    |                         |
|			     | with the mail    |                         |
|                            | server.          |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.pass  | Password to get  |                         |
| word <OutgoingMailService>`| authenticated    |                         |
| 			     | with the mail    |                         |
|                            | server.          |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.sock  | Port to connect  |                         |
| etFactory.port             | to if a socket   |                         |
| <OutgoingMailService>`     | factory is       |                         |
|                            | specified.       |                         |
+----------------------------+------------------+-------------------------+
| :ref:`exo.email.smtp.sock  | A class to       |                         |
| etFactory.class            | create SMTP      |                         |
| <OutgoingMailService>`     | sockets.         |                         |
+----------------------------+------------------+-------------------------+                
                                                                                                                                                                                                                   
.. _JODConverter:                                                                                                   

JODConverter
~~~~~~~~~~~~~

+-------------------------------+------------------+-------------------------+
| Name                          | Description      | Default                 |
+===============================+==================+=========================+
| :ref:`exo.jodconverter.enable | Enable           | true                    |
| <JODConverterConf>`           | JODConverter or  |                         |
|                               | not?             |                         |
+-------------------------------+------------------+-------------------------+
| :ref:`exo.jodconverter.port   | List of ports    | 2002                    |
| numbers <JODConverterConf>`   | used to create   |                         |
|                               | *soffice*        |                         |
|                               | processes.       |                         |
+-------------------------------+------------------+-------------------------+
| :ref:`exo.jodconverter.office | The home folder  | Blank (auto-detected)   |
| home <JODConverterConf>`      | of the Office    |                         |
| 			        | installation.    |                         |
+-------------------------------+------------------+-------------------------+
| :ref:`exo.jodconverter.taskqu | The maximum      | 30000                   |
| euetimeout <JODConverterConf>`| living time in   |                         |
| 			        | milliseconds of  |                         |
|                               | a task in the    |                         |
|                               | conversation     |                         |
|                               | queue.           |                         |
+-------------------------------+------------------+-------------------------+
| :ref:`exo.jodconverter.taskex | The maximum time | 120000                  |
| ecutiontimeout 	        | in milliseconds  |                         |
| <JODConverterConf>`           | to process a     |                         |
|                               | task.            |                         |
+-------------------------------+------------------+-------------------------+
| :ref:`exo.jodconverter.maxtas | The maximum      | 200                     |
| ksperprocess                  | number of tasks  |                         |
| <JODConverterConf>`           | to process by an |                         |
|                               | office server.   |                         |
+-------------------------------+------------------+-------------------------+
| :ref:`exo.jodconverter.retryt | The interval     | 120000                  |
| imeout <JODConverterConf>`    | time in          |                         |
|                               | milliseconds to  |                         |
|                               | try to restart   |                         |
|                               | an office server |                         |
|                               | in case it       |                         |
|                               | unexpectedly     |                         |
|                               | stops.           |                         |
+-------------------------------+------------------+-------------------------+


.. _SearchConnector:

Search connector
~~~~~~~~~~~~~~~~~

+----------------------------------+------------------+-------------------------+
| Name                             | Description      | Default                 |
+==================================+==================+=========================+
| :ref:`exo.[searchConnectorName]. | Turn on/off a    | true                    |
| connector.[informationType]      | specific Search  |                         |
| .enable <SearchConnector>`       | connector for a  |                         |
|   				   | certain          |                         |
|                             	   | information      |                         |
|                                  | type.            |                         |
+----------------------------------+------------------+-------------------------+        

.. _UnifiedSearch:

Unified Search
~~~~~~~~~~~~~~~   

+-----------------------------+------------------+-------------------------+
| Name                        | Description      | Default                 |
+=============================+==================+=========================+
| `exo.unified-search.engine. | Enable fuzzy     | true                    |
| fuzzy.enable <#PLFAdminGuid | search or not?   |                         |
| e.Configuration.UnifiedSear |                  |                         |
| ch>`__                      |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.unified-search.engine. | A float number   | 0.5                     |
| fuzzy.similarity <#PLFAdmin | between 0 and 1  |                         |
| Guide.Configuration.Unified | expressing how   |                         |
| Search>`__                  | much a returned  |                         |
|                             | word matches the |                         |
|                             | keyword. 1 is    |                         |
|                             | exact search.    |                         |
+-----------------------------+------------------+-------------------------+
| `exo.unified-search.exclude | List of          | ``.-``                  |
| d-characters <#PLFAdminGuid | characters that  |                         |
| e.Configuration.UnifiedSear | will not be      |                         |
| ch>`__                      | indexed (so      |                         |
|                             | could not be     |                         |
|                             | searched).       |                         |
+-----------------------------+------------------+-------------------------+

.. _Notification:
                                
Notification
~~~~~~~~~~~~~ 

+-----------------------------+------------------+-------------------------+
| Name                        | Description      | Default                 |
+=============================+==================+=========================+
| `exo.notification.Notificat | Cron expression  | 0 0 23 ? \* \* (11:00pm |
| ionDailyJob.expression <#PL | to schedule      | every day)              |
| FAdminGuide.Configuration.N | daily emails.    |                         |
| otification>`__             |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.Notificat | Cron expression  | 0 0 11 ? \* SUN (11:00am|
| ionWeeklyJob.expression <#P | to schedule      | every Sunday)           |
| LFAdminGuide.Configuration. | weekly emails.   |                         |
| Notification>`__            |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.service.Q | The delay time   | 60                      |
| ueueMessage.period <#PLFAdm | (in seconds)     |                         |
| inGuide.Configuration.Notif | between two      |                         |
| ication>`__                 | batches of sent  |                         |
|                             | mails.           |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.service.Q | The maximum      | 30                      |
| ueueMessage.numberOfMailPer | number of emails |                         |
| Batch <#PLFAdminGuide.Confi | sent each batch. |                         |
| guration.Notification>`__   |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.portalnam | The "from" field | eXo                     |
| e <#PLFAdminGuide.Configura | in notification  |                         |
| tion.Notification>`__       | emails.          |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.maxitems  | Maximum number   | 8                       |
| <#PLFAdminGuide.Configurati | of notifications |                         |
| on.Notification>`__         | displayed in the |                         |
|                             | popup list.      |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.viewall < | Living days of   | 30                      |
| #PLFAdminGuide.Configuratio | items displayed  |                         |
| n.Notification>`__          | in the View All  |                         |
|                             | page.            |                         |
+-----------------------------+------------------+-------------------------+
| `exo.notification.WebNotifi | Cron expression  | 0 0 23 ? \* \* (11:00pm |
| cationCleanJob.expression < | to schedule the  | every day)              |
| #PLFAdminGuide.Configuratio | job that cleans  |                         |
| n.Notification>`__          | web notification |                         |
|                             | old items.       |                         |
+-----------------------------+------------------+-------------------------+ 

.. _JCR:                                                                                           

JCR
~~~~   

+-----------------------------+------------------+-------------------------+
| Name                        | Description      | Default                 |
+=============================+==================+=========================+
| `exo.jcr.datasource.dialect | In most cases    | auto                    |
|  <#PLFAdminGuide.Database.C | the dialect is   |                         |
| onfiguringPLF>`__           | auto-detected.   |                         |
|                             | Follow the link  |                         |
|                             | to know          |                         |
|                             | exceptions.      |                         |
+-----------------------------+------------------+-------------------------+
| `exo.jcr.storage.enabled <# | Enable file      | true                    |
| PLFAdminGuide.Configuration | system storage   |                         |
| .DataDirectory>`__          | for JCR values?  |                         |
+-----------------------------+------------------+-------------------------+               
                                                                
.. _Webdav:

WebDav
~~~~~~~
+-----------------------------+------------------+-------------------------+
| Name                        | Description      | Default                 |
+=============================+==================+=========================+
| `exo.webdav.def-folder-node | Matching node    | nt:folder               |
| -type <#PLFAdminGuide.Confi | type of folders. |                         |
| guration.WebDAV>`__         |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.webdav.def-file-node-t | Matching node    | nt:file                 |
| ype <#PLFAdminGuide.Configu | type of files.   |                         |
| ration.WebDAV>`__           |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.webdav.def-file-mimety | The mimetype to  | application/octet-stream|
| pe <#PLFAdminGuide.Configur | exchange file    |                         |
| ation.WebDAV>`__            | data.            |                         |
+-----------------------------+------------------+-------------------------+
| `exo.webdav.update-policy < | The policy       | create-version          |
| #PLFAdminGuide.Configuratio | applied when     |                         |
| n.WebDAV>`__                | there is an      |                         |
|                             | update via       |                         |
|                             | WebDav.          |                         |
+-----------------------------+------------------+-------------------------+
| `exo.webdav.folder-icon-pat | The display icon | /eXoWCMResources/skin/  |
| h <#PLFAdminGuide.Configura | of a folder.     | images/file/nt-folder.  |
| tion.WebDAV>`__             |                  | png                     |
+-----------------------------+------------------+-------------------------+
| `exo.webdav.cache-control < | The              | text/\*:max-age=3600;   |
| #PLFAdminGuide.Configuratio | cache-control    | image/\*:max-age=1800;  |
| n.WebDAV>`__                | header that      | application/\*:max-age= |
|                             | defines cache    | 1800;\*/\*:no-cache     |
|                             | and cache live   |                         |
|                             | time.            |                         |
+-----------------------------+------------------+-------------------------+                  

.. _ECMS:                                  

ECMS                    
~~~~~~

+-----------------------------+------------------+-------------------------+
| Name                        | Description      | Default                 |
+=============================+==================+=========================+
| `exo.ecms.connector.drives. | Maximum size (in | 200                     |
| uploadLimit <#PLFAdminGuide | MB) allowed of   |                         |
| .Configuration.FileSizeLimi | an uploaded      |                         |
| t>`__                       | file.            |                         |
+-----------------------------+------------------+-------------------------+
| `exo.portal.uploadhandler.p | Turn on/off      | true                    |
| ublic-restriction <#PLFAdmi | public access to |                         |
| nGuide.Configuration.Upload | the upload       |                         |
| Handler>`__                 | service.         |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.connector.drives. | The maximum      | 3                       |
| clientLimit <#PLFUserGuide. | number of        |                         |
| ManagingYourDocuments.Worki | concurrent       |                         |
| ngWithBasicActions.Uploadin | uploaded files   |                         |
| gFiles>`__                  | in client side.  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.connector.drives. | The maximum      | 20                      |
| serverLimit <#PLFUserGuide. | number of        |                         |
| ManagingYourDocuments.Worki | concurrent       |                         |
| ngWithBasicActions.Uploadin | uploaded files   |                         |
| gFiles>`__                  | in server side.  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.search.excluded-m | Content of these | text/css,text/javascript|
| imetypes <#PLFUserGuide.Man | mimetypes will   | ,application/x-         |
| agingYourWebsites.Searching | not be searched. | javascript,             |
| ForContentInASite.Searching |                  | text /ecmascript        |
| ForContent>`__              |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.search.enableFuzz | Enable fuzzy     | true                    |
| ySearch <#PLFUserGuide.Mana | search or not?   |                         |
| gingYourWebsites.SearchingF |                  |                         |
| orContentInASite.SearchingF |                  |                         |
| orContent>`__               |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.search.fuzzySearc | A float number   | 0.8                     |
| hIndex <#PLFUserGuide.Manag | between 0 and 1  |                         |
| ingYourWebsites.SearchingFo | expressing how   |                         |
| rContentInASite.SearchingFo | much a returned  |                         |
| rContent>`__                | word matches the |                         |
|                             | keyword. 1 is    |                         |
|                             | exact search.    |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.lock.admin <#PLFU | Users or groups  | \*:/platform/s          |        
| serGuide.AdministeringeXoPl | who can manage   |  administrator          |
| atform.ContentAdministratio | locks.           |                         |
| n.WorkingWithRepository.Loc |                  |                         |
| ks>`__                      |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.friendly.enabled  | Enable friendly  | true                    |
| <#PLFRefGuide.Configuration | URL maker or     |                         |
| s.ExternalComponentPlugins. | not?             |                         |
| Content.FriendlyPlugin>`__  |                  |                         |
+-----------------------------+------------------+-------------------------+
| `exo.ecms.friendly.servletN | The friendly     | content                 |
| ame <#PLFRefGuide.Configura | name used when   |                         |
| tions.ExternalComponentPlug | making friendly  |                         |
| ins.Content.FriendlyPlugin> | URLs.            |                         |
| `__                         |                  |                         |
+-----------------------------+------------------+-------------------------+                                         

.. _ECMSWatchDocument:

ECMS Watch Document
~~~~~~~~~~~~~~~~~~~~ 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.ecms.watchdocument.sen | The "from" field | support@exoplatform.com     |
| der <#PLFAdminGuide.Configu | in the           |                             |
| ration.EmailNotificationOfD | notification     |                             |
| ocumentChanges>`__          | emails.          |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ecms.watchdocument.sub | The subject of   | "Your watching document is  |
| ject <#PLFAdminGuide.Config | the notification | changed"                    |
| uration.EmailNotificationOf | emails.          |                             |
| DocumentChanges>`__         |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ecms.watchdocument.mim | Mimetype of the  | text/html                   |
| etype <#PLFAdminGuide.Confi | message body.    |                             |
| guration.EmailNotificationO |                  |                             |
| fDocumentChanges>`__        |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ecms.watchdocument.con | The message      | Check it yourself in        |
| tent <#PLFAdminGuide.Config | body.            | ``exo-sample.properties``   |
| uration.EmailNotificationOf |                  |                             |
| DocumentChanges>`__         |                  |                             |
+-----------------------------+------------------+-----------------------------+                                                      

.. _ECMSDocumentversioning:

ECMS Document versioning
~~~~~~~~~~~~~~~~~~~~~~~~~~                 

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.ecms.documents.version | The drives that  | Managed                     |
| ing.drives <#PLFAdminGuide. | are enabled for  | Sites,Groups,Personal       |
| Configuration.DocumentVersi | Document         | Documents                   |
| oning>`__                   | versioning.      |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ecms.documents.version | The max number   | 0 (no limit)                |
| s.max <#PLFAdminGuide.Confi | of versions that |                             |
| guration.DocumentVersioning | a document can   |                             |
| >`__                        | have.            |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ecms.documents.version | The expiration   | 0 (no limit)                |
| s.expiration <#PLFAdminGuid | time (in days)   |                             |
| e.Configuration.DocumentVer | of a document    |                             |
| sioning>`__                 | version.         |                             |
+-----------------------------+------------------+-----------------------------+    

.. _ECMSDocumentviewer:

ECMS Document viewer
~~~~~~~~~~~~~~~~~~~~~ 

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.ecms.documents.pdfview | Max file size of | 10                          |
| er.max-file-size <#PLFAdmin | documents for    |                             |
| Guide.Configuration.Documen | preview, in MB   |                             |
| tViewer>`__                 |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ecms.documents.pdfview | Max number of    | 99                          |
| er.max-pages <#PLFAdminGuid | pages of         |                             |
| e.Configuration.DocumentVie | documents for    |                             |
| wer>`__                     | preview          |                             |
+-----------------------------+------------------+-----------------------------+       

.. _CalendarProperties:

Calendar
~~~~~~~~~ 

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+ 
| `exo.calendar.default.event | An integer       | 2 (equivalent to 1 hour)    |
| .suggest <#PLFAdminGuide.Co | number n, used   |                             |
| nfiguration.EndDateSuggesti | to               |                             |
| on>`__                      | auto-calculate   |                             |
|                             | and suggest the  |                             |
|                             | end time when    |                             |
|                             | users            |                             |
|                             | create/edit an   |                             |
|                             | event.           |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.calendar.default.task. | An integer       | 1 (equivalent to 30 mins)   |
| suggest <#PLFAdminGuide.Con | number n, used   |                             |
| figuration.EndDateSuggestio | to               |                             |
| n>`__                       | auto-calculate   |                             |
|                             | and suggest the  |                             |
|                             | end time when    |                             |
|                             | users            |                             |
|                             | create/edit a    |                             |
|                             | task.            |                             |
+-----------------------------+------------------+-----------------------------+

.. _SiteMetadataProperties:

Site metadata
~~~~~~~~~~~~~~           

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.intranet.portalConfig. | Don't change     | false                       |
| metadata.override <#PLFDevG | this unless you  |                             |
| uide.Site.CreateNew.Redeplo | customize the    |                             |
| ySiteExtension>`__          | Intranet site.   |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.intranet.portalConfig. | Don't change     | insert                      |
| metadata.importmode <#PLFDe | this unless you  |                             |
| vGuide.Site.CreateNew.Redep | customize the    |                             |
| loySiteExtension>`__        | Intranet site.   |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.acme.portalConfig.meta | Only affect when | false                       |
| data.override <#eXoAddonsGu | you install the  |                             |
| ide.ACME.Installation>`__   | ACME addon.      |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.ide.portalConfig.metad | Only affect when | true                        |
| ata.override <#eXoAddonsGui | you install the  |                             |
| de.IDE>`__                  | IDE addon.       |                             |
+-----------------------------+------------------+-----------------------------+

.. _DatasourceProperties:

 Datasource              
~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.jcr.datasource.name <# | JCR datasource   | java:/comp/env/exo-jcr      |
| PLFAdminGuide.Database.JNDI | name.            |                             |
| >`__                        |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.idm.datasource.name <# | IDM datasource   | java:/comp/env/exo-idm      |
| PLFAdminGuide.Database.JNDI | name.            |                             |
| >`__                        |                  |                             |
+-----------------------------+------------------+-----------------------------+                                                                      
.. _ClusteringProperties:

Clustering
~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| exo.cluster.partition.name  | Give a string to | DefaultPartition            |
|                             | identify your    |                             |
|                             | cluster, to      |                             |
|                             | avoid conflict   |                             |
|                             | with other       |                             |
|                             | clusters in the  |                             |
|                             | network.         |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.jcr.cluster.jgroups.tc | JGroups          |                             |
| p\* <#PLFAdminGuide.Cluster | configuration    |                             |
| ing.JGroups.JCR.TCP>`__     | for JCR using    |                             |
|                             | TCP.             |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.jcr.cluster.jgroups.ud | JGroups          |                             |
| p.\* <#PLFAdminGuide.Cluste | configuration    |                             |
| ring.JGroups.JCR.UDP>`__    | for JCR using    |                             |
|                             | UDP.             |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.idm.cluster.jgroups.tc | JGroups          |                             |
| p\* <#PLFAdminGuide.Cluster | configuration    |                             |
| ing.JGroups.IDM.TCP>`__     | for IDM using    |                             |
|                             | TCP.             |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.idm.cluster.jgroups.ud | JGroups          |                             |
| p.\* <#PLFAdminGuide.Cluste | configuration    |                             |
| ring.JGroups.IDM.UDP>`__    | for IDM using    |                             |
|                             | UDP.             |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.jcr.cluster.jgroups.co | Path to your     |                             |
| nfig <#PLFAdminGuide.Cluste | customized       |                             |
| ring.JGroups_xml>`__        | JGroups          |                             |
|                             | configuration    |                             |
|                             | file, applied to |                             |
|                             | JCR.             |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.jcr.cluster.jgroups.co | URL to your      |                             |
| nfig-url <#PLFAdminGuide.Cl | customized       |                             |
| ustering.JGroups_xml>`__    | JGroups          |                             |
|                             | configuration    |                             |
|                             | file, applied to |                             |
|                             | JCR.             |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.idm.cluster.jgroups.co | Path to your     |                             |
| nfig <#PLFAdminGuide.Cluste | customized       |                             |
| ring.JGroups_xml>`__        | JGroups          |                             |
|                             | configuration    |                             |
|                             | file, applied to |                             |
|                             | IDM.             |                             |
+-----------------------------+------------------+-----------------------------+                           

.. _QuartzSchedulerProperties:

Quartz Scheduler
~~~~~~~~~~~~~~~~~

 **Main Scheduler Properties**   
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+ 
| `exo.quartz.scheduler.insta | The name of the  | ExoScheduler                |
| nceName <#PLFAdminGuide.Con | scheduler        |                             |
| figuration.QuartzScheduler> | instance.        |                             |
| `__                         |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.scheduler.insta | The type of the  | AUTO                        |
| nceId <#PLFAdminGuide.Confi | scheduler        |                             |
| guration.QuartzScheduler>`_ | instance.        |                             |
| _                           |                  |                             |
+-----------------------------+------------------+-----------------------------+                                                                        

 **ThreadPool configuration Properties**                  

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.quartz.threadPool.clas | Is the name of   | org.quartz.simpl.SimpleThre |
| s <#PLFAdminGuide.Configura | the ThreadPool   | adPool                      |
| tion.QuartzScheduler>`__    | implementation   |                             |
|                             | used.            |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.threadPool.thre | It an integer    | 5 (which is the value of    |
| adPriority <#PLFAdminGuide. | value between    | Thread.NORM\_PRIORITY)      |
| Configuration.QuartzSchedul | Thread.MIN\_PRIO |                             |
| er>`__                      | RITY             |                             |
|                             | (which is 1) and |                             |
|                             | Thread.MAX\_PRIO |                             |
|                             | RITY             |                             |
|                             | (which is 10).   |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.threadPool.thre | It is the number | 25                          |
| adCount <#PLFAdminGuide.Con | of threads that  |                             |
| figuration.QuartzScheduler> | are available    |                             |
| `__                         | for concurrent   |                             |
|                             | execution of     |                             |
|                             | jobs.            |                             |
+-----------------------------+------------------+-----------------------------+                                         

 **JobStore configuration Properties**                  

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.quartz.jobStore.misfir | The number of    | 6000                        |
| eThreshold <#PLFAdminGuide. | milliseconds the |                             |
| Configuration.QuartzSchedul | scheduler will   |                             |
| er>`__                      | tolerate a       |                             |
|                             | trigger to pass  |                             |
|                             | its              |                             |
|                             | next-fire-time   |                             |
|                             | by, before being |                             |
|                             | considered       |                             |
|                             | misfired.        |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.class  | The Scheduler’s  | org.quartz.impl.jdbcjobstor |
| <#PLFAdminGuide.Configurati | JobStore class   | e.JobStoreTX                |
| on.QuartzScheduler>`__      | name.            |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.driver | The Driver       | org.quartz.impl.jdbcjobstor |
| DelegateClass <#PLFAdminGui | delegate which   | e.StdJDBCDelegate           |
| de.Configuration.QuartzSche | will understand  |                             |
| duler>`__                   | the database     |                             |
|                             | system dialect.  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.usePro | The flag which   | false                       |
| perties <#PLFAdminGuide.Con | instructs        |                             |
| figuration.QuartzScheduler> | JDBCJobStore     |                             |
| `__                         | that all values  |                             |
|                             | in JobDataMaps   |                             |
|                             | will be Strings. |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.dataSo | The name of the  | quartzDS                    |
| urce <#PLFAdminGuide.Config | DataSources      |                             |
| uration.QuartzScheduler>`__ | defined in the   |                             |
|                             | configuration    |                             |
|                             | properties file  |                             |
|                             | for quartz.      |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.tableP | The prefix used  | QRTZ\_                      |
| refix <#PLFAdminGuide.Confi | for to Quartz’s  |                             |
| guration.QuartzScheduler>`_ | tables in the    |                             |
| _                           | database.        |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.isClus | Set to "true" in | false                       |
| tered <#PLFAdminGuide.Confi | order to turn on |                             |
| guration.QuartzScheduler>`_ | clustering       |                             |
| _                           | features.        |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.cluste | Set the          | 20000                       |
| rCheckinInterval <#PLFAdmin | frequency (in    |                             |
| Guide.Configuration.QuartzS | milliseconds) at |                             |
| cheduler>`__                | which this       |                             |
|                             | instance         |                             |
|                             | "checks-in" with |                             |
|                             | other instances  |                             |
|                             | of the cluster.  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.maxMis | The maximum      | 20                          |
| firesToHandleAtATime <#PLFA | number of        |                             |
| dminGuide.Configuration.Qua | misfired         |                             |
| rtzScheduler>`__            | triggers the     |                             |
|                             | jobstore will    |                             |
|                             | handle in a      |                             |
|                             | given pass.      |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.dontSe | Setting this     | false                       |
| tAutoCommitFalse <#PLFAdmin | parameter to     |                             |
| Guide.Configuration.QuartzS | "true" tells     |                             |
| cheduler>`__                | Quartz not to    |                             |
|                             | call             |                             |
|                             | setAutoCommit(fa |                             |
|                             | lse)             |                             |
|                             | on connections   |                             |
|                             | obtained from    |                             |
|                             | the              |                             |
|                             | DataSource(s).   |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.acquir | Whether or not   | false                       |
| eTriggersWithinLock <#PLFAd | the acquisition  |                             |
| minGuide.Configuration.Quar | of next triggers |                             |
| tzScheduler>`__             | to fire should   |                             |
|                             | occur within an  |                             |
|                             | explicit         |                             |
|                             | database lock.   |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.lockHa | The class name   |                             |
| ndler.class <#PLFAdminGuide | to be used to    |                             |
| .Configuration.QuartzSchedu | produce an       |                             |
| ler>`__                     | instance of a    |                             |
|                             | "org.quartz.impl |                             |
|                             | .jdbcjobstore".  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.driver | A pipe-delimited |                             |
| DelegateInitString <#PLFAdm | list of          |                             |
| inGuide.Configuration.Quart | properties (and  |                             |
| zScheduler>`__              | their values)    |                             |
|                             | that can be      |                             |
|                             | passed to the    |                             |
|                             | DriverDelegate   |                             |
|                             | during           |                             |
|                             | initialization   |                             |
|                             | time.            |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.txIsol | A value of       | false                       |
| ationLevelSerializable <#PL | "true" tells     |                             |
| FAdminGuide.Configuration.Q | Quartz (when     |                             |
| uartzScheduler>`__          | using JobStoreTX |                             |
|                             | or CMT) to call  |                             |
|                             | setTransactionIs |                             |
|                             | olation(Connecti |                             |
|                             | on.TRANSACTION\_ |                             |
|                             | SERIALIZABLE)    |                             |
|                             | on JDBC          |                             |
|                             | connections.     |                             |
|                             | This can be      |                             |
|                             | helpful to       |                             |
|                             | prevent lock     |                             |
|                             | timeouts with    |                             |
|                             | some databases   |                             |
|                             | under high load, |                             |
|                             | and long-lasting |                             |
|                             | transactions.    |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.quartz.jobStore.select | Must be a SQL    | SELECT \* FROM {0}LOCKS     |
| WithLockSQL <#PLFAdminGuide | string that      | WHERE SCHED\_NAME = {1} AND |
| .Configuration.QuartzSchedu | selects a row in | LOCK\_NAME = ? FOR UPDATE   |
| ler>`__                     | the "LOCKS"      |                             |
|                             | table and places |                             |
|                             | a lock on the    |                             |
|                             | row.             |                             |
+-----------------------------+------------------+-----------------------------+

 **Datasources configuration**  
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.quartz.dataSource.quar | The JNDI URL for | java:/comp/env/exo-jpa\_por |
| tzDS.jndiURL <#PLFAdminGuid | a DataSource     | tal                         |
| e.Configuration.QuartzSched | that is managed  |                             |
| uler>`__                    | by eXo Platform. |                             |
+-----------------------------+------------------+-----------------------------+                             


.. _PasswordEncryptionProperties:

Password Encryption
~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.plidm.password.class < | The class that   | DatabaseReadingSaltEncoder  |
| #PLFAdminGuide.Configuratio | encrypts the     |                             |
| n.PasswordEncryption>`__    | user password    |                             |
|                             | before it is     |                             |
|                             | stored in the    |                             |
|                             | database.        |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.plidm.password.hash <# | The encrypt      | SHA-256                     |
| PLFAdminGuide.Configuration | algorithm.       |                             |
| .PasswordEncryption>`__     |                  |                             |
+-----------------------------+------------------+-----------------------------+                                             

.. _ElasticsearchProperties:

Elasticsearch Properties
~~~~~~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.es.version.minor <#PLF | The expected     | 5.6                         |
| AdminGuide.Configuration.El | minor            |                             |
| asticSearch>`__             | Elastisearch     |                             |
|                             | version          |                             |
|                             | compatible with  |                             |
|                             | eXo Platform.    |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.embedded.enabled <# | Allows to run an | true                        |
| PLFAdminGuide.Configuration | Elasticsearch    |                             |
| .ElasticSearch.ESClientProp | server embedded  |                             |
| erties>`__                  | in eXo Platform  |                             |
|                             | (not recommended |                             |
|                             | for production). |                             |
+-----------------------------+------------------+-----------------------------+
| `es.cluster.name <#PLFAdmin | Cluster name     | exoplatform-es              |
| Guide.Configuration.Elastic | identifies your  |                             |
| Search.ESEmbeddedNodeProper | Elasticsearch    |                             |
| ties>`__                    | cluster for      |                             |
|                             | auto-discovery.  |                             |
|                             | If you’re        |                             |
|                             | running multiple |                             |
|                             | clusters on the  |                             |
|                             | same network,    |                             |
|                             | make sure you’re |                             |
|                             | using unique     |                             |
|                             | names.           |                             |
+-----------------------------+------------------+-----------------------------+
| `es.node.name <#PLFAdminGui | Name of the mode | exoplatform-es-embedded     |
| de.Configuration.ElasticSea | for the embedded |                             |
| rch.ESEmbeddedNodePropertie | mode. If not     |                             |
| s>`__                       | specified, a     |                             |
|                             | name is          |                             |
|                             | generated        |                             |
|                             | dynamically at   |                             |
|                             | startup.         |                             |
+-----------------------------+------------------+-----------------------------+
| `es.network.host <#PLFAdmin | Sets both        | "127.0.0.1"                 |
| Guide.Configuration.Elastic | 'bind\_host' and |                             |
| Search.ESEmbeddedNodeProper | 'publish\_host'  |                             |
| ties>`__                    | params. More     |                             |
|                             | details          |                             |
|                             | `here <https://w |                             |
|                             | ww.elastic.co/gu |                             |
|                             | ide/en/elasticse |                             |
|                             | arch/reference/c |                             |
|                             | urrent/modules-n |                             |
|                             | etwork.html#adva |                             |
|                             | nced-network-set |                             |
|                             | tings>`__        |                             |
+-----------------------------+------------------+-----------------------------+
| `es.discovery.zen.ping.unic | In Unicast       | ["127.0.0.1"]               |
| ast.hosts <#PLFAdminGuide.C | dicovery mode,   |                             |
| onfiguration.ElasticSearch. | this parameter   |                             |
| ESEmbeddedNodeProperties>`_ | lets you set a   |                             |
| _                           | list of master   |                             |
|                             | nodes in the     |                             |
|                             | cluster to       |                             |
|                             | perform          |                             |
|                             | discovery when   |                             |
|                             | new nodes        |                             |
|                             | (master or data) |                             |
|                             | are started.     |                             |
+-----------------------------+------------------+-----------------------------+
| `es.http.port <#PLFAdminGui | TCP Port of the  | 9200                        |
| de.Configuration.ElasticSea | embedded ES      |                             |
| rch.ESEmbeddedNodePropertie | node.            |                             |
| s>`__                       |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `es.path.data <#PLFAdminGui | Local path to    | gatein/data                 |
| de.Configuration.ElasticSea | the directory    |                             |
| rch.ESEmbeddedNodePropertie | where to         |                             |
| s>`__                       | Elasticsearch    |                             |
|                             | will store index |                             |
|                             | data allocated   |                             |
|                             | for this node.   |                             |
+-----------------------------+------------------+-----------------------------+

 **Elasticsearch Client**    

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.es.search.server.url < | URL of the node  | "http://127.0.0.1:9200"     |
| #PLFAdminGuide.Configuratio | used for         |                             |
| n.ElasticSearch.ESClientPro | searching.       |                             |
| perties>`__                 | Required and     |                             |
|                             | exo.es.embedded. |                             |
|                             | enabled=false    |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.search.server.usern | Username used    |                             |
| ame <#PLFAdminGuide.Configu | for the BASIC    |                             |
| ration.ElasticSearch.ESClie | authentication   |                             |
| ntProperties>`__            | on the           |                             |
|                             | Elasticsearch    |                             |
|                             | node used for    |                             |
|                             | searching.       |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.search.server.passw | Password used    |                             |
| ord <#PLFAdminGuide.Configu | for the BASIC    |                             |
| ration.ElasticSearch.ESClie | authentication   |                             |
| ntProperties>`__            | on the           |                             |
|                             | Elasticsearch    |                             |
|                             | node used for    |                             |
|                             | searching.       |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.index.server.url <# | URL of the node  | "http://127.0.0.1:9200"     |
| PLFAdminGuide.Configuration | used for         |                             |
| .ElasticSearch.ESClientProp | indexing.        |                             |
| erties>`__                  |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.index.server.userna | Username used    |                             |
| me <#PLFAdminGuide.Configur | for the BASIC    |                             |
| ation.ElasticSearch.ESClien | authentication   |                             |
| tProperties>`__             | on the           |                             |
|                             | Elasticsearch    |                             |
|                             | node used for    |                             |
|                             | indexing.        |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.index.server.passwo | Password used    |                             |
| rd <#PLFAdminGuide.Configur | for the BASIC    |                             |
| ation.ElasticSearch.ESClien | authentication   |                             |
| tProperties>`__             | on the           |                             |
|                             | Elasticsearch    |                             |
|                             | node used for    |                             |
|                             | indexing.        |                             |
+-----------------------------+------------------+-----------------------------+                                     

 **Elasticsearch Indexing properties**                

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.es.indexing.batch.numb | Maximum number   | 1000                        |
| er <#PLFAdminGuide.Configur | of documents     |                             |
| ation.ElasticSearch.Indexin | that can be sent |                             |
| gProperties>`__             | to Elasticsearch |                             |
|                             | in one bulk      |                             |
|                             | request.         |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.indexing.request.si | Maximum size (in | 10485760 (= 10Mb)           |
| ze.limit <#PLFAdminGuide.Co | bytes) of an     |                             |
| nfiguration.ElasticSearch.I | Elasticsearch    |                             |
| ndexingProperties>`__       | bulk request.    |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.reindex.batch.size  | Size of the      | 100                         |
| <#PLFAdminGuide.Configurati | chunks of the    |                             |
| on.ElasticSearch.IndexingPr | reindexing       |                             |
| operties>`__                | batch.           |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.indexing.replica.nu | Number of        | 1                           |
| mber.default <#PLFAdminGuid | replicas of the  |                             |
| e.Configuration.ElasticSear | index.           |                             |
| ch.IndexingProperties>`__   |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.es.indexing.shard.numb | Number of shards | 5                           |
| er.default <#PLFAdminGuide. | of the index.    |                             |
| Configuration.ElasticSearch |                  |                             |
| .IndexingProperties>`__     |                  |                             |
+-----------------------------+------------------+-----------------------------+                                              
.. _EnableDisaleActType:

 Enable/Disable activity type
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.activity-type.activity | The property     | true                        |
| -type-key.enabled <#PLFAdmi | that allows to   |                             |
| nGuide.Configuration.Activi | enable or        |                             |
| tyType>`__                  | disable an       |                             |
|                             | activity having  |                             |
|                             | the type key     |                             |
|                             | `` activity-type |                             |
|                             | -key ``          |                             |
|                             | from posting in  |                             |
|                             | the streams.     |                             |
+-----------------------------+------------------+-----------------------------+                              

.. _FSProperties:

 File storage configuration
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.files.binaries.storage | Allows to define | fs                          |
| .type <#PLFAdminGuide.Confi | the file storage |                             |
| guration.fileStorageconfig> | way: File system |                             |
| `__                         | (type=fs) or     |                             |
|                             | RDBMS            |                             |
|                             | (type=rdbms).    |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.commons.FileStorageCle | Enables/disables | true                        |
| anJob.enabled <#PLFAdminGui | the job that     |                             |
| de.Configuration.fileStorag | cleans unused    |                             |
| econfig>`__                 | files.           |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.commons.FileStorageCle | The retention    | 30 days                     |
| anJob.retention-time <#PLFA | time of unused   |                             |
| dminGuide.Configuration.fil | files            |                             |
| eStorageconfig>`__          |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.commons.FileStorageCle | The cron job     | 0 0 11 ? \* SUN             |
| anJob.expression <#PLFAdmin | expression for   |                             |
| Guide.Configuration.fileSto | scheduling the   |                             |
| rageconfig>`__              | file cleaner job |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.files.storage.dir <#PL | The location     | {exo.data.dir}/files        |
| FAdminGuide.Configuration.f | where to store   |                             |
| ileStorageconfig>`__        | binary files in  |                             |
|                             | case of file     |                             |
|                             | system storage.  |                             |
|                             | In cluster mode, |                             |
|                             | this location    |                             |
|                             | (folder) should  |                             |
|                             | be shared.       |                             |
+-----------------------------+------------------+-----------------------------+                                   

.. _MongoDBConfiguration:

 MongoDB configuration
 ~~~~~~~~~~~~~~~~~~~~~~~
 
 MongoDB is the database for eXo Chat: all the below parameters could be configured in :ref:`chat.properties file <Configuration.ChatConfiguration>`       

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `dbServerType <#PLFAdminGui | Allows to define | mongo                       |
| de.Database.ChatDatabase>`_ | MongoDB type:    |                             |
| _                           | either Mongo or  |                             |
|                             | embed. Embed     |                             |
|                             | value is used    |                             |
|                             | for unit tests.  |                             |
+-----------------------------+------------------+-----------------------------+
| `dbServerHost <#PLFAdminGui | The host name or | localhost                   |
| de.Database.ChatDatabase>`_ | IP of MongoDB.   |                             |
| _                           |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `dbServerPort <#PLFAdminGui | The port number  | 27017                       |
| de.Database.ChatDatabase>`_ | to connect to    |                             |
| _                           | MongoDB host.    |                             |
+-----------------------------+------------------+-----------------------------+
| `dbServerHosts <#PLFAdminGu | The MongoDB      | localhost:27017             |
| ide.Database.ChatDatabase>` | nodes to connect |                             |
| __                          | to, as a         |                             |
|                             | comma-separated  |                             |
|                             | list of          |                             |
|                             | <host:port>      |                             |
|                             | values.          |                             |
+-----------------------------+------------------+-----------------------------+
| `dbName <#PLFAdminGuide.Dat | Name of the      | chat                        |
| abase.ChatDatabase>`__      | Mongo database   |                             |
|                             | name.            |                             |
+-----------------------------+------------------+-----------------------------+
| `dbAuthentication <#PLFAdmi | Enables or       | false                       |
| nGuide.Database.ChatDatabas | disables         |                             |
| e>`__                       | authentication   |                             |
|                             | to access        |                             |
|                             | MongoDB. When    |                             |
|                             | set to true this |                             |
|                             | means that       |                             |
|                             | authentication   |                             |
|                             | is required.     |                             |
+-----------------------------+------------------+-----------------------------+
| `dbUser <#PLFAdminGuide.Dat | Provide the      | EMPTY                       |
| abase.ChatDatabase>`__      | username to      |                             |
|                             | access the       |                             |
|                             | database if      |                             |
|                             | authentication   |                             |
|                             | needed.          |                             |
+-----------------------------+------------------+-----------------------------+
| `dbPassword <#PLFAdminGuide | Provide the      | EMPTY                       |
| .Database.ChatDatabase>`__  | password to      |                             |
|                             | access the       |                             |
|                             | database if      |                             |
|                             | authentication   |                             |
|                             | needed.          |                             |
+-----------------------------+------------------+-----------------------------+
| `chatPassPhrase <#PLFAdminG | The password to  | chat                        |
| uide.ChatAdministration.Con | access REST      |                             |
| figuration.ChatServer>`__   | service on the   |                             |
|                             | BRAND\_CHAT      |                             |
|                             | server.          |                             |
+-----------------------------+------------------+-----------------------------+
| `chatCronNotifCleanup <#PLF | The frequency of | 0 0/60 \* \* \* ?           |
| AdminGuide.ChatAdministrati | cleaning eXo     |                             |
| on.Configuration.ChatServer | Chat             |                             |
| >`__                        | notifications.Th |                             |
|                             | ey               |                             |
|                             | are cleaned up   |                             |
|                             | every one hour   |                             |
|                             | by default.      |                             |
+-----------------------------+------------------+-----------------------------+
| `teamAdminGroup <#PLFAdminG | The eXo group    | /platform/administrators    |
| uide.ChatAdministration.Con | who can create   |                             |
| figuration.ChatServer>`__   | teams.           |                             |
+-----------------------------+------------------+-----------------------------+
| `chatReadDays <#PLFAdminGui | Number of days   | 30 (days)                   |
| de.ChatAdministration.Confi | to display the   |                             |
| guration.ChatServer>`__     | corresponding    |                             |
|                             | chat messages.   |                             |
+-----------------------------+------------------+-----------------------------+
| `chatReadTotalJson <#PLFAdm | The number of    | 200                         |
| inGuide.ChatAdministration. | messages that    |                             |
| Configuration.ChatServer>`_ | you can get in   |                             |
| _                           | the Chat room.   |                             |
+-----------------------------+------------------+-----------------------------+
| `chatIntervalChat <#PLFAdmi | Time interval to | 5000                        |
| nGuide.ChatAdministration.C | refresh messages |                             |
| onfiguration.ChatClientUpda | in a chat.       |                             |
| tes>`__                     |                  |                             |
+-----------------------------+------------------+-----------------------------+
| `chatIntervalSession <#PLFA | Time interval to | 60000                       |
| dminGuide.ChatAdministratio | keep a chat      |                             |
| n.Configuration.ChatClientU | session alive in |                             |
| pdates>`__                  | milliseconds.    |                             |
+-----------------------------+------------------+-----------------------------+
| `chatIntervalStatus <#PLFAd | Time interval to | 60000                       |
| minGuide.ChatAdministration | refresh user     |                             |
| .Configuration.ChatClientUp | status in        |                             |
| dates>`__                   | milliseconds.    |                             |
+-----------------------------+------------------+-----------------------------+
| `chatIntervalNotif <#PLFAdm | Time interval to | 5000                        |
| inGuide.ChatAdministration. | refresh          |                             |
| Configuration.ChatClientUpd | Notifications in |                             |
| ates>`__                    | the main menu in |                             |
|                             | milliseconds.    |                             |
+-----------------------------+------------------+-----------------------------+
| `chatIntervalUsers <#PLFAdm | Time interval to | 60000                       |
| inGuide.ChatAdministration. | refresh Users    |                             |
| Configuration.ChatClientUpd | list in          |                             |
| ates>`__                    | milliseconds.    |                             |
+-----------------------------+------------------+-----------------------------+
| `chatTokenValidity <#PLFAdm | Time after which | 60000                       |
| inGuide.ChatAdministration. | a token will be  |                             |
| Configuration.ChatClientUpd | invalid. The use |                             |
| ates>`__                    | will then be     |                             |
|                             | considered       |                             |
|                             | offline.         |                             |
+-----------------------------+------------------+-----------------------------+

.. _Groovystatistics:

Groovy templates statistics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.statistics.groovy.temp | Enables/disables | true                        |
| late.enabled <#PLFAdminGuid | Groovy Templates |                             |
| e.Configuration.statisticsP | statistics that  |                             |
| arameter>`__                | is collected     |                             |
|                             | asynchronously.  |                             |
+-----------------------------+------------------+-----------------------------+                              

.. _CometDConfiguration:

CometD configuration
~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.cometd.oort.url <#PLFA | The CometD Oort  | "http://localhost:8080/come |
| dminGuide.Clustering.Settin | URL used in      | td/cometd",                 |
| gUpCluster>`__              | clustering mode. | localhost should be         |
|                             |                  | replaced by the hostname or |
|                             |                  | the IP of the cluster node. |
+-----------------------------+------------------+-----------------------------+
| `exo.cometd.oort.configType | The CometD       | multicast                   |
|  <#PLFAdminGuide.Clustering | configuration    |                             |
| .SettingUpCluster>`__       | type which could |                             |
|                             | be either        |                             |
|                             | "static" or      |                             |
|                             | "multicast".     |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.cometd.oort.cloud <#PL | A                |                             |
| FAdminGuide.Clustering.Sett | comma-separated  |                             |
| ingUpCluster>`__            | list of URLs of  |                             |
|                             | other Oort       |                             |
|                             | comets to        |                             |
|                             | connect to at    |                             |
|                             | startup.         |                             |
+-----------------------------+------------------+-----------------------------+                                      

.. _LastLoginTimeProperty:
 
Update of last login time                      
~~~~~~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.idm.user.updateLastLog | Enables/disables | true                        |
| inTime <#PLFAdminGuide.Conf | the update of    |                             |
| iguration.lastlogintime>`__ | last login time  |                             |
|                             | each time the    |                             |
|                             | user login.      |                             |
+-----------------------------+------------------+-----------------------------+                                 

.. _SpaceAdministratorsGroup:
 
 Define spaces administrators group
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.social.spaces.administ | Defines the list |                             |
| rators <#PLFAdminGuide.Conf | of spaces        |                             |
| iguration.SpacesAdministrat | administrators   |                             |
| ion>`__                     | groups.          |                             |
+-----------------------------+------------------+-----------------------------+                                    

.. _AssetsVersion:

 Assets versions used in static resources URLs
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.assets.version <#PLFAd | Defines the      | It is set to eXo Platform   |
| minGuide.Configuration.Asse | assets version.  | binary version.             |
| tsVersionConf>`__           |                  |                             |
+-----------------------------+------------------+-----------------------------+                                             

.. _UsernameCaseSensitive:

 Username case sensitive
 ~~~~~~~~~~~~~~~~~~~~~~~~~
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+ 
| `exo.auth.case.insensitive  | Defines if       | false.                      |
| <#PLFAdminGuide.Configurati | usernames in     |                             |
| on.CaseSensitiveUsername>`_ | PRODUCT are case |                             |
| _                           | sensitive or     |                             |
|                             | not.             |                             |
+-----------------------------+------------------+-----------------------------+

.. _UserInactivityDelay:                                        

 User inactivity delay
 ~~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+ 
| `exo.user.status.offline.de | Defines the time | 240000                      |
| lay <#PLFAdminGuide.Configu | laps which makes |                             |
| ration.UserInactivityDelay> | the user in      |                             |
| `__                         | offline status.  |                             |
|                             | Its value is     |                             |
|                             | expressed in     |                             |
|                             | milliseconds.    |                             |
+-----------------------------+------------------+-----------------------------+                              

.. _NotificationsChannels:

Notifications channels  
~~~~~~~~~~~~~~~~~~~~~~~

+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.notification.channels  | Defines the      | WEB\_CHANNEL, MAIL\_CHANNEL |
| <#PLFAdminGuide.Configurati | activated        |                             |
| on.Notification>`__         | notification     |                             |
|                             | channels.        |                             |
+-----------------------------+------------------+-----------------------------+                                  

.. _WikiBaseURI:

 Wiki application base URI 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `wiki.permalink.appuri <#PL | Defines the base | wiki                        |
| FAdminGuide.Configuration.W | URI for the wiki |                             |
| ikiBaseURI>`__              | application      |                             |
|                             | permalinks.      |                             |
+-----------------------------+------------------+-----------------------------+                                

.. _FilesUploadLimit:

 Files upload limit
 ~~~~~~~~~~~~~~~~~~~
 
+-----------------------------+------------------+-----------------------------+
| Name                        | Description      | Default                     |
+=============================+==================+=============================+
| `exo.ecms.connector.drives. | Maximum size (in | 200                         |
| uploadLimit <#PLFAdminGuide | MB) allowed of   |                             |
| .Configuration.FileSizeLimi | an uploaded      |                             |
| t>`__                       | file.            |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.social.activity.upload | Maximum size (in | 200                         |
| Limit <#PLFAdminGuide.Confi | MB) allowed of   |                             |
| guration.FileSizeLimit>`__  | an uploaded      |                             |
|                             | image through    |                             |
|                             | the CKEditor.    |                             |
+-----------------------------+------------------+-----------------------------+
| `exo.wiki.attachment.upload | Maximum size (in | 200                         |
| Limit <#PLFAdminGuide.Confi | MB) allowed of   |                             |
| guration.FileSizeLimit>`__  | an uploaded file |                             |
|                             | in Wiki          |                             |
|                             | application.     |                             |
+-----------------------------+------------------+-----------------------------+                                 


.. _Configuration.CaseSensitiveUsername:

===================================
Configure username case sensitive
===================================

By default, eXo Platform is case insensitive. You can configure it to become
case sensitive through a parameter in :ref:`exo.properties <Configuration.ConfigurationOverview>`
file:

-  ``exo.auth.case.insensitive``, default value set to true.

If you set the ``exo.auth.case.insensitive`` to true this means that the
username "user" is the same as "User" or "uSEr". If it is set to false,
this means that the user should take care of capital and minimal letters
when typing the username.


.. _Configuration.UserInactivityDelay:

====================================
User inactivity delay configuration
====================================

When a user does not make any action on the platform i.e he is inactive
for a time lapse, he is considered as offline.

The time lapse is configurable in :ref:`exo.properties <Configuration.ConfigurationOverview>`
file using this parameter ``exo.user.status.offline.delay``.

The parameter is expressed in millisecond and the value default is
240000 milliseconds.

.. code:: java

     # The delay when we consider a user as offline. Default value is 240000 milliseconds
    exo.user.status.offline.delay=240000
    
.. _Configuration.DataDirectory:

=============================
Data directory configuration
============================

JCR data is stored in both SQL databases and File System. JCR Database
configuration is explained in `Database <#PLFAdminGuide.Database>`__.
The JCR File System configuration is explained in this section.

Typically, the JCR File System data consists of four folders:

-  JCR indexes.

-  JCR values storage.

   To store JCR value, SQL database is used as primary storage and
   another directory can be used as a secondary, dedicated storage for
   BLOB data. It is optional and you can configure to not store BLOB
   data in File System, by changing the default configuration in the
   `exo.properties <#PLFAdminGuide.Configuration.ConfigurationOverview>`__
   file.

   ::

       exo.jcr.storage.enabled=true

-  JTA (Transaction information).

-  Swap data (temporary memory space).

By default, these four folders are located under a common directory that
is ``$PLATFORM_TOMCAT_HOME/gatein/data`` (Tomcat),
``$PLATFORM_JBOSS_HOME/standalone/data/gatein`` (JBoss).

In production, it is recommended to configure it to use a directory
separated from the package. Especially in cluster mode, it should be a
network shared folder.

**Configuration in Platform Tomcat**

In Tomcat, the directory is configured by the environment variable
``EXO_DATA_DIR``. Edit the ``bin/setenv-customize.(sh|bat)`` script:

::

    EXO_DATA_DIR=/mnt/nfs/shared/exo/data

You need to create the script file by copying/renaming the sample
``bin/setenv-customize.sample.(sh|bat)``. See `Customizing environment
variables <#PLFAdminGuide.InstallationAndStartup.CustomizingEnvironmentVariables>`__
for more information.

**Configuration in Platform JBoss**

In JBoss, the directory is configured by the system property
``exo.data.dir``. Edit ``standalone/configuration/standalone-exo.xml``
like below:

.. code:: xml

    <system-properties>
        ...
        <property name="exo.data.dir" value="/mnt/nfs/shared/exo/data"/>
        ...
    </system-properties>

Note that if you are configuring the cluster mode, the configuration
might be different. The file should be ``standalone-exo-cluster.xml``
and the property should be ``exo.shared.dir``. See :ref:`Setting up eXo Platform cluster <#PLFAdminGuide.Clustering.SettingUpCluster>`.

.. _Configuration.AssetsVersionConf:    

=============================
Assets version configuration
=============================

Between versions, eXo Platform makes various changes on various layers. To
avoid that browsers use cached assets and display old behavior, a
parameter ``exo.assets.version`` is added in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

When eXo Platform is updated, his parameter allows to:

-  Enforce browsers to reload javascript and css.

-  Build eXo Platform urls for resources serving.

-  Avoid asking users to clear their browser's cache.

By default, this parameter is set to eXo Platform package version, i.e for
the version 5.0.x it is set to 5.0.x.

.. code:: java

     # Assets versions used in static resources URLs. Useful to manage caches.
     exo.assets.version=5.0.x

.. _Configuration.QuartzScheduler:

==============================
Quartz Scheduler configuration
==============================

eXo Platform uses `Quartz Scheduler <http://www.quartz-scheduler.org/>`__,
the Java Framework for scheduling jobs, in a wide range of features.
When eXo Platform runs in cluster mode, it is important to prevent jobs to
execute concurrently. Quartz has its own cluster mode, with each
instance of eXo Platform server as a node of Quartz load balancing and
failover group.

Since the version 4.4 of eXo Platform, Quatrz is used in persisted mode. So
it is automatically configured in eXo Platform. As an administrator, you can
change default Quartz settings in eXo Platform through
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

By default, here are Quartz properties:

::

    #Configure Main Scheduler Properties
    #exo.quartz.scheduler.instanceName=ExoScheduler
    #exo.quartz.scheduler.instanceId=AUTO

    #Configure ThreadPool
    #exo.quartz.threadPool.class=org.quartz.simpl.SimpleThreadPool
    #exo.quartz.threadPool.threadPriority=5
    #exo.quartz.threadPool.threadCount=25

    #Configure JobStore
    #exo.quartz.jobStore.misfireThreshold=6000
    #exo.quartz.jobStore.class=org.quartz.impl.jdbcjobstore.JobStoreTX
    #For SQL server set exo.quartz.jobStore.driverDelegateClass=org.quartz.impl.jdbcjobstore.MSSQLDelegate
    #For postgres set exo.quartz.jobStore.driverDelegateClass=org.quartz.impl.jdbcjobstore.PostgreSQLDelegate
    #exo.quartz.jobStore.driverDelegateClass=org.quartz.impl.jdbcjobstore.StdJDBCDelegate
    #exo.quartz.jobStore.useProperties=false
    #exo.quartz.jobStore.dataSource=quartzDS
    #exo.quartz.jobStore.tablePrefix=QRTZ_
    #exo.quartz.jobStore.isClustered=false
    #exo.quartz.jobStore.clusterCheckinInterval=20000
    #exo.quartz.jobStore.maxMisfiresToHandleAtATime=20
    #exo.quartz.jobStore.dontSetAutoCommitFalse=false
    #exo.quartz.jobStore.acquireTriggersWithinLock=false
    #exo.quartz.jobStore.lockHandler.class=
    #exo.quartz.jobStore.driverDelegateInitString=
    #exo.quartz.jobStore.txIsolationLevelSerializable=false
    #exo.quartz.jobStore.selectWithLockSQL=SELECT * FROM {0}LOCKS WHERE SCHED_NAME = {1} AND LOCK_NAME = ? FOR UPDATE
    #exo.quartz.dataSource.quartzDS.jndiURL=java:/comp/env/exo-jpa_portal   
        

More details about the definition and default values of the above
properties could be found in the table `Properties
reference <#PLFAdminGuide.Configuration.Properties_reference>`__. You
can also refer to `Quartz Configuration
Reference <http://www.quartz-scheduler.org/documentation/quartz-2.x/configuration/>`__
documentation for more details about quartz parameters.

.. _Configuration.CustomizeMultiupload:

======================================================
Configure documents multiupload in the activity stream
======================================================

Through the :ref:`MultiUpload <MultiUpload>` feature, you are able to 
upload up to 20 files per activity having each one 200 MB as max size.

You can change the default behavior through
:ref:`exo.properties <Configuration.ConfigurationOverview>` file by 
configuring these two parameters:

-  ``exo.social.composer.maxToUpload=20``, default value set to 20.

-  ``exo.social.composer.maxFileSizeInMB=200``, default value set to 200
   MB.

.. _Configuration.JCRTransactionService:

===================
Transaction service
===================

The JCR transaction timeout is 420 seconds by default. If your
application runs longer transactions, you might need a bigger timeout.

Configure the timeout by adding the ``exo.jcr.transaction.timeout``
property in :ref:`exo.properties <Configuration.ConfigurationOverview>`
file.

::

    exo.jcr.transaction.timeout=3600

The value is in seconds.


.. _Configuration.ServerBaseURL:

===============
Server base URL
===============

The property ``exo.base.url`` is used to generate links in some cases,
like a topic link in an email notification.

Generally you need to configure it to the base URL that users use to
access eXo Platform. For example, if you use a reverse proxy, the URL
should be the proxy's host.

The following is the default configuration. To change it, edit
:ref:`exo.properties <Configuration.ConfigurationOverview>`
file.

::

    # The Server Base URL is the URL via which users access eXo platform. All links created (for emails etc) will be prefixed by this URL.
    # The base URL must be set to the same URL by which browsers will be viewing your eXo platform instance.
    # Sample: exo.base.url=https://intranet.mycompany.com
    exo.base.url=http://localhost:8080

.. _Configuration.WikiBaseURI:

=========================
Wiki application base URI
=========================

The property ``wiki.permalink.appuri`` allows you to define the base URI
for the wiki application permalinks.

It is configurable through
:ref:`exo.properties <Configuration.ConfigurationOverview>` file. 
Its default value is wiki.

The parameter ``wiki.permalink.appuri`` utility is to well redirect wiki
pages when moving wiki application to different location than the
default one.

::

    wiki.permalink.appuri=wiki
    
    
.. _Configuration.AccountSetup:

=============
Account setup
=============

At the first startup of eXo Platform, the Account Setup and Greetings!
screens will appear by default. However, in some scenarios, these
screens are not necessary, for example:

-  When you have an extension that declares sample users.

-  When you want to connect to an existing user directory.

To skip these screens, simply change the default value from "false" into
"true" in the :ref:`exo.properties <Configuration.ConfigurationOverview>`
file.

::

    exo.accountsetup.skip=true

.. _Configuration.ValidatorsConfiguration:

====================================
Custom data validators configuration
====================================

Custom data validator, or user-configurable validator is the mechanism
allowing users to define their own validation rules. For example, the
username must be lowercase, or shorter than 20 characters. In eXo Platform,
there are 6 validators that administrators can configure to use and the
architecture allows developers to add more validators as they wish.

The validators can be configured via properties in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

A configuration is created by adding an entry with the
``gatein.validators.`` prefix in
:ref:`exo.properties <Configuration.ConfigurationOverview>`
file. This prefix is followed by a validator name, a period '.' and a
validator aspect. Currently, there are the following validators and
validator aspects:

-  Validators:

   -  **username**: Validates the 'Username' field in the Create or Edit
      user form.

   -  **groupmembership**: There is a built-in regex that is currently
      not used to validate any field:

      ::

          GROUP_MEMBERSHIP_VALIDATION_REGEX = "^(\\p{Lower}[\\p{Lower}\\d\\._]+)(\\s*,\\s*(\\p{Lower}[\\p{Lower}\\d\\._]+))*$";

   -  **email**: Validates the Email Address field in the Create or Edit
      user form.

   -  **displayname**: Validates the Display Name field in the Create or
      Edit user form.

   -  **jobtitle**: Validates the Job Title field in the User Profile
      form.

   -  **grouplabel**: Validates the Label field in Add or Edit group
      form.

   -  **pagename**: Validates the page name field in the **Add new
      page** form. Its label is Page Name if you create a page from the
      Page ManagementAdd New Page menu. In the **Page Creation Wizard**,
      the label is Node Name.

-  Validator aspects:

   -  ``gatein.validators.{validatorName}.length.min``: The minimum
      length of the validated field.

   -  ``gatein.validators.{validatorName}.length.max``: The maximum
      length of the validated field.

   -  ``gatein.validators.{validatorName}.regexp``: The regular
      expression to which the validated field must conform.

   -  ``gatein.validators.{validatorName}.format.message``: The
      information message that is displayed when the field does not
      conform to the specified regular expression.

See details about the "*username*\ " validator as below. For
instructions on how to add a new validator (not in the above list), see
:ref:`Developing your own validator <#PLFDevGuide.AuthenticationAndIdentity.DevelopingValidators>`.

**Configuration of username validator**

By default, the username will be validated as follows:

-  The length must be between 3 and 30 characters.

-  Only lowercase letters, numbers, underscores (\_) and period (.) can
   be used.

-  No consecutive underscores (\_) or periods (.) can be used.

-  Must start with a lowercase letter.

-  Must end with a lowercase letter or number.

.. note:: Some components that leverage GateIn depend on usernames being all
          lowercase. Therefore, you are strongly recommended to use a
          lowercase username only.

If you want to validate that username format is email-like, you could
use the following configuration:

::

    # validators
    gatein.validators.username.regexp=^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4}$
    gatein.validators.username.format.message=Username must be a valid email address

When the username field does not conform to this rule, the account is
not created and there will be a warning message:

::

    The field "User Name" must match the format "Username must be a valid email address".

In case you do not define ``gatein.validators.username.format.message``,
the value of ``gatein.validators.username.regexp`` will be used in the
warning message:

::

    The field "User Name" must match the format "^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4}$".

.. _OutgoingMailService:


=====================
Outgoing mail service
=====================

eXo Platform includes an email sending service that needs to be configured
before it can function properly. This service, for instance, is used to
send notifications of connection requests.

The service requires an external SMTP server that allows accounts to
send email from applications. A suggestion is to use Google SMTP, as
detailed below.

In configuration, you need to provide your account and password, and
other information so that eXo Platform can connect to the SMTP server.

The configuration file
`exo.properties <#PLFAdminGuide.Configuration.ConfigurationOverview>`__
is as follows:

Here is the default configuration (it will not work of course, you will
need to edit it):

::

    # Email display in "from" field of emails sent by eXo platform.
    exo.email.smtp.from=noreply@exoplatform.com
    # SMTP Server hostname.
    exo.email.smtp.host=localhost
    # SMTP Server port.
    exo.email.smtp.port=25
    # True to enable the secure (TLS) SMTP. See RFC 3207.
    exo.email.smtp.starttls.enable=false
    # True to enable the SMTP authentication.
    exo.email.smtp.auth=false
    # Username to send for authentication. Sample: exo.email.smtp.username=account@gmail.com
    exo.email.smtp.username=
    # Password to send for authentication.
    exo.email.smtp.password=
    # Specify the port to connect to when using the specified socket factory. Sample: exo.email.smtp.socketFactory.port=465
    exo.email.smtp.socketFactory.port=
    # This class will be used to create SMTP sockets. Sample: exo.email.smtp.socketFactory.class=javax.net.ssl.SSLSocketFactory
    exo.email.smtp.socketFactory.class=

Read the inline comments to understand each property. Here are some
remarks:

-  You need to provide SMTP server host/port, a username/password to be
   authenticated by that server. Others are optional.

-  Typically, administrators want to mask the *From* field in the system
   emails with something like *no-reply@exoplatform.com* so that the
   receivers recognize it is robotic. Many SMTP services allow you to
   set *From* field in outgoing emails to another email address than the
   authenticated account. That's why here you see the property
   ``exo.email.smtp.from``.

   If this parameter is not valid, the value of
   ``exo.email.smtp.username`` will be used instead.

-  If you want to use SMTP gateway over SSL, configure a certificate
   truststore containing your SMTP server's public certificate.
   Depending on the key sizes, you may then also need to install Java
   Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy
   Files for your Java Runtime Environment.

**Using Gmail as your SMTP server**

Here is the sample using *smtp.gmail.com* server:

::

    exo.email.smtp.from=noreply@exoplatform.com
    exo.email.smtp.host=smtp.gmail.com
    exo.email.smtp.port=465
    exo.email.smtp.starttls.enable=true
    exo.email.smtp.auth=true
    exo.email.smtp.username=exo.test100@gmail.com
    exo.email.smtp.password=***
    exo.email.smtp.socketFactory.port=465
    exo.email.smtp.socketFactory.class=javax.net.ssl.SSLSocketFactory

To make the configuration work, you need to:

-  Register a Google account that is *exo.test100@gmail.com* in the
   sample.

-  Enable POP and IMAP for that account. This can be done simply in your
   Gmail settings, see the screenshot below.

   |image0|

`Here <https://support.google.com/mail/answer/78775?hl=en>`__ is a
checklist provided by Google to help you solve problem if any.

Besides, for securing your account, Google may block access from an app
and send you an email to review the access. So in case the mail service
does not work, check your inbox and get the link to allow the app
access.

.. note:: In case of Gmail, ``exo.email.smtp.from`` must be a real account
          that you own. It does not need to be a Gmail account, as you can
          guess by the sample. You will configure your main account (that is
          ``exo.email.smtp.username``) to add this *from* email as another
          "send as".

To do so, follow `this guide of
Google <https://support.google.com/mail/answer/22370?hl=en>`__.

In case the *from* parameter is not valid, it does not fail the email
sending and the main account will be displayed instead.

.. _Configuration.ChangingSenderInformationOfEmailNotifications:

=================================================
Changing sender information of email notification
=================================================

In eXo Platform, email notifications are sent to users when significant
actions involving them occur (for example, new users, connection
request, space invitation, and more). These emails help them to track of
activities taking place in their Social Intranet.

As an administrator, you can configure information (name and email
address) of the sender, from which all notifications are sent, via two
ways:

-  In UI, click AdministrationPortalNotifications. Then edit Email
   Notification Sender section.

-  Via ``exo.properties`` file. See :ref:`Configuration overview <Configuration.ConfigurationOverview>`
   if you have not created this file yet.

   ::

       exo.notification.portalname=eXo
       exo.email.smtp.from=noreply@exoplatform.com

   In which:

   -  ``exo.notification.portalname``: Name of the sender. The default
      value is ``eXo``.

   -  ``exo.email.smtp.from``: Email address of the sender. The default
      value is ``noreply@exoplatform.com``.
      
.. _Configuration.EmailNotificationOfDocumentChanges:

=================================================
Subscribing to notifications of document changes
================================================

The function Watch document in Sites Explorer allows users to receive
notification by email when a document is updated. The email address of
receivers is the email they declare in their profile. Administrators can
customize the sender, subject, mimetype and content of the notification.

.. note:: To get the email notification feature work, you first need to
          configure :ref:`Outgoing mail service <OutgoingMailService>` first.

To customize the email notification, simply add the following properties
in :ref:`exo.properties <Configuration.ConfigurationOverview>` file.

.. code:: java

    # Email content for WatchDocumentService
    exo.ecms.watchdocument.subject=Your watching document is changed
    exo.ecms.watchdocument.mimetype=text/html
    exo.ecms.watchdocument.content=Dear $user_name,<br><br>The document $doc_name ($doc_title) has changed.<br><br>Please go to <a href="$doc_url">$doc_title</a> to see this change.<br><br>

In which:

+-------------------------------+----------------------+----------------------+
| Property                      | Default value        | Description          |
+===============================+======================+======================+
| **exo.ecms.watchdocument.subj | Your watching        | The subject of the   |
| ect**                         | document is changed  | email notification.  |
+-------------------------------+----------------------+----------------------+
| **exo.ecms.watchdocument.mime | text/html            | The format of the    |
| type**                        |                      | email content. There |
|                               |                      | are two types:       |
|                               |                      | text/html and        |
|                               |                      | text/plain.          |
+-------------------------------+----------------------+----------------------+
| **exo.ecms.watchdocument.cont | Dear                 | The content of the   |
| ent**                         | $user\_name,<br><br> | email notification.  |
|                               | The                  |                      |
|                               | document $doc\_name  |                      |
|                               | ($doc\_title) has    |                      |
|                               | changed.<br><br>Plea |                      |
|                               | se                   |                      |
|                               | go to <a             |                      |
|                               | href="$doc\_url">$do |                      |
|                               | c\_title</a>         |                      |
|                               | to see this          |                      |
|                               | change.<br><br>      |                      |
+-------------------------------+----------------------+----------------------+

You can use four parameters below in the
``exo.ecms.watchdocument.content`` property:

-  **$user\_name**: The full name of the receiver.

-  **$doc\_name**: The name of the document.

-  **$doc\_title**: The title of the document.

-  **$doc\_url**: The link to view the document in Sites Explorer.

.. _Configuration.WebDAV:

=====================
WebDAV configuration
=====================

The embedded WebDAV server lets you configure some parameter via :ref:`exo.properties file <Configuration.ConfigurationOverview>`.

.. code:: java

    # JCR Webdav configuration
    exo.webdav.def-folder-node-type=nt:folder
	exo.webdav.def-file-node-type=nt:file
	exo.webdav.def-file-mimetype=application/octet-stream
	exo.webdav.update-policy=update
	exo.webdav.folder-icon-path=/eXoWCMResources/skin/images/file/nt-folder.png
	exo.webdav.cache-control=text/*:max-age=3600;image/*:max-age=1800;application/*:max-age=1800;*/*:no-cache

+-------------------------------------+--------------------------------------+
| ``exo.webdav.def-folder-node-type`` |Default (JCR) node type which is used |
|									  |for the creation of collections.      |
+-------------------------------------+--------------------------------------+
| ``exo.webdav.def-file-node-type``   |Default (JCR) node type which is used |
|									  |for the creation of files. 			 |
+-------------------------------------+--------------------------------------+
| ``exo.webdav.def-file-mimetype``    |A mime-type is detected by file 		 |
|									  |extension or HTTP request header. If  |
|									  |those are not found, this parameter   |
|									  |is used.								 |
+-------------------------------------+--------------------------------------+
| ``exo.webdav.update-policy``        | This defines the behavior when a PUT |
|									  |	command is executed against an       |
|									  |	existing resource:                   |
|									  |   - add: It tries to add new resource| 
|									  |	    with the same name.				 |
|									  |	  - create-version: It creates a new |
|									  |		version of the resource.         |
|									  |	  - Otherwise, the PUT command       |
|									  |     updates the resource and its last| 
|									  |     modification date.               |	 
+-------------------------------------+--------------------------------------+
| ``exo.webdav.folder-icon-path``     |The default path is an icon in        |
|                                     |eXoWCMResources webapp.               |
+-------------------------------------+--------------------------------------+
| ``exo.webdav.cache-control``        |This determines the live time of the  |
|                                     |caches for each type of responses. Use| 
|                                     |no-cache if you want a type to be not |
|                                     |cached.                               |
+-------------------------------------+--------------------------------------+

.. _Configuration.OpenInOfficeConfiguration:

============================
Open in Office configuration
============================

With the Open in Office feature, you are able to easily edit documents,
spreadsheets and presentations in the native applications installed on
your client, without keeping a local copy.

By default, there are 4 labels displayed for corresponding file types as
below:

+------------------------+---------------------------------------------------+
| Label                  | File types                                        |
+========================+===================================================+
| Open in Word           | docx, doc, docm, dot, dotm, dotx.                 |
+------------------------+---------------------------------------------------+
| Open in Excel          | xltx, xltm, xlt, xlsx, xlsm, xlsb, xls, xll,      |
|                        | xlam, xla.                                        |
+------------------------+---------------------------------------------------+
| Open in Powerpoint     | pptx, pptm, ppt, ppsx, ppsm, pps, ppam, ppa,      |
|                        | potx, potm, pot                                   |
+------------------------+---------------------------------------------------+
| Open on Desktop        | Non-MS Office files, such as Open Document text   |
|                        | files (odp, ods, odt, and more) or archive files  |
|                        | (zip, rar, war, and more).                        |
+------------------------+---------------------------------------------------+

As an administrator, you can easily configure the file types associated
with the application named as in "Open in Word", and set a new label via
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

::

    exo.remote-edit.$CATEGORY=$SET_OF_FILETYPES
    exo.remove-edit.$CATEGORY.label=$LABEL

-  Replace *$CATEGORY* with any text as you want, but it should
   represent the application in correspondence to the file types defined
   in *$SET\_OF\_FILETYPES*.

-  Replace *$LABEL* with the application label that will be displayed in
   the UI, for example "Word" or "MS Word".

Here are some examples:

-  Changing the default labels from "Open in Word", "Open in Excel", and
   "Open in Powerpoint" into "Open in MS Word", "Open in MS Excel" and
   "Open in MS Powerpoint":

   ::

       #MS Word
       exo.remote-edit.word=docx,doc,docm,dot,dotm,dotx
       exo.remote-edit.word.label=MS Word

       #MS Excel
       exo.remote-edit.excel=xltx,xltm,xlt,xlsx,xlsm,xlsb,xls,xll,xlam,xla
       exo.remote-edit.excel.label=MS Excel

       #MS Powerpoint
       exo.remote-edit.powerpoint=pptx,pptm,ppt,ppsx,ppsm,pps,ppam,ppa,potx,potm,pot
       exo.remote-edit.powerpoint.label=MS Powerpoint

   |image1|

-  Adding a new label "Open in LibreOffice" for some Open Document Text
   file types:

   ::

       exo.remote-edit.libreoffice=odp,ods,odt
       exo.remote-edit.libreoffice.label=LibreOffice

   |image2|

-  Setting a new label "Open in Writer" for some both Word and Open
   Document Text file types:

   ::

       exo.remote-edit.writer=docx,doc,odm,odt
       exo.remote-edit.writer.label=Writer

   |image3|
   
.. _JODConverterConf:

===========================
JODConverter configuration
===========================

In Sites Explorer or Activity Stream, users can preview documents of
various types, without downloading it. To support this feature, eXo Platform
uses the JODConverter service that requires OpenOffice or LibreOffice to
be installed locally (in the same machine with the eXo Platform server).

**Installing OpenOffice/LibreOffice**

Follow `OpenOffice
guideline <http://www.openoffice.org/installation/>`__ or `LibreOffice
guideline <http://www.libreoffice.org/get-help/installation/>`__ to
install.

Note that those softwares might be installed in some Linux distributions
by the OS already.

.. note:: JODConverter is already built in eXo Platform, so you do not need to install it.

**Sigar Framework**

In Windows, `Sigar <http://www.hyperic.com/products/sigar>`__ is
recommended. JODConverter uses Sigar - if available - to manage Office
processes. Without Sigar, there is possibility that Office processes are
not stopped successfully when you shut down eXo Platform, and it causes
problem in your next start.

So `download <http://sourceforge.net/projects/sigar/files/>`__ the
following files and install them to the lib folder
(``$PLATFORM_TOMCAT_HOME/lib`` in Tomcat,
``$PLATFORM_JBOSS_HOME/standalone/deployments/platform.ear/lib`` in
JBoss:

-  ``sigar.jar``

-  ``sigar-x86-winnt.dll`` for Windows 32.

-  ``sigar-amd64-winnt.dll`` for Windows 64.

**JODConverter version**

eXo Platform uses `JODConverter
v3.0 <https://code.google.com/p/jodconverter/wiki/WhatsNewInVersion3>`__
that enhances processing different file types much.

**Activating and deactivating**

JODConverter is activated by default. You can deactivate it (and
consequently not use the preview feature) by setting
``exo.jodconverter.enable=false`` in
`exo.properties <#PLFAdminGuide.Configuration.ConfigurationOverview>`__
file.

**Configurations**

.. note:: In most cases, you do not need to configure JODConverter because it
          can work with default configurations. However, if you are using
		  OpenOffice 4 (or later), or have installed the Office server
		  untypically, you will need to specify
		  **exo.jodconverter.officehome** by yourself. See :ref:`Specifying exo.jodconverter.officehome <JODConverter.Customize_OfficeHome>`.

JODConverter configurations can be edited in the ``exo.properties``
file. See :ref:`Configuration overview <Configuration.ConfigurationOverview>` if the
file has not been created yet.

::

    # JOD Converter
    exo.jodconverter.enable=true
    exo.jodconverter.portnumbers=2002
    exo.jodconverter.officehome=
    exo.jodconverter.taskqueuetimeout=30000
    exo.jodconverter.taskexecutiontimeout=120000
    exo.jodconverter.maxtasksperprocess=200
    exo.jodconverter.retrytimeout=120000

+-----------------------------------+-------------+-----------------------------+
| Key                               | Default     | Description                 |
|                                   | value       |                             |
+===================================+=============+=============================+
| ``exo.jodconverter.portnumbers``  | 2002        | List of ports, separated by |
|                                   |             | commas - those used by each |
|                                   |             | JODConverter processing     |
|                                   |             | thread. The number of       |
|                                   |             | office instances is equal   |
|                                   |             | to the number of ports.     |
+-----------------------------------+-------------+-----------------------------+
| ``exo.jodconverter.officehome``   | See         | The absolute path to Office |
|                                   | `here <#Off | installed folder.           |
|                                   | iceHome>`__ |                             |
+-----------------------------------+-------------+-----------------------------+
| ``exo.jodconverter.taskqueuetimeo | 30000       | The maximum living time of  |
| ut``                              |             | a task in the conversation  |
|                                   |             | queue. The task will be     |
|                                   |             | removed from the queue if   |
|                                   |             | the waiting time is longer  |
|                                   |             | than **taskQueueTimeout**.  |
+-----------------------------------+-------------+-----------------------------+
| ``exo.jodconverter.taskexecutiont | 120000      | The maximum time to process |
| imeout``                          |             | a task. If the processing   |
|                                   |             | time of a task is longer    |
|                                   |             | than                        |
|                                   |             | **taskExecutionTimeout**,   |
|                                   |             | this task will be aborted   |
|                                   |             | and the next task is        |
|                                   |             | processed.                  |
+-----------------------------------+-------------+-----------------------------+
| ``exo.jodconverter.maxtasksperpro | 200         | The maximum number of tasks |
| cess``                            |             | are processed.              |
+-----------------------------------+-------------+-----------------------------+
| ``exo.jodconverter.retrytimeout`` | 120000      | The interval time to        |
|                                   |             | restart the Office services |
|                                   |             | after an unexpected crash.  |
+-----------------------------------+-------------+-----------------------------+

.. _JODConverter.Customize_OfficeHome:

**Specifying exo.jodconverter.officehome**

Again, the default configuration should work in many cases. Most likely
you need to change it for OpenOffice 4.

.. note:: Note that ``EXO_JODCONVERTER_OFFICEHOME`` variable is not used as of
          4.1.0. The customize script does not overlap JODConverter
          configuration anymore, so only use ``exo.properties`` for it.

Here are some examples of the property:

-  In Windows:
   ``exo.jodconverter.officehome=C:\\Program Files (x86)\\OpenOffice 4``


.. note:: Remember to use double slash (**\\\\**) for Windows.

-  In OS X:
   ``exo.jodconverter.officehome=/Applications/OpenOffice.app/Contents``
   (OpenOffice 4) or
   ``exo.jodconverter.officehome=/Applications/LibreOffice.app/Contents``
   (LibreOffice).

-  In Linux: ``exo.jodconverter.officehome=/opt/openoffice4``.

   In Linux, if you do not know the path, you might check the
   followings:

   -  ``/opt/openoffice.org3``

   -  ``/opt/libreoffice``

   -  ``/usr/lib/openoffice``

   -  ``/usr/lib/libreoffice``

**Services details**

To support as many as possible document types, it is recommended you
install all available services of Open Office. However, if you do not
want to do so, refer to the following table to know which packages are
needed for which services.

+-------------+---------------+-----------------------+-----------------------+
| File        | Service names | Open Office           | Libre Office          |
| extensions  |               | installation package  | installation package  |
+=============+===============+=======================+=======================+
| ``doc``     | writer        | openoffice.org-writer | libreoffice-writer    |
|             |               |                       |                       |
| ``docx``    |               |                       |                       |
|             |               |                       |                       |
| ``odt``     |               |                       |                       |
+-------------+---------------+-----------------------+-----------------------+
| ``odf``     | math          | openoffice.org-math   | libreoffice-math      |
+-------------+---------------+-----------------------+-----------------------+
| ``odg``     | draw          | openoffice.org-draw   | libreoffice-draw      |
+-------------+---------------+-----------------------+-----------------------+
| ``odp``     | impress       | openoffice.org-impres | libreoffice-impress   |
|             |               | s                     |                       |
| ``ppt``     |               |                       |                       |
|             |               |                       |                       |
| ``pptx``    |               |                       |                       |
+-------------+---------------+-----------------------+-----------------------+
| ``ods``     | calc          | openoffice.org-calc   | libreoffice-calc      |
|             |               |                       |                       |
| ``ots``     |               |                       |                       |
|             |               |                       |                       |
| ``xls``     |               |                       |                       |
|             |               |                       |                       |
| ``xlsx``    |               |                       |                       |
|             |               |                       |                       |
| ``xlt``     |               |                       |                       |
+-------------+---------------+-----------------------+-----------------------+

.. _Configuration.FileSizeLimit:

===============================
Limiting size of uploaded files
===============================

**In Documents application**

When you upload a file in Documents or Sites Explorer, its size is
limited to 200 MB by default.

To change this limit, edit the ``exo.ecms.connector.drives.uploadLimit``
property in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

For example:

::

    exo.ecms.connector.drives.uploadLimit=300

.. note:: As of 4.1, this configuration also takes effect on files uploaded
          from Activity Stream (using the Share function).

**In activities posts and comments**

In a message post or a comment, it is possible to attach an image
through the CKEditor. By default the image size is limited to 200 MB.

You can change this limit by editing the value of the
``exo.social.activity.uploadLimit`` property in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

For example:

::

    exo.social.activity.uploadLimit=200

**In Wiki application**

Same as for the previous applications, files upload size in Wiki is
limited, by default to 200 MB which could be redefined through the
property ``exo.wiki.attachment.uploadLimit`` in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

For example:

::

    exo.wiki.attachment.uploadLimit=200

.. note:: The size is in MB for all the three properties.

.. warning:: If you are using eXo Platform in JBoss application server, note that in
			 addition to the parameters described above aiming to customize files
			 size, you should configure the value of the parameter
			 ``max-post-size`` in ``standalone/configuration/standalone-exo.xml``
			 which is set by default to 200 MB in eXo Platform package.

			 .. code:: xml

					<http-listener name="default" socket-binding="http" redirect-socket="https" max-post-size="209715200"/>

.. _Configuration.UploadHandler:

============================================
Limiting public access to the upload service
============================================

By default, unauthenticated users are not allowed to upload resources to
the server through the Upload component on UI or by accessing directly
the "/upload" handler, because this may cause some problems of server
disk space. However, you can definitely configure the UploadHandler to
allow this.

To change this restriction, edit the
``exo.portal.uploadhandler.public-restriction`` property in the
:ref:`exo.properties <Configuration.ConfigurationOverview>`file as follows:

::

    exo.portal.uploadhandler.public-restriction=false

.. _Configuration.CustomizeSiteData:

=====================
Customizing site data
=====================

eXo Platform provides 2 built-in sites: Intranet and ACME. In case you want
to customize data of these sites, for example, modifying or overwriting
the existing data, use the externalized parameters in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

**Intranet**

-  ``exo.intranet.portalConfig.metadata.override``: Allow (*true*) or
   not allow (*false*) overriding the Intranet data. See :ref:`Overriding Portal Data <#sect-Reference_Guide-Data_Import_Strategy-Overriding_Portal_Data>`
   for more details.

-  ``exo.intranet.portalConfig.metadata.importmode``: Customize data
   import strategy (*CONSERVE*, *INSERT*, *MERGE*, or *OVERWRITE*). See
   :ref:`here <#sect-Reference_Guide-Data_Import_Strategy-Import_Strategy>`
   for more details about these modes.

.. _Configuration.AutocreatingTaxonomyTree:

================================================
Enabling/Disabling auto-creating a taxonomy tree
================================================

eXo Platform allows you to enable/disable auto-creating a taxonomy tree
during a new site creation by adding the
``ecms.taxonomy.autoCreateWithNewSite`` parameter to
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

.. code:: java

     # Configuration for a taxonomy tree
     ecms.taxonomy.autoCreateWithNewSite=false

By default, the parameter is set to ``false``, it means the creation of
a taxonomy tree is disabled when you create a new site.

To enable the function, simply set the parameter to ``true``.

.. _Configuration.ActivityType:

====================================
Enabling/Disabling any activity type
====================================

eXo Platform allows you to enable/disable any activity type. Disabling an
activity type means that this kind of activities will not be posted in
the streams.

To enable/disable an activity type, you need to add
``exo.activity-type.activity-type-key.enabled`` parameter to
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

.. code:: java

     # Configuration for activity type enabling/disabling
     exo.activity-type.activity-type-key=false

By default, the parameter is set to ``true``, it means the activity of
type `` activity-type-key`` is enabled i.e it posts in the streams.

To disable the activity type, simply set the parameter to ``false``.

.. note:: In the ``exo.activity-type.activity-type-key.enabled``,
		  activity-type-key could take many values depending on the activity
		  type:

			-  DEFAULT\_ACTIVITY
			-  SPACE\_ACTIVITY
			-  USER\_ACTIVITIES\_FOR\_SPACE
			-  exosocial\\:relationship
			-  LINK\_ACTIVITY
			-  sharecontents\\:spaces
			-  USER\_PROFILE\_ACTIVITY
			-  DOC\_ACTIVITY
			-  files\\:spaces
			-  sharefiles\\:spaces
			-  contents\\:spaces
			-  cs-calendar\\:spaces
			-  TaskAdded
			-  ks-forum\\:spaces
			-  ks-answer\\:spaces
			-  ks-poll\\:spaces
			-  ks-wiki\\:spaces
			-  USER\_ACTIVITIES\_FOR\_RELATIONSHIP

.. _Configuration.SpacesAdministration:

=====================================
Configure spaces administration group
=====================================

By default, only the super user is able to manage all the spaces of the
platform:

-  Create pages on spaces.

-  Add/delete/promote members.

-  Add/modify/delete space data (Wiki pages, forum Posts, activities,
   tasks...).

With eXo Platform 5.0 it is possible to define a group of users to
manage spaces. This group of users is able to edit and delete all kind
of spaces: visible and hidden.

The group of spaces administrators could be defined by adding this
property to
`exo.properties <#PLFAdminGuide.Configuration.ConfigurationOverview>`__
file:

-  ``exo.social.spaces.administrators``

.. note:: -  You should specify the membership type (\*, member, manager...)
              in the value of the property.

			 -  It is possible to specify a list of groups separated by commas **,**.

In this example, all users of the two groups /platform/administrators
and /developers are allowed to manage spaces:
exo.social.spaces.administrators=\*:/platform/administrators,\*:/developers

.. _Configuration.Logs:

=====
Logs
=====

The logs of PRODUCT are controlled by the `Java Logging
API <http://docs.oracle.com/javase/7/docs/technotes/guides/logging/index.html>`__.

By default, the logs are configured to:

-  log errors and warnings on the console.

-  log ``$PLATFORM_TOMCAT_HOME/logs/platform.log`` (Tomcat), or
   ``$PLATFORM_JBOSS_HOME/standalone/log/server.log`` (JBoss).

The logs are configured via the file:

-  ``$PLATFORM_TOMCAT_HOME/conf/logging.properties`` (Tomcat). Please
   refer to `Tomcat's Logging
   Documentation <http://tomcat.apache.org/tomcat-7.0-doc/logging.html>`__
   for more information on how to adjust this file to your needs.

-  ``$PLATFORM_JBOSS_HOME/standalone/configuration/logging.properties``
   (JBoss).

.. _Configuration.JCR:

=================
JCR Configuration
=================

Because JCR Configuration is a very advanced topic, it is recommended
you:

-  Learn about `eXo JCR
   configuration <../../reference/html/JCRReferenceGuide.html>`__.

-  Use default values, change them only if you know what you are doing.

-  Understand how to configure datasource in the
   :ref:`Database <Database>` chapter.

The configurations introduced here are a subset of JCR configurations.
There are many JCR configurations which are packed in ``.war`` files, so
you have to unpack to edit them. To avoid unpacking them, the subset is
externalized to be configured easily in
:ref:`exo.properties <Configuration.ConfigurationOverview>` file.

Here is the list of externalized configurations with their short
descriptions.

-  Repository:

   ::

       exo.jcr.repository.default=repository
       exo.jcr.workspace.default=collaboration
       exo.jcr.workspace.system=system

   In which, "repository", "collaboration" and "system" are names of
   default repository, default workspace and system workspace
   respectively. Refer to :ref:`Repository
   Configuration <#JCR.eXoJCRconfiguration.RepositoryConfiguration>`
   for details.

-  Datasource:

   ::

       exo.jcr.datasource.name=java:/comp/env/exo-jcr          
       exo.jcr.datasource.dialect=auto
       exo.jcr.db-structure-type=single

   These configurations are applied to all workspaces. Refer to
   :ref:`Workspace <#JCR.eXoJCRconfiguration.WorkspaceConfiguration>` for
   details.

-  Jgroups:

   ::

       exo.jcr.cluster.jgroups.config-url=file:${exo.jcr.cluster.jgroups.config}

   This externalizes the **jgroups-configuration** parameter of all
   workspace caches, query-handlers and lock-managers. Refer to
   :ref:`Workspace <#JCR.eXoJCRconfiguration.WorkspaceConfiguration>` for
   details.

-  Value Storage:

   ::

       exo.jcr.storage.enabled=true

   This externalizes the **enabled** property of file system
   value-storage (that is configured at workspace level). The **true**
   value (default) means all binary values are stored in file system.
   The **false** value means all binary values are stored in the
   database. Refer to :ref:`Value Storage plugin for data container <#JCR.ConfigurationPersister.ValueStoragePlugin>` 
   for details.

.. |image0| image:: images/gmail_settings_1.png
.. |image1| image:: images/openinoffice/openinmsoffice.png
.. |image2| image:: images/openinoffice/openinlibreoffice.png
.. |image3| image:: images/openinoffice/openinwriter.png
