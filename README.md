# RhythmBox

This application is a live drummer that you can control using buttons or MIDI CC
with at least 1 controller, as an arranger or a [BeatBuddy][] pedal would.
The drum loops are described in simple [JSON files][].
The application either outputs MIDI notes, and can also generate sounds
internally using SFZ instruments.
For now the sound generation uses [SFZero][], which has many limitations.
It is possible to use it within a VST host with any drum machine,
or with an external sound generator.
Since it uses [JUCE][], it should be almost cross platform,
although I only tested Windows and Linux, and a tiny bit of Android.
Contributions and comments are welcome, as well as beat description files.
I'll put up some forum or sharing platform at some point.

[BeatBuddy]: https://singularsound.com/
[JSON files]: https://sfztools.github.io/rhythmbox/drum-beat-description-files
[JUCE]: https://juce.com/
[SFZero]: http://stevefolta.github.io/SFZero/

[![Travis](https://img.shields.io/travis/com/sfztools/rhythmbox.svg?label=Linux-macOS&style=popout&logo=travis)](https://travis-ci.com/sfztools/rhythmbox)
[![AppVeyor](https://img.shields.io/appveyor/ci/sfztools/rhythmbox.svg?label=Windows&style=popout&logo=appveyor)](https://ci.appveyor.com/project/sfztools/rhythmbox)

## Installation

Windows binaries are available on the [releases page][],
along with Raspberry Pi binaries.

See the [build documentation page][] about how to build the application
from the source code.

[build documentation page]: https://sfztools.github.io/rhythmbox/build
[releases page]: https://github.com/paulfd/rhythmbox/releases

## Usage

The usage is quite straightforward.
Upon launching the application you have to select at least a [beat description][]
by clicking on Rhythms.
You will be presented with a list of the current beat descriptions you have
previously entered, as well as a button to add more.
To load a rhythm, just double click it.
You may also load an [Sfz file][] in the same way, or use the MIDI output.

Once the rhythm is loaded, you can use the buttons to launch the rhythm,
fills and parts.
You can also use a midi controller
by setting the proper input channel and input CC in the options.
After this, the behavior is:
- a tap starts the live rhythm, and if already started it makes a fill.
- a long tap transitions into the next part.
- 2 taps trigger the ending.

[beat description]: https://sfztools.github.io/rhythmbox/drum-beat-description-files
[Sfz file]: https://sfztools.github.io/rhythmbox/drum-sfz-files

## Contact and contributions

Feel free to post an issue, or contact me by [email](mailto:paulfd@outlook.fr)
if you need. Any contribution is welcome.
There are many things to improve in the code and most notably in the GUI
which is terrible but I'm very bad at this.
However the best is probably to build beat descriptions/sfz files
and share the love! :)

## Acknowledgments

The original SFZero code is from [Steve Folta](http://stevefolta.github.io/SFZero/).
There are many updates to the original codebase.
The one I'm using has been improved by Leo Olivers
and cleaned up by [MatkatMusic](https://github.com/matkatmusic).

JUCE is owned by [ROLI](https://roli.com/).
