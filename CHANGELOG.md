# Changelog

## [0.3.0](https://github.com/visgl/react-google-maps/compare/v0.2.1...v0.3.0) (2023-11-09)


### ⚠ BREAKING CHANGES

* removed MapProps.onLoadMap

### Features

* cleanup map, remove onLoadMap prop ([d5e7dfd](https://github.com/visgl/react-google-maps/commit/d5e7dfdf74d76395ffbc1bcd2afda62a12eb7e57))
* implement props for all map-events with custom MapEvent type ([820a301](https://github.com/visgl/react-google-maps/commit/820a301e4a30e2b7bbbe7c82c69675f9c410813e))
* update map viewport when props are changed ([0b1d800](https://github.com/visgl/react-google-maps/commit/0b1d800dc5e4b9bf0b1ddb42b9fed392b23b8dae))

## [0.2.1](https://github.com/visgl/react-google-maps/compare/v0.2.0...v0.2.1) (2023-11-07)


### Bug Fixes

* add types to package exports ([#62](https://github.com/visgl/react-google-maps/issues/62)) ([1ab493a](https://github.com/visgl/react-google-maps/commit/1ab493a71ddaeff3b31caec10be1fd4728d51362))

## [0.2.0](https://github.com/visgl/react-google-maps/compare/v0.1.2...v0.2.0) (2023-11-07)


### Features

* new MapControl component ([#51](https://github.com/visgl/react-google-maps/issues/51)) ([7eb49ed](https://github.com/visgl/react-google-maps/commit/7eb49ed55eb548c342f83bcdbf9dc655655bafe7))
* standalone examples (CodeSandbox) ([#48](https://github.com/visgl/react-google-maps/issues/48)) ([959c6e3](https://github.com/visgl/react-google-maps/commit/959c6e3d57d896d4f76640e01b3ad0a33dea3fae))


### Bug Fixes

* replace prop `gmpDraggable` with `draggable` in AdvancedMarker ([#53](https://github.com/visgl/react-google-maps/issues/53)) ([1dbf477](https://github.com/visgl/react-google-maps/commit/1dbf477dfa2e471edf9a9daacd5e5e384a48d8de))
* update usage of useMapsLibrary in AdvancedMarker ([#55](https://github.com/visgl/react-google-maps/issues/55)) ([b01fc8b](https://github.com/visgl/react-google-maps/commit/b01fc8bbafae569fbb21a3175deb5b66762eb083))

## [0.1.2](https://github.com/visgl/react-google-maps/compare/v0.1.1...v0.1.2) (2023-11-01)


### Miscellaneous Chores

* add registry-url to release action ([9fa403b](https://github.com/visgl/react-google-maps/commit/9fa403bd4d6dfc31b84683543868b0bfbe70e2b9))

## [0.1.1](https://github.com/visgl/react-google-maps/compare/v0.1.0...v0.1.1) (2023-11-01)


### Bug Fixes

* empty commit to trigger release-please ([b04a942](https://github.com/visgl/react-google-maps/commit/b04a9421fc290c3ca6eacc02391726beab4bba4b))

## [0.1.0](https://github.com/visgl/react-google-maps/compare/v0.0.5...v0.1.0) (2023-10-27)


### ⚠ BREAKING CHANGES

* loading multiple libraries at once is no longer supported, changed the return type of useMapsLibrary.

### Features

* useMapsLibrary returns API object instead of boolean ([#26](https://github.com/visgl/react-google-maps/issues/26)) ([a3aa4c5](https://github.com/visgl/react-google-maps/commit/a3aa4c5e10228003206c8de3305f857df50d73d1))
