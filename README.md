# weather-app

Weather app from The Odin Project. Gets data from openweathermap.org and displays the current weather.

NOTES: 
 - Enter a ZIP code, city name, or city and state (separated by a single comma) in the input box, then press the 'Get Weather' button.
 - Program flow: 
	After the 'Get Weather' button is pressed, the program will use string.split, then determine what input format was given based on the length of the array. It will also determine if a ZIP or City was entered by checking for a number in the [0] position of the array.
	The program uses that to make the appropriately formatted API call to openweathermap.org
	When the request comes back, it stores the unprocessed JSON file in localStorage then processes it out of localStorage, creating a new object with the relevant information from the JSON and storing the new object in a separate localStorage key.
	Using that new object, the current weather is displayed.
 - In order to get hourly/daily/map functionality from openweathermap, coordinates are required for the API call, which would require a geocaching API as well; all of the geocaching APIs I found were subscription based, so those functions will wait until a future date.

TODO:
 - Add functionality to the hourly forecast/daily outlook tabs, as well as a current weather radar map
 - Improve design; currently it is coded to distinguish parts of the flex layout
 - Module-ize the JavaScript; it is currently in one .js file. This isn't really a problem since the program only does one overall task (get current weather data for an input), but once the other two functions are coded in, it will be easier to run it from multiple files.
 - Better format the view for mobile devices
