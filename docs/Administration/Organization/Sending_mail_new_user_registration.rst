.. _ManagingYourOrganization.SendingMailUserCreation:

Sending mail about users registration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In eXo Platform registration page is by default disabled. An 
administrator can enable it by following this `guide <ManagingPermissions>` 
to make it accessible to guests so they can register to eXo Platform by
themselves.

To be notified about new users registration, an administrator can
configure eXo Platform to send him emails by following these steps:

1. Configure your SMTP server by following the :ref:`Outgoing mail service <#PLFAdminGuide.Configuration.OutgoingMailService>` guide.

2. Configure the service used for sending emails in ``portal.war/WEB-INF/conf/admin/admin-configuration.xml``. 
   This file contains descriptions for each available parameter, 
   including:

   -  Two mandatory parameters:

      -  ``sendMailAfterRegistration``: Set this parameter to "true" to
      enable email sending after a user registration.

      -  ``mailTo``: Add your email address in which you wish to receive
      notifications about new registrations.

   -  Optional configurations of mail content:

      -  ``mailFrom``: This will be used as from header in the mail.

      -  ``mailSubject``: The Subject of the mail.

      -  ``mailMessage``: The content of the mail.

.. tip:: Use the **${user.userName}** token for **mailSubject** and**mailMessage** to be then replaced by the real username that have been registred.

To check if your configuration takes effect, restart the server and
register a new user. An email that notifies of newly registered user
should be sent to you.
