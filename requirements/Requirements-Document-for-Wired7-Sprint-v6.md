# Allow users to find the rocket launch site closest to their location

### Description
Now that travel to Mars is possible, people from all over the world want a ticket to space.  This feature will allow users to find the nearest launch site to their current location.

### Requirements

- Prompt user for location access on "launch sites near me" button press.  Button should be in the center (vertical and horizontal) of the view. There's an ember plugin called ember-cli-geo (https://github.com/igorpreston/ember-cli-geo) that should offer html5 geolocation out of the box.  This won't work in older browsers but we can handle that scenario later.

- Send location to backend (currently non-existent) via GET request: /location?lat={LATITUDE}&lon={LONGITUDE}

- Coordinates and city name for 20 launch site cities around the world (your choice) should be populated in a mysql database through a migration.

- The backend should return the nearest city name and its distance from the user's current location ({:city => city_name, :distance => 300 miles})

- Backend API framework: Sinatra (http://www.sinatrarb.com/)

- ORM: Sinatra ActiveRecord (https://github.com/janko-m/sinatra-activerecord)
