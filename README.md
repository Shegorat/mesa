# mesa - Media Scanner Advanced

**mesa** (Media Scanner Advanced) is a utility for detecting and extracting embedded multimedia resources from binary files, archives, game assets, and custom containers.

The tool can scan files for known media signatures, report discovered resources, and optionally extract them for further processing.

## Supported Formats

### Video

* BIK
* BK2
* VP6

### Audio

* MP2
* MP3
* OGG
* SND
* WAV
* WEM (Wwise OGG)

### Images

* BMP
* JPG
* PNG

## Planned Support

### Video

* AVI
* MKV
* MP4
* SWF

### Audio

* AIFF
* FSB

### Images

* DDS
* GIF
* TGA
* TIFF

## Command Line Options

| Option                  | Description                                                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `-i`, `--input <file>`  | Input file to scan                                                                                                              |
| `-o`, `--output <dir>`  | Output directory for extracted files                                                                                            |
| `-x`                    | Extract detected files                                                                                                          |
| `-e`                    | Remove extracted files                                                                                                          |
| `-m <matchers>`         | Comma-separated list of enabled matchers (`bik`, `bk2`, `vp6`, `snd`, `wwise`, `bmp`, `png`, `jpg`, `wav`, `ogg`, `mp2`, `mp3`) |
| `-ws <size>`            | Search window size                                                                                                              |
| `-l`, `--log <file>`    | Write log output to file                                                                                                        |
| `-s`                    | Silent mode (show results only)                                                                                                 |
| `-t`, `--target <file>` | Generate target file without extracted data (FreeArc mode)                                                                      |
| `-h`, `--help`          | Display help information                                                                                                        |

## Examples

Scan a file:

```bash
mesa -i biks.tar
```

Scan and extract detected resources:

```bash
mesa -i game.dat -x -o extracted
```

Scan only for audio streams:

```bash
mesa -i archive.bin -m wav,ogg,mp3,mp2
```

## Support the Project

[![Support on Patreon](https://c5.patreon.com/external/logo/become_a_patron_button.png)](https://www.patreon.com/Shegorat)

If you find this project useful, consider supporting development on Patreon.
