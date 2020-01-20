# dsdtoflac
This tool converts DSD files to FLAC files using ffmpeg. The conversion process works as follows:

1. An album is converted directly from DSF to FLAC in a temporary location.
1. The volume of each FLAC file is collected.
1. The highest peak is determined across the FLAC files.
1. The album is then converted directly from DSF to FLAC while applying a 30k lowpass filter and volume adjustment such that the highest peak of any song on the PCM converted results at a 0DB peak

There are other tools that do similar work. Unfortunately these other tools do not peak level across the album, but instead across individual songs.
