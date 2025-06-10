# Telemetry extension for 3D Slicer

This extension allows 3D Slicer extensions to gather information on what software features are used.
This information helps demonstrating impact, which is essential for getting continuous funding for maintenance and improvements.
Knowing what modules and features are used also help developers decide what parts of the software they should focus their developer efforts on.

## What information is collected

The extension only counts how many times a certain features is used, when (which day), approximate where (which city).
Individual users are not attempted to be identified in any way: all data is aggregated, no information is stored per user. Usage statistics data will be available similarly to Slicer download statistics.

## How to disable data collection

3D Slicer core (content of the installation package downloaded from download.slicer.org) does not contain any code for collecting or sending software usage statistics.
If a user does not install the Telemetry extension then data cannot be collected.
If an extension wants to collect such data then it has to ask the user to install the Telemetry extension and enable usage data collection.
![screenshotExtensionPermissions](https://raw.githubusercontent.com/BerDom-Ing/SlicerTelemetry/refs/heads/main/Telemetry/Resources/Pictures/screenshotExtensionPermissions.png)

## How developers should use it

To record usage events in your extension, add the following line in your code, replacing `"component"` with your extension name and `"event"` with the event you want to record:

slicer.app.logUsageEvent("component", "event")

## Any concerns or questions?

Please report any concerns or questions at the [Slicer Forum](https://discourse.slicer.org/t/should-we-start-collecting-software-usage-data/30873/81).
