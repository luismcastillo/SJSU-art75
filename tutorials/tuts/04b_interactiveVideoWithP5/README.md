# Interactive Video with P5
### How to set up a new GitHub repository for your Net Art / Project 3 and enable GitHub pages to host it online


 ◇─◇──◇────◇────◇────◇────◇────◇─◇─◇
<br>

(work in progress)

#### **On this page:**
1. [HTML5 Video](#-html5-video)
2. [Prepping Video Files](#-prepping-video-files)
3. More to come....

<br>

# ▼△▼△▼ HTML5 Video

Note, we are not using Vimeo or YouTube to host our video in an iframe!

Using P5, we are playing video directly from our browser. The plus side is that we have a lot more control. The down side is that we don't have an internet giant to do the heavy lifting, so we have to keep our files small and maneagable.


# ▼△▼△▼ Prepping Video Files

Codecs are types of video compression, ie .mp4, .mov, .webM...

[Not all browsers and mobile devices](https://www.w3schools.com/tags/tag_video.asp) can play all video codecs, so it is a good idea to always have two files for each video, an .mp4 (H264) and a .webM.

#### 1) .mp4
You can export the .mp4 right out of premiere. In exports, select H264 (which is an mp4 codec), then open up **the presets drop-down menu** to find "mobile device 480p wide".

(You can try out other compression sizes too, just check out the file sizes - estimated at the bottom - and try to keep them as small as possible.

![premiere export menu](images/videoFilePrep_0.png)

And there is your .mp4!

#### 2) .webM
To get your .webM file it is a little trickier. You can either download a plugin for Premiere (this is free to do, YouTube tutorial [here](https://www.youtube.com/watch?v=L7a5r8lbo0A) should work), or you can download a free video converter like [Miro](http://www.mirovideoconverter.com/.)

If using Miro, you drag your video into the top, then select webM from the dropdown.

![Miro Video Converter](images/miro_1.png)
