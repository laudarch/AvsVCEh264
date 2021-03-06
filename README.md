
#AvsVCEh264
Avisynth to H.264 Video Encoding using OpenVideo Encode library that provides an OpenCL API that leverages the video compression engine (VCE) on AMD platforms.

## Usage

```
AvsVCEh264 -i input.avs -o output.264 -c myConfig.ini
```

##Configuration file
You can use configuration files located in configs folder or create your own.
If you have questions about settings values you can read and take as an example default_explained.ini configuration file.

## Limitations
### Software
- The OpenVideo library is currently supported only on Windows 7 (maybe Vista).
- Lastest version of AviSynth. Download from [http://avisynth.nl/](http://avisynth.nl/ "official website").
- Catalyst driver release 12.8+.

### Hardware
TrinityAPU, Radeon HD 7000 Series (Tahiti XT, CapeVerde) or newer GPU.

##Build
To build you need AMD APP SDK 2.7 or later and a compiler (Mingw, Microsoft Visual Studio 2008 or 2010)

##AMD:
VCE, OVC, OVE: It is unclear, in PDF documents referred to VCE (Video Codec Engine),
in the libraries (OpenVideo), the prefix used is OVE_ but I can not find anything on the internet about it.
AMD does not provide any documentation about its technology VCE, OVC or OVE.

## TODO
- Stdout output support.
- Set default input switch values for Output.
- Pause / ~~Cancel~~ buttons.
- Reduce number of global variables.
- ~~Memory leaks!~~
- ~~Timer.~~
- Unicode support
- 64bit version
- Publish binaries
- ~~!mod16 videos / cropOffset.~~
- ~~Buffered / Multi thread.~~
- Do case insensitive config file.

## History
- Fixed green bottom bar on videos whose height was not a multiple of 16.
- Now the encoding and decoding is done in separate threads and they make use of a circular buffer.
- Removed huge memory leak that held UV planes of all frames
- Added abort key (F8)
- Improved info shown during the encoding.
- Added monitor/info thread and buffer class
- Added sample config files (speed, quality & balanced)
- Added Timer class.
- New config system, now use .ini files.
- First release / prototype.

