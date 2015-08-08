````
                     __                                   ___.
___________    ____ |  | _______     ____   ____          \_ |__ _____    ____   ____   ___________
\____ \__  \ _/ ___\|  |/ /\__  \   / ___\_/ __ \   ______ | __ \\__  \  /    \ /    \_/ __ \_  __ \
|  |_> > __ \\  \___|    <  / __ \_/ /_/  >  ___/  /_____/ | \_\ \/ __ \|   |  \   |  \  ___/|  | \/
|   __(____  /\___  >__|_ \(____  /\___  / \___  >         |___  (____  /___|  /___|  /\___  >__|
|__|       \/     \/     \/     \//_____/      \/              \/     \/     \/     \/     \/

````
# package-banner
Generates a fancy banner from a package.json file

## Usage

```js
var PackageBanner = require('package-banner');

// Basic Usage
var banner = new PackageBanner().build();

/*!
 *                      __                                   ___.
 * ___________    ____ |  | _______     ____   ____          \_ |__ _____    ____   ____   ___________
 * \____ \__  \ _/ ___\|  |/ /\__  \   / ___\_/ __ \   ______ | __ \\__  \  /    \ /    \_/ __ \_  __ \
 * |  |_> > __ \\  \___|    <  / __ \_/ /_/  >  ___/  /_____/ | \_\ \/ __ \|   |  \   |  \  ___/|  | \/
 * |   __(____  /\___  >__|_ \(____  /\___  / \___  >         |___  (____  /___|  /___|  /\___  >__|
 * |__|       \/     \/     \/     \//_____/      \/              \/     \/     \/     \/     \/
 * package-banner 0.1.0
 * Description: Generates a fancy banner from a package.json file
 * Author: Isaac Suttell <isaac@isaacsuttell.com>
 * License: MIT
 */

```

## Options

```js
var PackageBanner = require('package-banner');

var banner = new PackageBanner({
  /**
   * Either takes a path or an object. It defaults to the package.json in your process.cwd()
   * @type    {String|Object}
   */
  pkg: 'package.json',

  /**
   * ASCII Font to use
   * @type    {String}
   */
  font: 'graffiti',

  /**
   * Should an ascii art title be generated?
   * @type    {Boolean}
   */
  fancy: true,

  /**
   * Default line ending us UNIX
   * @type    {String}
   */
  lineEnding: '\n',

  /**
   * Wrap everything in a comment or just create the text
   * @type    {Boolean}
   */
  wrap: true,

  /**
   * Add a line break at the end
   * @type    {Boolean}
   */
  lastLineBreak: true,

  /**
   * Add a timestamp which can be useful for automated build systems
   * @type    {Boolean}
   */
  timestamp: false,

  /**
   * An array of keys to include in order
   * @type    {Array}
   */
  keys: ['name', 'description', 'author', 'homepage', 'bugs', 'license'],

}).build();

```

## License
The MIT License (MIT)

Copyright (c) 2015 Isaac Suttell

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
