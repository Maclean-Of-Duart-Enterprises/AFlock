# AFlock
AFlock is an Android application based on Joshua Michael's flock camera research and work and updates based on his maps. All information is unconfirmed but based on the camera manufacturers records and OSMand Maps.

#AFlock
#AFlock is an independent, open-source Android application for viewing surveillance-camera records and using maps, saved records, and address information offline.

- Version: 1.3.0
- Package: "com.macleanofduartenterprises.AFlock"
- Android: 8.0 or newer
- License: MIT
- Developer: Maclean Of Duart Enterprises

Features

- Automatically loads the current Flock Surveillance camera dataset.
- Displays ALPR, camera/PTZ, audio, drone, Unique, and other records.
- Includes information and classifications from the Unique Cameras page.
- Searches camera names, types, operators, statuses, features, and identifiers.
- Caches camera data for offline use and falls back to saved data when the source is unavailable.
- Stores synchronized surveillance records for offline searching.
- Provides a bundled worldwide offline overview map.
- Supports downloadable MapLibre vector-map regions and incremental updates.
- Includes worldwide offline GeoNames place searching.
- Downloads detailed OpenStreetMap address packs for selected areas.
- Imports compatible osmdroid raster-map ZIP files.
- Provides device, light, and dark themes.
- Includes strict offline mode and map-storage management.
- Uses resilient OpenStreetMap Overpass access only as a supplementary source or fallback.

Camera and Map Sources

The primary Flock Surveillance map sources and camera information are provided by Joshua Michael:

- Main map: https://flocksurveillance.org/index.html
- Camera dataset: https://flocksurveillance.org/data/cameras.tsv
- Unique Cameras: https://flocksurveillance.org/unique.html

Additional sources include:

- OpenStreetMap: Supplementary camera records and detailed address information
  https://www.openstreetmap.org/copyright
- GeoNames: Bundled worldwide populated-place index
  https://www.geonames.org/
- Natural Earth: Bundled worldwide country overview
  https://www.naturalearthdata.com/

Each source retains its own license, attribution requirements, and terms.

Offline Operation

AFlock can retain camera records, maps, and address information on the device. The bundled worldwide overview and GeoNames place index work without a connection. Detailed vector regions and address packs must be downloaded before going offline.

Strict offline mode prevents MapLibre from requesting online map resources.

Privacy and Accuracy

AFlock does not require an account. Offline searches remain on the device, and Android backup and device-transfer extraction are disabled.

Camera records may be incomplete, outdated, generalized, duplicated, or inaccurate. Shared coordinates may represent approximate or placeholder locations and should not be treated as proof of an exact camera position.

AFlock is not affiliated with Flock Safety, flocksurveillance.org, Joshua Michael, OpenStreetMap, GeoNames, Natural Earth, or MapLibre.

Building

Requirements:

- JDK 17
- Android SDK Platform 35
- Android SDK Build Tools 35.0.0

Build and test with:

./gradlew clean testDebugUnitTest lintDebug assembleRelease

The unsigned APK will be created at:

app/build/outputs/apk/release/app-release-unsigned.apk

Sign releases with your own protected Android signing key. Never commit signing keys or passwords to the source repository.

License

AFlock source code is available under the MIT License. External libraries, maps, and datasets retain their respective licenses.
