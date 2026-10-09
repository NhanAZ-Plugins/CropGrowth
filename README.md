# CropGrowth

CropGrowth plays growth particles and a bone meal sound when a player uses bone meal on supported crops and plants in an Axolotl-PM world.

[![Build](https://github.com/NhanAZ-Plugins/CropGrowth/actions/workflows/build.yml/badge.svg)](https://github.com/NhanAZ-Plugins/CropGrowth/actions/workflows/build.yml)
[![License](https://img.shields.io/github/license/NhanAZ-Plugins/CropGrowth)](LICENSE)

## Behavior

The plugin listens for right clicks with bone meal. It adds an effect for supported plants, including saplings, bamboo, flowers, cave vines, sea pickles, torchflowers and pitcher crops. It also handles some adjacent block and water cases. The server remains responsible for the actual growth and item use.

There are no commands, permissions or configuration options.

![CropGrowth example](https://user-images.githubusercontent.com/60387689/178136951-db5c3b65-80c2-462b-b3cf-50b90992d7b5.png)

## Requirements and compatibility

- Axolotl-PM with plugin API `5.9.0` or newer.
- PHP 8.1 or newer in the Axolotl-PM 5 toolchain.

The source uses torchflower and pitcher crop block IDs that are absent from PocketMine-MP API 5.7.0 and present in 5.9.0. PHPStan level max passes against the 5.9.0 API and the pinned Axolotl-PM source in CI. The tested Axolotl-PM runtime is recorded in release evidence. This does not establish compatibility with every Axolotl-PM 5.x release.

## Installation

Download `CropGrowth.phar` from a verified [GitHub release](https://github.com/NhanAZ-Plugins/CropGrowth/releases), place it in the server's `plugins/` directory and restart the server.

## Building and testing

The [build workflow](.github/workflows/build.yml) installs locked Composer development dependencies, runs PHPStan level max, builds the PHAR with [DevTools](https://github.com/NhanAZ/DevTools), and verifies its contents and digest. The workflow pins its build tools and Axolotl-PM source. A clean server startup check verifies that the PHAR loads. Particle and sound behavior with a Bedrock client requires an in-game check.

## License and support

The plugin source is licensed under [GPL-3.0](LICENSE). For help, use [NhanAZ Discord](https://discord.gg/j2X83ujT6c).
