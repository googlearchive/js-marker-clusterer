**Please note:** This repository is not currently maintained, and is kept for historical purpose only.

Marker Clusterer – A Google Maps JavaScript API utility library
==============

A Google Maps JavaScript API v3 library to create and manage per-zoom-level clusters for large amounts of markers.
![Analytics](https://maps-ga-beacon.appspot.com/UA-12846745-20/js-marker-clusterer/readme?pixel)

[Reference documentation](https://googlemaps.github.io/js-marker-clusterer/docs/reference.html)

Migrated from the [Google Maps JavaScript API utility libraries on Google Code](https://code.google.com/p/google-maps-utility-library-v3/).

## Usage

Download or clone `markerclusterer.js` and images `m1.png` to `m5.png`, save images in `images` folder.

To use your own custom cluster images just name your images `m[1-5].png` or set the `imagePath` option to the location and name of your images like this: `imagePath: 'customImages/cat'` for images `cat1.png` to `cat5.png`.

index.html

    ...

    <div id="map-container"><div id="map"></div></div>
    <script src="markerclusterer.js"></script>
    <script>
        function initialize() {
            var center = new google.maps.LatLng(51.5074, 0.1278);

            var map = new google.maps.Map(document.getElementById('map'), {
              zoom: 3,
              center: center,
              mapTypeId: google.maps.MapTypeId.ROADMAP
            });

            var markers = [];
            var marker = new google.maps.Marker({
                position: new google.maps.LatLng(51.5074, 0.1278)
            });
            markers.push(marker);

            var options = {
                imagePath: 'images/m'
            };

            var markerCluster = new MarkerClusterer(map, markers, options);
        }

        google.maps.event.addDomListener(window, 'load', initialize);
    </script>
    ...
    

## Live Demos

[![Marker Clusterer Screenshot](https://googlemaps.github.io/js-marker-clusterer/screenshot.png)](https://googlemaps.github.io/js-marker-clusterer/docs/examples.html)

[Examples page](https://googlemaps.github.io/js-marker-clusterer/docs/examples.html)

## Contributing

Want to contribute? Check out the [contributing guide](CONTRIBUTING.md)!

## License

Copyright 2014 Google Inc. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
