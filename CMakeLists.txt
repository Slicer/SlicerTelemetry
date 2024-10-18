cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(MyFirstExtension)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/Slicer/SlicerTelemetry")
set(EXTENSION_CATEGORY "Developer Tools")
set(EXTENSION_CONTRIBUTORS "Dominguez Bernardo")
set(EXTENSION_DESCRIPTION "This extension allows 3D Slicer extensions to gather information on what software features are used.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/Slicer/SlicerTelemetry/main/Telemetry.jpg")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/Slicer/SlicerTelemetry/main/Telemetry/Resources/Pictures/screenshotDialog1.png https://raw.githubusercontent.com/Slicer/SlicerTelemetry/main/Telemetry/Resources/Pictures/screenshotDialog2.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(MyFirstModule)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
