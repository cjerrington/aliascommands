---
layout: post
title: "Get-SystemUpTime"
categories: Powershell
tags: productivity
excerpt_separator: "<!--more-->"
---

{% highlight ruby %}
  function Get-SystemUptime{
    $operatingSystem = Get-WmiObject Win32_OperatingSystem
    [Management.ManagementDateTimeConverter]::ToDateTime($operatingSystem.LastBootUpTime)
  }
{% endhighlight %}

<!--more-->

In PowerShell you can get the system uptime of your computer. 

The output would be similar to: Monday, September 18, 2017 9:04:07 PM
