# GPS Location Visualization

This project visualizes GPS location data collected from an IoT GPS sensor
using Azure Maps.

## Architecture

CounterFit GPS
→ Azure IoT Hub
→ Azure Function
→ Azure Blob Storage
→ Azure Maps

## Technologies

- CounterFit
- Azure IoT Hub
- Azure Functions
- Azure Blob Storage
- Azure Maps
- HTML
- JavaScript

## GPS Data

GPS data is stored in the `gps-data` Blob Storage container.

The web application retrieves the stored GPS data and displays the
recorded locations as points on an Azure Maps map.

## Visualization

The application uses Azure Maps Web SDK and GeoJSON points.

GPS coordinates are converted to the GeoJSON format:

longitude, latitude

## Deployment

This application is deployed using Azure Static Web Apps.

The Azure Maps subscription key is stored as a GitHub Actions
repository secret (`AZURE_MAPS_KEY`) and injected during deployment.
It is not stored directly in the source code.