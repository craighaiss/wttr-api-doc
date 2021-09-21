---
title: Troubleshooting
tags: [troubleshooting]
keywords: troubleshooting
last_updated: Sep 21, 2021
summary: "How to troubleshoot issues that may occur when using the wttr.in API."
sidebar: mydoc_sidebar
permalink: troubleshooting.html
---

# Troubleshooting issues

The following issues may occur when using the wttr.in API.

## Non-valid characters in the output
Due to an issue with the current Windows 32-bit version of curl, output from the wttr.in API may include non-valid characters.

Until the issue is resolved by a future release of Windows, you can use one of the following workarounds.
- Instead of curl, use the `Invoke-Web-Request` command in Windows Powershell.

    ```
(Invoke-Web-Request http://wttr.in).Content
    ```

- Install the [Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install-win10) and use an alternate shell, such as bash.

## Missing or double-width diagonal wind direction characters
Some Windows terminal applications, such as conhost.exe, use double-width arrow glyphs. This results in either a missing character for certain wind directions, a broken table in the output, or both.

Other terminal applications that use double-width glyphs include ConEmu.exe, ConEmu64.exe, and terminal applications built on ConEmu, such as cmder.exe.

You can resolve this issue using one of the following workarounds.

- Use [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal-preview/9n0dx20hk701?activetab=pivot:overviewtab), which you can download for free from the Microsoft Store. If you still see issues after installing Windows Terminal, try maximizing the terminal window.

- Replace the diagonal wind direction characters in the response data with forward and back slashes prior to rendering the output, as shown below.

    ```
$w = (curl wttr.in -UserAgent curl).Content;
$formattedWeather = $w.Substring(0, $w.lastIndexOf($([char]0x2518)) + 1).replace($([char]0x2196), $([char]0x005C)).replace($([char]0x2197), $([char]0x002F)).replace($([char]0x2198), $([char]0x005C)).replace($([char]0x2199), $([char]0x002F));
    ```
