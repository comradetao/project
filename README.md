# ISS Project - CS50x

ISS Project represents the combined lessons of the CS50x online class and dozens, if not hundreds, of
hours of deep diving into Android development. This app shows users the current position, altitude and velocity
of the International Space Station (ISS). It also calculates the current great circle distance and straight
line distance to the ISS from a location that the user chooses though a Google Maps interface.

## How to use it?

Fire it right up and the app will start tracking the ISS using a background. To change the user's location, 
shown as "My Latitude" and "My Longitude" on the main activity, press the "Set My Location Using Google Maps"
button. When the map pops up, drag the marker to the location you choose, and then hit the back button. 
It's that simple.

## Who Provides the iSS Tracking Data?

Tracking data is provided through https://wheretheiss.at/w/developer.

## What Are These Distances Being Calculated?

The great circle distance is the shortest distance around the globe, assuming perfect sphericalness, and placing
the path at sea level, that it would take to reach from the user's selected location to the point directly below
the ISS. The calculations use the haversine formula.

The straight line distance is the distance of the line connecting the user's selected location, again at sea level, 
and the actual location of the ISS. The user's selected location and location of the ISS are converted to Cartesian coordinates
with the center of the earth at the origin. The calculation uses the Pythagorean theorem.

## Other Technical Details
The app tracks the ISS using a background service and funnels the data into Android LiveData so UI elements can
"observe" changes and update when the data updates. All of the data shown in the main activity si reformatted for
standardization and uses metric units. Latitude and Longitude are converted from decimal to degree, minute, second format.

## Special Thanks
Special thanks to Coding in Flow, CodingwithMitch, the gentle folk in StackOverflow, and the countless YouTubers
who struggle to keep their content up to date in the shifting sands of the Android environment.

## Future Hoped-for Features
3D wireframe model showing the user's position and the ISS position.
GPS tracking integrationfor the user's location, including altitude.
