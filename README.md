# VC Map

**Provided by:** [Virtual City Systems](https://vc.systems)

## Description

VC Map is an open-source JavaScript framework and API for building dynamic, interactive web maps. It displays 2D data, oblique imagery, and large 3D datasets, including terrain, vector data, mesh models, and point clouds. Users can switch between 2D, oblique, and 3D views and add map layers that are accessible across views.

Built on GIS and web technologies such as [OpenLayers](https://github.com/openlayers/openlayers) and [Cesium](https://github.com/cesiumGS/cesium/), VC Map supports data from multiple sources and formats, including open OGC standards and interfaces. It provides ready-to-use tools and widgets, and an API for building custom applications, embedding maps in web pages, and extending functionality with plugins.

VC Map applications can run in modern web browsers on desktop and mobile devices.

## Images

![VC Map component diagram](./documentation/VC_Map_Diagram.png)

## Installation Prerequisites

- Node.js and npm. The provided documentation does not specify minimum versions.
- A modern web browser to run the application.

## Installation Instructions

1. Clone the [VC Map UI repository](https://github.com/virtualcitySYSTEMS/map-ui).
2. Navigate to the repository directory and install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run start
   ```

4. Open [http://localhost:8080](http://localhost:8080) in a browser.

## Built Image Registry

Not specified in the provided documentation.

## License

This project is licensed under the MIT License.

Copyright (c) 2022 virtualcitySYSTEMS

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## External technical resources

- [VC Map Core (`@vcmap/core`)](https://github.com/virtualcitySYSTEMS/map-core)
- [VC Map UI (`@vcmap/ui`)](https://github.com/virtualcitySYSTEMS/map-ui)
- [VC Map Plugin CLI (`@vcmap/plugin-cli`)](https://github.com/virtualcitySYSTEMS/map-plugin-cli)
- [VC Map UI webpack 5 integration template](https://github.com/virtualcitySYSTEMS/map-ui-webpack5-example)
- [VC Map Core demo](https://github.com/virtualcitySYSTEMS/map-core-demo)
- [OpenLayers](https://github.com/openlayers/openlayers)
- [Cesium](https://github.com/cesiumGS/cesium/)

## User Guide References

- [Getting started](documentation/GET_STARTED.md)
- [Plugin CLI documentation](https://github.com/virtualcitySYSTEMS/map-plugin-cli)
- [API Story documentation](https://lib.virtualcitymap.de/ui/6.0/story/)

## Additional Information

### Architecture

VC Map consists of four main architectural layers:

- **VC Map Core:** A thin abstraction layer and wrapper around OpenLayers and Cesium. It provides common data and feature management and synchronizes data and user actions between 2D, oblique, and 3D views.
- **Configuration Management:** A flexible system for managing application content—such as layers, views, tools, and plugins—in JSON configuration files. Configurations can be changed, extended, and serialized at runtime through an API.
- **Modern User Interface:** UI components for map tools and widgets, implemented with Vue.js and HTML5, plus lower-level elements developers can use to build custom dialogs.
- **Plugin API:** An API for adding tools, functionality, and user dialogs. Plugins can be configured in an application or loaded dynamically, and can use the VC Map Core, configuration management, and UI components.

### Components

#### [`@vcmap/core`](https://github.com/virtualcitySYSTEMS/map-core)

Provides an abstraction layer for 2D, 3D, and oblique maps, including:

- Map abstractions for Cesium, OpenLayers, and oblique imagery.
- Layers.
- Interactions.
- Styles.
- Application, module, and configuration handling.

#### [`@vcmap/ui`](https://github.com/virtualcitySYSTEMS/map-ui)

Provides a configurable and extendable user interface. It extends the `@vcmap/core` application handling with a plugin concept and a `windowManager`.

#### [`@vcmap/plugin-cli`](https://github.com/virtualcitySYSTEMS/map-plugin-cli)

Provides tools to create, develop, and build plugins for `@vcmap/ui`. It also documents the plugin concept.

#### Additional examples

- [Webpack 5 integration template for `@vcmap/ui`](https://github.com/virtualcitySYSTEMS/map-ui-webpack5-example) — example integration in a webpack 5 project.
- [Demo application for `@vcmap/core`](https://github.com/virtualcitySYSTEMS/map-core-demo) — demonstrates implementing a different UI on top of the core.

### Project and component documentation

- Content tree API: [CONTENT_TREE](documentation/CONTENT_TREE.md)
- Window manager API: [WINDOWS](documentation/WINDOWS.md)
- Navbar, ButtonManager, and ToolboxManager: [BUTTONS](documentation/BUTTONS.md) and [TOOLBOX](documentation/TOOLBOX.md)
- Orientation tools.
- Action concept: [ACTIONS](documentation/ACTIONS.md)
- Plugin concept: [Plugin API](https://github.com/virtualcitySYSTEMS/map-plugin-cli)
- Search API: [SEARCH](documentation/SEARCH.md)
- I18n API: [INTERNATIONALIZATION](documentation/INTERNATIONALIZATION.md)
- Categories API: [CATEGORIES](documentation/CATEGORIES.md)
- Context menu API: [CONTEXT_MENU](documentation/CONTEXT_MENU.md)
- Feature info: [FEATURE_INFO](documentation/FEATURE_INFO.md)
- [State and application link](documentation/STATE.md)
- [Help concept](documentation/HELP.md)
- Copyright and attributions: [ATTRIBUTIONS](documentation/ATTRIBUTIONS.md)

### Release cycle and version management

- **Major releases:** Planned approximately annually and may include breaking changes. Major releases also incorporate the latest versions of Cesium and OpenLayers.
- **Patches and minor releases:** Planned approximately every two months. These may update OpenLayers and, where there are no breaking changes, Cesium.
- **Plugin compatibility:** Plugins designed for a major version are intended to work with its minor and patch releases.
- **Bug-fix support:** Provided for the current major version and the preceding major version.

### Roadmap

**Core**

- Clustering — priority 4.
- Style refactoring — priority 4.

**UI**

- Overlay API support.

### Plugins

The following public repositories in the [virtualcitySYSTEMS GitHub organization](https://github.com/virtualcitySYSTEMS) identify themselves as VC Map plugins. This list includes general-purpose and project-specific plugins; it does not indicate release status or maintenance level.

#### Map tools and navigation

- [Clipping Tool](https://github.com/virtualcitySYSTEMS/map-clipping-tool)
- [Create Link](https://github.com/virtualcitySYSTEMS/map-create-link)
- [Drawing](https://github.com/virtualcitySYSTEMS/map-draw)
- [Dynamic Layer](https://github.com/virtualcitySYSTEMS/map-dynamic-layer)
- [Event Control](https://github.com/virtualcitySYSTEMS/map-event-control)
- [Gamepad](https://github.com/virtualcitySYSTEMS/map-gamepad)
- [Geofence](https://github.com/virtualcitySYSTEMS/map-geofence)
- [Layer Settings](https://github.com/virtualcitySYSTEMS/map-layer-settings)
- [Layer Slider](https://github.com/virtualcitySYSTEMS/map-layer-slider)
- [Link Button](https://github.com/virtualcitySYSTEMS/map-link-button)
- [List View](https://github.com/virtualcitySYSTEMS/map-list-view)
- [Module Selector](https://github.com/virtualcitySYSTEMS/map-module-selector)
- [MultiView](https://github.com/virtualcitySYSTEMS/map-multi-view)
- [Panorama](https://github.com/virtualcitySYSTEMS/map-panorama)
- [Swipe Tool](https://github.com/virtualcitySYSTEMS/map-swipe-tool)
- [Walk Mode](https://github.com/virtualcitySYSTEMS/map-walk)

#### Analysis, visualization, and export

- [Cesium Filters](https://github.com/virtualcitySYSTEMS/map-cesium-filters)
- [Cesium Inspector](https://github.com/virtualcitySYSTEMS/map-cesium-inspector)
- [Export](https://github.com/virtualcitySYSTEMS/map-export)
- [Flight](https://github.com/virtualcitySYSTEMS/map-flight)
- [Height Profile](https://github.com/virtualcitySYSTEMS/map-heightprofile)
- [Line of Sight](https://github.com/virtualcitySYSTEMS/map-line-of-sight)
- [Measurement](https://github.com/virtualcitySYSTEMS/map-measurement)
- [Print](https://github.com/virtualcitySYSTEMS/map-print)
- [Shadow](https://github.com/virtualcitySYSTEMS/map-shadow)
- [Solar Balloon](https://github.com/virtualcitySYSTEMS/map-solar-balloon)
- [Solar Revenue](https://github.com/virtualcitySYSTEMS/map-solar-revenue)
- [Transparent Terrain](https://github.com/virtualcitySYSTEMS/map-transparent-terrain)
- [Viewshed](https://github.com/virtualcitySYSTEMS/map-viewshed)

#### Search, data, and domain plugins

- [Handwerker App](https://github.com/virtualcitySYSTEMS/map-handwerker-app)
- [KnowUrHeat](https://github.com/virtualcitySYSTEMS/map-knowurheat)
- [Search Coordinate](https://github.com/virtualcitySYSTEMS/map-search-coordinate)
- [Search Düsseldorf](https://github.com/virtualcitySYSTEMS/map-search-duesseldorf)
- [Search Esri](https://github.com/virtualcitySYSTEMS/map-search-esri)
- [Search Nominatim](https://github.com/virtualcitySYSTEMS/map-search-nominatim)
- [Search WFS](https://github.com/virtualcitySYSTEMS/map-search-wfs)
- [SensorThings](https://github.com/virtualcitySYSTEMS/map-sensorthings)
- [XPlan](https://github.com/virtualcitySYSTEMS/map-xplan)

### Included datasets

The datasets for Berlin and Osnabrück included in the project’s application configurations are for development use only. Contact [Virtual City Systems](https://vc.systems) for information about other uses.
