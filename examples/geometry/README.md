# Geometry Example

![image](https://github.com/ArielBenichou/react-google-maps/assets/21100652/d32d7052-0ec0-4f2f-84a2-d31e6629dfa6)

This is an example to show how to setup a Google map with some geometry component, notably the `<Circle />`, `<Polygon />` and `<Polyline />` components.

## Usage

To use these components, you need to copy the components you want from the `src/components` folder into your project.

## Google Maps Platform API Key

This example does not come with an API key. Running the examples locally requires a valid API key for the Google Maps Platform.
See [the official documentation][get-api-key] on how to create and configure your own key.

The API key has to be provided via an environment variable `GOOGLE_MAPS_API_KEY`. This can be done by creating a
file named `.env` in the example directory with the following content:

```shell title=".env"
GOOGLE_MAPS_API_KEY="<YOUR API KEY HERE>"
```

If you are on the CodeSandbox playground you can also choose to [provide the API key like this](https://codesandbox.io/docs/learn/environment/secrets)

## Development

Go into the example-directory and run

```shell
npm install
```

To start the example with the local library run

```shell
npm run start-local
```

The regular `npm start` task is only used for the standalone versions of the example (CodeSandbox for example)

[get-api-key]: https://developers.google.com/maps/documentation/javascript/get-api-key

# Components Documentation

## `<Circle>` Component

React component to display a [Circle](https://developers.google.com/maps/documentation/javascript/shapes#circles) instance.

### Usage

```tsx
import React from 'react';
import {APIProvider, Map} from '@vis.gl/react-google-maps';
import {Circle} from './components/circle'; // import from your local file

const App = () => (
  <APIProvider apiKey={'Your API key here'}>
    <Map defaultZoom={8} defaultCenter={{lat: 53.54992, lng: 10.00678}}>
      <Circle center={{lat: 53.54992, lng: 10.00678}} radius={15000} />
    </Map>
  </APIProvider>
);
export default App;
```

### Props

The CircleProps interface extends the [google.maps.CircleOptions interface](https://developers.google.com/maps/documentation/javascript/reference/polygon#Circle) and includes all possible options available for a Circle. Additionally, it is possible to add different event listeners, e.g. the click event with the `onClick` property.

```tsx
interface CircleProps extends google.maps.CircleOptions {
  onClick?: (e: google.maps.MapMouseEvent) => void;
  onDrag?: (e: google.maps.MapMouseEvent) => void;
  onDragStart?: (e: google.maps.MapMouseEvent) => void;
  onDragEnd?: (e: google.maps.MapMouseEvent) => void;
  onMouseOver?: (e: google.maps.MapMouseEvent) => void;
  onMouseOut?: (e: google.maps.MapMouseEvent) => void;
  onRadiusChanged?: (r: ReturnType<google.maps.Circle['getRadius']>) => void;
  onCenterChanged?: (p: ReturnType<google.maps.Circle['getCenter']>) => void;
}
```

To see a Circle on the Map, the `center` and `radius` properties needs to be set.

## `<Polygon>` Component

React component to display a [Polygon](https://developers.google.com/maps/documentation/javascript/shapes#circles) instance.

### Usage

```tsx
import React from 'react';
import {APIProvider, Map} from '@vis.gl/react-google-maps';
import {Polygon} from './components/polygon'; // import from your local file

const App = () => (
  <APIProvider apiKey={'Your API key here'}>
    <Map defaultZoom={5} defaultCenter={{lat: 24, lng: -72}}>
      {/* Draw the Bermuda triangle */}
      <Polygon
        paths={[
          {lat: 25.774, lng: -80.19},
          {lat: 18.466, lng: -66.118},
          {lat: 32.321, lng: -64.757}
        ]}
      />

      {/* Draw the Bermuda triangle with an encoded path */}
      <Polygon encodedPaths={['o~h|CnbmhN~irk@_m{tAw`qsAgyhG']} />
    </Map>
  </APIProvider>
);
export default App;
```

### Props

The PolygonProps interface extends the [google.maps.PolygonOptions interface](https://developers.google.com/maps/documentation/javascript/reference/polygon#Polygon) and includes all possible options available for a Polygon. Additionally, it is possible to add different event listeners, e.g. the click event with the `onClick` property.

```tsx
interface PolygonProps extends google.maps.PolygonOptions {
  onClick?: (e: google.maps.MapMouseEvent) => void;
  onDrag?: (e: google.maps.MapMouseEvent) => void;
  onDragStart?: (e: google.maps.MapMouseEvent) => void;
  onDragEnd?: (e: google.maps.MapMouseEvent) => void;
  onMouseOver?: (e: google.maps.MapMouseEvent) => void;
  onMouseOut?: (e: google.maps.MapMouseEvent) => void;
  encodedPaths?: string[];
}
```

To see a Polygon on the Map, the `paths` or `encodedPaths` properties needs to be set.

## `<Polyline>` Component

React component to display a [Polyline](https://developers.google.com/maps/documentation/javascript/shapes#circles) instance.

### Usage

```tsx
import React from 'react';
import {APIProvider, Map} from '@vis.gl/react-google-maps';
import {Polyline} from './components/polyline'; // import from your local file

const App = () => (
  <APIProvider apiKey={'Your API key here'}>
    <Map defaultZoom={5} defaultCenter={{lat: 24, lng: -72}}>
      {/* Draw the Bermuda triangle */}
      <Polyline
        path={[
          {lat: 25.774, lng: -80.19},
          {lat: 18.466, lng: -66.118},
          {lat: 32.321, lng: -64.757}
        ]}
      />

      {/* Draw the Bermuda triangle with an encoded path */}
      <Polyline encodedPath={'o~h|CnbmhN~irk@_m{tAw`qsAgyhG'} />
    </Map>
  </APIProvider>
);
export default App;
```

### Props

The PolylineProps interface extends the [google.maps.PolylineOptions interface](https://developers.google.com/maps/documentation/javascript/reference/polyline#Polyline) and includes all possible options available for a Polyline. Additionally, it is possible to add different event listeners, e.g. the click event with the `onClick` property.

```tsx
interface PolylineProps extends google.maps.PolylineOptions {
  onClick?: (e: google.maps.MapMouseEvent) => void;
  onDrag?: (e: google.maps.MapMouseEvent) => void;
  onDragStart?: (e: google.maps.MapMouseEvent) => void;
  onDragEnd?: (e: google.maps.MapMouseEvent) => void;
  onMouseOver?: (e: google.maps.MapMouseEvent) => void;
  onMouseOut?: (e: google.maps.MapMouseEvent) => void;
  encodedPath?: string;
}
```

To see a Polyline on the Map, the `path` or `encodedPath` properties needs to be set.
