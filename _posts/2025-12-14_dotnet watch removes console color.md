---
title: dotnet watch removes console color
date: 2025-12-14 18:00 +0100
categories: [DotNet, Shorts]
tags: [dotnet, .net, c#, bug, short]
image:
  path: /assets/img/consoleColorsWorking.png
  alt: console colors working
---

## The Problem

While developing a custom static site generator using Blazor I used `dotnet watch run` to run my generator and enable live reload of the generated pages.
This worked just as I wanted. When I started to improve the console output to be more helpful for the user, I used colored console output to highlight certain messages. I noticed that the colored messages were shown just fine when I ran the project using `dotnet run` but were missing using `dotnet watch run`.

![console colors working](/assets/img/consoleColorsWorking.png)
_Example with working colors_

![console colors not working](/assets/img/consoleColorsMissing.png)
_Example with missing colors_

## The solution

After a few failed attempts, I found a GitHub issue mentioning the same problem [link](https://github.com/dotnet/aspnetcore/issues/25317).

This seems to be a problem in `dotnet watch`, where the colors are not forwarded.
The best thing to fix the problem was to use `$env:DOTNET_SYSTEM_CONSOLE_ALLOW_ANSI_COLOR_REDIRECTION=1`.
