.. _Installation:

#########################
Installation and Startup
#########################

    eXo Platform is packaged as a deployable enterprise archive defined by
    the Java EE specification, and as a configuration directory. In this
    chapter, you will see the following topics:

    -  :ref:`System requirements <SystemRequirements>`
       Specifications which are required for running eXo Platform.

    -  :ref:`Installing eXo Platform Trial docker image <EETrial>`
       Steps needed to install eXo Platform Trial.

    -  :ref:`Installing eXo Platform CommunityEdition <CommunityEdition>`
       Steps needed to install eXo Platform Community Edition.

    -  :ref:`Registering your installation <Registration>`
       Instructions for how to register your installation the eXo Tribe.

    -  :ref:`Unlocking your trial with an unlock key <unlockTrial>`
       Instructions for how to unlock the free 30-day trial.

    -  :ref:`Installing eXo Platform Enterprise Edition <EnterpriseEdition>`
       Instructions on how to install the enterprise edition.

    -  :ref:`Task Management Installation <TasksInstallation>`
       Steps for how to install and uninstall Task Management.

    -  :ref:`eXo Chat Installation <ChatInstallation>`
       Steps for how to install and uninstall eXo Chat through two
       modes: The embedded mode and standalone mode.

    -  :ref:`Web Conferencing Installation <WebConfInstall>`
       Steps for how to install and uninstall eXo Web Conferencing.

    -  :ref:`Customizing environment variables <CustomizingEnvironmentVariables>`
       How to customize environment variables, such as JVM Memory and GC
       settings.

    -  :ref:`Startup profiles <eXoProfiles>`
       The runtime profiles which are used to enable/disable modules of
       eXo Platform.

    -  :ref:`Troubleshooting <Troubleshooting>`
       How to solve problems you may encounter when starting up eXo 
       Platform.
       
.. _SystemRequirements:

====================
System requirements       
====================

.. warning:: The requirements cited below are provisional and may change according to quality tests findings.

To run eXo Platform 5.1, your system is required to meet the following 
specifications or higher:

-  CPU: Multi-core recommended, 2GHz minimum.

-  Memory: The eXo Platform package is optimized with default settings: max
   heap size = 4GB and non-heap size = 256MB; so the available memory
   should be at least 4GB. It is recommended you have a memory of 8GB
   (4GB free for database services and file system caches).

-  Free disk space: 10GB minimum

-  Java 9+: JDK 9 is required for eXo Platform 5.1 version. Set the
   **JAVA\_HOME** environment variable to point to your JDK
   installation.

-  Java 7 and below is incompatible for eXo Platform 5.1 version.

-  Browser Compatibility:

   +------------+-----------------+-----------------+-----------------+-----------------+
   | Operating  | Recommended     | Supported       | Compatible      | Incompatible    |
   | system     | browser         | browser         | browser         | browser         |
   +============+=================+=================+=================+=================+
   | Windows    | -  Firefox ESR  | -  Internet     |                 | -  Internet     |
   |            |    52.4         |    Explorer 11  |                 |    Explorer 10  |
   |            |                 |                 |                 |    and below    |
   |            | -  Edge 15      | -  Edge,        |                 |                 |
   |            |                 |    Chrome,      |                 |                 |
   |            | -  Chrome 62    |    Firefox -    |                 |                 |
   |            |                 |    Latest       |                 |                 |
   |            |                 |    stable       |                 |                 |
   |            |                 |                 |                 |                 |                                                                                       
   +------------+-----------------+-----------------+-----------------+-----------------+
   | Linux      | -  Firefox ESR  | -  Firefox -    | -  Chrome - the |                 |
   |            |    52.4         |    the last     |    latest       |                 |
   |            |                 |    stable       |    stable       |                 |
   |            |                 |                 |                 |                 |                                                                                      
   +------------+-----------------+-----------------+-----------------+-----------------+
   | Mac OS     | -  Firefox ESR  | -  Firefox -    | -  Safari 11,10 | -  Safari 8 and |
   |            |    52.4         |    the last     |                 |    below        |
   |            |                 |    stable       |                 |                 |
   |            | -  Chrome 62    |                 |                 |                 |
   |            |                 | -  Chrome - the |                 |                 |
   |            |                 |    last stable  |                 |                 |
   |            |                 |                 |                 |                 |                                                                                       
   +------------+-----------------+-----------------+-----------------+-----------------+
   | Android    |                 | -  Chrome 55    | -  Chrome - the |                 |
   |            |                 |                 |    latest       |                 |
   |            |                 |                 |    stable       |                 |
   |            |                 |                 |                 |                 |
   |            |                 |                 | -  Firefox -    |                 |
   |            |                 |                 |    the latest   |                 |
   |            |                 |                 |    stable       |                 |
   |            |                 |                 |                 |                 |                                                                                      
   +------------+-----------------+-----------------+-----------------+-----------------+
   | iOS        |                 | -  Chrome 55    | -  Chrome - the |                 |
   |            |                 |                 |    latest       |                 |
   |            |                 | -  Safari 9     |    stable       |                 |
   |            |                 |                 |                 |                 |
   |            |                 |                 | -  Safari 8     |                 |
   |            |                 |                 |                 |                 |                                                                                      
   +------------+-----------------+-----------------+-----------------+-----------------+

.. note:: The eXo server will run on the port 8080 by default, so make sure this port is not currently in use or configure eXo Platform to use another port.

.. _EETrial:

================================
eXo Platform Trial Docker image
================================

In this section, we will provide how to install the Trial edition of
eXo Platform and the steps following the installation from registering the
software to unlocking it.

Here are the steps to follow:

-  :ref:`Starting the Docker Image <EETrial.start>`

-  :ref:`Registering your software <EETrial.register>`

-  :ref:`Setting up the admin accounts <EETrial.admins>`

.. _EETrial.start:

Starting the Docker Image
~~~~~~~~~~~~~~~~~~~~~~~~~~~

The trial edition of the commercial version of eXo Platform is available as
docker container in various versions: 5.1.0, 5.0.1, 4.4.3 ...

In this section, you will learn how to start and stop it.

.. warning:: eXo Platform's Community Edition and the trial version of the commercial Enterprise Edition are only available as a Docker install
			 to facilitate deployment for testing. Owners of the full commercial version are not supported based on a Docker install, this
			 Docker-related documentation is therefore not relevant to them.
			 Subscribed customers can refer to next sections to install their commercial package.

The docker image of the trial version of eXo Platform Enterprise Edition
supports **only** HSQL database for testing purposes.

To be able to start eXo Platform Trial Docker image, these prerequisites
should be satisfied:

-  Docker daemon version 12+ installed on your machine.

-  Internet connection.

-  4GB of RAM available and 1GB of free disk space.

Having the above requirement satisfied, you can start eXo Platform trial
edition using this command:

::

    docker run --rm -v exo_trial_data:/srv -p 8080:8080 exoplatform/exo-trial

A log message appears indicating the startup of the server:

::

    2017-09-19 12:34:54,573 | INFO  | Server startup in 80328 ms [org.apache.catalina.startup.Catalina<main>]

The platform is then accessible via `http://localhost:8080 <#>`__.

To stop the server, just click on Ctrl+c in the keyboard or run the
command:

::

    docker stop <your-container-ID>

The container-ID is known via the command:

::

    docker ps

.. tip:: For more details about eXo Platform Trial edition Docker image: versions, how to configure, how to add/remove add-ons..., you can consult this `documentation <https://hub.docker.com/r/exoplatform/exo-trial/>`__.

.. _EETrial.register:

Registering your software
~~~~~~~~~~~~~~~~~~~~~~~~~~~

eXo Tribe provides access to an enormous community of eXo Platform users
and developers.

As a result, registration is needed so that you can post questions in
the community to get help from other IT professionals around the world.
Also, by registering your installation in the tribe, you will contribute
to anonymous statistics published on the tribe website and help
improving the eXo Platform.

After a successful installation, at the first startup, you will be
redirected to the *Register your Software* screen as follows:

|image0|

.. note:: For the Enterprise edition, you have to accept the Terms and Conditions Agreement before going to the registration.

From the *Register your Software* screen, click Register your software
to start the registration. If you do not want to register this time,
just click the Skip button, but remember that skipping is allowed only
twice.

|image1|

Click the Authorize button to activate the authorization process (you
can select Cancel to skip registering this time, but remember that
canceling is also allowed only twice), if successful, you will see this
message:

|image2|

It means the registration has completed. Now you can select Continue to
start using eXo Platform. Once this is registered, you will never be asked
for registration again.

.. note:: -  If the eXo Tribe website can't be reached, you will get this message:
				
				|image3|
			 In this case, clicking the Continue button still allows you to start using eXo Platform as normal, but you will be asked to register again after next server startup.
		 
		  -  Upgrading to a new platform version will require a new  registration.

		  -  For the Enterprise edition, it is possible to skip the registration completely by unlocking it with :ref:`an official key <EETrial.unlock.UnlockKey>`.

		  -  If the authorization process failed, try to redo the registration or contact `our support team <https://community.exoplatform.com/portal/intranet/>`__ for more details.

.. _EETrial.admins:

Setting up the admin accounts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

After registering your installation to benefit from eXo Platform community
advantages, you are asked to set up administrators accounts.

This screen appears allowing you to fill in information for users
promoted as the administrators of the platform:

|image4|

In the first part of the screen, the user will belong to the group
/platform/administrators. The second part of the screen allows you to
redefine the super user **root** password.

.. _CommunityEdition:

===========================================
Installing eXo Platform Community Edition
===========================================

eXo Platform Community Edition is distributed as a convenient Docker image
available with different versions: 5.1, 5.0, 4.4, 4.3...

`Docker <https://www.docker.com>`__ is a software container platform
which enables enterprises to build agile software delivery pipelines to
ship new features faster, more securely and with confidence for both
Linux, Windows Server, and Linux-on-mainframe apps.

.. warning:: eXo Platform's Community Edition and the trial version of the
			 commercial Enterprise Edition are only available as a Docker install
			 to facilitate deployment for testing. Owners of the full commercial
			 version are not supported based on a Docker install, this
			 Docker-related documentation is therefore not relevant to them.
			 Subscribed customers can refer to next sections to install their commercial package.

In this section, we will provide the needed steps to install an eXo Platform
Community Edition docker image.

This docker image of eXo Platform supports HSQL database for testing purposes
and MySQL for eXo Platformion environments.

To try the eXo Platform community edition docker image, some prerequisites
should be satisfied:

-  Docker daemon version 12+ installed on your machine.

-  Internet connection.

-  4GB of RAM available and 1GB of free disk space.

To start and test eXo Platform Community Edition, simply execute this
command:

::

    docker run -v exo_data:/srv/exo -p 8080:8080 exoplatform/exo-community

The execution of this command will launch a container of the last
millestone version of eXo Platform PLF\_VERSION and the version is updated
every week after each weekly release:

.. note:: You can set a custom name to your container by adding the option ``--name custom_name`` to the start command.


::

    2017-09-19 09:37:10,271 | INFO  | Server startup in 176588 ms [org.apache.catalina.startup.Catalina<main>]

The above log message indicates the server startup. You can start
exploring eXo Platform Community Edition by visiting the URL
`http://localhost:8080 <#>`__ and then follow the instructions.

To shutdown the server, you can either click on the keyboard buttons
Ctrl+c or execute this command:

::

    docker stop <your-container-name>

.. note:: To list all docker conatainers that already exist on your machine with their different parameters, just execute this command:

			::

				docker ps -a

			An example of the result of the cited command:

			::

				CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS                           PORTS                    NAMES
				6d6d74d07030        exoplatform/exo-community   "/opt/exo/start_eX..."   6 minutes ago       Up 6 minutes                     0.0.0.0:8080->8080/tcp   agitated_williams
				ee949d337207        exoplatform/exo-community   "/opt/exo/start_eX..."   About an hour ago   Exited (130) About an hour ago                            vibrant_feynman
		
			To just paste parameters of the running container, the command to execute is:

			::

				docker ps


With a docker container, it is possible to start eXo Platform in debug or dev
mode: by adding --debug or --dev:

-  Debug mode: You should add the option *--debug* to the start command
   cited above and you should specify the debug port by the parameter
   ``-p 8000:8000``.

   A log message appears indication that the debug mode is active:

   ::

       Listening for transport dt_socket at address: 8000

-  Dev mode: You should add the option *--dev* to the start command
   cited above.

.. tip:: For more details about eXo Platform Community Docker image: versions, how to configure, how to add/remove add-ons..., you can consult this `documentation <https://hub.docker.com/r/exoplatform/exo-community/>`__.

.. _Registration:

=============================
Registering your installation
=============================

eXo Tribe provides access to an enormous community of eXo Platform users
and developers. As a result, registration is needed so that you can post
questions in the community to get help from other IT professionals
around the world. Also, by registering your installation in the tribe,
you will contribute to anonymous statistics published on the tribe
website and help improving the product.

After a successful installation, at the first startup, you will be
redirected to the *Register your Software* screen as follows:

|image5|

.. note:: For the Enterprise edition, you have to accept the Terms and Conditions Agreement before going to the registration.

From the *Register your Software* screen, click Register your software
to start the registration. If you do not want to register this time,
just click the Skip button, but remember that skipping is allowed only
twice.

|image6|

Click the Authorize button to activate the authorization process (you
can select Cancel to skip registering this time, but remember that
canceling is also allowed only twice), if successful, you will see this
message:

|image7|

It means the registration has completed. Now you can select Continue to
start using eXo Platform. Once this is registered, you will never be asked
for registration again.

.. note:: -  If the eXo Tribe website can't be reached, you will get this message:

			|image8|

			In this case, clicking the Continue button still allows you to start using eXo Platform as normal, but you will be asked to register
			again after next server startup.

		  -  Upgrading to a new platform version will require a new registration.

		  -  For the Enterprise edition, it is possible to skip the  registration completely by unlocking it with :ref:`an official key <EETrial.unlock.UnlockKey>`.

		  -  If the authorization process failed, try to redo the registration or contact `our support team <https://community.exoplatform.com/portal/intranet/>`__for more details.

.. _unlockTrial:

=======================================
Unlocking your trial with an unlock key
=======================================

eXo Platform offers **commercial editions** as a 30-day trial. Thus, you will
see a trial banner at the page footer.

|image9|

-  During the trial period, the message of the trial banner is "You have
   XX days left in your evaluation" where XX is the number of days left
   for your trial.

-  After the trial period, the trial banner turns into red with the
   "Your evaluation period has expired XX days ago" text where XX is the
   number of days as from the expired trial.
   
.. _EETrial.unlock.UnlockKey:   

Unlocking your trial with an unlock key
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You need to purchase a key to unlock the evaluation.

The unlock is done via Unlock Evaluation screen. Open this screen by
clicking Buy a Subscription on the trial banner.

|image10|

On this screen:

-  If you have not purchased a key yet, click the **subscription plan**
   link. It should open the `Editions
   page <http://www.exoplatform.com/company/en/products/editions>`__
   which helps you choose a plan.

   Then, go to `eXo Buy page <https://exoplatform.com/buy>`__ to
   complete the purchase.

   |image11|

 .. note:: You may copy the Product Code from the Unlock screen and submit it in the Buy page, otherwise a new code will be generated and sent to you along with the key.
		   If you have any trouble, please contact *support@exoplatform.com*.


-  If you have received a key already, come back to Unlock Evaluation
   screen to activate your subscription. Enter your *Unlock Key* (and
   *Product Code* if you received one) and click Unlock.

   This function validates your key against the product code. If the key
   is invalid, it displays a message like "*Sorry this evaluation key is
   not valid*\ ". On success, it just redirects you to the previous
   page.
   
   
.. _EnterpriseEdition:


==========================================
Installing eXo Platform Enterprise Edition
==========================================

In this section, we will provide how to install the enterpise edition of
eXo Platform in the two application servers: Tomcat and Jboss.

-  :ref:`Installing the Tomcat bundle <EnterpriseEdition.TomcatInstall>`
   Steps to install eXo Platform enterprise edition in Tomcat.

-  :ref:`Installing eXo Platform as a Windows service <EnterpriseEdition.TomcatInstallWinService>`
   Steps to install eXo Platform as a Windows service.

-  :ref:`Installing on JBoss EAP <EnterpriseEdition.JbossInstall>`
   Steps to install eXo Platform enterprise edition in Jboss.

.. _EnterpriseEdition.TomcatInstall:

Installing the Tomcat bundle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The eXo Platform Tomcat bundle is a ready-made package on top of the Tomcat 8.5
application server. So, you just need to download and extract the
package (named ``eXo-Platform-5.1.0.zip``, for example) on your server.
In this guideline, ``$PLATFORM_TOMCAT_HOME`` is the folder path of the
extracted package.

Starting up the server
-----------------------

eXo Platform is started with a built-in startup script file, which is
``start_eXo.sh`` for Linux and OS X (Mac), and ``start_eXo.bat`` for
Windows. Double-click, or run it in console (Terminal or Command
Prompt):

-  Linux/OS X: ``$PLATFORM_TOMCAT_HOME/start_eXo.sh``

-  Windows: ``%PLATFORM_TOMCAT_HOME%\start_eXo.bat``

The server is started successfully when you see a message like this:

::

    INFO: Server startup in 120619 ms

To start eXo Platform as a background process, use the **--background**
option:

-  Linux/OS X: ``$PLATFORM_TOMCAT_HOME/start_eXo.sh --background``

-  Windows: ``%PLATFORM_TOMCAT_HOME%\start_eXo.bat --background``

You can always check the log files under ``$PLATFORM_TOMCAT_HOME/logs``.

Shutting down the server
-------------------------

If you have started eXo Platform in console (without --background option),
just press **Ctrl+C** to stop it.

In case it is running as background process, you can use the
``stop_eXo`` script:

-  Linux/OS X: ``$PLATFORM_TOMCAT_HOME/stop_eXo.sh``

-  Windows: ``%PLATFORM_TOMCAT_HOME%\stop_eXo.bat``

If you still see the process running, you may forcefully stop it. There
are several ways: using Task Manager (Windows), or running
``stop_eXo.sh -force`` (Linux/OS X), or using ``kill -9`` command
(Linux/OS X).

Starting up eXo Platform in the Dev/Debug mode
------------------------------------------------

In eXo Platform, the Debug mode is generally like other Java applications
using
`JDWP <http://docs.oracle.com/javase/7/docs/technotes/guides/jpda/jdwp-spec.html>`__,
whereas the Dev mode is specific for debugging JavaScript, CSS and
configurations.

To start eXo Platform in the Debug mode, use the **--debug** option:

-  Linux/OS X: ``$PLATFORM_TOMCAT_HOME/start_eXo.sh --debug``

-  Windows: ``%PLATFORM_TOMCAT_HOME%\start_eXo.bat --debug``

The **--debug** option actually adds a JVM option to the Java process:

-  **-agentlib:jdwp=transport=dt\_socket,address=8000,server=y,suspend=n**

To start eXo Platform in the Dev mode, use the **--dev** option. This option
adds two JVM options:

-  **-Dorg.exoplatform.container.configuration.debug**

-  **-Dexo.product.developing=true**

    **Note**

    The Debug and Dev modes are turned off by default and are not
    recommended in production environment because of performance impact.
    See more details in :ref:`Developer guide <#PLFDevGuide.GettingStarted.DebugAndDevMode>`.

.. _EnterpriseEdition.TomcatInstallWinService:

Installing eXo Platform as a Windows service
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section is a tutorial to teach you how to configure eXo Platform as a
windows service. To configure eXo Platform to run as a windows service, two
ways are possible.

The first way: Through Tomcat native installer
------------------------------------------------

   This section describes how to configure eXo Platform as a Windows service
   in a standard Tomcat installation.

   For that purpose follow this procedure:

1. Use a sample batch script, you can take a look at apache tomcat
   `documentation <https://tomcat.apache.org/tomcat-8.5-doc/windows-service-howto.html>`__
   or you can use `this script <https://github.com/exo-samples/docs-samples/blob/master/exo-as-win-service-script/service_eXo.bat>`__
   ``service_eXo.bat`` and put it under ``eXo_Platform_tomcat_home\bin\``.

2. Open a command prompt and run this command:

   ::

       service_exo.bat install eXo-service

   Where eXo-service is the service name.

   This will install eXo Platform as a windows service which will be started
   at the system's startup.

3. To uninstall the service, run this command:

   ::

       tomcat8.exe //DS//eXo-service

The second way: Using the NSSM tool
-------------------------------------

   The non sucking service manager `NSSM <https://nssm.cc/>`__ is a tool
   that helps you to create a windows service based on your
   application's startup script.

   To create your eXo Platform windows service using NSSM, follow this
   procedure:

1. Download the `NSSM <https://nssm.cc/>`__ tool from `here <https://nssm.cc/download>`__.

2. Place the NSSM executable file i.e ``nssm.exe`` in a folder which already exists in your PATH or follow these steps:

   -  Create a folder nssm under ``C:\Program Files\`` and place
      ``nssm.exe`` in it.

   -  Add the folder ``C:\Program Files\nssm`` to your PATH environement
      variable using this command in a command prompt:

      ::

          setx PATH "%PATH%;C:\Program Files\nssm" /M

3. In a command prompt, run this command:

   ::

       nssm install <servicename>

   This will open a nssm window allowing you to browse and select your
   application startup script.

   |image12|

4. Point to eXo Platform startup script ``start_eXo.bat`` and click on
   Install service button.

5. You can now run eXo Platform through this command:

   ::

       nssm start <servicename>

6. To stop eXo Platform server, use this command:

   ::

       nssm stop <servicename>

   More details about NSSM commands in this `link <https://nssm.cc/usage>`__.

.. _EnterpriseEdition.JbossInstall:

Installing on JBoss EAP
~~~~~~~~~~~~~~~~~~~~~~~~~

eXo Platform 5.1 version integrates with JBoss EAP 7.1.

Prerequisites
---------------

-  Have JBoss EAP 7.1 extracted in ``$PLATFORM_JBOSS_HOME``. You can
   download and install JBoss EAP 7.1 by following instructions on this
   `link <https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.1/html/installation_guide/installing_jboss_eap>`__.

-  Have the eXo Platform package for JBoss EAP downloaded into your local.

Installing eXo Platform on JBoss EAP
--------------------------------------

1. Extract your downloaded eXo Platform package.

2. Copy all extracted folders and files into ``$PLATFORM_JBOSS_HOME``.

.. note:: This step will overwrite some files of JBoss EAP with new files of eXo Platform.

3. Optionally, if you want to customize the JVM Options, create a copy of
   ``$PLATFORM_JBOSS_HOME/bin/standalone-customize.sample.conf`` on Linux
   or ``$PLATFORM_JBOSS_HOME/bin/standalone-customize.sample.conf.bat`` on
   Windows. Rename the copy to ``standalone-customize.conf`` (or
   ``standalone-customize.conf.bat`` on Windows), then edit it with your
   JVM Options.

4. Start up the server.

-  On Linux and OS X:

   ::

       $PLATFORM_JBOSS_HOME/bin/standalone.sh

-  On Windows:

   ::

       %PLATFORM_JBOSS_HOME%\bin\standalone.bat

The server starts up successfully when you see the following message in
your log/console 

	::

		INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.1.0.GA (WildFly Core 3.0.10.Final-redhat-1) started in 115316ms - Started 4570 of 4826 services (602 services are lazy, passive or on-demand)


5. Shut down the server.

-  On Linux and OS X

	::

       $PLATFORM_JBOSS_HOME/bin/jboss-cli.sh --connect command=:shutdown
                   

-  On Windows

	::

       %PLATFORM_JBOSS_HOME%\bin\jboss-cli.bat --connect command=:shutdown
                   

The server stops successfully when you see the following message in your
log/console::

    INFO  [org.jboss.as] (MSC service thread 1-4) WFLYSRV0050: JBoss EAP 7.1.0.GA (WildFly Core 3.0.10.Final-redhat-1) stopped in 13470ms


.. note:: Since JBoss EAP 6.3, there is a new blocking timeout property for
			JBoss startup.

			This property is not a timeout per deployment but a timeout on
			container stability and if ``jboss.as.management.blocking.timeout``
			is reached during startup then all applications will be undeployed
			and the container shutdown.
	
			The default value is set to 300s which is too low for eXo Platform in
			which we overrode the value.

			::

				JAVA_OPTS="$JAVA_OPTS -Djboss.as.management.blocking.timeout=604800"

.. |image0| image:: images/installation/register_step1.jpg
.. |image1| image:: images/installation/register_step2.png
.. |image2| image:: images/installation/register_step3.png
.. |image3| image:: images/installation/register_lost_connection.png
.. |image4| image:: images/installation/Admin-accounts.png
.. |image5| image:: images/installation/register_step1.jpg
.. |image6| image:: images/installation/register_step2.png
.. |image7| image:: images/installation/register_step3.jpg
.. |image8| image:: images/installation/register_lost_connection.png
.. |image9| image:: images/unlock_trial/trial_banner.png
.. |image10| image:: images/unlock_trial/unlock_evaluation.png
.. |image11| image:: images/unlock_trial/buy_page.png
.. |image12| image:: images/installation/nssm.png
