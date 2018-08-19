# generate-nice-timetables

The project contains a Jupyter Notebook to get the transit schedule between a given origin-destination pair on a given date from the Google Directions API.

## Requirements

In addition to installing the packages from `REQUIREMENTS.txt`, you should also get a Google API key for a project that has access both to the [Directions](https://developers.google.com/maps/documentation/directions/intro#TravelModes) and [Geocoding](https://developers.google.com/maps/documentation/geocoding/intro#ReverseGeocoding) API. We will use these to get the actual schedules and to determine which municipality the stops are located in. Visit [this page](https://console.cloud.google.com/getting-started) and read the documentation to get started.

## Usage
You should first set your Google API key in the envirorment (for example, in Terminal on a Mac, you could do this by `export GOOGLE_API_KEY="MY_API_KEY"`) before launching the notebook server. The notebook is commented and self contained so you can just run the whole thing.

## Contributing

Feel free to submit pull requests; help would be especially appreciated in turning this into a proper Python package and command line tool.

## Roadmap

Ideally, I would like to create a CLI tool that is submitted to PIP and generates the timetable in one line. For example, it could be used as
 
``` bash
transit_timetable \
	-o "Budapest, Hungary" \
	-d "Balatonhenye, Hungary" \
	-t 2018-10-20 \
	-k GOOGLE_API_KEY \
	-O timetable.html
```
