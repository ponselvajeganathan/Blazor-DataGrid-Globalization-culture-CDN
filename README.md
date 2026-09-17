# Blazor Server DataGrid Globalization with Culture Files Loaded from CDN

## Overview

This sample demonstrates how to localize a Syncfusion Blazor DataGrid in a Blazor Server application by loading culture resources from the server/CDN and applying a specific culture to the application. The project configures request localization using the `de-DE` culture and registers a custom implementation of `ISyncfusionStringLocalizer` to provide localized resource strings for Syncfusion components. This approach allows Grid UI elements such as filtering, sorting, paging, and other built-in text to be displayed using culture-specific translations.

## Key Features

- Uses the Syncfusion Blazor DataGrid component to demonstrate globalization and localization behavior.
- Registers Syncfusion services through `builder.Services.AddSyncfusionBlazor()`.
- Registers a custom localization provider using `builder.Services.AddSingleton(typeof(ISyncfusionStringLocalizer), typeof(SyncfusionLocalizer))`.
- Applies application-wide localization through `app.UseRequestLocalization("de-DE")`.
- Loads culture resources from server-side localization assets and applies localized messages within Syncfusion components.
- Demonstrates culture-based UI rendering for Grid interactions using externalized localization resources.

## Prerequisites

* Visual Studio 2022 or Visual Studio Code

## How to Run the Project

**Visual Studio 2022**

1. Checkout this repository to a local folder.
2. Open `BlazorServerGlobalziation.sln` in Visual Studio 2022.
3. Restore NuGet packages by building the solution.
4. Run the application.
5. Navigate to the page hosting the Syncfusion DataGrid example and observe the localized Grid UI generated using the configured culture resources.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open the integrated terminal.
3. Navigate to the project directory.

```bash
dotnet restore
dotnet run
```

## Project Structure

- `Pages/` — contains the Razor page that hosts the Syncfusion DataGrid globalization sample.
- `Program.cs` — registers Syncfusion Blazor services, configures `ISyncfusionStringLocalizer`, and applies the `de-DE` request localization culture.
- `Resources/` — contains localization resource files consumed by the custom localization implementation.
- `Data/` — contains sample data and supporting data-access classes used by the Grid sample.
- `Shared/SyncfusionLocalizer.cs` — custom implementation of `ISyncfusionStringLocalizer` used to supply localized Syncfusion component strings. 
- `wwwroot/` — stores static assets and culture-related resources used by the sample.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- For detailed globalization and localization guidance, see the Syncfusion Blazor DataGrid documentation: https://help.syncfusion.com/grid-sdk/blazor/data-grid/global-local

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.
