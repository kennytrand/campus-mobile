## now@ucsandiego.app

## License

	MIT

## Installation

	// From your project folder run:
	npm install

## Bugs

### Android
#### App crashing immediately after build?

Most likely being caused by the google-play version conflict between react-native-maps and react-native-google-analytics-bridge

Fix:

Open node_modules/react-native-maps/android/build.gradle

Update so file looks like this

	...
	dependencies {
		compile 'com.facebook.react:react-native:+'
		compile "com.google.android.gms:play-services-base:**+**"
		compile "com.google.android.gms:play-services-maps:**+**"
	}


## Building

### Android
[Lovely script](https://github.com/UCSD/now-mobile-build-scripts) made by @a6wu to make everything easier

	// From an empty directory
	//Build APK one liner:
	git clone https://github.com/UCSD/now-mobile-build-scripts.git && cd now-mobile-build-scripts && npm install && node build-apk.js

	//Build APK and install on device one liner:
	git clone https://github.com/UCSD/now-mobile-build-scripts.git && cd now-mobile-build-scripts && npm install && node build-apk.js && adb install ./bld/android/app/build/outputs/apk/app-release.apk

### Availabile Cards
* TopBanner
	* For upcoming current events
* Weather & Surf
	* 5 day weather report
	* Surf report link
* Shuttle
	* Nearest shuttle stops and arrival times
	* Shuttle stop info to view all shuttles en route
* Dining
	* Nearest dining options with menu and nutritional information
	* View all dining link
* Events
	* Upcoming events
	* View all events link
* Quick Links
	* A list of helpful links from our legacy app
	* View all quick links link
* News
	* Latest news articles
	* View all news link
* Maps
	* Searchable campus map
	* View all link

### Future
#### Cards
* Class Schedule
* Survey
* WebReg

#### Extra
* Functionality
	* Add/Remove Cards
	* Re-order cards
	* Push Notifications
	* 2-factor authentication
* Library
* Calendar
* Cape
* Chatbot
* Movie showtimes

#### Technical
* Tablet support
* SSO
* Personalization


### Screenshots
![Alt text](/../screenshots/screenshots/splash.png?raw=true "Splash Screen")

![Alt text](/../screenshots/screenshots/weather.png?raw=true "Weather")

![Alt text](/../screenshots/screenshots/events.png?raw=true "Events")

![Alt text](/../screenshots/screenshots/news.png?raw=true "News")

![Alt text](/../screenshots/screenshots/dining.png?raw=true "Dining")

![Alt text](/../screenshots/screenshots/nearby.png?raw=true "Nearby Places")

![Alt text](/../screenshots/screenshots/shuttle_detail.png?raw=true "Shuttle Detail")

![Alt text](/../screenshots/screenshots/all_events.png?raw=true "All Events")
