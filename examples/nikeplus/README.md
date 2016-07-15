# Nike+ Example

This is a sample Node.js project that pulls all valid activities from the Nike+ API and saves them as GPX files using the [GPS to GPX library](https://github.com/impatrickhooper/gps-to-gpx). Detailed documentation can be found as comments throughout the example code.

To download this example, first clone the repository:

```
git clone https://github.com/impatrickhooper/gps-to-gpx.git
```

To run this example successfully, you'll first need to grab a Nike+ API access token. See the comments in [this `constants.js` file](https://github.com/impatrickhooper/gps-to-gpx/blob/master/examples/nikeplus/src/constants.js) for more info. Once you've obtained and inserted your access token into the example code, run the following commands in sequence:

```
cd gps-to-gpx/examples/nikeplus
npm start
```

The program will run and output any relevant information (API errors or file I/O messages) to the console. When it's finished, you can find your GPX files in the `gps-to-gpx/examples/nikeplus/data` folder.

Since the Nike+ API does not include timestamps, the example saves GPX files in 2 ways: without time (in the `gps-to-gpx/examples/nikeplus/data/without-time` folder) and with estimated time (in the `gps-to-gpx/examples/nikeplus/data/with-estimated-time` folder). The estimated timestamps are very rough calculations based on the duration of the activity and number of waypoints. Please keep in mind this is just a quick example, so I wouldn't recommend using the estimated timestamps unless you're in a pinch. I have to imagine there are better ways (personally, I've successfully used [this tool from GOTOES](http://gotoes.org/strava/Add_Timestamps_To_GPX.php)).

To clean up any GPX files generated by the program, you can use:

```
npm run clean
```