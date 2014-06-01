nodetsdb-client
===============

Library to obtain datapoints from OpenTSDB in JavaScript. Requiere jQuery to work. If you are looking for a NodeJS module, please look at [nodetsdb](https://www.npmjs.org/package/nodetsdb)

## Authors

* Roberto Martin

## Installation

Just link it in your HTML after jQuery

## Usage


```javascript
 var nodetsdb = new Nodetsdb({host:'opentsdbserver.com', port:4242});
 
 var queryconf = {start:'2013/04/04-12:00:00',end:'2013/04/18-15:46:17'
                , metric:'city.weather.temp', aggregator:'avg'
                , tags:{id:44640, quality:0}};
 
 nodetsdb.getDataPoints(queryconf, function(data){
	 		 if(datapoints){
				console.log(datapoints);
			 }else{
				console.log('No datapoints');
			 } 
  		});
```

## Release History

* 0.1.0 Initial release
