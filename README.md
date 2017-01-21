# Personality Sunburst Chart

![last-release](https://img.shields.io/github/tag/personality-insights/sunburst-chart.svg)
[![npm-version](https://img.shields.io/npm/v/personality-sunburst-chart.svg)](https://www.npmjs.com/package/personality-sunburst-chart)
[![npm-license](https://img.shields.io/npm/l/personality-sunburst-chart.svg)](https://www.npmjs.com/package/personality-sunburst-chart)
[![npm-downloads](https://img.shields.io/npm/dm/personality-sunburst-chart.svg)](https://www.npmjs.com/package/personality-sunburst-chart)
[![Build Status](https://travis-ci.org/personality-insights/sunburst-chart.svg?branch=master)](https://travis-ci.org/personality-insights/sunburst-chart)
[![codecov.io](https://codecov.io/github/personality-insights/sunburst-chart/coverage.svg?branch=master)](https://codecov.io/github/personality-insights/sunburst-chart?branch=master)

Obtain a sunburst chart visualization for a personality profile.  For use in an HTML page.

## Installation

```sh
$ npm install personality-sunburst-chart
```

## Usage

Include the personality-sunburst-chart script, JQuery and D3 in your HTML page.
```
<script src="path/to/personality-sunburst-chart.standalone.js"></script>
<script src="https://code.jquery.com/jquery-2.2.0.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.5.14/d3.min.js"></script>
```

Create an element to contain the chart in your HTML page.
<div id='sunburstChartContainer'></div>

Generate the visualization for a personality profile.
```JavaScript
  var PersonalityTraitDescriptions = require('personality-trait-descriptions');

  // version refers to the version of Watson Personality Insights to use, v2 or v3
  var chart = new PersonalitySunburstChart('sunburstChart', {'version': 'v3'});

  // render the profile image for a personality profile (version as specified in creating the chart)
  // and a profile photo - the photo will be inserted into the center of the sunburst visualization
  chart.show(profile, 'path/to/profile_photo.jpg');

  ```

  See the complete [example code](./examples/example_v3.html).

## License

This library is licensed under Apache 2.0. Full license text is
available in [LICENSE](LICENSE).

## Changelog

__15-01-2017__
 * Added support for v3 profiles - d3 tree json wrapper provided for v2 and v3 personality profiles to generate the input required by the d3 sunburst-chart created in lib/personality-chart-renderer.js
 * Only traits, needs and values will be displayed by the sunburst-chart.
