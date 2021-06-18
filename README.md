
# Weather-app-in-Java-Script


We need to fetch weather data from a weather forecasting the platform using APIs

After fetching data we need to extract our required information from that weather data e.g: weather_condition, temperature etc


## JavaScript code

In forecast.js first, you need to initialize your API key

After this we need to create two function getCity() and getWeather(). Using these functions we will fetch the city data and weather_condition of that city from AccuWeather

In getCity() and getWeather() we need to define two variables url and query.

In the above code, after setting the API key, URLs and Query we need to call the fetch() method and pass the rrl + query as an argument which makes a complete web address resource to access the data. The Fetch API accesses resources across the network. You can make HTTP requests (using GET, POST, and other methods), download, and upload files. fetch() starts a request and returns a promise. When the request completes, the promise is resolved with the Response object.

getCity() and getWeather() are asynchronous functions since they are marked with the async keyword. As fetch() return a promise so you have to wait for it to be resolved that's why we have marked it with an await keyword.
We are returning the 0-index of data return data[0] because when the promise becomes resolve it will return 2 types of data [0] and [1]. The most accurate one will always be the first one [0], so that's why we are returning [0]-index of data

In the end, we will get a response object in the JSON formate of city details from getCity() same is the case with getWeather() as they are returning promises we will deal with these promises in the app.js file.

this function is returning an object having city details and weather details.

because the async function always returns a promise so in the code below we are getting the name of the city from the user and passing the city name as an argument to updateCity() function and as we know updateCity() function will return a promise so we need to deal with that promise (if the promise is resolved 'then' what? and if it is not resolved 'catch' the error)

When the promise becomes resolved we have to update our user interface to show the details to the user.

So in the code, above we pass the resolved promise to the updateUI() function(which will update our User Interface)

In the updateUI() function we are simply first getting the sub details(e.g: Temperature, weather condition, etc) of city and weather details and rendering those details on the screen.
## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)

  
## Authors

- [@nitinkumar388](https://github.com/nitinkumar388)

  
## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

  
## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.

  
