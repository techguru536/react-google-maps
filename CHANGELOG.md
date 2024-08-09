# Changelog

## 1.0.0 (2024-08-09)


### ⚠ BREAKING CHANGES

* **map:** Introduction of map instance caching needed a change to the DOM-Structure produced by the map component (added a div-element owned by the Map component to contain the map instance).
* **map:** The type passed to the `onProjectionChange` is changed from `MapCameraChangedEvent` to `MapEvent`, so there are no longer camera-props available for this event
* removed the `useStreetViewPanorama()` and `useDirectionsService()` hooks.
* The behaviour of the props controlling camera parameters (center, zoom, heading and tilt) changed. Unless you are using controlled props, you have to change the prop names from e.g. `center` to `defaultCenter` (the same goes for `zoom`, `heading` and `tilt`).
* removed MapProps.onLoadMap
* loading multiple libraries at once is no longer supported, changed the return type of useMapsLibrary.

### Features

* add example for drawing tools ([#220](https://github.com/techguru536/react-google-maps/issues/220)) ([e230977](https://github.com/techguru536/react-google-maps/commit/e2309779e28fff09ed32ac2c2959564e196eaa4f))
* add new prop InfoWindow.shouldFocus ([#254](https://github.com/techguru536/react-google-maps/issues/254)) ([07a03f6](https://github.com/techguru536/react-google-maps/commit/07a03f639371959fd7fc3c6cf222f81fe81c089d))
* add solution-channel parameter ([#334](https://github.com/techguru536/react-google-maps/issues/334)) ([e0da181](https://github.com/techguru536/react-google-maps/commit/e0da1813a3018a6378efc88a611495da1594f926))
* **advanced-marker:** add style prop to add styles to content-element ([#337](https://github.com/techguru536/react-google-maps/issues/337)) ([0bd3c7f](https://github.com/techguru536/react-google-maps/commit/0bd3c7f785ef984a168fda18c3b3436009e33517))
* **advanced-marker:** add support for `clickable` option ([#341](https://github.com/techguru536/react-google-maps/issues/341)) ([7617107](https://github.com/techguru536/react-google-maps/commit/76171078fa75e53b9d330d35fc4ed0f970b467c6))
* Allow &lt;Pin&gt; glyphs to be passed as children (close [#98](https://github.com/techguru536/react-google-maps/issues/98)) ([#99](https://github.com/techguru536/react-google-maps/issues/99)) ([eb0f41b](https://github.com/techguru536/react-google-maps/commit/eb0f41be1c92abe99e7a9c1468fb9a5c75de0997))
* better handling for missing map configuration ([#308](https://github.com/techguru536/react-google-maps/issues/308)) ([61646ae](https://github.com/techguru536/react-google-maps/commit/61646aef91c440b5698852ff1c4d0344a585359b))
* cleanup map, remove onLoadMap prop ([3fee940](https://github.com/techguru536/react-google-maps/commit/3fee940ee0c455eebd83e5719945b962a9a7f68f))
* handle API-key errors in map-component ([#165](https://github.com/techguru536/react-google-maps/issues/165)) ([c620dcb](https://github.com/techguru536/react-google-maps/commit/c620dcbd16cda284ff0f9df96038869feec91513))
* implement dynamic library loading ([5280114](https://github.com/techguru536/react-google-maps/commit/52801147ea68700c7122a96853e168ea28d878d2))
* implement props for all map-events with custom MapEvent type ([c56b8b3](https://github.com/techguru536/react-google-maps/commit/c56b8b3fd9459f40b0fcd3b5f551f42033ab98c8))
* **infowindow:** add `className` and `style` props ([9951871](https://github.com/techguru536/react-google-maps/commit/9951871ad062896a4f69a22e21d825d8fb139c43))
* **infowindow:** add missing options and events ([9951871](https://github.com/techguru536/react-google-maps/commit/9951871ad062896a4f69a22e21d825d8fb139c43))
* **infowindow:** InfoWindow overhaul ([#335](https://github.com/techguru536/react-google-maps/issues/335)) ([9951871](https://github.com/techguru536/react-google-maps/commit/9951871ad062896a4f69a22e21d825d8fb139c43))
* **map:** implement initial version of map-instance caching ([#349](https://github.com/techguru536/react-google-maps/issues/349)) ([62ab005](https://github.com/techguru536/react-google-maps/commit/62ab0059344f010ab22ef1e4496da1c94b20a16f))
* new MapControl component ([#51](https://github.com/techguru536/react-google-maps/issues/51)) ([8c83d3b](https://github.com/techguru536/react-google-maps/commit/8c83d3b3ca68647067314d7e06560f7632581ccc))
* restore map state when changing mapId ([#213](https://github.com/techguru536/react-google-maps/issues/213)) ([33f1924](https://github.com/techguru536/react-google-maps/commit/33f192415340df22e4c44fc18d8bd554ec619b2f))
* standalone examples (CodeSandbox) ([#48](https://github.com/techguru536/react-google-maps/issues/48)) ([a8d9812](https://github.com/techguru536/react-google-maps/commit/a8d9812df3f4ca6974fa78752dce71ade44f0cd0))
* update map viewport when props are changed ([23d3907](https://github.com/techguru536/react-google-maps/commit/23d3907ea3ae89ea2974e926b97a744d46e77035))
* useMapsLibrary returns API object instead of boolean ([#26](https://github.com/techguru536/react-google-maps/issues/26)) ([23691fa](https://github.com/techguru536/react-google-maps/commit/23691faac3dc23f54dfb15fbf83b84634671a6da))


### Bug Fixes

* add `loading=async` to maps API url ([c514894](https://github.com/techguru536/react-google-maps/commit/c514894e04739f0aa6478b442d9fbc71e7753397))
* add map camera state tracking ([#84](https://github.com/techguru536/react-google-maps/issues/84)) ([a844c8a](https://github.com/techguru536/react-google-maps/commit/a844c8acb96aeef238304df0eb15738c645ec0d0))
* add types to package exports ([#62](https://github.com/techguru536/react-google-maps/issues/62)) ([9960daf](https://github.com/techguru536/react-google-maps/commit/9960dafb171266c7b1383c28f83f35fec69f23d7))
* **advanced-marker:** remove content element in cleanup ([#351](https://github.com/techguru536/react-google-maps/issues/351)) ([b7ac2b3](https://github.com/techguru536/react-google-maps/commit/b7ac2b3a4172e2173333f94c3cc1d227c21d92f8))
* allow AdvancedMarker to accept space-separated multiple class names ([#143](https://github.com/techguru536/react-google-maps/issues/143)) ([dd2e7f2](https://github.com/techguru536/react-google-maps/commit/dd2e7f294b3db9cb770496a1f00944eed0d1c715))
* api-loader didn't call callback on repeat load calls ([46d7318](https://github.com/techguru536/react-google-maps/commit/46d7318f9735fcf761f555c6295bade1dd513bfd))
* avoid re-render on every importLibrary() call ([#135](https://github.com/techguru536/react-google-maps/issues/135)) ([5fa57b4](https://github.com/techguru536/react-google-maps/commit/5fa57b4462016ec3d12eba142c7b37a87677e109))
* **docs:** use correct spelling of JavaScript ([#312](https://github.com/techguru536/react-google-maps/issues/312)) ([ef5a37f](https://github.com/techguru536/react-google-maps/commit/ef5a37fe88f522a84eefb0666657f6e3885b3953))
* don't use potentially unreliable addListener functions ([#158](https://github.com/techguru536/react-google-maps/issues/158)) ([d541d2e](https://github.com/techguru536/react-google-maps/commit/d541d2e9967d874b44efad9ef3f1a3421e89d835))
* empty commit to trigger release-please ([aca2b4b](https://github.com/techguru536/react-google-maps/commit/aca2b4b094d8e4ed91b085b2289b6c85e47cbce7))
* export api-loading-status types ([#231](https://github.com/techguru536/react-google-maps/issues/231)) ([5b1fb62](https://github.com/techguru536/react-google-maps/commit/5b1fb62353b06d7302799250416538bb7aedf28c)), closes [#230](https://github.com/techguru536/react-google-maps/issues/230)
* export event-types ([#167](https://github.com/techguru536/react-google-maps/issues/167)) ([376fde1](https://github.com/techguru536/react-google-maps/commit/376fde1ecddfaf8538071f466594d7cc971a9fec))
* export type properly ([#170](https://github.com/techguru536/react-google-maps/issues/170)) ([661dd49](https://github.com/techguru536/react-google-maps/commit/661dd495d70974aee3f548934402715290d55832))
* infowindow double rendering and eslint warnings ([#185](https://github.com/techguru536/react-google-maps/issues/185)) ([6d885da](https://github.com/techguru536/react-google-maps/commit/6d885dae3c5fd6e2221fd197ff7e4d146b144887))
* InfoWindow.shouldFocus doesn't work with false as value ([#278](https://github.com/techguru536/react-google-maps/issues/278)) ([1091c94](https://github.com/techguru536/react-google-maps/commit/1091c94193582de66ac04cdf49dd447e292f977b))
* **infowindow:** add missing cleanup for infowindow ([9951871](https://github.com/techguru536/react-google-maps/commit/9951871ad062896a4f69a22e21d825d8fb139c43))
* **infowindow:** better dependency checks, using `useDeepCompareEffect` where needed ([9951871](https://github.com/techguru536/react-google-maps/commit/9951871ad062896a4f69a22e21d825d8fb139c43))
* **infowindow:** removed unneeded dependency in infowindow hooks ([9951871](https://github.com/techguru536/react-google-maps/commit/9951871ad062896a4f69a22e21d825d8fb139c43))
* map controls crashing when invalid key is provided ([#290](https://github.com/techguru536/react-google-maps/issues/290)) ([1589712](https://github.com/techguru536/react-google-maps/commit/1589712cbfc537cb40c73b877281382879d5cb21))
* **map:** (un)register map instance without id ([8e0162b](https://github.com/techguru536/react-google-maps/commit/8e0162b8748c508f4f6e8ac213f511265651dcc8))
* **map:** change event-type of projectionChanged event to MapEvent ([#346](https://github.com/techguru536/react-google-maps/issues/346)) ([5160d56](https://github.com/techguru536/react-google-maps/commit/5160d56562d9696687c46848662dddb69e03882d))
* **map:** fix changing the map-id ([aa59203](https://github.com/techguru536/react-google-maps/commit/aa5920391e75691274314db683cdc51c4fb4e9b9))
* **map:** set container position to relative ([#356](https://github.com/techguru536/react-google-maps/issues/356)) ([03493ac](https://github.com/techguru536/react-google-maps/commit/03493ac8c1cebf494f1c718a908be26731405515))
* **map:** set other container position to relative ([#357](https://github.com/techguru536/react-google-maps/issues/357)) ([4a2fff8](https://github.com/techguru536/react-google-maps/commit/4a2fff80f69a56bcdebe83e5b38b49f95d02f7b9))
* markers not removed in strict mode ([#15](https://github.com/techguru536/react-google-maps/issues/15)) ([857d279](https://github.com/techguru536/react-google-maps/commit/857d27906ecce5c45b63f9c1959bb8f8763f290a)), closes [#14](https://github.com/techguru536/react-google-maps/issues/14)
* memoize context-values to avoid excessive re-renders ([#287](https://github.com/techguru536/react-google-maps/issues/287)) ([8b3692c](https://github.com/techguru536/react-google-maps/commit/8b3692cfa02e3e5fd8543ac3ce93231983bbb379)), closes [#285](https://github.com/techguru536/react-google-maps/issues/285)
* move @types/google.maps to dependencies ([#115](https://github.com/techguru536/react-google-maps/issues/115)) ([d9a8e33](https://github.com/techguru536/react-google-maps/commit/d9a8e331b9cf7dcd9158c6cc543bf3fad8dff2ef)), closes [#106](https://github.com/techguru536/react-google-maps/issues/106)
* omit map prop from markers ([#305](https://github.com/techguru536/react-google-maps/issues/305)) ([29724c0](https://github.com/techguru536/react-google-maps/commit/29724c053d4a41ee11d98ccab1baaeec78ef5362))
* output an error when useMap is called outside APIProvider ([#117](https://github.com/techguru536/react-google-maps/issues/117)) ([1700089](https://github.com/techguru536/react-google-maps/commit/1700089992349de605cf84c4133e9838a04a4d40))
* prepare for first publishing ([274bcfa](https://github.com/techguru536/react-google-maps/commit/274bcfa7864927fdefdcc54a79519dd3da896e83))
* prevent passing empty parameters to ApiLoader ([#193](https://github.com/techguru536/react-google-maps/issues/193)) ([aaa4e12](https://github.com/techguru536/react-google-maps/commit/aaa4e1247d231ad4433daa6df7f283995daffdb4))
* remove deep-link into fast-deep-equal package ([#208](https://github.com/techguru536/react-google-maps/issues/208)) ([2c7d48e](https://github.com/techguru536/react-google-maps/commit/2c7d48efef804b6225fad81426b2aac29795679c))
* replace prop `gmpDraggable` with `draggable` in AdvancedMarker ([#53](https://github.com/techguru536/react-google-maps/issues/53)) ([801821d](https://github.com/techguru536/react-google-maps/commit/801821d676aa4ee927d8299c29a23e70062652e5))
* trigger release for new library function from commit 31f2655 ([b54dcc9](https://github.com/techguru536/react-google-maps/commit/b54dcc91abf957342a6b634b104a3d7b60daab15))
* update ControlPosition values ([#71](https://github.com/techguru536/react-google-maps/issues/71)) ([fa678e7](https://github.com/techguru536/react-google-maps/commit/fa678e7f2dac46b5dd6fd1ce908a553d94bef95d))
* update usage of useMapsLibrary in AdvancedMarker ([#55](https://github.com/techguru536/react-google-maps/issues/55)) ([3f3bc12](https://github.com/techguru536/react-google-maps/commit/3f3bc12784c1c396f780c8b909d2cc99bb19335f))
* use moveCamera and useLayoutEffect for faster map-updates ([f28081a](https://github.com/techguru536/react-google-maps/commit/f28081ae4cc239f26adc7173634a2811c15d3389))
* use parameter `v` instead of `version` ([94fcbcc](https://github.com/techguru536/react-google-maps/commit/94fcbcc360dc32a3786850bc320d278b8ee968f7))


### Miscellaneous Chores

* add registry-url to release action ([626d9e4](https://github.com/techguru536/react-google-maps/commit/626d9e40a59401cd89686b08a2cb78635326edc2))
* tag 1.0.0 release ([d405c55](https://github.com/techguru536/react-google-maps/commit/d405c551473b338c7d14ff1c34ccc67853d48a30))


### Code Refactoring

* improved state-handling implementation ([#181](https://github.com/techguru536/react-google-maps/issues/181)) ([84225c6](https://github.com/techguru536/react-google-maps/commit/84225c6d0b9314cae45c7eb9dc4d7195e36eba21))
* remove obsolete hooks ([#219](https://github.com/techguru536/react-google-maps/issues/219)) ([f0879c9](https://github.com/techguru536/react-google-maps/commit/f0879c96312e060b83ff855c6ec843c4a582eb2f))

## [1.0.0](https://github.com/visgl/react-google-maps/compare/v0.11.2...v1.0.0) (2024-05-11)


### Miscellaneous Chores

* tag 1.0.0 release ([afb67a7](https://github.com/visgl/react-google-maps/commit/afb67a7b076e83c025a147d488a93c33150c5b15))

## [0.11.2](https://github.com/visgl/react-google-maps/compare/v0.11.1...v0.11.2) (2024-05-10)


### Bug Fixes

* **map:** set other container position to relative ([#357](https://github.com/visgl/react-google-maps/issues/357)) ([8e77d70](https://github.com/visgl/react-google-maps/commit/8e77d70c272ac243c5d53f3dd6c02f508104226f))

## [0.11.1](https://github.com/visgl/react-google-maps/compare/v0.11.0...v0.11.1) (2024-05-10)


### Bug Fixes

* **advanced-marker:** remove content element in cleanup ([#351](https://github.com/visgl/react-google-maps/issues/351)) ([128df87](https://github.com/visgl/react-google-maps/commit/128df8730b7e1549e530a108192e7bae0699f199))
* **map:** set container position to relative ([#356](https://github.com/visgl/react-google-maps/issues/356)) ([7fa2b71](https://github.com/visgl/react-google-maps/commit/7fa2b711952a2472c409c38cd39edc1866cecbe3))

## [0.11.0](https://github.com/visgl/react-google-maps/compare/v0.10.0...v0.11.0) (2024-05-08)


### ⚠ BREAKING CHANGES

* **map:** Introduction of map instance caching needed a change to the DOM-Structure produced by the map component (added a div-element owned by the Map component to contain the map instance).
* **map:** The type passed to the `onProjectionChange` is changed from `MapCameraChangedEvent` to `MapEvent`, so there are no longer camera-props available for this event

### Features

* **advanced-marker:** add support for `clickable` option ([#341](https://github.com/visgl/react-google-maps/issues/341)) ([ca96e54](https://github.com/visgl/react-google-maps/commit/ca96e540a2117f7437745e8e1f71f83ef6c04e25))
* **map:** implement initial version of map-instance caching ([#349](https://github.com/visgl/react-google-maps/issues/349)) ([4a6e83a](https://github.com/visgl/react-google-maps/commit/4a6e83a26f06131baac288e3474d0e3163715f92))


### Bug Fixes

* **map:** change event-type of projectionChanged event to MapEvent ([#346](https://github.com/visgl/react-google-maps/issues/346)) ([83f9309](https://github.com/visgl/react-google-maps/commit/83f93091c858663b0183dd62bdc212a246013072))

## [0.10.0](https://github.com/visgl/react-google-maps/compare/v0.9.0...v0.10.0) (2024-05-03)


### Features

* add solution-channel parameter ([#334](https://github.com/visgl/react-google-maps/issues/334)) ([f93e43e](https://github.com/visgl/react-google-maps/commit/f93e43ee444a86dbc1b594d0c256229e6d207957))
* **advanced-marker:** add style prop to add styles to content-element ([#337](https://github.com/visgl/react-google-maps/issues/337)) ([e942fb5](https://github.com/visgl/react-google-maps/commit/e942fb5f5543a0a27e9987ee4324825958f08fdf))
* **infowindow:** add `className` and `style` props ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** add missing options and events ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** InfoWindow overhaul ([#335](https://github.com/visgl/react-google-maps/issues/335)) ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))


### Bug Fixes

* **infowindow:** add missing cleanup for infowindow ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** better dependency checks, using `useDeepCompareEffect` where needed ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))
* **infowindow:** removed unneeded dependency in infowindow hooks ([92854c9](https://github.com/visgl/react-google-maps/commit/92854c9103c90a8f0ad1c16eba729402b1e36919))

## [0.9.0](https://github.com/visgl/react-google-maps/compare/v0.8.3...v0.9.0) (2024-04-18)


### Features

* better handling for missing map configuration ([#308](https://github.com/visgl/react-google-maps/issues/308)) ([b318d67](https://github.com/visgl/react-google-maps/commit/b318d676088e6f0ef787ffa911c552a12ecb4895))


### Bug Fixes

* **docs:** use correct spelling of JavaScript ([#312](https://github.com/visgl/react-google-maps/issues/312)) ([f38d3c4](https://github.com/visgl/react-google-maps/commit/f38d3c4004663fd1850c00dca7ddfb7e92b8d5cf))
* omit map prop from markers ([#305](https://github.com/visgl/react-google-maps/issues/305)) ([8a38acf](https://github.com/visgl/react-google-maps/commit/8a38acf04ab665bbeeeef87a87d195bcbf44ccea))

## [0.8.3](https://github.com/visgl/react-google-maps/compare/v0.8.2...v0.8.3) (2024-04-04)


### Bug Fixes

* api-loader didn't call callback on repeat load calls ([743878a](https://github.com/visgl/react-google-maps/commit/743878a33abe2b0fb6bfe96377df07066536e51e))
* map controls crashing when invalid key is provided ([#290](https://github.com/visgl/react-google-maps/issues/290)) ([5052dfb](https://github.com/visgl/react-google-maps/commit/5052dfbf3735ff07319b7bd7108ae9448b0c2840))

## [0.8.2](https://github.com/visgl/react-google-maps/compare/v0.8.1...v0.8.2) (2024-03-29)


### Bug Fixes

* memoize context-values to avoid excessive re-renders ([#287](https://github.com/visgl/react-google-maps/issues/287)) ([bea68f9](https://github.com/visgl/react-google-maps/commit/bea68f923e9326188baebd8a89b9ad5cbf891303)), closes [#285](https://github.com/visgl/react-google-maps/issues/285)

## [0.8.1](https://github.com/visgl/react-google-maps/compare/v0.8.0...v0.8.1) (2024-03-26)


### Bug Fixes

* InfoWindow.shouldFocus doesn't work with false as value ([#278](https://github.com/visgl/react-google-maps/issues/278)) ([2f4b508](https://github.com/visgl/react-google-maps/commit/2f4b508a3da87f778496043dc7d5b40f47837d1f))

## [0.8.0](https://github.com/visgl/react-google-maps/compare/v0.7.1...v0.8.0) (2024-03-20)


### Features

* add new prop InfoWindow.shouldFocus ([#254](https://github.com/visgl/react-google-maps/issues/254)) ([c83ea37](https://github.com/visgl/react-google-maps/commit/c83ea375295699ed4e3c3a4a6f097cad1a4aca7d))

## [0.7.1](https://github.com/visgl/react-google-maps/compare/v0.7.0...v0.7.1) (2024-02-23)


### Bug Fixes

* export api-loading-status types ([#231](https://github.com/visgl/react-google-maps/issues/231)) ([9695034](https://github.com/visgl/react-google-maps/commit/9695034d3c51936c2c701b7fb8be4a864f349c3e)), closes [#230](https://github.com/visgl/react-google-maps/issues/230)

## [0.7.0](https://github.com/visgl/react-google-maps/compare/v0.6.1...v0.7.0) (2024-02-15)


### ⚠ BREAKING CHANGES

* removed the `useStreetViewPanorama()` and `useDirectionsService()` hooks.

### Features

* add example for drawing tools ([#220](https://github.com/visgl/react-google-maps/issues/220)) ([75e91c4](https://github.com/visgl/react-google-maps/commit/75e91c4a3b3893ac3d97b5689682bcca5262aac9))
* restore map state when changing mapId ([#213](https://github.com/visgl/react-google-maps/issues/213)) ([0db363f](https://github.com/visgl/react-google-maps/commit/0db363f9c0291135b31ac387d4513bbaf652517a))


### Code Refactoring

* remove obsolete hooks ([#219](https://github.com/visgl/react-google-maps/issues/219)) ([69b2373](https://github.com/visgl/react-google-maps/commit/69b23734270e8754a518790620872dc1f4136cc7))

## [0.6.1](https://github.com/visgl/react-google-maps/compare/v0.6.0...v0.6.1) (2024-02-08)


### Bug Fixes

* remove deep-link into fast-deep-equal package ([#208](https://github.com/visgl/react-google-maps/issues/208)) ([f0be380](https://github.com/visgl/react-google-maps/commit/f0be3803eeb3aa0c80b19b42977e714dcb746a2f))

## [0.6.0](https://github.com/visgl/react-google-maps/compare/v0.5.4...v0.6.0) (2024-02-07)


### ⚠ BREAKING CHANGES

* The behaviour of the props controlling camera parameters (center, zoom, heading and tilt) changed. Unless you are using controlled props, you have to change the prop names from e.g. `center` to `defaultCenter` (the same goes for `zoom`, `heading` and `tilt`).

### Code Refactoring

* improved state-handling implementation ([#181](https://github.com/visgl/react-google-maps/issues/181)) ([904b918](https://github.com/visgl/react-google-maps/commit/904b918427da071477ed4bb8c2c65006b35dff88))

## [0.5.4](https://github.com/visgl/react-google-maps/compare/v0.5.3...v0.5.4) (2024-02-01)


### Bug Fixes

* prevent passing empty parameters to ApiLoader ([#193](https://github.com/visgl/react-google-maps/issues/193)) ([0601753](https://github.com/visgl/react-google-maps/commit/0601753c03539dc1180272b31aafab911ebe9c2c))

## [0.5.3](https://github.com/visgl/react-google-maps/compare/v0.5.2...v0.5.3) (2024-02-01)


### Bug Fixes

* add `loading=async` to maps API url ([cb1336f](https://github.com/visgl/react-google-maps/commit/cb1336fc97dda8b3ad99c3f9a9a560cf8186056b))
* use parameter `v` instead of `version` ([0626fb6](https://github.com/visgl/react-google-maps/commit/0626fb6411ada3293d0f4a640dff07d0e19fc805))

## [0.5.2](https://github.com/visgl/react-google-maps/compare/v0.5.1...v0.5.2) (2024-02-01)


### Bug Fixes

* trigger release for new library function from commit 31f2655 ([b5a13e5](https://github.com/visgl/react-google-maps/commit/b5a13e598d97ae65304df6f79d05247b847e670b))

## [0.5.1](https://github.com/visgl/react-google-maps/compare/v0.5.0...v0.5.1) (2024-01-31)


### Bug Fixes

* infowindow double rendering and eslint warnings ([#185](https://github.com/visgl/react-google-maps/issues/185)) ([404cc06](https://github.com/visgl/react-google-maps/commit/404cc06253a92f120f97f72179949a8f4c0fc87b))

## [0.5.0](https://github.com/visgl/react-google-maps/compare/v0.4.3...v0.5.0) (2024-01-18)


### Features

* handle API-key errors in map-component ([#165](https://github.com/visgl/react-google-maps/issues/165)) ([26ccc15](https://github.com/visgl/react-google-maps/commit/26ccc15d640346ce71157d387fbc56720234fa4c))


### Bug Fixes

* don't use potentially unreliable addListener functions ([#158](https://github.com/visgl/react-google-maps/issues/158)) ([7309efa](https://github.com/visgl/react-google-maps/commit/7309efa1db8b392ebe2840e5d527a92419c9fc2a))
* export event-types ([#167](https://github.com/visgl/react-google-maps/issues/167)) ([cdd6b72](https://github.com/visgl/react-google-maps/commit/cdd6b72f848bf5b54618862788e1a3a221fcdce1))
* export type properly ([#170](https://github.com/visgl/react-google-maps/issues/170)) ([e561031](https://github.com/visgl/react-google-maps/commit/e56103149f15977ae0e7f62dd359cd3759b71fc9))

## [0.4.3](https://github.com/visgl/react-google-maps/compare/v0.4.2...v0.4.3) (2024-01-05)


### Bug Fixes

* allow AdvancedMarker to accept space-separated multiple class names ([#143](https://github.com/visgl/react-google-maps/issues/143)) ([eab53e2](https://github.com/visgl/react-google-maps/commit/eab53e2ffa69325fb927b16d59f6aa7faa589a49))

## [0.4.2](https://github.com/visgl/react-google-maps/compare/v0.4.1...v0.4.2) (2023-12-22)


### Bug Fixes

* avoid re-render on every importLibrary() call ([#135](https://github.com/visgl/react-google-maps/issues/135)) ([32b5894](https://github.com/visgl/react-google-maps/commit/32b5894518a22793c236bcab33291f25b48f7367))

## [0.4.1](https://github.com/visgl/react-google-maps/compare/v0.4.0...v0.4.1) (2023-12-01)


### Bug Fixes

* move @types/google.maps to dependencies ([#115](https://github.com/visgl/react-google-maps/issues/115)) ([9b788e1](https://github.com/visgl/react-google-maps/commit/9b788e10722ecbc8d483313c7d746b90f67afc87)), closes [#106](https://github.com/visgl/react-google-maps/issues/106)
* output an error when useMap is called outside APIProvider ([#117](https://github.com/visgl/react-google-maps/issues/117)) ([5c30c3d](https://github.com/visgl/react-google-maps/commit/5c30c3d5a36af57a649ca3201f7dd0c3819e6035))

## [0.4.0](https://github.com/visgl/react-google-maps/compare/v0.3.3...v0.4.0) (2023-11-28)


### Features

* Allow &lt;Pin&gt; glyphs to be passed as children (close [#98](https://github.com/visgl/react-google-maps/issues/98)) ([#99](https://github.com/visgl/react-google-maps/issues/99)) ([6374453](https://github.com/visgl/react-google-maps/commit/637445313c8c9364cbf1f32346d3438fc0589d74))

## [0.3.3](https://github.com/visgl/react-google-maps/compare/v0.3.2...v0.3.3) (2023-11-13)


### Bug Fixes

* add map camera state tracking ([#84](https://github.com/visgl/react-google-maps/issues/84)) ([1dc1584](https://github.com/visgl/react-google-maps/commit/1dc158436c4ffde60548486da5410b46e989fc5b))

## [0.3.2](https://github.com/visgl/react-google-maps/compare/v0.3.1...v0.3.2) (2023-11-09)


### Bug Fixes

* use moveCamera and useLayoutEffect for faster map-updates ([e493d5f](https://github.com/visgl/react-google-maps/commit/e493d5ffa350efebddd5ef63bb57495954478877))

## [0.3.1](https://github.com/visgl/react-google-maps/compare/v0.3.0...v0.3.1) (2023-11-09)


### Bug Fixes

* update ControlPosition values ([#71](https://github.com/visgl/react-google-maps/issues/71)) ([1dd144a](https://github.com/visgl/react-google-maps/commit/1dd144ac3deac53a77d870ba8cf1e4623786a620))

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
