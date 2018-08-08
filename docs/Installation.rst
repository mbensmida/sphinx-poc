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


.. |image0| image:: images/installation/register_step1.jpg
.. |image1| image:: images/installation/register_step2.png
.. |image2| image:: images/installation/register_step3.png
.. |image3| image:: images/installation/register_lost_connection.png
.. |image4| image:: images/installation/Admin-accounts.png

