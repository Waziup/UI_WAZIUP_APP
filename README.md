# UI_WAZIUP_APP

Web application comparing the data from the WAZIUP Weather Station with weather forecasts coming from multiple weather forecasting services.

 
To run the application on your own server first it must be cloned to your machine by using GitHub desktop, git clone command, etc. Currently, the application is configured by default to collect data gathered by the WAZIUP UI Weather station. So, for this application to work with another WAZIUP Weather Station, it is necessary to change the configuration under Data.js, by setting the following parameters:

-	location: Is the geographic location used by the forecast services.
"<Latitude>, <Longitude>" eg: "38.67,-9.2"

-	elasticsearchUrl: This is the url of the service which provides historic data of the WAZIUP Weather Station.
Eg: "http://elasticsearch.waziup.io/waziup-ui-weather/_search"

-	elasticsearchSearchQuery: The query string used on the request for historic data from the WAZIUP Weather Station.
Eg: "name:WeatherStationUI"

-	brokerUrl: URL of the WAZIUP Orion context broker which provides data of current Weather data from the station.
Eg: "http://broker.waziup.io/v2/entities/WeatherStationUI"

-	fiwareService: Service identifier of the WAZIUP Orion context broker.
Eg: "waziup"

-	fiwareServicePath: Service path of the WAZIUP Orion context broker.
Eg: "/UI/WEATHER"

After setting the configuration parameters the application must be compiled and then deployed usually by running the command "meteor build" under the src folder, other deployment options are also available and can be consulted at:

https://guide.meteor.com/deployment.html
