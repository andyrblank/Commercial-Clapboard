# Commercial-Clapboard

This is a post processing BASH / Shell script designed for use with Tvheadend (tvheadend.org) to scan for commercials, transcode to H264 & cut commercials from the H264 file. The script also uses the xmltv output of mc2xml to name recordings for Plex/Kodi(XBMC) to scrape properly.

The Post Processing Code in the Tvheadend configuration should be as follows:

/path/to/script/Convert.sh %f %b %c %C %t %d %e %S %E

Below is a description from Tvheadend of the output variables and their mappings in the script.

# $1 Full path to recording (%f) /home/user/Videos/News.mkv
# $2 Basename of recording (%b) News.mkv
# $3 Channel name (%c) BBC world
# $4 Who created this recording (%C) user
# $5 Program title (%t) News
# $6 Program description (%d) News and stories...
# $7 Error message (%e) Aborted by user
# $8 Start time stamp of recording, UNIX epoch (%S)
# $9 Stop time stamp of recording, UNIX epoch (%E)

source: https://tvheadend.org/projects/tvheadend/wiki/Digital_Video_Recorder_configuration

This scripts was designed on Ubuntu Server 14.04 and requires the following installed:

* Comskip Linux port from here: http://forum.kodi.tv/showthread.php?tid=150084
* HandBrake CLI
* xmllint (libxml2)
* perl
* mencoder
* ffmpeg
* mc2xml setup with TVHeadend as instructed here (https://tvheadend.org/boards/4/topics/10322) 
