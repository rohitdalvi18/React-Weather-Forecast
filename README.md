# React-Weather-Forecast

Weather application built with ReactJS. Dynamically recognizes user's location, based on browser's settings or IP. Weather can be searched both by location on the map or entering city in the search bar.

## Usage:

- Clone the repository

```sh
$ cd react-weather-app
$ npm i -d
$ touch .env
$ touch ./proxy/env.json
```

- Generate 2 API keys: one from
  [Google](https://developers.google.com/maps/documentation/javascript/get-api-key)
  and another from [Open Weather Map](https://openweathermap.org/api).
- Update .env file in the project root directory with the following:

> API_KEY_GOOGLE_GEOCODING = YOUR_GOOGLE_GEOCODING_API_KEY<br>
> API_KEY_GOOGLE_MAPS = YOUR_GOOGLE_MAPS_API_KEY<br>
> API_KEY_OW = YOUR_OPENWEATHERMAP_API_KEY

Two PHP proxies are used to access the Openweathermap and Google geocoding
services from the backend.

- Update ./proxy/env.json file with the following content (please note the
  quotes - they are required here, unlike in `.env`):

```sh
{
  "API_KEY_GOOGLE_GEOCODING" = "YOUR_GOOGLE_GEOCODING_API_KEY"
  "API_KEY_OW": "YOUR_OPENWEATHERMAP_API_KEY"
}
```

- Update ./proxy/.htaccess file to reflect your referring domain.

## Run your App:

```sh
$ npm run start
```

App will be accessible at `http://localhost:8080`

## Build your App:

```sh
$ npm run build:prod
```

- Open /build/index.html in your browser and, if everything works as intended,
- Upload contents of BUILD folder to your hosting provider.
