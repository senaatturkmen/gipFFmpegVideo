# gipFFmpegVideo
A GlistEngine plugin that plays a video and draws it on the screen using FFmpeg library. For instant, the plugin is compatible with Windows and Linux.

## Installation
Fork & clone this project into 
> C:\dev\glist\glistplugins (on Windows)
> ~/dev/glist/glistplugins (on Linux)

*Notice For Linux Developers* :
Please install necessary libraries before running the plugin:
> sudo apt-get install libavcodec58 libavcodec-dev libavformat58 libavformat-dev libavfilter7 libavfilter-dev libavdevice58 libavdevice-dev libavutil56 libavutil-dev libswscale5 libswscale-dev libao-dev libportaudio libportaudio-dev

##### *Notice for all*

Please add the PATH variable to eclipse paths by:

Right Click the GlistApp project once on the left, inside the Project Explorer

Then:

> Project > Properties > C/C++ Build > Environment

then click PATH followed by clicking Edit on the right. There, at the end of the paths, add:

> ${workspace_loc}\\..\\..\\..\\..\glistplugins\gipFFmpegSound\prebuilts\bin

## Usage
1. Add gipFFmpegVideo into plugins of your GlistApp/CMakeLists.txt
> set(PLUGINS gipFFmpegVideo)

2. Include gipFFmpegVideo.h in GameCanvas.h
> #include "gipFFmpegVideo.h"

3. Define gipFFmpegVideo object
> gipFFmpegVideo video;

4. Load video
> void GameCanvas::setup() {
>     video.loadVideo("videofilename");
> }

5. Update
> void GameCanvas::update() {
>     video.update();
> }

6. Draw
> void GameCanvas::draw() {
>     video.draw(x, y);
> }

## Plugin Licence
Apache 2
