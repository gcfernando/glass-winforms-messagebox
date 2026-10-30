# Glass.Message

Themed Windows Forms dialogs, inline input, progress windows and toast notifications for C# desktop applications.

## Overview

Glass.Message provides message dialogs returning `DialogResult`, a fluent builder, rich input results, async dialogs, progress controllers and toasts. It targets `net481`, `net8.0-windows`, `net9.0-windows` and `net10.0-windows` and runs on Windows.

## Install

From your Windows Forms application directory:

```powershell
dotnet add package Glass.Message
```

## Quick start

Call from your application's UI (STA) thread:

```csharp
using Glass;
using System.Windows.Forms;

DialogResult result = GlassMessage.Show(
    "Save your changes?", "Unsaved changes",
    MessageBoxIcon.Question, MessageBoxButtons.YesNoCancel);
```

Glass takes the icon **before** the buttons. Check overload signatures when migrating a `MessageBox.Show` call.

## Usage and configuration

```csharp
var result = GlassMessage.Create("Enter a display name.")
    .Title("Profile")
    .InputText("Name")
    .Buttons("Save", "Cancel")
    .ShowEx();

if (result.Button == DialogResult.OK)
{
    string name = result.InputText;
}
```

Use `ShowEx`/`ShowExAsync` to obtain input and checkbox state. Two custom labels return OK/Cancel; three return Yes/No/Cancel. Async methods are awaitable and non-blocking but still require the UI thread.

Set `GlassMessage.DefaultTheme = GlassTheme.AutoDetect()` at startup to choose the current Windows theme. This selects a preset when called; refresh it from your application's theme-change handling when needed. Built-in presets are shared mutable objects. Keep custom themes alive while their dialogs are open. Mica/Acrylic and rounded-corner effects depend on the Windows version and settings.

## Documentation and development

The [repository guide](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/README.md) covers source builds, tests, support and signing. The [full reference](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/REFERENCE.md) includes progress-controller recipes, theme customization, screenshots, async cancellation, accessibility and API signatures. See the [changelog](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/CHANGELOG.md) for version history.

Source builds require the selected SDK and Windows targeting packs. UI/stress tests require a Windows desktop session. Optional developer signing can be skipped when no certificate is configured; a successful build does not imply signed binaries.

## Support and license

Use [issues](https://github.com/gcfernando/glass-winforms-messagebox/issues) for reproducible bugs and the [security policy](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/SECURITY.md) for private vulnerability reports. MIT, copyright Gehan Fernando; see the [license](https://github.com/gcfernando/glass-winforms-messagebox/blob/main/LICENSE).
