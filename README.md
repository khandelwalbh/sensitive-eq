# Running the project
 - Clone this [project repo](https://lmgtfy.app/?q=how+to+pull+a+github+repository). 
 - Is [NPM](https://www.npmjs.com/get-npm) installed globally on your computer?
 - Make sure Angular CLI 11 is installed globally also.
 - Install the project dependencies with `npm i`.
 - Run the project with `npm run start`.

Note:
This project needs full access to your computer's audio!
Windows machines typically allow easy access to system audio devices.
MacOS blocks system audio and you'll likely need a third-party audio device [like sound-flower](https://github.com/mattingalls/Soundflower/releases/) or [EQ-MAC](https://eqmac.app/)

![EQ Example](https://github.com/highfiiv/sensitive-eq/tree/master/src/assets/eq-example.gif)

## Pitching in
Submit a PR :)

## WIP
This project is a work-in-progress and has no gaurantee of functionality in any way.
 1. When haptic devices connect certain audio frequency bands should be mappable to specific haptic engines.

## How the audio system works
Short version:
 - Volume dB peaks into frequency ranges you set on each of 16 "bands"
 - How far into the range is calculated as .1 - 1.0 vib command

Longer version:
 - 12 times per second the audio updates and triggers this math. (not sure of the perfect frequency yet)
 - The user sets range levels on each frequency band
 - When audio levels rise dB levels peak into the user's range
 - The range is always 0-100% (translated to 0.1 - 1.0)
 - 0.1 - 1.0 is used for haptic values

## TODOs
 1. FEATURE: Assigning selected frequency values to specific haptics the device may have.
 2. FIX: An optional video upload adds the video blob to `video` src as expected but not playable for unknown reason
 3. FEATURE: Record JSON scripts of these "peak" values for playback on other script playing/editing softwares
 4. FEATURE: Edit a JSON script of recorded peak sensitivity scores

## LICENSE
MIT - Please submit PRs to this repo for the community's use and progress on this audio-haptic project.
Copyright 2021 - HighFiiv

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
