# RVL-Node Types

TypeScript type definitions for RVL-Node and friends.

# Installation

Install as a dev dependency with npm:

```bash
npm install --save-dev rvl-node-types
```

# Usage

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

# License

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
