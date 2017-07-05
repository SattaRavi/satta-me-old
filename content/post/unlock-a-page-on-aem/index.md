---
date: 2016-11-11T23:16:39-07:00
paging: true
title: unlock a page on aem
tags: ['aem', 'wcms']
---

Today I had the opportunity to play with Adobe Experience Manager to perform some mundane tasks. This was my first encounter with AEM. While exploring the Granite UI to edit pages, i accidentally locked a page which hid few menus items.

{{< figure src="1.png" >}}

changed to

{{< figure src="2.png" >}}

The unlock menu disappeared from menu as well

To unlock the page, navigate to ```url:port/crx/explorer/``` to open up the content repository

{{< figure src="3.png" >}}

Login and then click on the Content Explorer menu.

Now navigate to the page that got locked and open up the node to reveal the ```jcr:content``` node.

Right-click on the ```jcr:content``` node to unlock the page

{{< figure src="4.png" >}}

> **Note:**
> Only the original user and the account admin has the privilege to unlock a locked page.

> [source](https://helpx.adobe.com/experience-manager/kb/UnlockALockedPage.html)
