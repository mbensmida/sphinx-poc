
.. _BuildingOnlineCommunity:

============================
Building an online community
============================

Many users ask for building a Community site like
http://community.exoplatform.com. In this site, they want to allow their
users to register by themselves, or publish some pages, such as Forum.
This tutorial will guide you how to do these tasks via UI.

    **Note**

    This tutorial has some limitations due to using UI only. For
    example, you can allow users to access the Register page, but when a
    user finishes his registration, he is not automatically redirected
    to Home page. To go further, you need to do some development tasks.
    And if you meet any troubles, go to `eXo
    Forum <http://community.exoplatform.com/portal/intranet/forum>`__ to
    get some help.

Before you follow the step-by-step instruction to allow Guest access,
let's learn the "portal manner" of access control:

-  **Publishing sites and pages**

When you access *intranet* site, you are asked to log in, because the
access permission of the site is *\*:/platform/users* by default. So, to
publish any resource under the "intranet" site, you need to make the
site public first. And what happens then?

When the site is public, but all the pages are private, then you are
still seeing a login form. If there is one public page, the portal will
redirect you there without login. If there are several public pages, the
topmost one in the site navigation will be the default redirection.

Knowing this, you can allow anonymous users to access some public pages.
In the example, you will publish Wiki and Forum, and put a new page
called "Welcome" as the default page for anonymous access.

-  **How to enable users to register themselves**

eXo Platform provides a built-in *Register* page already. See the
screenshot below:

|image0|

The page is not a public one, but the membership *\*:/platform/guests*
has access permission, so if the site is public, anonymous users can
type the URL */portal/intranet/Register* to access this page. You can
put a link in the *Welcome* page so that the user does not have to type
the URL.

The Welcome page should also give a *Login* link. Hereunder is the web
content (simplified) you should add to Welcome page:

.. code:: html

    <a href="/portal/login">Sign in</a>
    <a href="/portal/intranet/Register">Register</a>

-  **Site Navigation**

You have read that the topmost page in Site Navigation will be picked up
for redirection, when users access */portal/intranet*. The Site
Navigation can be edited by clicking EditSiteNavigation from the top
navigation bar.

See the screenshot. You can right-click on a page (actually a "node")
and choose Move Up (several times) to change the order of the pages.

|image1|

In the example, you publish Welcome, Wiki and Forum pages so you should
"Move Up" the Welcome page to the top, but below the *Home* page. This
makes Welcome the default page for anonymous while keeping *Home* the
default page for logged users.

You want the Welcome page to offer anonymous users the "Login/Register"
links, but logged-in users should not see it. Though they always can
access by typing page URL, it is nice to hide Welcome page from the Left
Navigator.

To do that, right-click again and choose "Edit this Node", then uncheck
the *Visible* box in the form:

|image2|

-  **Left Navigator**

You can publish the Left Navigator for anonymous access. It is a smart
navigator that shows users a page link if and only when the user has
access permission to the page, so anonymous only see public pages.

The Left Navigator is in fact "some containers and portlets" included in
the Site Layout, so you can edit it by clicking EditSiteLayout.

Exactly, you need to publish the portlet **UICompanyNavigationPortlet**
and publish its containers as well. See the illustration. There are
three (nested) containers, the outermost one is public by default.

|image3|

-  **Publishing a content**

Almost every page is a portal page which consists of containers and
portlets. It is the portlet that brings content to you. In order to
allow anonymous users to view a content, you need to publish: the
portlet that presents the content, the containers of the portlet, the
page and the site. See the following illustration, note that containers
can be nested:

|image4|

The content access also is managed by the relevant application. Wiki
application allows you to set permission for any individual page. In
Forum, the permissions can be set for topic, forum and category. In case
of Content, each content has its publication lifecycle.

-  **Make it public**

To publish the **intranet** site, go to either of its page, like Home
page, and click EditSiteLayout from the top navigation bar, then select
Site's Config from the Edit Inline Composer window. In the
PermissionsAccess, tick the *Everyone* checkbox.

|image5|

The *Everyone* checkbox is also available when you edit a page and its
portlets and containers.

When you are on the page you want to edit, click EditPageLayout from the
top navigation bar. This will open a layout of the portlets and the
containers, and a **Page Editor** floating box.

-  To edit the page access permission: click View Page properties.

-  To edit a portlet's access permission: hover your cursor over the
   portlet area to see a toolbar.

-  To edit a container's access permission: similar as the portlets, but
   you need to click the **Containers** tab in the Page Editor window.

**Building an online community by example**

In this example, you build a "Welcome" page and make it the default page
for anonymous users and give them links to login or register. You also
publish the Forum and Wiki page to allow anonymous users to view.

You should have administrator privileges. Remember to Save your
modification at every step.

Publish the intranet site.

Publish the left navigator, or more exactly the portlet
**UICompanyNavigationPortlet** and its containers.

See the above `Left
Navigator <#PLFUserGuide.AdministeringeXoPlatform.BuildingOnlineCommunity.LeftNavigator>`__
for details.

Create a web content that gives the links to login and register, as
follows:

Click AdministrationContentSites Explorer. You can create the content
somewhere in a general drive, for example
``Sites Management:/intranet``.

Choose the template *Web Content*:

|image6|

Input title as "welcome" for example. Click **Source** (see the
screenshot) then put the following code to its content:

.. code:: html

    <table style="width: 100%">
        <tbody>
            <tr>
                <td style="width: 1px; white-space: nowrap">Please login if you have an account already:</td>
                <td><a class="btn btn-primary" href="/portal/login">Sign in</a></td>
            </tr>
            <tr>
                <td style="width: 1px; white-space: nowrap">Or register a new one:</td>
                <td><a class="btn btn-primary" href="/portal/intranet/Register">Register</a></td>
            </tr>
        </tbody>
    </table>

|image7|

Save and publish the content.

|image8|

Create a *Welcome* page. Take care to create the page in the same level
with the Home page.

Add the **Content Detail** portlet to the page. Edit the portlet to
select the content you created.

|image9|

Publish the portlet and the page.

Move up the *Welcome* page as described in `Site
Navigation <#PLFUserGuide.AdministeringeXoPlatform.BuildingOnlineCommunity.SiteNavigation>`__.
Also, make the page **invisible**.

Publish *Forum* page.

Publish *Wiki* page. As the Wiki Home is restricted by default, publish
it as well.

The following image shows the screen when an anonymous user accesses
*/portal*.

|image10|

.. |image0| image:: images/community/register_page.png
.. |image1| image:: images/community/site_navigation.png
.. |image2| image:: images/community/edit_node.png
.. |image3| image:: images/community/left_navigator.png
.. |image4| image:: images/community/publish_content.png
.. |image5| image:: images/community/publish_site.png
.. |image6| image:: images/community/select_template.png
.. |image7| image:: images/community/content.png
.. |image8| image:: images/community/ecms_publish.png
.. |image9| image:: images/community/select_content.png
.. |image10| image:: images/community/anonymous.png
