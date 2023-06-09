# MMM-NextTrains
A MagicMirror module that displays when Sydney trains depart from a selected station, using raw GTFS data provided by the [NSW Transport API](https://opendata.transport.nsw.gov.au/).


## Dependencies
  * A [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror) installation


## Examples
![name-of-you-image](/screenshots/screenshot1.png)


## Installation

### Linux 
  1. Clone this repository into your MagicMirror/modules directory.
  2. ```sudo apt-get install libsqlite3-dev```
  3. cd into MagicMirror/modules/NextTrains directory folder
  4. ```npm install sqlite3 --build-from-source --sqlite=/usr```
  5. ```sudo apt-get install sqlite3```
  6. Create an account on [Transport NSW OpenData](https://opendata.transport.nsw.gov.au/)
  7. Create an application and obtain an API key from [Transport NSW OpenData Applications](https://opendata.transport.nsw.gov.au/applications)
  8. Make a copy of the sample server config file ```cp ./server.conf.sample ./server.conf```
  9. Replace <YOUR_API_KEY_HERE> in `server.conf` with your api key
  10. Insert the example configurations into your MagicMirror config file
  
### Windows
- No Windows version available yet
  
  
 ## Config
 
 ### Example configurations for config.js:
```
{
	module: 'NextTrains',
	position: 'bottom_right',
	config: {
			station: "Central Station",
			maxTrains: 10
		}
}
```

### Config Options
| **Option** | **Description** |
| --- | --- |
| `station` | The name of the Sydney train station to monitor e.g. "Central Station" or "North Sydney Station"|
| `staticInterval` | How often the widget should refresh it's static data (in seconds), default is `1800`. |
| `realTimeInterval` | How often the widget should refresh it's realtime data (in seconds), default is `10`. |
| `maxTrains` | The maximum number of trains to display at a time, default is `10` |
| `delaysFormat` | Either `m`, `s` or `m:s` Determines what format to display delays in, default is `m` |
| `lateCriticalLimit` | After how many seconds to highlight a delay as critically late (red text), default is `600` |
| `etd` | Estimated time of departure - show departure time in time format, default is `false` |

---


<a href="https://www.buymeacoffee.com/CptMeetKat" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>
