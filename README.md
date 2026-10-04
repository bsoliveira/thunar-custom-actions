# Thunar Custom Actions

A collection of simple Bash scripts for common file operations, designed primarily for use as custom actions in **Thunar**.

## Scripts

### Audio

| Script                | Description                                 |
| --------------------- | ------------------------------------------- |
| `audio-converter-mp3` | Convert audio files to MP3                  |
| `audio-remove-cover`  | Remove embedded cover images from MP3 files |

### GPG

| Script        | Description                                  |
| ------------- | -------------------------------------------- |
| `gpg-encrypt` | Encrypt files using GPG symmetric encryption |
| `gpg-decrypt` | Decrypt GPG-encrypted files                  |

### Images

| Script                   | Description                                     |
| ------------------------ | ----------------------------------------------- |
| `image-converter-jpg`    | Convert images to JPEG                          |
| `image-converter-png`    | Convert images to PNG                           |
| `image-converter-webp`   | Convert images to WebP                          |
| `image-optimize-web`     | Optimize JPEG, PNG, and WebP images for web use |
| `image-remove-metadata`  | Remove metadata from JPEG, PNG, and WebP images |
| `image-metadata-report`  | Generate a text report with image metadata      |
| `image-resize-thumbnail` | Resize images to a maximum dimension of 320 px  |
| `image-resize-small`     | Resize images to a maximum dimension of 480 px  |
| `image-resize-medium`    | Resize images to a maximum dimension of 800 px  |
| `image-resize-large`     | Resize images to a maximum dimension of 1024 px |

### Video

| Script                 | Description                               |
| ---------------------- | ----------------------------------------- |
| `video-extract-mp3`    | Extract audio from videos as MP3          |
| `video-optimize-share` | Optimize videos for sharing               |
| `video-optimize-tv`    | Optimize video file(s) for TV playback    |

## Dependencies

Install the required packages on Debian:

```bash
sudo apt install imagemagick ffmpeg libimage-exiftool-perl eyed3 gnupg
```

| Tool        | Used by                            |
| ----------- | ---------------------------------- |
| ImageMagick | Image scripts                      |
| FFmpeg      | Audio and video conversion scripts |
| ExifTool    | `image-metadata-report`            |
| eyeD3       | `audio-remove-cover`               |
| GnuPG       | GPG scripts                        |

## Installation

Clone the repository and make the scripts executable:

```bash
git clone git@github.com:bsoliveira/thunar-custom-actions.git
cd thunar-custom-actions
chmod +x *
```

The scripts can then be used directly from the terminal or configured as **Custom Actions in Thunar**.

## Usage

All scripts provide a help option:

```bash
./script-name --help
```

Most scripts accept one or more files:

```bash
./script-name file1 file2 file3
```

Scripts do not overwrite existing output files.

## License

Use, modify, and distribute freely.
