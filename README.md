# RVL-Node Types

TypeScript type definitions for [rvl-node](https://github.com/nebrius/rvl-node) and friends.

## Installation

Install as a dev dependency with npm:

```bash
npm install --save-dev rvl-node-types
```

## Usage

```TypeScript
import { IWaveChannel } from 'rvl-node-types'

const myChannel: IWaveChannel = {
  a: 128,
  w_t: 4,
  w_x: 0,
  phi: 0,
  b: 0
};
```

Note: it is recommended that you use the [rvl-node-animations](https://github.com/nebrius/rvl-node-animations) helper library to create these parameters, as creating them by hand is complicated.

## Theory

RVL Node uses a rendering engine based on sin waves. RVL Node layers four waves on top of each other to create interesting and aesthetically pleasing LED animations. Think of this like CSS layers. They can include transparency to create a layering effect.

All waves are defined in the HSV color space that has been mapped to 8-bit integers. A hue of 180 degrees is represented by the value `128`, a saturation of 25% is represented by the value `64`, and so on and so forth.

A wave is defined using the following mathematical formula:

```
f(t, x) = a * sin(w_t * t + w_x * x + phi) + b
```

This function takes 5 variables from the user (a, w_x, w_t, phi, b), and 2 from the engine (x, t). This allows someone to create a wave that can vary over time, over the length of the LED strip, can be constant, or any of the above. Each channel (hue, saturation, value, and alpha) have their own wave assigned to them. 4 channels per layer, times 4 layers, means 80 coefficients total!

## License

Copyright (c) Bryan Hughes <bryan@nebri.us>

This file is part of Raver Lights Node Types.

Raver Lights Node Types is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

Raver Lights Node Types is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with Raver Lights Node Types.  If not, see <http://www.gnu.org/licenses/>.
