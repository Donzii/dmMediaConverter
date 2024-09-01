# dmMediaConverter
## by Marius Dalacu https://sites.google.com/site/dmsimpleapps/
dmMediaConverter is a cross-platform FFmpeg frontend (GUI) exposing some of its features. It is intended to be simple and easy to use but also to be able to achieve complex tasks. I have inspired myself from a lot of media converters like Handbrake, WinFF and MkvMergeGui. 
One feature was lacking from most of them, video stream copy (pass-through), that made me build this.

![Screenshot 2023-02-10 090745](https://github.com/Donzii/dmMediaConverter/assets/7527643/148ce53c-bff5-42cd-9213-dfc35733fd44)


### Main features:
*  **stream copy** (video, audio, subtitle)
*  **stream conversion** - almost any codec into: 
    *  video - **h264, h265**, vp8, vp9, MPEG4, AV1
    *  audio - **aac**, mp3, flac, ac3, eac3, pcm, vorbis, opus
    *  subtitles - srt, ass, ssa, mov_text, dvdsub

*  **add multiple streams** into one mkv, mp4  or any other container known by FFmpeg that accepts multiple streams (with or without reencoding). Supports multiple video streams in the same file. Also you can reorder stream position.
*  **stream profiles** - create and apply audio and video profiles
*  **merge files** with the same properties - no reencoding. Ex. Files made by a phone or camera.
*  **merge different** kind of files (different codecs, resolution, etc.) into one file. It chooses an output with the biggest width of all source files. 
*  **split** a file by given time points (no reencoding)
*  **trim** a video (no reencoding)
*  **bulk convert** files using stream profiles or manual settings (no filter options for manual)
*  **job queue** - you can add multiple tasks into a job queue
*  **parallel jobs** - you can run multiple jobs in the same time (multithreading)
*  audio **auto gain detect** - it will parse the whole file and find the proper gain value (reencode)
*  **picture settings** - with **changes immediately displayed** (reencode)
    *  **scaling** - change video resolution (use -1 to keep the aspect ratio)
    *  cropping and padding
    *  **auto crop** - detect best crop values for encoder
    *  **rotate** picture in 90 degrees increments
    *  grayscale
    *  deinterlace
    *  de-shake
    *  **burn subtitles** (only text based for now)
    *  **watermark**
    *  **Image adjustments** like brightness, contrast, gamma, etc. 
    *  **3D conversions**: Convert between different stereoscopic image formats.. Ex. side by side to anaglyph. 
    *  manually add FFmpeg video stream filters
*  video **aspect correction** - no reencoding
*  write stream **tags** like language and title, also container title and creation time -  no reencoding
*  **metadada editor** - copy, add or modify any metadata to stream and container.
*  **chapters editor** - create,  import or edit chapters. Simple and efficient.
*  **HW encoding**, it supports **Nvidia** cards and **Intel Quick Sync** Video technologies for h264 and h265 depending on hw. For intel you must install [Intel Media SDK 2016](https://software.intel.com/en-us/media-sdk/download) or newer.
*  **multiplatform**
