# MPKK Transit information

This custom component fetches information from cracow [ttss](http://www.ttss.krakow.pl/) with information when next train or bus will be on specified

# Manual Installation

Copy `custom_components/mpkk` to `<config>/custom_components/mpkk` directory.

# Installation using hacs

You can add this repository to [your hacs](https://hacs.xyz/)

# Home Assistant configuration

You can configure multiple bus/tram stops:

``` YAML
sensor:
  - platform: mmpk
    name: 'Jarzebiny'
    stop_id: 2685
    direction: 'Bronowice Małe'
```

* `name` - Name of the component
* `stop_id` - Id of the stop. You can retrieve it by visiting [ttss](http://www.ttss.krakow.pl/) finding your stop. Search in webdeveloper console for request like http://www.ttss.krakow.pl/internetservice/services/lookup/autocomplete/json?query=bia%C5%82ucha&language=en In returned json you should find id of the stop
* `direction` - for what direction you want to filter all trains
