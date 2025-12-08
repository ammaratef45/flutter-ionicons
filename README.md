# Ionicons

![](https://img.shields.io/pub/v/ionicons)
![](https://img.shields.io/github/license/KMBAL/flutter-ionicons)
![](https://img.shields.io/github/issues/KMBAL/flutter-ionicons)

This package is a fork of the [ionicons](https://pub.dev/packages/ionicons) package. It includes the icons from
[Ionicons](https://ionicons.com/) [v7.4.0](https://github.com/ionic-team/ionicons/releases/tag/v7.4.0). The naming
convention is the same as the CSS names, all dashes replaced with underscores.

## Usage

```dart
import 'package:kmbal_ionicons/kmbal_ionicons.dart';

// ...

Icon(Ionicons.add)
Icon(Ionicons.add_outline)
Icon(Ionicons.add_sharp)
```

## Contributing

### Prerequisites

1. Install `make`
2. Install [`nvm`](https://github.com/nvm-sh/nvm)
3. Use `nvm` to install the version of Node in `.nvmrc`
4. Install Dart and Flutter

### Updating to a new version of Ionicons

1. In `Makefile`, update `IONICON_VERSION` to the version of Ionicons you want to update to (available versions can be found [here](Visit https://github.com/ionic-team/ionicons/releases)).
2. Run `make ttf` to generate the TTF font file.
3. Run `make gen` to generate the Dart code.
4. Update the minor version number in `pubspec.yaml`.
5. Update `CHANGELOG.md`.

### Adding custom icons

Custom icons are stored in `src/extra_icons/kmbal`. To add a new custom icon:

1. Copy the icon SVG to `src/extra_icons/kmbal`
   1. It must be called `kmbal-<name>.svg` where `<name>` is the kebab-case name of the icon.
   2. The SVG must have a `viewBox` of `0 0 512 512` (see `src/extra_icons/kmbal/kmbal-bank.svg` as an example).
2. Run `make ttf` to generate the TTF font file.
3. Run `make gen` to generate the Dart code.
4. Update the minor version number in `pubspec.yaml`.
5. Update `CHANGELOG.md`.

### Testing

1. `cd ./example`
2. `make build`
3. `make serve`
