# Pouches

A Windower 4 addon for Final Fantasy XI that automatically uses stacks of consumable items like pouches, coffers, cases, and other self-targeted usable items.

## Installation

1. Download `Pouches.lua` and place it in your `Windower4/addons/Pouches/` folder
2. Load the addon in-game with `//lua load pouches`

## Usage

```
//pouches <item name>
```

The addon will find all matching items in your main inventory and use them one at a time until depleted or interrupted.

### Examples

```
//pouches Gr. Velkk Coffer
//pouches Lucky Egg
//pouches528 Gil Coffer
//pouches Mog Pell (Red)
```

Auto-translate brackets are supported:

```
//pouches {Gr. Velkk Coffer}
```

## How It Works

- Scans your main inventory for the specified item
- Uses each item with the appropriate delay based on its cast time
- Automatically continues until all items are used or you interrupt it

## Stopping

To stop the addon mid-use, simply type:

```
/heal
```

Entering healing mode sets your status to non-idle, which halts the use loop.

## Requirements

- Windower 4
- The following libraries (included with Windower):
  - logger
  - tables
  - strings
  - resources

## Limitations

- Only works with items that can target `<me>` (Self)
- Items must be in your main inventory (not sack, case, etc.)
- Cannot use items while your character status is not idle (status 0)

## Tips

For opening large quantities of coffers that drop sellable items, pair this addon with [SellNPC](https://github.com/Ivaar/Windower-addons) to automatically sell junk as your inventory fills up.

## Credits

- **Author:** Omnys@Valefor
- **License:** BSD 3-Clause

## License

Copyright © 2016, Omnys of Valefor. All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

- Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
- Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
- Neither the name of Pouches nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL OMNYS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
