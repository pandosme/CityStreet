# CityStreet

This ACAP is based on [DetectX](https://github.com/pandosme/DetectX), an open-source package.  
The model is trained the dataset https://universe.roboflow.com/simone-bernabe/smart-city-pedestrian-bike-detection.  
Note that this ACAP is a proof-of-concept and has not been validated in a city environment.

![escooter](https://raw.githubusercontent.com/pandosme/CityStreet/main/pictures/escooter.jpg)

# Labels
- Cyclist
- E-scooter
- Person
- Vehicle

# Pre-requsite
- Axis Camera based on ARTPEC-8.

# User interface
The user interface is designed to validate detection and apply various filters.

## Detections
Detections is shown in video as bounding box and table.  The events are shown in a separate table and may be delayed depending on settings.

### Confidence
Initial filter to reduce the number of false detection. 

### Set Area of Intrest
Additional filter to reduce the number of false detection. Click button and use mouse to define an area that the center of the detection must be within.

### Set Minimum Size
Additional filter to reduce the number of false detection. Click button and use mouse to define a minimum width and height that the detection must have.

## Advanced
Additional filters to apply on the detection and output.

### Detection transition
A minumum time that the detection must be stable before an event is fired.  It define how trigger-happy the evant shall be.

### Min event state duration
The minumum event duration a detection may have.  

### Labels Processed
Enable or disable selected labels.

## Integration
The service fires two different events targeting different use cases.  Service may monitor these event using camera event syste, ONVIF event stream and MQTT.
## Label state
A stateful event (high/low) for each detected label.  The event includes property state (true/false).  

# History

### 3.2.0
- Initial commit

