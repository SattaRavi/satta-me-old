---
date: 2016-11-20T23:16:17-07:00
paging: true
title: sharepoint hide ribbon
tags: ['sharepoint']
---

Came across a scenario where the SharePoint Ribbon needed to be hidden from users who were authenticated but only has **Read** permissions

Find and update the ribbon snippet on master page to reflect like something below.

{{< gist SattaRavi d648a5d7d2a6f68d544ef9711bf6f7a9 >}}

> To learn more on permissions
> https://msdn.microsoft.com/EN-US/library/ms412690