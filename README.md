# JavaFX Maps Package  

## Overview  
This package provides powerful map integration for JavaFX applications, allowing developers to select map providers, customize controls, and dynamically manage elements such as markers, polygons, and other shapes. It also supports event tracking and real-time updates, giving full control over map objects during runtime.

---

## Features  

### 1. Multiple Map Providers  
You can choose from several popular map providers:  
- **OpenStreetMap**  
- **Google Maps**  
- **Google Satellite**  
- **Google Hybrid**  
- **Google Terrain**  
- **MapTiler Satellite**  
- **Mapbox Satellite v9**  



---

### 2. Custom Control Panel  
A **custom control panel** allows developers to manage map-related user actions and dynamically adjust map behavior.

#### Control Panel Capabilities  
- Show or hide zoom buttons  
- Enable/disable drawing tools  
- Switch between map providers  

### 3. Interactive Map Shapes  
The package allows adding and manipulating shapes dynamically during the application’s runtime. Supported shapes include:  
- **Markers**: Pins or icons at specific locations  
- **Polygons**: Multi-point areas  
- **Circles**: Defined by center and radius  
- **Polylines**: Lines connecting multiple points  

### 4. Event Tracking  
Developers can track actions such as adding, updating, or deleting items on the map. You can also listen for user interactions like mouse clicks or shape updates.

### 5. Real-time Object Control  
Modify the properties of map objects during runtime, such as updating the location or changing icons.

#### Usage Example  


## Usage Scenarios  
1. **Real-time Tracking:** Track moving objects by updating marker positions in real time.  
2. **Custom Drawing Tools:** Allow users to draw zones, routes, or other shapes on the map.  
3. **Dynamic Provider Switching:** Switch between different map providers based on context (e.g., terrain vs satellite view).

---

## API Summary  

### Classes  
- **`MapView`**: Core class representing the map.  
- **`ControlPanel`**: Customizable control panel.  
- **`Marker`**: Represents a marker on the map.  
- **`Polygon`**: Represents a polygon with multiple vertices.  
- **`Circle`**: Represents a circle with a center and radius.  
- **`Polyline`**: Represents a connected series of points forming a line.  

### Key Methods  
| Method                           | Description                                      |
|----------------------------------|--------------------------------------------------|
| `setProvider(MapProvider)`       | Set the map provider (e.g., Google, OpenStreetMap). |
| `addMarker(Marker)`              | Add a marker to the map.                         |
| `addPolygon(Polygon)`            | Add a polygon to the map.                        |
| `setOnMarkerAdded(Consumer<Marker>)` | Track marker addition events.             |
| `setOnShapeUpdated(Consumer<Shape>)` | Track shape updates.                     |

---

## Installation  
1. **Add the library to your project dependencies.**  
2. **Ensure your project includes JavaFX** and any necessary map provider APIs (e.g., Google Maps API).  
3. **Initialize the map in your application:**
   ```java
   WakebMapView view = new WakebMapView(MapProvider.GOOGLE, 7, 24.774265, 46.738586, bp);
   view.addControlLayer(Color.DARKCYAN, Orientation.HORIZONTAL,"marker.png");
   ```

---

## Conclusion  
This JavaFX Maps package provides developers with a comprehensive toolkit to create interactive, feature-rich map applications. It supports multiple providers, customizable controls, event tracking, and real-time updates, making it suitable for use cases such as real-time tracking, route planning, and location-based services.
