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

    -  :ref:`Outgoing mail service <Configuration.OutgoingMailService>`
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


+------------------------------+------------------+-----------------------------+
| Name                         | Description      | Default                     |
+==============================+==================+=============================+
| exo.base.url    			   | Generates links. | http://localhost:8080       |
+------------------------------+------------------+-----------------------------+
| exo.accountsetup.skip  	   | Skips "account   | false                       |
| 							   | setup" screen or |                             |
|            				   | not?             |                             |
+------------------------------+------------------+-----------------------------+
| exo.super.user 			   | The predefined   | root                        |
| 							   | super user's     |                             |
| 							   | name.            |                             |
+------------------------------+------------------+-----------------------------+
| exo.portal.resetpassword.e   | The expiration   | 24 (hours)                  |
| xpiretime   				   | time of a reset  |                             |
| 							   | password link.   |                             |
+------------------------------+------------------+-----------------------------+               

- :ref:`exo.base.url <Configuration.ServerBaseURL>: Generates links, default to **http://localhost:8080**.       
- :ref:`exo.accountsetup.skip <Configuration.ccountSetup>: Skips "accounts etup" screen or not, default to **false**.                       
- :ref:`exo.super.user <Configuration.PredefinedUserGroupMembership> : The predefined super user's name, default to **root**.                                
- :ref:exo.portal.resetpassword.expiretime <Configuration.ForgotPassword> : The expiration time of a reset password link, default fo **24 (hours)**                                                                                                            

.. _SMTP:

SMTP
~~~~~                    

- :ref:`exo.email.smtp.from <Configuration.OutgoingMailService>: The "From" field in outgoing emails, default to **noreply@exoplatform.com**.                                         
- :ref:`exo.email.smtp.host <Configuration.OutgoingMailService>: The external mail server, default to **localhost**.                   
- :ref:`exo.email.smtp.port <Configuration.OutgoingMailService>: The external port, default to **25**.                          
- :ref: `exo.email.smtp.starttls.enable <Configuration.OutgoingMailService>: Enable TLS or not, default to **false**.                                                                                              
- :ref: `exo.email.smtp.auth <Configuration.OutgoingMailService>: Enable SMTP authentication or not, default to **false**.                                                                                                                                   
- :ref: `exo.email.smtp.username <Configuration.OutgoingMailService>: Username to get authenticated with the mail server.                                                                                                                                                                         
- :ref: `exo.email.smtp.password <Configuration.OutgoingMailService>: Password to get authenticated with the mail server.                                                                                                                                                                                                               
- :ref: `exo.email.smtp.socketFactory.port <Configuration.OutgoingMailService>: Port to connect to if a socket factory is specified.  
-:ref:exo.email.smtp.socketFactory.class <Configuration.OutgoingMailService>: A class to create SMTP sockets.                                                                                                                                                                                                             
          
.. _JODConverter:                                                                                                   

JODConverter
~~~~~~~~~~~~~
- :ref:exo.jodconverter.enable <Configuration.JODConverter>: Enable JODConverter or not, default to **true**.            
- :ref:exo.jodconverter.portnumbers <Configuration.JODConverter>: List of ports used to create soffice processes, default to **2002**.            
- :ref:exo.jodconverter.officehome <Configuration.JODConverter>: The home folder of the Office installation, default set to blank (auto-detected).            
- :ref:exo.jodconverter.taskqueuetimeout <Configuration.JODConverter>: The maximum living time in milliseconds of a task in the conversation queue, default set to **30000**.            
- :ref:exo.jodconverter.taskexecutiontimeout <Configuration.JODConverter>: The maximum time in milliseconds to process a task, default set to **120000**.            
- :ref:exo.jodconverter.maxtasksperprocess <Configuration.JODConverter>: The maximum number of tasks to process by an office server, default set to **200**.            
- :ref:exo.jodconverter.retrytimeout <Configuration.JODConverter>: The interval time in milliseconds to try to restart an office server in case it unexpectedly stops., default set to **120000**.            

.. _SearchConnector:

Search connector
~~~~~~~~~~~~~~~~~

- :ref:exo.[searchConnectorName].connector.[informationType].enable <Configuration.SearchConnector>: Turn on/off a specific Search connector for a certain information type, default to **true**.        

.. UnifiedSearch:

Unified Search
~~~~~~~~~~~~~~~          

- :ref:exo.unified-search.engine.fuzzy.enable <Configuration.UnifiedSearch>: Enable fuzzy search or not, default to **true**.
- :ref:exo.unified-search.engine.fuzzy.similarity <Configuration.UnifiedSearch>: A float number between 0 and 1 expressing how much a returned word matches the keyword. 1 is exact search, default to **0.5**.
- :ref:exo.unified-search.excluded-characters <Configuration.UnifiedSearch>: List of characters that will not be indexed (so could not be searched)., default to ``.-``.

.. _Notification:
                                
Notification
~~~~~~~~~~~~~            

- :ref:`exo.notification.NotificationDailyJob.expression <Configuration.Notification>: Cron expression to schedule daily emails, default to **0 0 23 ? \* \* (11:00pm every day)** .    
- :ref:`exo.notification.NotificationWeeklyJob.expression <Configuration.Notification>: Cron expression to schedule weekly emails, default to *0 0 11 ? * SUN (11:00am every Sunday)** .    
- :ref:`exo.notification.service.QueueMessage.period <Configuration.Notification>: The delay time (in seconds) between two batches of sent mails, default to **60** .    
- :ref:`exo.notification.service.QueueMessage.numberOfMailPerBatch <Configuration.Notification>: The maximum number of emails sent each batch, default to **30** .    
- :ref:`exo.notification.portalname <Configuration.Notification>: The "from" field in notification emails, default to **eXo** .    
- :ref:`exo.notification.maxitems <Configuration.Notification>: Maximum number of notifications displayed in the popup list, default to **8** .    
- :ref:`exo.notification.viewall <Configuration.Notification>: Living days of items displayed in the View All page., default to **30** .    
- :ref:`exo.notification.WebNotificationCleanJob.expression <Configuration.Notification>: Cron expression to schedule the job that cleans web notification old items., default to **0 0 23 ? * * (11:00pm every day)** .    

.. _JCR:                                                                                           

JCR
~~~~   

- :ref:exo.jcr.datasource.dialect <Database.ConfiguringPLF>: In most cases the dialect is auto-detected. Follow the link to know exceptions, default to **auto**.                
- :ref:exo.jcr.storage.enabled <Database.DataDirectory>: Enable file system storage for JCR values?, default to **true**.                
                                                                
.. _Webdav:

WebDav
~~~~~~~

- :ref:exo.webdav.def-folder-node-type <Configuration.WebDAV>: Matching node type of folders, default to **nt:folder**.                  
- :ref:exo.webdav.def-file-node-type <Configuration.WebDAV>: Matching node type of files., default to **nt:file**.                  
- :ref:exo.webdav.def-file-mimetype <Configuration.WebDAV>: The mimetype to exchange file data, default to **application/octet-stream**.                  
- :ref:exo.webdav.update-policy <Configuration.WebDAV>: The policy applied when there is an update via WebDav, default to **create-version**.                  
- :ref:exo.webdav.folder-icon-path <Configuration.WebDAV>: The display icon of a folder., default to **/eXoWCMResources/skin/images/file/nt-folder.png**.                  
- :ref:exo.webdav.cache-control <Configuration.WebDAV>: The cache-control header that defines cache and cache live time, default to **text/\*:max-age=3600;image/\*:max-age=1800;application/\*:max-age=1800;\*/\*:no-cache**.                  

.. _ECMS:                                  

ECMS                    
~~~~~~

- :ref:exo.ecms.connector.drives.uploadLimit <Configuration.FileSizeLimit>: Maximum size (in MB) allowed of an uploaded file, defalut to **200**.
- :ref:exo.portal.uploadhandler.public-restriction <Configuration.UploadHandler>: Turn on/off public access to the upload service, defalut to **true**.
- :ref:exo.ecms.connector.drives.clientLimit <Uploading-files>: The maximum number of concurrent uploaded files in client side, defalut to **3**.
- :ref:exo.ecms.connector.drives.serverLimit <Uploading-files>: The maximum number of concurrent uploaded files in server side, defalut to **20**.
- :ref:exo.ecms.search.excluded-mimetypes <SearchingForContent>: Content of these mimetypes will not be searched, defalut to **text/css,text/javascript,application/x-javascript,text/ecmascript**.
- :ref:exo.ecms.search.enableFuzzySearch <SearchingForContent>: Enable fuzzy search or not?, defalut to **true**.
- :ref:exo.ecms.search.fuzzySearchIndex <SearchingForContentt>: A float number between 0 and 1 expressing how much a returned word matches the keyword. 1 is exact search, defalut to **0.8**.
- :ref:exo.ecms.lock.admin <WorkingWithRepository.Locks>: Users or groups who can manage locks, default to **\*:/platform/administrators**.                                         
- :ref:exo.ecms.friendly.enabled <#PLFRefGuide.Configurations.ExternalComponentPlugins.Content.FriendlyPlugin>: Enable friendly URL maker or not?, default to **true**.                                         
- :ref:exo.ecms.friendly.servletName <#PLFRefGuide.Configurations.ExternalComponentPlugins.Content.FriendlyPlugin>: The friendly name used when making friendly URLs, default to **content**.                                         

.. _ECMSWatchDocument:

ECMS Watch Document
~~~~~~~~~~~~~~~~~~~~ 
    
- :ref:exo.ecms.watchdocument.sender <Configuration.EmailNotificationOfDocumentChanges>: The "from" field in the notification emails, defalut to **support@exoplatform.com**.
- :ref:exo.ecms.watchdocument.subject <Configuration.EmailNotificationOfDocumentChanges>: The subject of the notification emails, defalut to **"Your watching document is changed"**.
- :ref:exo.ecms.watchdocument.mimetype <Configuration.EmailNotificationOfDocumentChanges>: Mimetype of the message body, defalut to **text/html**.
- :ref:exo.ecms.watchdocument.content <Configuration.EmailNotificationOfDocumentChanges>: The message body, Check it yourself in ``exo-sample.properties`` file.                                                       

.. _ECMSDocumentversioning:

ECMS Document versioning
~~~~~~~~~~~~~~~~~~~~~~~~~~                 

 `exo.ecms.documents.version  The drives that   Managed                     
 ing.drives <#PLFAdminGuide.  are enabled for   Sites,Groups,Personal       
 Configuration.DocumentVersi  Document          Documents                   
 oning>`__                    versioning.                                   

 `exo.ecms.documents.version  The max number    0 (no limit)                
 s.max <#PLFAdminGuide.Confi  of versions that                              
 guration.DocumentVersioning  a document can                                
 >`__                         have.                                         

 `exo.ecms.documents.version  The expiration    0 (no limit)                
 s.expiration <#PLFAdminGuid  time (in days)                                
 e.Configuration.DocumentVer  of a document                                 
 sioning>`__                  version.                                      

 **ECMS Document Viewer**    

 `exo.ecms.documents.pdfview  Max file size of  10                          
 er.max-file-size <#PLFAdmin  documents for                                 
 Guide.Configuration.Documen  preview, in MB                                
 tViewer>`__                                                                

 `exo.ecms.documents.pdfview  Max number of     99                          
 er.max-pages <#PLFAdminGuid  pages of                                      
 e.Configuration.DocumentVie  documents for                                 
 wer>`__                      preview                                       

 **Calendar**                

 `exo.calendar.default.event  An integer        2 (equivalent to 1 hour)    
 .suggest <#PLFAdminGuide.Co  number n, used                                
 nfiguration.EndDateSuggesti  to                                            
 on>`__                       auto-calculate                                
                              and suggest the                               
                              end time when                                 
                              users                                         
                              create/edit an                                
                              event.                                        

 `exo.calendar.default.task.  An integer        1 (equivalent to 30 mins)   
 suggest <#PLFAdminGuide.Con  number n, used                                
 figuration.EndDateSuggestio  to                                            
 n>`__                        auto-calculate                                
                              and suggest the                               
                              end time when                                 
                              users                                         
                              create/edit a                                 
                              task.                                         

 **Site metadata**           

 `exo.intranet.portalConfig.  Don't change      false                       
 metadata.override <#PLFDevG  this unless you                               
 uide.Site.CreateNew.Redeplo  customize the                                 
 ySiteExtension>`__           Intranet site.                                

 `exo.intranet.portalConfig.  Don't change      insert                      
 metadata.importmode <#PLFDe  this unless you                               
 vGuide.Site.CreateNew.Redep  customize the                                 
 loySiteExtension>`__         Intranet site.                                

 `exo.acme.portalConfig.meta  Only affect when  false                       
 data.override <#eXoAddonsGu  you install the                               
 ide.ACME.Installation>`__    ACME addon.                                   

 `exo.ide.portalConfig.metad  Only affect when  true                        
 ata.override <#eXoAddonsGui  you install the                               
 de.IDE>`__                   IDE addon.                                    

 **Datasource**              

 `exo.jcr.datasource.name <#  JCR datasource    java:/comp/env/exo-jcr      
 PLFAdminGuide.Database.JNDI  name.                                         
 >`__                                                                       

 `exo.idm.datasource.name <#  IDM datasource    java:/comp/env/exo-idm      
 PLFAdminGuide.Database.JNDI  name.                                         
 >`__                                                                       

 **Clustering**              

 exo.cluster.partition.name   Give a string to  DefaultPartition            
                              identify your                                 
                              cluster, to                                   
                              avoid conflict                                
                              with other                                    
                              clusters in the                               
                              network.                                      

 `exo.jcr.cluster.jgroups.tc  JGroups                                       
 p\* <#PLFAdminGuide.Cluster  configuration                                 
 ing.JGroups.JCR.TCP>`__      for JCR using                                 
                              TCP.                                          

 `exo.jcr.cluster.jgroups.ud  JGroups                                       
 p.\* <#PLFAdminGuide.Cluste  configuration                                 
 ring.JGroups.JCR.UDP>`__     for JCR using                                 
                              UDP.                                          

 `exo.idm.cluster.jgroups.tc  JGroups                                       
 p\* <#PLFAdminGuide.Cluster  configuration                                 
 ing.JGroups.IDM.TCP>`__      for IDM using                                 
                              TCP.                                          

 `exo.idm.cluster.jgroups.ud  JGroups                                       
 p.\* <#PLFAdminGuide.Cluste  configuration                                 
 ring.JGroups.IDM.UDP>`__     for IDM using                                 
                              UDP.                                          

 `exo.jcr.cluster.jgroups.co  Path to your                                  
 nfig <#PLFAdminGuide.Cluste  customized                                    
 ring.JGroups_xml>`__         JGroups                                       
                              configuration                                 
                              file, applied to                              
                              JCR.                                          

 `exo.jcr.cluster.jgroups.co  URL to your                                   
 nfig-url <#PLFAdminGuide.Cl  customized                                    
 ustering.JGroups_xml>`__     JGroups                                       
                              configuration                                 
                              file, applied to                              
                              JCR.                                          

 `exo.idm.cluster.jgroups.co  Path to your                                  
 nfig <#PLFAdminGuide.Cluste  customized                                    
 ring.JGroups_xml>`__         JGroups                                       
                              configuration                                 
                              file, applied to                              
                              IDM.                                          

 **Quartz Scheduler**        

 Main Scheduler Properties   

 `exo.quartz.scheduler.insta  The name of the   ExoScheduler                
 nceName <#PLFAdminGuide.Con  scheduler                                     
 figuration.QuartzScheduler>  instance.                                     
 `__                                                                        

 `exo.quartz.scheduler.insta  The type of the   AUTO                        
 nceId <#PLFAdminGuide.Confi  scheduler                                     
 guration.QuartzScheduler>`_  instance.                                     
 _                                                                          

 ThreadPool configuration    
 Properties                  

 `exo.quartz.threadPool.clas  Is the name of    org.quartz.simpl.SimpleThre 
 s <#PLFAdminGuide.Configura  the ThreadPool    adPool                      
 tion.QuartzScheduler>`__     implementation                                
                              used.                                         

 `exo.quartz.threadPool.thre  It an integer     5 (which is the value of    
 adPriority <#PLFAdminGuide.  value between     Thread.NORM\_PRIORITY)      
 Configuration.QuartzSchedul  Thread.MIN\_PRIO                              
 er>`__                       RITY                                          
                              (which is 1) and                              
                              Thread.MAX\_PRIO                              
                              RITY                                          
                              (which is 10).                                

 `exo.quartz.threadPool.thre  It is the number  25                          
 adCount <#PLFAdminGuide.Con  of threads that                               
 figuration.QuartzScheduler>  are available                                 
 `__                          for concurrent                                
                              execution of                                  
                              jobs.                                         

 JobStore configuration      
 Properties                  

 `exo.quartz.jobStore.misfir  The number of     6000                        
 eThreshold <#PLFAdminGuide.  milliseconds the                              
 Configuration.QuartzSchedul  scheduler will                                
 er>`__                       tolerate a                                    
                              trigger to pass                               
                              its                                           
                              next-fire-time                                
                              by, before being                              
                              considered                                    
                              misfired.                                     

 `exo.quartz.jobStore.class   The Scheduler’s   org.quartz.impl.jdbcjobstor 
 <#PLFAdminGuide.Configurati  JobStore class    e.JobStoreTX                
 on.QuartzScheduler>`__       name.                                         

 `exo.quartz.jobStore.driver  The Driver        org.quartz.impl.jdbcjobstor 
 DelegateClass <#PLFAdminGui  delegate which    e.StdJDBCDelegate           
 de.Configuration.QuartzSche  will understand                               
 duler>`__                    the database                                  
                              system dialect.                               

 `exo.quartz.jobStore.usePro  The flag which    false                       
 perties <#PLFAdminGuide.Con  instructs                                     
 figuration.QuartzScheduler>  JDBCJobStore                                  
 `__                          that all values                               
                              in JobDataMaps                                
                              will be Strings.                              

 `exo.quartz.jobStore.dataSo  The name of the   quartzDS                    
 urce <#PLFAdminGuide.Config  DataSources                                   
 uration.QuartzScheduler>`__  defined in the                                
                              configuration                                 
                              properties file                               
                              for quartz.                                   

 `exo.quartz.jobStore.tableP  The prefix used   QRTZ\_                      
 refix <#PLFAdminGuide.Confi  for to Quartz’s                               
 guration.QuartzScheduler>`_  tables in the                                 
 _                            database.                                     

 `exo.quartz.jobStore.isClus  Set to "true" in  false                       
 tered <#PLFAdminGuide.Confi  order to turn on                              
 guration.QuartzScheduler>`_  clustering                                    
 _                            features.                                     

 `exo.quartz.jobStore.cluste  Set the           20000                       
 rCheckinInterval <#PLFAdmin  frequency (in                                 
 Guide.Configuration.QuartzS  milliseconds) at                              
 cheduler>`__                 which this                                    
                              instance                                      
                              "checks-in" with                              
                              other instances                               
                              of the cluster.                               

 `exo.quartz.jobStore.maxMis  The maximum       20                          
 firesToHandleAtATime <#PLFA  number of                                     
 dminGuide.Configuration.Qua  misfired                                      
 rtzScheduler>`__             triggers the                                  
                              jobstore will                                 
                              handle in a                                   
                              given pass.                                   

 `exo.quartz.jobStore.dontSe  Setting this      false                       
 tAutoCommitFalse <#PLFAdmin  parameter to                                  
 Guide.Configuration.QuartzS  "true" tells                                  
 cheduler>`__                 Quartz not to                                 
                              call                                          
                              setAutoCommit(fa                              
                              lse)                                          
                              on connections                                
                              obtained from                                 
                              the                                           
                              DataSource(s).                                

 `exo.quartz.jobStore.acquir  Whether or not    false                       
 eTriggersWithinLock <#PLFAd  the acquisition                               
 minGuide.Configuration.Quar  of next triggers                              
 tzScheduler>`__              to fire should                                
                              occur within an                               
                              explicit                                      
                              database lock.                                

 `exo.quartz.jobStore.lockHa  The class name                                
 ndler.class <#PLFAdminGuide  to be used to                                 
 .Configuration.QuartzSchedu  produce an                                    
 ler>`__                      instance of a                                 
                              "org.quartz.impl                              
                              .jdbcjobstore".                               

 `exo.quartz.jobStore.driver  A pipe-delimited                              
 DelegateInitString <#PLFAdm  list of                                       
 inGuide.Configuration.Quart  properties (and                               
 zScheduler>`__               their values)                                 
                              that can be                                   
                              passed to the                                 
                              DriverDelegate                                
                              during                                        
                              initialization                                
                              time.                                         

 `exo.quartz.jobStore.txIsol  A value of        false                       
 ationLevelSerializable <#PL  "true" tells                                  
 FAdminGuide.Configuration.Q  Quartz (when                                  
 uartzScheduler>`__           using JobStoreTX                              
                              or CMT) to call                               
                              setTransactionIs                              
                              olation(Connecti                              
                              on.TRANSACTION\_                              
                              SERIALIZABLE)                                 
                              on JDBC                                       
                              connections.                                  
                              This can be                                   
                              helpful to                                    
                              prevent lock                                  
                              timeouts with                                 
                              some databases                                
                              under high load,                              
                              and long-lasting                              
                              transactions.                                 

 `exo.quartz.jobStore.select  Must be a SQL     SELECT \* FROM {0}LOCKS     
 WithLockSQL <#PLFAdminGuide  string that       WHERE SCHED\_NAME = {1} AND 
 .Configuration.QuartzSchedu  selects a row in  LOCK\_NAME = ? FOR UPDATE   
 ler>`__                      the "LOCKS"                                   
                              table and places                              
                              a lock on the                                 
                              row.                                          

 Datasources configuration   

 `exo.quartz.dataSource.quar  The JNDI URL for  java:/comp/env/exo-jpa\_por 
 tzDS.jndiURL <#PLFAdminGuid  a DataSource      tal                         
 e.Configuration.QuartzSched  that is managed                               
 uler>`__                     by eXo Platform.                              

 **Password Encryption**     

 `exo.plidm.password.class <  The class that    DatabaseReadingSaltEncoder  
 #PLFAdminGuide.Configuratio  encrypts the                                  
 n.PasswordEncryption>`__     user password                                 
                              before it is                                  
                              stored in the                                 
                              database.                                     

 `exo.plidm.password.hash <#  The encrypt       SHA-256                     
 PLFAdminGuide.Configuration  algorithm.                                    
 .PasswordEncryption>`__                                                    

 **Elasticsearch             
 Properties**                

 `exo.es.version.minor <#PLF  The expected      5.6                         
 AdminGuide.Configuration.El  minor                                         
 asticSearch>`__              Elastisearch                                  
                              version                                       
                              compatible with                               
                              eXo Platform.                                 

 `exo.es.embedded.enabled <#  Allows to run an  true                        
 PLFAdminGuide.Configuration  Elasticsearch                                 
 .ElasticSearch.ESClientProp  server embedded                               
 erties>`__                   in eXo Platform                               
                              (not recommended                              
                              for production).                              

 `es.cluster.name <#PLFAdmin  Cluster name      exoplatform-es              
 Guide.Configuration.Elastic  identifies your                               
 Search.ESEmbeddedNodeProper  Elasticsearch                                 
 ties>`__                     cluster for                                   
                              auto-discovery.                               
                              If you’re                                     
                              running multiple                              
                              clusters on the                               
                              same network,                                 
                              make sure you’re                              
                              using unique                                  
                              names.                                        

 `es.node.name <#PLFAdminGui  Name of the mode  exoplatform-es-embedded     
 de.Configuration.ElasticSea  for the embedded                              
 rch.ESEmbeddedNodePropertie  mode. If not                                  
 s>`__                        specified, a                                  
                              name is                                       
                              generated                                     
                              dynamically at                                
                              startup.                                      

 `es.network.host <#PLFAdmin  Sets both         "127.0.0.1"                 
 Guide.Configuration.Elastic  'bind\_host' and                              
 Search.ESEmbeddedNodeProper  'publish\_host'                               
 ties>`__                     params. More                                  
                              details                                       
                              `here <https://w                              
                              ww.elastic.co/gu                              
                              ide/en/elasticse                              
                              arch/reference/c                              
                              urrent/modules-n                              
                              etwork.html#adva                              
                              nced-network-set                              
                              tings>`__                                     

 `es.discovery.zen.ping.unic  In Unicast        ["127.0.0.1"]               
 ast.hosts <#PLFAdminGuide.C  dicovery mode,                                
 onfiguration.ElasticSearch.  this parameter                                
 ESEmbeddedNodeProperties>`_  lets you set a                                
 _                            list of master                                
                              nodes in the                                  
                              cluster to                                    
                              perform                                       
                              discovery when                                
                              new nodes                                     
                              (master or data)                              
                              are started.                                  

 `es.http.port <#PLFAdminGui  TCP Port of the   9200                        
 de.Configuration.ElasticSea  embedded ES                                   
 rch.ESEmbeddedNodePropertie  node.                                         
 s>`__                                                                      

 `es.path.data <#PLFAdminGui  Local path to     gatein/data                 
 de.Configuration.ElasticSea  the directory                                 
 rch.ESEmbeddedNodePropertie  where to                                      
 s>`__                        Elasticsearch                                 
                              will store index                              
                              data allocated                                
                              for this node.                                

 **Elasticsearch Client**    

 `exo.es.search.server.url <  URL of the node   "http://127.0.0.1:9200"     
 #PLFAdminGuide.Configuratio  used for                                      
 n.ElasticSearch.ESClientPro  searching.                                    
 perties>`__                  Required and                                  
                              exo.es.embedded.                              
                              enabled=false                                 

 `exo.es.search.server.usern  Username used                                 
 ame <#PLFAdminGuide.Configu  for the BASIC                                 
 ration.ElasticSearch.ESClie  authentication                                
 ntProperties>`__             on the                                        
                              Elasticsearch                                 
                              node used for                                 
                              searching.                                    

 `exo.es.search.server.passw  Password used                                 
 ord <#PLFAdminGuide.Configu  for the BASIC                                 
 ration.ElasticSearch.ESClie  authentication                                
 ntProperties>`__             on the                                        
                              Elasticsearch                                 
                              node used for                                 
                              searching.                                    

 `exo.es.index.server.url <#  URL of the node   "http://127.0.0.1:9200"     
 PLFAdminGuide.Configuration  used for                                      
 .ElasticSearch.ESClientProp  indexing.                                     
 erties>`__                                                                 

 `exo.es.index.server.userna  Username used                                 
 me <#PLFAdminGuide.Configur  for the BASIC                                 
 ation.ElasticSearch.ESClien  authentication                                
 tProperties>`__              on the                                        
                              Elasticsearch                                 
                              node used for                                 
                              indexing.                                     

 `exo.es.index.server.passwo  Password used                                 
 rd <#PLFAdminGuide.Configur  for the BASIC                                 
 ation.ElasticSearch.ESClien  authentication                                
 tProperties>`__              on the                                        
                              Elasticsearch                                 
                              node used for                                 
                              indexing.                                     

 **Elasticsearch Indexing    
 properties**                

 `exo.es.indexing.batch.numb  Maximum number    1000                        
 er <#PLFAdminGuide.Configur  of documents                                  
 ation.ElasticSearch.Indexin  that can be sent                              
 gProperties>`__              to Elasticsearch                              
                              in one bulk                                   
                              request.                                      

 `exo.es.indexing.request.si  Maximum size (in  10485760 (= 10Mb)           
 ze.limit <#PLFAdminGuide.Co  bytes) of an                                  
 nfiguration.ElasticSearch.I  Elasticsearch                                 
 ndexingProperties>`__        bulk request.                                 

 `exo.es.reindex.batch.size   Size of the       100                         
 <#PLFAdminGuide.Configurati  chunks of the                                 
 on.ElasticSearch.IndexingPr  reindexing                                    
 operties>`__                 batch.                                        

 `exo.es.indexing.replica.nu  Number of         1                           
 mber.default <#PLFAdminGuid  replicas of the                               
 e.Configuration.ElasticSear  index.                                        
 ch.IndexingProperties>`__                                                  

 `exo.es.indexing.shard.numb  Number of shards  5                           
 er.default <#PLFAdminGuide.  of the index.                                 
 Configuration.ElasticSearch                                                
 .IndexingProperties>`__                                                    

 **Enable/Disable activity   
 type**                      

 `exo.activity-type.activity  The property      true                        
 -type-key.enabled <#PLFAdmi  that allows to                                
 nGuide.Configuration.Activi  enable or                                     
 tyType>`__                   disable an                                    
                              activity having                               
                              the type key                                  
                              `` activity-type                              
                              -key ``                                       
                              from posting in                               
                              the streams.                                  

 **File storage              
 configuration**             

 `exo.files.binaries.storage  Allows to define  fs                          
 .type <#PLFAdminGuide.Confi  the file storage                              
 guration.fileStorageconfig>  way: File system                              
 `__                          (type=fs) or                                  
                              RDBMS                                         
                              (type=rdbms).                                 

 `exo.commons.FileStorageCle  Enables/disables  true                        
 anJob.enabled <#PLFAdminGui  the job that                                  
 de.Configuration.fileStorag  cleans unused                                 
 econfig>`__                  files.                                        

 `exo.commons.FileStorageCle  The retention     30 days                     
 anJob.retention-time <#PLFA  time of unused                                
 dminGuide.Configuration.fil  files                                         
 eStorageconfig>`__                                                         

 `exo.commons.FileStorageCle  The cron job      0 0 11 ? \* SUN             
 anJob.expression <#PLFAdmin  expression for                                
 Guide.Configuration.fileSto  scheduling the                                
 rageconfig>`__               file cleaner job                              

 `exo.files.storage.dir <#PL  The location      {exo.data.dir}/files        
 FAdminGuide.Configuration.f  where to store                                
 ileStorageconfig>`__         binary files in                               
                              case of file                                  
                              system storage.                               
                              In cluster mode,                              
                              this location                                 
                              (folder) should                               
                              be shared.                                    

 **MongoDB configuration**:  
 Database for eXo Chat: all  
 the below parameters could  
 be configured in            
 `chat.properties            
 file <#PLFAdminGuide.Config 
 uration.ChatConfiguration>` 
 __                          

 `dbServerType <#PLFAdminGui  Allows to define  mongo                       
 de.Database.ChatDatabase>`_  MongoDB type:                                 
 _                            either Mongo or                               
                              embed. Embed                                  
                              value is used                                 
                              for unit tests.                               

 `dbServerHost <#PLFAdminGui  The host name or  localhost                   
 de.Database.ChatDatabase>`_  IP of MongoDB.                                
 _                                                                          

 `dbServerPort <#PLFAdminGui  The port number   27017                       
 de.Database.ChatDatabase>`_  to connect to                                 
 _                            MongoDB host.                                 

 `dbServerHosts <#PLFAdminGu  The MongoDB       localhost:27017             
 ide.Database.ChatDatabase>`  nodes to connect                              
 __                           to, as a                                      
                              comma-separated                               
                              list of                                       
                              <host:port>                                   
                              values.                                       

 `dbName <#PLFAdminGuide.Dat  Name of the       chat                        
 abase.ChatDatabase>`__       Mongo database                                
                              name.                                         

 `dbAuthentication <#PLFAdmi  Enables or        false                       
 nGuide.Database.ChatDatabas  disables                                      
 e>`__                        authentication                                
                              to access                                     
                              MongoDB. When                                 
                              set to true this                              
                              means that                                    
                              authentication                                
                              is required.                                  

 `dbUser <#PLFAdminGuide.Dat  Provide the       EMPTY                       
 abase.ChatDatabase>`__       username to                                   
                              access the                                    
                              database if                                   
                              authentication                                
                              needed.                                       

 `dbPassword <#PLFAdminGuide  Provide the       EMPTY                       
 .Database.ChatDatabase>`__   password to                                   
                              access the                                    
                              database if                                   
                              authentication                                
                              needed.                                       

 `chatPassPhrase <#PLFAdminG  The password to   chat                        
 uide.ChatAdministration.Con  access REST                                   
 figuration.ChatServer>`__    service on the                                
                              BRAND\_CHAT                                   
                              server.                                       

 `chatCronNotifCleanup <#PLF  The frequency of  0 0/60 \* \* \* ?           
 AdminGuide.ChatAdministrati  cleaning eXo                                  
 on.Configuration.ChatServer  Chat                                          
 >`__                         notifications.Th                              
                              ey                                            
                              are cleaned up                                
                              every one hour                                
                              by default.                                   

 `teamAdminGroup <#PLFAdminG  The eXo group     /platform/administrators    
 uide.ChatAdministration.Con  who can create                                
 figuration.ChatServer>`__    teams.                                        

 `chatReadDays <#PLFAdminGui  Number of days    30 (days)                   
 de.ChatAdministration.Confi  to display the                                
 guration.ChatServer>`__      corresponding                                 
                              chat messages.                                

 `chatReadTotalJson <#PLFAdm  The number of     200                         
 inGuide.ChatAdministration.  messages that                                 
 Configuration.ChatServer>`_  you can get in                                
 _                            the Chat room.                                

 `chatIntervalChat <#PLFAdmi  Time interval to  5000                        
 nGuide.ChatAdministration.C  refresh messages                              
 onfiguration.ChatClientUpda  in a chat.                                    
 tes>`__                                                                    

 `chatIntervalSession <#PLFA  Time interval to  60000                       
 dminGuide.ChatAdministratio  keep a chat                                   
 n.Configuration.ChatClientU  session alive in                              
 pdates>`__                   milliseconds.                                 

 `chatIntervalStatus <#PLFAd  Time interval to  60000                       
 minGuide.ChatAdministration  refresh user                                  
 .Configuration.ChatClientUp  status in                                     
 dates>`__                    milliseconds.                                 

 `chatIntervalNotif <#PLFAdm  Time interval to  5000                        
 inGuide.ChatAdministration.  refresh                                       
 Configuration.ChatClientUpd  Notifications in                              
 ates>`__                     the main menu in                              
                              milliseconds.                                 

 `chatIntervalUsers <#PLFAdm  Time interval to  60000                       
 inGuide.ChatAdministration.  refresh Users                                 
 Configuration.ChatClientUpd  list in                                       
 ates>`__                     milliseconds.                                 

 `chatTokenValidity <#PLFAdm  Time after which  60000                       
 inGuide.ChatAdministration.  a token will be                               
 Configuration.ChatClientUpd  invalid. The use                              
 ates>`__                     will then be                                  
                              considered                                    
                              offline.                                      

 `exo.statistics.groovy.temp  Enables/disables  true                        
 late.enabled <#PLFAdminGuid  Groovy Templates                              
 e.Configuration.statisticsP  statistics that                               
 arameter>`__                 is collected                                  
                              asynchronously.                               

 **CometD configuration**    

 `exo.cometd.oort.url <#PLFA  The CometD Oort   "http://localhost:8080/come 
 dminGuide.Clustering.Settin  URL used in       td/cometd",                 
 gUpCluster>`__               clustering mode.  localhost should be         
                                                replaced by the hostname or 
                                                the IP of the cluster node. 

 `exo.cometd.oort.configType  The CometD        multicast                   
  <#PLFAdminGuide.Clustering  configuration                                 
 .SettingUpCluster>`__        type which could                              
                              be either                                     
                              "static" or                                   
                              "multicast".                                  

 `exo.cometd.oort.cloud <#PL  A                                             
 FAdminGuide.Clustering.Sett  comma-separated                               
 ingUpCluster>`__             list of URLs of                               
                              other Oort                                    
                              comets to                                     
                              connect to at                                 
                              startup.                                      

 **Update of last login      
 time**                      

 `exo.idm.user.updateLastLog  Enables/disables  true                        
| inTime <#PLFAdminGuide.Conf  the update of                                 
 iguration.lastlogintime>`__  last login time                               
                              each time the                                 
                              user login.                                   

 **Define spaces             
 administrators group**      

 `exo.social.spaces.administ  Defines the list                              
 rators <#PLFAdminGuide.Conf  of spaces                                     
 iguration.SpacesAdministrat  administrators                                
 ion>`__                      groups.                                       

 **Assets versions used in   
 static resources URLs**     

 `exo.assets.version <#PLFAd  Defines the       It is set to PRODUCT binary 
 minGuide.Configuration.Asse  assets version.   version.                    
 tsVersionConf>`__                                                          

 **Username case sensitive** 

 `exo.auth.case.insensitive   Defines if        false.                      
 <#PLFAdminGuide.Configurati  usernames in                                  
 on.CaseSensitiveUsername>`_  PRODUCT are case                              
 _                            sensitive or                                  
                              not.                                          

 **User inactivity delay**   

 `exo.user.status.offline.de  Defines the time  240000                      
 lay <#PLFAdminGuide.Configu  laps which makes                              
 ration.UserInactivityDelay>  the user in                                   
 `__                          offline status.                               
                              Its value is                                  
                              expressed in                                  
                              milliseconds.                                 

 **Notifications channels**  

 `exo.notification.channels   Defines the       WEB\_CHANNEL, MAIL\_CHANNEL 
 <#PLFAdminGuide.Configurati  activated                                     
 on.Notification>`__          notification                                  
                              channels.                                     

 **Wiki application base     
 URI**                       

 `wiki.permalink.appuri <#PL  Defines the base  wiki                        
 FAdminGuide.Configuration.W  URI for the wiki                              
 ikiBaseURI>`__               application                                   
                              permalinks.                                   

 **Files upload limit**      

 `exo.ecms.connector.drives.  Maximum size (in  200                         
 uploadLimit <#PLFAdminGuide  MB) allowed of                                
 .Configuration.FileSizeLimi  an uploaded                                   
 t>`__                        file.                                         

 `exo.social.activity.upload  Maximum size (in  200                         
 Limit <#PLFAdminGuide.Confi  MB) allowed of                                
 guration.FileSizeLimit>`__   an uploaded                                   
                              image through                                 
                              the CKEditor.                                 

 `exo.wiki.attachment.upload  Maximum size (in  200                         
 Limit <#PLFAdminGuide.Confi  MB) allowed of                                
 guration.FileSizeLimit>`__   an uploaded file                              
                              in Wiki                                       
                              application.                                  


