# Retrofit2Example

This is a sample project to show how to use Square Retrofit2 Library in your Android Apps.

## MainActivity
Main test activity. Preserves data and UX state on rotation of device.
Uses material design construct by having styles.xml and v21/styles.xml works with colors.xml
Handles device rotation well.
Pay attention to runOnUiThread runnable. It takes care of cases where 'runOnUiThread' may not update UX on roation as Activity may not have been recreated.
## GetWeatherApi
The API to access weather
### Async API: 
getWeatherFromApi, results are passed back to caller in a Callback on a different thread.
### Sync API: 
getWeatherFromApiSync, not called from a UX thread. Blocking call, places the call from a thread.
### GetWeatherRestAdapter: 
Defines the REST adapter and also a container for Weather API.
## Weather: 
is a plain old java object that mirrors names on the JSON response.
## Open issues: 
Did not check error issues. So app may crash on Retrofit errors.
Openweather now requires you to use their API. Set your own API key in OPEN_WEATHER_API (GetWeatherRestAdapter.java), I have kept mine in case you need to do few minor tests
