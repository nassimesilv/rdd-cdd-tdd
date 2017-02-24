#Weather
Give temperature for a city and a measurement unity. An easy way to know if you should wear a jacket or a parka.  

##Install
```sh
$ npm install meow
$ npm install chalk
$ npm install update-notifier
$ npm install YQL
$ npm install lodash
```

##Usage
```sh
const meow = require('meow');

const cli = meow({
	help: [
		'Usage',
		'  $ weather <input>',
		'',
		'Options',
		'  city [Default: Dhaka]',
		'  country [Default: Bangladesh]',
		'  scale (C/F) [Default: Celcius]',
		'',
		'Examples',
		'  $ weather London UK C',
		'  London, UK',
		'  Condition: Partly Cloudy',
		'  Temperature: 32C'
	]
});

const chalk = require('chalk');

console.log(chalk.red(city + ', ' + country));
console.log(chalk.cyan('Condition: ' + chalk.yellow(condition)));
console.log(chalk.cyan('Temperature: ' + chalk.yellow(temperature)));

const updateNotifier = require('update-notifier');

updateNotifier({ pkg}).notify();

```

###Functions

```sh
function _toCelcius(temp) {
	return Math.round(((temp - 32) * 5) / 9);
}

const YQL = require('yql');

query = new YQL('select * from weather.forecast where woeid in (select woeid from geo.places(1) where text="Dhaka, Bangladesh")');

const _ = require('lodash');

if (_.isEmpty(opts))
```

Convert temperature from degrees to Celcius

```sh
weather(cli.input, (err, result))
```
The function weather update the weather in the console, return Dhaka Bangladesh if parameters are null
Parameters: City, unity


```sh
index(opts, callback)
```
Get the weather from the database
Parameters: void
Return: condition, temperature
