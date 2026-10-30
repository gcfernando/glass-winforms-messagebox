---
layout: default
title: "Glass.Message — Documentation and Guides"
description: "A modern Windows Forms MessageBox library with async dialogs, inputs, progress bars and toast notifications."
permalink: /documentation/
---

# Glass.Message Documentation

Find installation, WinForms dialog examples and the source contracts behind Glass.Message.

<a id="explore-more"></a>
<a id="markdown-source-library"></a>
<a id="read-online"></a>

## 🧭 Choose a guide

| Task | Guide |
|---|---|
| Add the library to a Windows Forms app | [Quick start](REFERENCE.md#-quick-start) and [installation](REFERENCE.md#-installation) |
| Migrate MessageBox calls safely | [Overview and argument ordering](REFERENCE.md#-the-one-line-pitch) |
| Use inputs, async dialogs, progress or toasts | [Usage guide](REFERENCE.md#-complete-usage-guide) and [API overview](REFERENCE.md#-api-overview) |
| Customize themes and defaults | [Configuration](REFERENCE.md#-configuration) and [styling](REFERENCE.md#-styling-and-customization) |
| Build and verify changes | [Development and testing](REFERENCE.md#-running-the-demo) and [project requirements](REFERENCE.md#-requirements) |
| Read the package-facing guide | [NuGet README](README.nuget.md) |
| Review historical release changes | [Changelog](CHANGELOG.md) |

## 🔗 Source references

[Public facade](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/Glass.Message/GlassMessage.cs) · [Fluent builder](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/Glass.Message/GlassBuilder.cs) · [Progress controller](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/Glass.Message/GlassProgressController.cs) · [Release workflow](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/.github/workflows/release.yml)

Dialog creation belongs on the WinForms UI thread. The progress controller supports marshaled worker updates; this does not make all dialog APIs callable from arbitrary threads.

## 🌐 Published documentation

This index is also rendered by the repository's GitHub Pages site. Relative links above point to the authored repository documents; package READMEs target NuGet readers and may use absolute GitHub links.

[Repository](https://github.com/gcfernando/glass-winforms-messagebox) · [Project overview](README.md)
