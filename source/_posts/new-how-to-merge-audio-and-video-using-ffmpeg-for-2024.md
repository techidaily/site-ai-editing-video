---
title: New How to Merge Audio and Video Using FFmpeg for 2024
date: 2024-04-24T07:08:36.675Z
updated: 2024-04-25T07:08:36.675Z
tags: 
  - ai
  - animation videos
categories: 
  - ai
description: This Article Describes New How to Merge Audio and Video Using FFmpeg for 2024
excerpt: This Article Describes New How to Merge Audio and Video Using FFmpeg for 2024
keywords: ffmpeg merge audio and video,ai animation mastering ffmpeg how to merge audio and video with ease,mastering ffmpeg how to merge audio and video with ease,5 simple tools to merge video and audio online,ai animation how to merge audio and video using ffmpeg,how to merge audio and video using ffmpeg,ai animation ai animation how to merge audio and video using ffmpeg
thumbnail: https://www.lifewire.com/thmb/ZDnyMd5y1TI-4l8Th58f2C_oJzA=/400x300/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/F8conferencelogo-7ec4475dc6624114aea076c2611df199.jpg
---

## How to Merge Audio and Video Using FFmpeg

Welcome to the world of video production! Whether you're a beginner or an experienced video creator, one of the most important skills to master is merging audio and video seamlessly. In this article, we'll focus on FFmpeg, a powerful command-line tool that can help you easily merge audio and video.

FFmpeg is open-source software that allows you to convert, edit, and stream multimedia files. It's widely used by professionals and enthusiasts and has many capabilities, including merging audio and video files. This guide will walk you through merging audio and video using FFmpeg. So, whether you're creating a YouTube video, a podcast, or a movie, you'll have the skills to make it sound and look great.

![merge audio and video with ffmpeg](https://images.wondershare.com/filmora/article-images/ffmpeg-merge-audio-and-video.JPG)

## Preparation

Are you ready to master the art of merging audio and video? Then let's dive into the world of FFmpeg, a powerful and versatile tool that can help you achieve professional results.

With FFmpeg, you can record, convert, and stream audio and video files in any format, making it a complete and cross-platform solution. It's also a great tool for decoding, encoding, transcoding, muxing, demuxing, streaming, filtering, and playing any media type.

But before we start merging video files using FFmpeg, it's important to understand the basics of container formats and video codecs. These are the building blocks of your videos, and the specific types you're working with will determine the method you'll use to merge them. So, buckle up, and let's get started!

### How To Combine Video With Two Audio Using FFmpeg

Are you looking to add multiple audio tracks to your video? With FFmpeg, you can easily combine video with two audio streams. Whether creating a foreign-language version of your video or adding an alternate audio track, this method will help you achieve professional results. This section will guide you through combining video with two audio streams using FFmpeg's command-line interface. So, let's get started!

**Mixing Two Audios Into a Video**

Combining multiple audio tracks into one video can be done easily with FFmpeg's command-line interface. In this example, we will combine two audio tracks into one video so that the voiceover will play over the background music. Here's the step-by-step process:

Step1 **Open** your command prompt or terminal and navigate to the directory where your video and audio files are located.

Step2 **Replace** "**video1.mp4**" and "**audio1.mp3**" with the names of your actual video and audio files.

_ffmpeg \\_

_\-i video1.mp4 -i audio1.mp3 \\_

Step3 The **\-c:v copy** flag tells FFmpeg to copy the video stream from the source file without re-encoding it. This helps to speed up the process and avoid quality loss.

_\-c:v copy \\_

_\-filter\_complex " \\_

Step4 The command "**amix=inputs=2:duration=longest**" tells amix to accept 2 inputs (**0:a and 1:a**) and **combine** them into an output stream called **audio\_out**, with the duration of the longest input.

_\[0:a\]\[1:a\] amix=inputs=2:duration=longest \[audio\_out\] \\_

Step5 **Map** the video stream **(0:v)** and the mixed audio stream **(audio\_out)** into the final output video.

_\-map 0:v -map "\[audio\_out\]" \\_

Step6 The **\-y flag** tells FFmpeg to overwrite the output file if it already exists.

_\-y output.mp4_

Once complete, you'll find the newly created video file with the mixed audio in the specified output location.

**Mixing Two Audios Into a Video Adjusting Volume**

We will be taking a step further and show you how to merge two audio tracks into a video while adjusting the volume of one of the audio tracks. This can be useful when you want to emphasize one audio track over the other, for example, to make the voiceover more prominent in a video.

And here's the step-by-step process:

Step1 **Start** the command by specifying the input files.

_ffmpeg \\_

 _\-i video1.mp4 -i audio1.mp3 \\_

Step2 **Use** the **filter\_complex** option to specify a filter graph.

 _\-filter\_complex " \\_

 _\[0:a\] volume=0.5 \[music\];_

Step3 **Use** the **amix** filter to take the "**music**" stream and **audio1.mp3** and **mix** them.

 _\[music\]\[1:a\] amix=inputs=2:duration=longest \[audio\_out\] \\_

 _" \\_

Step4 **Use** the **map** option to **specify** which streams from the input files should be included in the output file.

 _\-map 0:v -map "\[audio\_out\]" \\_

Step5 **Specify** the output file name as "**output.mp4**" and the **\-y flag** to overwrite the output file without asking for confirmation if it already exists.

 _\-y output.mp4_

**Mixing Two Audios Into a Video With Delay**

When creating videos, sometimes the audio needs to be synced with the video, or you want to add a delay to the audio track. Here's how to add delay to an audio track using FFmpeg.

Step1 **Use** the **adelay filter** to add delay to the audio track.

_\[1:a\] adelay=2100|2100 \[voice\];_

Step2 **Mix** the delayed audio track with the original audio track

_\[0:a\]\[voice\] amix=inputs=2:duration=longest \[audio\_out\]_

Step3 **Map** the video and audio tracks to the output file

_\-map 0:v -map "\[audio\_out\]"_

Step4 **Use** the **\-y flag** to overwrite the output file

_\-y output.mp4_

The final command would look like this:

_ffmpeg \\_

 _\-i video1.mp4 -i audio1.mp3 \\_

 _\-filter\_complex " \\_

 _\[1:a\] adelay=2100|2100 \[voice\]; \\_

 _\[0:a\]\[voice\] amix=inputs=2:duration=longest \[audio\_out\] \\_

 _" \\_

 _\-map 0:v -map "\[audio\_out\]" \\_

 _\-y output.mp4_

This command will delay the audio track by 2100 milliseconds and then mix it with the original audio track, resulting in a new video file with the delayed audio.

## It May Interest You - Merge Audio and Video Files With Filmora

While FFmpeg is a powerful tool for merging audio and video files, its learning curve can be steep for some users. If you're looking for an easier option, you may consider using video editing software like Filmora.

### What Is Filmora?

[Wondershare Filmora](https://tools.techidaily.com/wondershare/filmora/download/) is a video editing software that allows users to create professional-looking videos easily. It offers a user-friendly interface, making it an excellent option for those needing a more extensive video editing experience.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For Win 7 or later(64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For macOS 10.14 or later

This software offers an intuitive interface and a wide range of features that make it easy to merge audio and video files, even for beginners. In addition, Filmora provides various options for editing and enhancing the audio and video files, giving you more control over the final output. Filmora is a great alternative to FFmpeg for those who want to merge audio and video files quickly and easily.

### How To Combine Audio and Video Files Using Filmora

Filmora is a user-friendly video editing software that allows you to easily combine audio and video files to create a polished and professional final product. So here's the step-by-step process of combining audio and video files using Filmora.

Step1 **Import** audio and video files into Filmora using **drag-and-drop** or the "**Import Media**" button.

![filmora import media](https://images.wondershare.com/filmora/guide/get-started-with-filmora-02.png)

Step2 **Place** the media files in the timeline and **align** the video with the audio.

![filmora align media](https://images.wondershare.com/filmora/article-images/filmora-align-videos.jpg)

Step3 **Replace** the original audio by **right-clicking** the video, **selecting** "**Detach Audio**," deleting the original audio, and **replacing** it with new audio.

![filmora detach audio](https://images.wondershare.com/filmora/guide/detach-audio-windows-01.png)

Step4 **Export** the final video by selecting a format and **clicking** "**Export**," or publish directly to YouTube or burn to DVD.

![filmora export video](https://images.wondershare.com/filmora/guide/export-by-selecting-local-tab.png)

## People Also Ask

Here are some frequently asked questions regarding the merging function of FFmpeg and other related topics:

### Q1\. How To Merge Image and Video in FFmpeg?

To merge an image and a video using FFmpeg, first, use the **\-loop** option on the image to loop it for the duration of the video, then use the overlay filter to overlay the image on the video. The command would look like this:

_ffmpeg -i video.mp4 -i image.jpg -filter\_complex "\[0:v\]\[1:v\] overlay=0:0" -pix\_fmt yuv420p -c:a copy output.mp4_

This command takes the input video and image, applies the overlay filter to overlay the image on the video starting at the top left corner (**0:0**), and outputs the result to **output.mp4**. The **\-pix\_fmt yuv420p** and **\-c:a copy** options ensure compatibility with most devices.

### Q2\. Can I Merge 2 MP4 Files Into 1?

Yes, you can merge two MP4 files into one using Filmora. To do this, follow these steps:

Step1 **Open** Filmora and **import** the video files

Step2 **Drag** the videos to the timeline

Step3 **Align** the second video with the first without leaving any gaps

Step4 **Click** "**Export**" and **select** desired settings

Step5 **Click** "**Export**" again to **save** the combined video on your computer.

### Q3\. How Can I Merge the Video and Subtitle?

To merge video and subtitle in Filmora, follow these steps:

Step1 **Open** Filmora and **import** your SRT subtitle file.

Step2 **Place** the SRT file on the timeline and **right-click** on it. Select "**Advanced Edit**" from the options.

Step3 **Adjust** the subtitle's time code, text, color, font, and other settings. When finished, **choose** "**Export Subtitle file**" to save the changes.

Still want to learn more tricks about adding subtitles to your video? Check out the video below:

## Conclusion

Using FFmpeg and Filmora, you can easily combine video with audio, merge multiple video files, and add subtitles to your videos. Both tools offer different features and learning curves, so it's important to understand what you need before choosing one. Filmora is a great option for beginners and those who want a user-friendly interface, while FFmpeg is a powerful command-line tool for advanced users.

* "**\-i INPUT\_FILE.mp4**" flag specifies INPUT\_FILE.mp4 as the input source.
* "**\-i AUDIO.wav**," tells FFmpeg to take AUDIO.wav as an input source.
* The "**\-c:v copy**" flag is a short form of "**\-codec:v copy**," which means to copy the video stream from the source files to the destination file.
* The "**\-c:a aac**" flag means selecting all the audio streams from the source files and then encoding them with the AAC encoder.
* "**mp4**" specifies the name of the output file.

Step3 In case you don't want any audio conversion, **drop** the aac part in the command and **replace** it with copy; the command would look like this:

_ffmpeg -i INPUT\_FILE.mp4 -i AUDIO.aac -c:v copy -c:a copy OUTPUT\_FILE.mp4_

\-->

### How To Combine Video With Two Audio Using FFmpeg

Are you looking to add multiple audio tracks to your video? With FFmpeg, you can easily combine video with two audio streams. Whether creating a foreign-language version of your video or adding an alternate audio track, this method will help you achieve professional results. This section will guide you through combining video with two audio streams using FFmpeg's command-line interface. So, let's get started!

**Mixing Two Audios Into a Video**

Combining multiple audio tracks into one video can be done easily with FFmpeg's command-line interface. In this example, we will combine two audio tracks into one video so that the voiceover will play over the background music. Here's the step-by-step process:

Step1 **Open** your command prompt or terminal and navigate to the directory where your video and audio files are located.

Step2 **Replace** "**video1.mp4**" and "**audio1.mp3**" with the names of your actual video and audio files.

_ffmpeg \\_

_\-i video1.mp4 -i audio1.mp3 \\_

Step3 The **\-c:v copy** flag tells FFmpeg to copy the video stream from the source file without re-encoding it. This helps to speed up the process and avoid quality loss.

_\-c:v copy \\_

_\-filter\_complex " \\_

Step4 The command "**amix=inputs=2:duration=longest**" tells amix to accept 2 inputs (**0:a and 1:a**) and **combine** them into an output stream called **audio\_out**, with the duration of the longest input.

_\[0:a\]\[1:a\] amix=inputs=2:duration=longest \[audio\_out\] \\_

Step5 **Map** the video stream **(0:v)** and the mixed audio stream **(audio\_out)** into the final output video.

_\-map 0:v -map "\[audio\_out\]" \\_

Step6 The **\-y flag** tells FFmpeg to overwrite the output file if it already exists.

_\-y output.mp4_

Once complete, you'll find the newly created video file with the mixed audio in the specified output location.

**Mixing Two Audios Into a Video Adjusting Volume**

We will be taking a step further and show you how to merge two audio tracks into a video while adjusting the volume of one of the audio tracks. This can be useful when you want to emphasize one audio track over the other, for example, to make the voiceover more prominent in a video.

And here's the step-by-step process:

Step1 **Start** the command by specifying the input files.

_ffmpeg \\_

 _\-i video1.mp4 -i audio1.mp3 \\_

Step2 **Use** the **filter\_complex** option to specify a filter graph.

 _\-filter\_complex " \\_

 _\[0:a\] volume=0.5 \[music\];_

Step3 **Use** the **amix** filter to take the "**music**" stream and **audio1.mp3** and **mix** them.

 _\[music\]\[1:a\] amix=inputs=2:duration=longest \[audio\_out\] \\_

 _" \\_

Step4 **Use** the **map** option to **specify** which streams from the input files should be included in the output file.

 _\-map 0:v -map "\[audio\_out\]" \\_

Step5 **Specify** the output file name as "**output.mp4**" and the **\-y flag** to overwrite the output file without asking for confirmation if it already exists.

 _\-y output.mp4_

**Mixing Two Audios Into a Video With Delay**

When creating videos, sometimes the audio needs to be synced with the video, or you want to add a delay to the audio track. Here's how to add delay to an audio track using FFmpeg.

Step1 **Use** the **adelay filter** to add delay to the audio track.

_\[1:a\] adelay=2100|2100 \[voice\];_

Step2 **Mix** the delayed audio track with the original audio track

_\[0:a\]\[voice\] amix=inputs=2:duration=longest \[audio\_out\]_

Step3 **Map** the video and audio tracks to the output file

_\-map 0:v -map "\[audio\_out\]"_

Step4 **Use** the **\-y flag** to overwrite the output file

_\-y output.mp4_

The final command would look like this:

_ffmpeg \\_

 _\-i video1.mp4 -i audio1.mp3 \\_

 _\-filter\_complex " \\_

 _\[1:a\] adelay=2100|2100 \[voice\]; \\_

 _\[0:a\]\[voice\] amix=inputs=2:duration=longest \[audio\_out\] \\_

 _" \\_

 _\-map 0:v -map "\[audio\_out\]" \\_

 _\-y output.mp4_

This command will delay the audio track by 2100 milliseconds and then mix it with the original audio track, resulting in a new video file with the delayed audio.

## It May Interest You - Merge Audio and Video Files With Filmora

While FFmpeg is a powerful tool for merging audio and video files, its learning curve can be steep for some users. If you're looking for an easier option, you may consider using video editing software like Filmora.

### What Is Filmora?

[Wondershare Filmora](https://tools.techidaily.com/wondershare/filmora/download/) is a video editing software that allows users to create professional-looking videos easily. It offers a user-friendly interface, making it an excellent option for those needing a more extensive video editing experience.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For Win 7 or later(64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For macOS 10.14 or later

This software offers an intuitive interface and a wide range of features that make it easy to merge audio and video files, even for beginners. In addition, Filmora provides various options for editing and enhancing the audio and video files, giving you more control over the final output. Filmora is a great alternative to FFmpeg for those who want to merge audio and video files quickly and easily.

### How To Combine Audio and Video Files Using Filmora

Filmora is a user-friendly video editing software that allows you to easily combine audio and video files to create a polished and professional final product. So here's the step-by-step process of combining audio and video files using Filmora.

Step1 **Import** audio and video files into Filmora using **drag-and-drop** or the "**Import Media**" button.

![filmora import media](https://images.wondershare.com/filmora/guide/get-started-with-filmora-02.png)

Step2 **Place** the media files in the timeline and **align** the video with the audio.

![filmora align media](https://images.wondershare.com/filmora/article-images/filmora-align-videos.jpg)

Step3 **Replace** the original audio by **right-clicking** the video, **selecting** "**Detach Audio**," deleting the original audio, and **replacing** it with new audio.

![filmora detach audio](https://images.wondershare.com/filmora/guide/detach-audio-windows-01.png)

Step4 **Export** the final video by selecting a format and **clicking** "**Export**," or publish directly to YouTube or burn to DVD.

![filmora export video](https://images.wondershare.com/filmora/guide/export-by-selecting-local-tab.png)

## People Also Ask

Here are some frequently asked questions regarding the merging function of FFmpeg and other related topics:

### Q1\. How To Merge Image and Video in FFmpeg?

To merge an image and a video using FFmpeg, first, use the **\-loop** option on the image to loop it for the duration of the video, then use the overlay filter to overlay the image on the video. The command would look like this:

_ffmpeg -i video.mp4 -i image.jpg -filter\_complex "\[0:v\]\[1:v\] overlay=0:0" -pix\_fmt yuv420p -c:a copy output.mp4_

This command takes the input video and image, applies the overlay filter to overlay the image on the video starting at the top left corner (**0:0**), and outputs the result to **output.mp4**. The **\-pix\_fmt yuv420p** and **\-c:a copy** options ensure compatibility with most devices.

### Q2\. Can I Merge 2 MP4 Files Into 1?

Yes, you can merge two MP4 files into one using Filmora. To do this, follow these steps:

Step1 **Open** Filmora and **import** the video files

Step2 **Drag** the videos to the timeline

Step3 **Align** the second video with the first without leaving any gaps

Step4 **Click** "**Export**" and **select** desired settings

Step5 **Click** "**Export**" again to **save** the combined video on your computer.

### Q3\. How Can I Merge the Video and Subtitle?

To merge video and subtitle in Filmora, follow these steps:

Step1 **Open** Filmora and **import** your SRT subtitle file.

Step2 **Place** the SRT file on the timeline and **right-click** on it. Select "**Advanced Edit**" from the options.

Step3 **Adjust** the subtitle's time code, text, color, font, and other settings. When finished, **choose** "**Export Subtitle file**" to save the changes.

Still want to learn more tricks about adding subtitles to your video? Check out the video below:

## Conclusion

Using FFmpeg and Filmora, you can easily combine video with audio, merge multiple video files, and add subtitles to your videos. Both tools offer different features and learning curves, so it's important to understand what you need before choosing one. Filmora is a great option for beginners and those who want a user-friendly interface, while FFmpeg is a powerful command-line tool for advanced users.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

## A Guide to Use Distortion Effect in Premeiere Pro

##### Create High-Quality Video - Wondershare Filmora

An easy and powerful YouTube video editor

Numerous video and audio effects to choose from

Detailed tutorials are provided by the official channel

[Try It Free](https://tools.techidaily.com/wondershare/filmora/download/) [Try It Free](https://tools.techidaily.com/wondershare/filmora/download/)

Premiere Pro is one of the most popular timeline-based video editing software, with over 9 million users. It’s the successor to Adobe Premiere, and it comes with cool distortion effects. We'll look at Premiere Pro distortion effects and how to use them.

#### In this article

01 [How to Use Distortion Effect in Premiere Pro?](#part1)

02 [Bonus! Free Distortion Effects for Premiere Pro](#part2)

Adobe Premiere Pro offers a wide variety of beneficial editing tools and effects. Below are some of the impressive distortion effects you'll find in Premiere Pro and how to use them in your project.

#### 1\. Corner Pin Effect

This effect distorts your image by simply changing the position of its corners. You can use the Corner pin effect to twist, skew, shrink, or stretch an image. Additionally, you can use it to simulate movement or perspective pivoting from the edge of your clip like a door opening.

You can directly manipulate the properties of the Corner Pin effect in the Program monitor by clicking the Transform right next to Corner Pin. To adjust the properties, drag one of the corner handles.

1. To use this effect, open Premiere Pro and click File. Choose Import from the drop-down menu. The File Explorer window will open and allow you to find your footage. Select the video file you want to import, then click Open.
2. Go to Effects Control and click Distortion. Choose Corner Pin Effect from the drop-down menu.

![use corner pin effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-1.png)

1. You can now pin each corner from its original point to another specific point by adjusting the slider on the Upper Left, Upper Right, Lower Left, and Lower Right. You can also highlight your selection tool when working with the Corner Pin effect.

![use corner pin effect in premiere pro - pin corner](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-2.png)

#### 2\. Lens Distortion Effect

This distortion effect Premiere Pro simulates the distorted lens through which people view the clip.

1\. Go to Effects Control>Distortion>Lens Distortion Effect.

2\. Choose the settings you want to use from the available options and adjust the slider.

* The Vertical and Horizontal Decentering control displaces the lens' focal and makes the image bend and smear. The image will wrap in on itself at extreme settings.
* The Curvature setting alters the curvature of the lens. You can specify a positive value to make the image convex, while the negative value makes the image concave.
* The Vertical and Horizontal Prism FX setting created results similar to horizontal decentering and vertical, but the image does not wrap in on itself at extreme values.
* Use the Fill Color option to specify the background color, and Fill Alpha to make your background transparent.

![lens distortion effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-3.png)

#### 3\. Magnify Effect

This effect allows you to enlarge a selected area of your clip. The Magnify effect acts as a magnifying glass set over an area of an image. You can also use this effect to scale the whole image far beyond 100 percent and still maintain resolution.

1\. To use this effect, go to Effect Control>Distortion>Magnify.

2\. Next, go to the left side of the Effects Control panel and make the necessary adjustments to suit your preferences.

* Shape: This control specifies the magnified area shape.
* Center: The Center control allows you to specify the center of the magnified section.
* Magnification: This setting lets users specify the percentage of the magnification of the area they have selected, while the values represent the scale percentage.
* Link: The Link control allows you to specify how the effect will link the Size, Feather, and Magnification amount, to enable them to decrease or increase proportionally. You will disable the Resize Layer option if you set the Link control to any of the available settings except None. Setting the Link control to any setting except None disables Resize Layer. Size & Feather To Magnification allows you to specify that the edge feather and size of the magnified section decrease or increase proportionally regarding the magnification adjustment.
* Size: This control allows you to specify the magnified area size in pixels.
* Feather: With the Feather option, you can specify the amount of feather the effect applies to the magnified area edge. Lower values will sharpen the edge. Higher values will soften the edge while blending the edge with the layer that's behind it.
* Opacity: This control allows you to specify the transparency of the magnified region.
* Scaling: Use this option to specify the kind of scaling the effect is using to magnify an image.
* Blending Mode: Use this control to specify the blend mode the effect will use to combine the original clip with the magnified area. The None option shows transparent pixels around the magnified section.
* Resize Layer: Selecting this option means the effect will only use the boundaries as the clip's edge when the magnified region extends beyond the original boundaries of the clip. Deselecting the Resize Layer means that the boundaries of the clip will crop any area of your image outside the bounding box of the original clip.

![magnify effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-4.png)

#### 4\. Mirror Effect

This distortion Premiere Pro effect splits an image along a line while reflecting one side onto the other. Where the reflection appears and which side will be reflected is determined by the reflection angles.

1\. Head over to Effect Control>Distortion>Mirror to use this effect.

2\. Adjust the controls until you get the results you desire.

* Reflection Angle: With the Reflection Angle control, you can specify the angle of reflection and where it appears on the clip. A zero-degree angle reflects the left-hand side on the right.
* Reflection Center: This control allows you to specify the position of the line. You need to click the box, then drag the resulting crosshair up to the area in the image where you would like to place the line.

![mirror effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-5.png)

#### 5\. Offset Effect

This effect pans your image within a clip, and visual details pushed off one side of this image will appear on the opposite side. You have to perform the offset with subpixel precision at the best quality.

Also, you can use Offset with a combination of other effects. Head over to Effect Control>Distortion>Offset to use this effect.

![offset effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-6.png)

#### 6\. Spherize Effect

The Spherize effect allows users to wrap a video clip around a spherical shape. You can use it to give texts and objects a three-dimensional effect. Go to Effect Control>Distortion>Spherize and adjust the radius and center of the sphere.

![spherize effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-7.png)

#### 7\. Transform Effect

This effect applies 2-dimensional geometric transformations to your clip. You can use this effect to skew clips along any axis.

1\. Go to Effect Control>Distortion>Transform to apply this effect to your clip.

2\. Use Transform settings to adjust Opacity, Skew, Rotation, Scale, Anchor Point, and more.

![transform effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-8.png)

#### 8\. Turbulent Displace Effect

This fun effect utilizes fractal noise to create turbulent Premiere Pro distortion effects in your image. You can use the Turbulent Displace effect to add movement to your clip.

1\. Head to Effect Control>Distortion>Turbulent Displace.

2\. Adjust the following controls:

* Displacement
* Amount
* Size
* Offset (Turbulence)
* Complexity
* Evolution
* Pinning
* Resize Layer
* Antialiasing For Best Quality

![Turbulent Displace effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-9.png)

#### 9\. Twirl Effect

The Twirl effect allows you to rotate your clip around its center. It rotates the image more sharply in the middle than at the edge. You can use it on faces to make a funny clip. Navigate to Effect Control>Distortion>Twirl to start using this effect. Next, use the settings to adjust how much angle it twirls and the radius.

![Twirl effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-10.png)

#### 10\. Wave Warp Effect

This effect is one of the most popular Premiere Pro distortion effects. It generates the appearance of a wave as it's traveling across an image. The Wave Warp effect allows you to produce various wave shapes, including sine, circular, and square waves.

It's automatically animated at a steady speed across the time range, and that's without frames. You need to set keyframes to vary speeds.

1\. Head to Effect Control>Distortion>Wave Warp to apply this effect in your video clip.

2\. Now, change the wave speed, direction, height, width, and type to suit your preference.

![Wave Warp effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-11.png)

## Bonus! Free Distortion Effects for Premiere Pro

### 1\. Liquid Distortion Effect

This effect can distort the content in a clip and can be used to shift into the next clip. It could be utilized in editing or used as a transition.

![free distortion effect for premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-12.png)

### 2\. Earthquake Effect

This effect adds a shaking motion to the video clip you add it to; it works as a transition but could also be a useful editing tool.

![free distortion effect for premiere pro - earthquake effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-13.png)

### 3\. Glass Effect

This effect can add various blurs to the video clip and be used to transition from one clip to the next.

![free distortion effect for premiere pro - glass effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-14.png)

### 4\. TV Effect

This effect imitates the view of a television being turned on or off. You can use it to introduce a new video clip. It would also be a great start or end to the entire video.

![free distortion effect for premiere pro - TV effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-15.png)

### 5\. Glitch Effect

This effect adds a glitch to the video clip. You can use it in editing or as a transition from one clip to the next.

![free distortion effect for premiere pro - Glitch effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-16.png)

## Conclusion

**●** You can add any of these Premiere Pro distortion effects to make your videos more catchy. In turn, they will get more attention and views. Premiere Pro comes with tons of distortion effects and a responsive interface.

[Try It Free](https://tools.techidaily.com/wondershare/filmora/download/) [Try It Free](https://tools.techidaily.com/wondershare/filmora/download/)

Premiere Pro is one of the most popular timeline-based video editing software, with over 9 million users. It’s the successor to Adobe Premiere, and it comes with cool distortion effects. We'll look at Premiere Pro distortion effects and how to use them.

#### In this article

01 [How to Use Distortion Effect in Premiere Pro?](#part1)

02 [Bonus! Free Distortion Effects for Premiere Pro](#part2)

Adobe Premiere Pro offers a wide variety of beneficial editing tools and effects. Below are some of the impressive distortion effects you'll find in Premiere Pro and how to use them in your project.

#### 1\. Corner Pin Effect

This effect distorts your image by simply changing the position of its corners. You can use the Corner pin effect to twist, skew, shrink, or stretch an image. Additionally, you can use it to simulate movement or perspective pivoting from the edge of your clip like a door opening.

You can directly manipulate the properties of the Corner Pin effect in the Program monitor by clicking the Transform right next to Corner Pin. To adjust the properties, drag one of the corner handles.

1. To use this effect, open Premiere Pro and click File. Choose Import from the drop-down menu. The File Explorer window will open and allow you to find your footage. Select the video file you want to import, then click Open.
2. Go to Effects Control and click Distortion. Choose Corner Pin Effect from the drop-down menu.

![use corner pin effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-1.png)

1. You can now pin each corner from its original point to another specific point by adjusting the slider on the Upper Left, Upper Right, Lower Left, and Lower Right. You can also highlight your selection tool when working with the Corner Pin effect.

![use corner pin effect in premiere pro - pin corner](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-2.png)

#### 2\. Lens Distortion Effect

This distortion effect Premiere Pro simulates the distorted lens through which people view the clip.

1\. Go to Effects Control>Distortion>Lens Distortion Effect.

2\. Choose the settings you want to use from the available options and adjust the slider.

* The Vertical and Horizontal Decentering control displaces the lens' focal and makes the image bend and smear. The image will wrap in on itself at extreme settings.
* The Curvature setting alters the curvature of the lens. You can specify a positive value to make the image convex, while the negative value makes the image concave.
* The Vertical and Horizontal Prism FX setting created results similar to horizontal decentering and vertical, but the image does not wrap in on itself at extreme values.
* Use the Fill Color option to specify the background color, and Fill Alpha to make your background transparent.

![lens distortion effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-3.png)

#### 3\. Magnify Effect

This effect allows you to enlarge a selected area of your clip. The Magnify effect acts as a magnifying glass set over an area of an image. You can also use this effect to scale the whole image far beyond 100 percent and still maintain resolution.

1\. To use this effect, go to Effect Control>Distortion>Magnify.

2\. Next, go to the left side of the Effects Control panel and make the necessary adjustments to suit your preferences.

* Shape: This control specifies the magnified area shape.
* Center: The Center control allows you to specify the center of the magnified section.
* Magnification: This setting lets users specify the percentage of the magnification of the area they have selected, while the values represent the scale percentage.
* Link: The Link control allows you to specify how the effect will link the Size, Feather, and Magnification amount, to enable them to decrease or increase proportionally. You will disable the Resize Layer option if you set the Link control to any of the available settings except None. Setting the Link control to any setting except None disables Resize Layer. Size & Feather To Magnification allows you to specify that the edge feather and size of the magnified section decrease or increase proportionally regarding the magnification adjustment.
* Size: This control allows you to specify the magnified area size in pixels.
* Feather: With the Feather option, you can specify the amount of feather the effect applies to the magnified area edge. Lower values will sharpen the edge. Higher values will soften the edge while blending the edge with the layer that's behind it.
* Opacity: This control allows you to specify the transparency of the magnified region.
* Scaling: Use this option to specify the kind of scaling the effect is using to magnify an image.
* Blending Mode: Use this control to specify the blend mode the effect will use to combine the original clip with the magnified area. The None option shows transparent pixels around the magnified section.
* Resize Layer: Selecting this option means the effect will only use the boundaries as the clip's edge when the magnified region extends beyond the original boundaries of the clip. Deselecting the Resize Layer means that the boundaries of the clip will crop any area of your image outside the bounding box of the original clip.

![magnify effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-4.png)

#### 4\. Mirror Effect

This distortion Premiere Pro effect splits an image along a line while reflecting one side onto the other. Where the reflection appears and which side will be reflected is determined by the reflection angles.

1\. Head over to Effect Control>Distortion>Mirror to use this effect.

2\. Adjust the controls until you get the results you desire.

* Reflection Angle: With the Reflection Angle control, you can specify the angle of reflection and where it appears on the clip. A zero-degree angle reflects the left-hand side on the right.
* Reflection Center: This control allows you to specify the position of the line. You need to click the box, then drag the resulting crosshair up to the area in the image where you would like to place the line.

![mirror effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-5.png)

#### 5\. Offset Effect

This effect pans your image within a clip, and visual details pushed off one side of this image will appear on the opposite side. You have to perform the offset with subpixel precision at the best quality.

Also, you can use Offset with a combination of other effects. Head over to Effect Control>Distortion>Offset to use this effect.

![offset effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-6.png)

#### 6\. Spherize Effect

The Spherize effect allows users to wrap a video clip around a spherical shape. You can use it to give texts and objects a three-dimensional effect. Go to Effect Control>Distortion>Spherize and adjust the radius and center of the sphere.

![spherize effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-7.png)

#### 7\. Transform Effect

This effect applies 2-dimensional geometric transformations to your clip. You can use this effect to skew clips along any axis.

1\. Go to Effect Control>Distortion>Transform to apply this effect to your clip.

2\. Use Transform settings to adjust Opacity, Skew, Rotation, Scale, Anchor Point, and more.

![transform effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-8.png)

#### 8\. Turbulent Displace Effect

This fun effect utilizes fractal noise to create turbulent Premiere Pro distortion effects in your image. You can use the Turbulent Displace effect to add movement to your clip.

1\. Head to Effect Control>Distortion>Turbulent Displace.

2\. Adjust the following controls:

* Displacement
* Amount
* Size
* Offset (Turbulence)
* Complexity
* Evolution
* Pinning
* Resize Layer
* Antialiasing For Best Quality

![Turbulent Displace effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-9.png)

#### 9\. Twirl Effect

The Twirl effect allows you to rotate your clip around its center. It rotates the image more sharply in the middle than at the edge. You can use it on faces to make a funny clip. Navigate to Effect Control>Distortion>Twirl to start using this effect. Next, use the settings to adjust how much angle it twirls and the radius.

![Twirl effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-10.png)

#### 10\. Wave Warp Effect

This effect is one of the most popular Premiere Pro distortion effects. It generates the appearance of a wave as it's traveling across an image. The Wave Warp effect allows you to produce various wave shapes, including sine, circular, and square waves.

It's automatically animated at a steady speed across the time range, and that's without frames. You need to set keyframes to vary speeds.

1\. Head to Effect Control>Distortion>Wave Warp to apply this effect in your video clip.

2\. Now, change the wave speed, direction, height, width, and type to suit your preference.

![Wave Warp effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-11.png)

## Bonus! Free Distortion Effects for Premiere Pro

### 1\. Liquid Distortion Effect

This effect can distort the content in a clip and can be used to shift into the next clip. It could be utilized in editing or used as a transition.

![free distortion effect for premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-12.png)

### 2\. Earthquake Effect

This effect adds a shaking motion to the video clip you add it to; it works as a transition but could also be a useful editing tool.

![free distortion effect for premiere pro - earthquake effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-13.png)

### 3\. Glass Effect

This effect can add various blurs to the video clip and be used to transition from one clip to the next.

![free distortion effect for premiere pro - glass effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-14.png)

### 4\. TV Effect

This effect imitates the view of a television being turned on or off. You can use it to introduce a new video clip. It would also be a great start or end to the entire video.

![free distortion effect for premiere pro - TV effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-15.png)

### 5\. Glitch Effect

This effect adds a glitch to the video clip. You can use it in editing or as a transition from one clip to the next.

![free distortion effect for premiere pro - Glitch effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-16.png)

## Conclusion

**●** You can add any of these Premiere Pro distortion effects to make your videos more catchy. In turn, they will get more attention and views. Premiere Pro comes with tons of distortion effects and a responsive interface.

[Try It Free](https://tools.techidaily.com/wondershare/filmora/download/) [Try It Free](https://tools.techidaily.com/wondershare/filmora/download/)

Premiere Pro is one of the most popular timeline-based video editing software, with over 9 million users. It’s the successor to Adobe Premiere, and it comes with cool distortion effects. We'll look at Premiere Pro distortion effects and how to use them.

#### In this article

01 [How to Use Distortion Effect in Premiere Pro?](#part1)

02 [Bonus! Free Distortion Effects for Premiere Pro](#part2)

Adobe Premiere Pro offers a wide variety of beneficial editing tools and effects. Below are some of the impressive distortion effects you'll find in Premiere Pro and how to use them in your project.

#### 1\. Corner Pin Effect

This effect distorts your image by simply changing the position of its corners. You can use the Corner pin effect to twist, skew, shrink, or stretch an image. Additionally, you can use it to simulate movement or perspective pivoting from the edge of your clip like a door opening.

You can directly manipulate the properties of the Corner Pin effect in the Program monitor by clicking the Transform right next to Corner Pin. To adjust the properties, drag one of the corner handles.

1. To use this effect, open Premiere Pro and click File. Choose Import from the drop-down menu. The File Explorer window will open and allow you to find your footage. Select the video file you want to import, then click Open.
2. Go to Effects Control and click Distortion. Choose Corner Pin Effect from the drop-down menu.

![use corner pin effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-1.png)

1. You can now pin each corner from its original point to another specific point by adjusting the slider on the Upper Left, Upper Right, Lower Left, and Lower Right. You can also highlight your selection tool when working with the Corner Pin effect.

![use corner pin effect in premiere pro - pin corner](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-2.png)

#### 2\. Lens Distortion Effect

This distortion effect Premiere Pro simulates the distorted lens through which people view the clip.

1\. Go to Effects Control>Distortion>Lens Distortion Effect.

2\. Choose the settings you want to use from the available options and adjust the slider.

* The Vertical and Horizontal Decentering control displaces the lens' focal and makes the image bend and smear. The image will wrap in on itself at extreme settings.
* The Curvature setting alters the curvature of the lens. You can specify a positive value to make the image convex, while the negative value makes the image concave.
* The Vertical and Horizontal Prism FX setting created results similar to horizontal decentering and vertical, but the image does not wrap in on itself at extreme values.
* Use the Fill Color option to specify the background color, and Fill Alpha to make your background transparent.

![lens distortion effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-3.png)

#### 3\. Magnify Effect

This effect allows you to enlarge a selected area of your clip. The Magnify effect acts as a magnifying glass set over an area of an image. You can also use this effect to scale the whole image far beyond 100 percent and still maintain resolution.

1\. To use this effect, go to Effect Control>Distortion>Magnify.

2\. Next, go to the left side of the Effects Control panel and make the necessary adjustments to suit your preferences.

* Shape: This control specifies the magnified area shape.
* Center: The Center control allows you to specify the center of the magnified section.
* Magnification: This setting lets users specify the percentage of the magnification of the area they have selected, while the values represent the scale percentage.
* Link: The Link control allows you to specify how the effect will link the Size, Feather, and Magnification amount, to enable them to decrease or increase proportionally. You will disable the Resize Layer option if you set the Link control to any of the available settings except None. Setting the Link control to any setting except None disables Resize Layer. Size & Feather To Magnification allows you to specify that the edge feather and size of the magnified section decrease or increase proportionally regarding the magnification adjustment.
* Size: This control allows you to specify the magnified area size in pixels.
* Feather: With the Feather option, you can specify the amount of feather the effect applies to the magnified area edge. Lower values will sharpen the edge. Higher values will soften the edge while blending the edge with the layer that's behind it.
* Opacity: This control allows you to specify the transparency of the magnified region.
* Scaling: Use this option to specify the kind of scaling the effect is using to magnify an image.
* Blending Mode: Use this control to specify the blend mode the effect will use to combine the original clip with the magnified area. The None option shows transparent pixels around the magnified section.
* Resize Layer: Selecting this option means the effect will only use the boundaries as the clip's edge when the magnified region extends beyond the original boundaries of the clip. Deselecting the Resize Layer means that the boundaries of the clip will crop any area of your image outside the bounding box of the original clip.

![magnify effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-4.png)

#### 4\. Mirror Effect

This distortion Premiere Pro effect splits an image along a line while reflecting one side onto the other. Where the reflection appears and which side will be reflected is determined by the reflection angles.

1\. Head over to Effect Control>Distortion>Mirror to use this effect.

2\. Adjust the controls until you get the results you desire.

* Reflection Angle: With the Reflection Angle control, you can specify the angle of reflection and where it appears on the clip. A zero-degree angle reflects the left-hand side on the right.
* Reflection Center: This control allows you to specify the position of the line. You need to click the box, then drag the resulting crosshair up to the area in the image where you would like to place the line.

![mirror effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-5.png)

#### 5\. Offset Effect

This effect pans your image within a clip, and visual details pushed off one side of this image will appear on the opposite side. You have to perform the offset with subpixel precision at the best quality.

Also, you can use Offset with a combination of other effects. Head over to Effect Control>Distortion>Offset to use this effect.

![offset effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-6.png)

#### 6\. Spherize Effect

The Spherize effect allows users to wrap a video clip around a spherical shape. You can use it to give texts and objects a three-dimensional effect. Go to Effect Control>Distortion>Spherize and adjust the radius and center of the sphere.

![spherize effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-7.png)

#### 7\. Transform Effect

This effect applies 2-dimensional geometric transformations to your clip. You can use this effect to skew clips along any axis.

1\. Go to Effect Control>Distortion>Transform to apply this effect to your clip.

2\. Use Transform settings to adjust Opacity, Skew, Rotation, Scale, Anchor Point, and more.

![transform effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-8.png)

#### 8\. Turbulent Displace Effect

This fun effect utilizes fractal noise to create turbulent Premiere Pro distortion effects in your image. You can use the Turbulent Displace effect to add movement to your clip.

1\. Head to Effect Control>Distortion>Turbulent Displace.

2\. Adjust the following controls:

* Displacement
* Amount
* Size
* Offset (Turbulence)
* Complexity
* Evolution
* Pinning
* Resize Layer
* Antialiasing For Best Quality

![Turbulent Displace effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-9.png)

#### 9\. Twirl Effect

The Twirl effect allows you to rotate your clip around its center. It rotates the image more sharply in the middle than at the edge. You can use it on faces to make a funny clip. Navigate to Effect Control>Distortion>Twirl to start using this effect. Next, use the settings to adjust how much angle it twirls and the radius.

![Twirl effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-10.png)

#### 10\. Wave Warp Effect

This effect is one of the most popular Premiere Pro distortion effects. It generates the appearance of a wave as it's traveling across an image. The Wave Warp effect allows you to produce various wave shapes, including sine, circular, and square waves.

It's automatically animated at a steady speed across the time range, and that's without frames. You need to set keyframes to vary speeds.

1\. Head to Effect Control>Distortion>Wave Warp to apply this effect in your video clip.

2\. Now, change the wave speed, direction, height, width, and type to suit your preference.

![Wave Warp effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-11.png)

## Bonus! Free Distortion Effects for Premiere Pro

### 1\. Liquid Distortion Effect

This effect can distort the content in a clip and can be used to shift into the next clip. It could be utilized in editing or used as a transition.

![free distortion effect for premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-12.png)

### 2\. Earthquake Effect

This effect adds a shaking motion to the video clip you add it to; it works as a transition but could also be a useful editing tool.

![free distortion effect for premiere pro - earthquake effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-13.png)

### 3\. Glass Effect

This effect can add various blurs to the video clip and be used to transition from one clip to the next.

![free distortion effect for premiere pro - glass effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-14.png)

### 4\. TV Effect

This effect imitates the view of a television being turned on or off. You can use it to introduce a new video clip. It would also be a great start or end to the entire video.

![free distortion effect for premiere pro - TV effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-15.png)

### 5\. Glitch Effect

This effect adds a glitch to the video clip. You can use it in editing or as a transition from one clip to the next.

![free distortion effect for premiere pro - Glitch effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-16.png)

## Conclusion

**●** You can add any of these Premiere Pro distortion effects to make your videos more catchy. In turn, they will get more attention and views. Premiere Pro comes with tons of distortion effects and a responsive interface.

[Try It Free](https://tools.techidaily.com/wondershare/filmora/download/) [Try It Free](https://tools.techidaily.com/wondershare/filmora/download/)

Premiere Pro is one of the most popular timeline-based video editing software, with over 9 million users. It’s the successor to Adobe Premiere, and it comes with cool distortion effects. We'll look at Premiere Pro distortion effects and how to use them.

#### In this article

01 [How to Use Distortion Effect in Premiere Pro?](#part1)

02 [Bonus! Free Distortion Effects for Premiere Pro](#part2)

Adobe Premiere Pro offers a wide variety of beneficial editing tools and effects. Below are some of the impressive distortion effects you'll find in Premiere Pro and how to use them in your project.

#### 1\. Corner Pin Effect

This effect distorts your image by simply changing the position of its corners. You can use the Corner pin effect to twist, skew, shrink, or stretch an image. Additionally, you can use it to simulate movement or perspective pivoting from the edge of your clip like a door opening.

You can directly manipulate the properties of the Corner Pin effect in the Program monitor by clicking the Transform right next to Corner Pin. To adjust the properties, drag one of the corner handles.

1. To use this effect, open Premiere Pro and click File. Choose Import from the drop-down menu. The File Explorer window will open and allow you to find your footage. Select the video file you want to import, then click Open.
2. Go to Effects Control and click Distortion. Choose Corner Pin Effect from the drop-down menu.

![use corner pin effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-1.png)

1. You can now pin each corner from its original point to another specific point by adjusting the slider on the Upper Left, Upper Right, Lower Left, and Lower Right. You can also highlight your selection tool when working with the Corner Pin effect.

![use corner pin effect in premiere pro - pin corner](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-2.png)

#### 2\. Lens Distortion Effect

This distortion effect Premiere Pro simulates the distorted lens through which people view the clip.

1\. Go to Effects Control>Distortion>Lens Distortion Effect.

2\. Choose the settings you want to use from the available options and adjust the slider.

* The Vertical and Horizontal Decentering control displaces the lens' focal and makes the image bend and smear. The image will wrap in on itself at extreme settings.
* The Curvature setting alters the curvature of the lens. You can specify a positive value to make the image convex, while the negative value makes the image concave.
* The Vertical and Horizontal Prism FX setting created results similar to horizontal decentering and vertical, but the image does not wrap in on itself at extreme values.
* Use the Fill Color option to specify the background color, and Fill Alpha to make your background transparent.

![lens distortion effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-3.png)

#### 3\. Magnify Effect

This effect allows you to enlarge a selected area of your clip. The Magnify effect acts as a magnifying glass set over an area of an image. You can also use this effect to scale the whole image far beyond 100 percent and still maintain resolution.

1\. To use this effect, go to Effect Control>Distortion>Magnify.

2\. Next, go to the left side of the Effects Control panel and make the necessary adjustments to suit your preferences.

* Shape: This control specifies the magnified area shape.
* Center: The Center control allows you to specify the center of the magnified section.
* Magnification: This setting lets users specify the percentage of the magnification of the area they have selected, while the values represent the scale percentage.
* Link: The Link control allows you to specify how the effect will link the Size, Feather, and Magnification amount, to enable them to decrease or increase proportionally. You will disable the Resize Layer option if you set the Link control to any of the available settings except None. Setting the Link control to any setting except None disables Resize Layer. Size & Feather To Magnification allows you to specify that the edge feather and size of the magnified section decrease or increase proportionally regarding the magnification adjustment.
* Size: This control allows you to specify the magnified area size in pixels.
* Feather: With the Feather option, you can specify the amount of feather the effect applies to the magnified area edge. Lower values will sharpen the edge. Higher values will soften the edge while blending the edge with the layer that's behind it.
* Opacity: This control allows you to specify the transparency of the magnified region.
* Scaling: Use this option to specify the kind of scaling the effect is using to magnify an image.
* Blending Mode: Use this control to specify the blend mode the effect will use to combine the original clip with the magnified area. The None option shows transparent pixels around the magnified section.
* Resize Layer: Selecting this option means the effect will only use the boundaries as the clip's edge when the magnified region extends beyond the original boundaries of the clip. Deselecting the Resize Layer means that the boundaries of the clip will crop any area of your image outside the bounding box of the original clip.

![magnify effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-4.png)

#### 4\. Mirror Effect

This distortion Premiere Pro effect splits an image along a line while reflecting one side onto the other. Where the reflection appears and which side will be reflected is determined by the reflection angles.

1\. Head over to Effect Control>Distortion>Mirror to use this effect.

2\. Adjust the controls until you get the results you desire.

* Reflection Angle: With the Reflection Angle control, you can specify the angle of reflection and where it appears on the clip. A zero-degree angle reflects the left-hand side on the right.
* Reflection Center: This control allows you to specify the position of the line. You need to click the box, then drag the resulting crosshair up to the area in the image where you would like to place the line.

![mirror effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-5.png)

#### 5\. Offset Effect

This effect pans your image within a clip, and visual details pushed off one side of this image will appear on the opposite side. You have to perform the offset with subpixel precision at the best quality.

Also, you can use Offset with a combination of other effects. Head over to Effect Control>Distortion>Offset to use this effect.

![offset effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-6.png)

#### 6\. Spherize Effect

The Spherize effect allows users to wrap a video clip around a spherical shape. You can use it to give texts and objects a three-dimensional effect. Go to Effect Control>Distortion>Spherize and adjust the radius and center of the sphere.

![spherize effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-7.png)

#### 7\. Transform Effect

This effect applies 2-dimensional geometric transformations to your clip. You can use this effect to skew clips along any axis.

1\. Go to Effect Control>Distortion>Transform to apply this effect to your clip.

2\. Use Transform settings to adjust Opacity, Skew, Rotation, Scale, Anchor Point, and more.

![transform effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-8.png)

#### 8\. Turbulent Displace Effect

This fun effect utilizes fractal noise to create turbulent Premiere Pro distortion effects in your image. You can use the Turbulent Displace effect to add movement to your clip.

1\. Head to Effect Control>Distortion>Turbulent Displace.

2\. Adjust the following controls:

* Displacement
* Amount
* Size
* Offset (Turbulence)
* Complexity
* Evolution
* Pinning
* Resize Layer
* Antialiasing For Best Quality

![Turbulent Displace effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-9.png)

#### 9\. Twirl Effect

The Twirl effect allows you to rotate your clip around its center. It rotates the image more sharply in the middle than at the edge. You can use it on faces to make a funny clip. Navigate to Effect Control>Distortion>Twirl to start using this effect. Next, use the settings to adjust how much angle it twirls and the radius.

![Twirl effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-10.png)

#### 10\. Wave Warp Effect

This effect is one of the most popular Premiere Pro distortion effects. It generates the appearance of a wave as it's traveling across an image. The Wave Warp effect allows you to produce various wave shapes, including sine, circular, and square waves.

It's automatically animated at a steady speed across the time range, and that's without frames. You need to set keyframes to vary speeds.

1\. Head to Effect Control>Distortion>Wave Warp to apply this effect in your video clip.

2\. Now, change the wave speed, direction, height, width, and type to suit your preference.

![Wave Warp effect in premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-11.png)

## Bonus! Free Distortion Effects for Premiere Pro

### 1\. Liquid Distortion Effect

This effect can distort the content in a clip and can be used to shift into the next clip. It could be utilized in editing or used as a transition.

![free distortion effect for premiere pro](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-12.png)

### 2\. Earthquake Effect

This effect adds a shaking motion to the video clip you add it to; it works as a transition but could also be a useful editing tool.

![free distortion effect for premiere pro - earthquake effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-13.png)

### 3\. Glass Effect

This effect can add various blurs to the video clip and be used to transition from one clip to the next.

![free distortion effect for premiere pro - glass effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-14.png)

### 4\. TV Effect

This effect imitates the view of a television being turned on or off. You can use it to introduce a new video clip. It would also be a great start or end to the entire video.

![free distortion effect for premiere pro - TV effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-15.png)

### 5\. Glitch Effect

This effect adds a glitch to the video clip. You can use it in editing or as a transition from one clip to the next.

![free distortion effect for premiere pro - Glitch effect](https://images.wondershare.com/filmora/article-images/2022/04/premiere-pro-distortion-effects-16.png)

## Conclusion

**●** You can add any of these Premiere Pro distortion effects to make your videos more catchy. In turn, they will get more attention and views. Premiere Pro comes with tons of distortion effects and a responsive interface.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

## How to Add Text Behind Objects in Video

Adding text behind objects in your videos can be a great way to start your videos. For example, you can do so to create an attractive intro or startup a video. So, if you hope to make a video like a pro, let's learn how to add text behind objects in your videos by Filmora.

![add text behind objects by filmora](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-1.png)

## Part 1\. What Are The Benefits of Adding Text Behind Objects in Videos?

Your videos must maintain quality to create content worthy of a huge audience. You may have a YouTube channel or be starting down the road. Then you must give this a try because

### Give a cool look

Adding text behind an object in a video looks cool! Now, your object could be a silhouette of a person or a huge skyscraper. You can add a text tile behind the object, creating the illusion. Due to this, the text will be flying in real-time.

### Show creativity

Blasting your channel with innovative and creative content is the key to building a big audience. But, of course, you can always opt for many ways to create a video showing your creativity. One of those ways is to add text behind your object.

You can create an attractive intro by adding text behind objects that captivate the viewer. It ensures that your subscribers stay tuned to your channel and your content.

### Build up a solid audience

Every day can be a real struggle if you are a daily content creator on YouTube. The audience demands good content. But your daily videos can get boring if you do not use new methods to edit your videos.

You can add text behind videos to spice up your intros and hook your daily audience even more. That will show the audience that you are genuinely putting in the effort.

## Part 2\. What Will You Need To Add Text Behind Videos?

Now there are a few things that you will need to add text behind videos. First, take a look at the basic priorities to perform this feature.

### 1\. A Static Object Video

Adding text behind an object can be tricky if the object isn't static. For example, the effect will be ruined if an object moves around a lot in a video.

Our goal is to create a smooth text behind the video effect. And this can only be achieved if the target object remains static in the video and does not move about its position.

### 2\. A Video Editing Software - Wondershare Filmora

Once you select a video source, you aim to add it to a video editor. For this purpose, [Wondershare Filmora](https://tools.techidaily.com/wondershare/filmora/download/) would be your best choice. Wondershare Filmora allows you to create innovative and attractive videos.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For Win 7 or later(64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For macOS 10.14 or later

It has a very engaging system UI, allowing even beginner users to get their hands on it instantly. You will learn how to add text behind your videos with a few simple steps.

![wondershare filmora home interface](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-2.png)

Now that you know the requirements for the video, let's move on to the step-by-step guide to add text to your video.

## Part 3\. Step-by-Step Guide To Add Text Behind Videos

We look at two examples of how to add text behind videos in Wondershare Filmora.

* A static video with an object that can be easily masked out.
* A video with high contrast and a clean background.

### Add Text behind a Static Video

First, we will go with adding text behind a static object. For this, scroll more to get the step-by-step process.

##### Step1 Download Wondershare Filmora

If you are a beginner just starting in the video editing business, Wondershare Filmora is the best choice. Follow the steps below to download the free version of Wondershare Filmora:

* First, download the Wondershare Filmora on your PC or Mac.
* Open the setup and install the Wondershare Filmora.

After downloading the Wondershare Filmora software, let's edit the video. Scroll below to learn how to start the editing process!

##### Step2 Add the Video to the Timeline

We will first look at the static video example. For this, follow the below instructions:

* You have to start by importing your video in the import library.
* From the import library, you can click on the video and drag it down below to the timeline.

![adding video to the timeline](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-3.png)

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** Adding video to the timelines will allow you to create a workspace to edit your video.

Now let's move on to how we will add the text tile to our video.

##### Step3 Add the Text Tile

It is time to add the text tile you will animate behind the object. To do that, follow the steps mentioned as such.:

* Go to the **Titles** icon on the bar above the import library.
* A drop-down option will be available on the left side.
* Scroll down to the **Plain text**.
* Here, you can see many text tiles to add to your video.
* You can choose anyone you like.
* The most commonly used tile is the **Basic 6**.
* When you add the text tile to the timeline, you must ensure that the text is of equal length to the video.
* To do that, drag the right corner of the text tile and drag it to the right to match the length of the video.

![choose the text tile](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-4.png)

##### Step4 Edit the Text Tile

After you have added the text tile you desire, you need to type in the text. For this article, we will keep it simple. We will be typing a simple statement such as "**Hello, World.**"

* Double-click the Text tile to open the settings menu.
* After the settings menu is opened, type in the text box on the import window.

You will notice changes on the main window that your text has changed.

![edit the text tile](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-5.png)

* After the text appears, you can make the font look as desired.
* Look above the text window, and you will see the type of text font selected.
* Click on the drop-down option and choose whatever you like.

Let's move on to animate the text tile.

##### Step5 Animate the text tile

After adding text, it is time to animate it. This animation will decide how your text will appear behind the target object.

* First, you must open the text settings by **double-clicking** on the text tile in the timeline.
* In the settings opened in the import window, you will have to click on the animation tab in the upper left corner, aside from the **Preset**
* Now scroll down to where you will see the **Right Roll**
* Click on **Right Roll** and then click on the **OK** in the bottom right corner of the import window.

![animate the text](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-6.png)

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** You may notice now that the text appears in front of our object. Don't worry now! We are getting there. With a few simple steps, we will see the results.

Now let us move on to the more significant part of the editing, masking the object. Again, look ahead to see how you can mask the object!

##### Step6 Mask the Object

To mask our object, we will need to be technical. We will begin by adding the same footage of the static object on our timeline. Follow the steps mentioned below:

* Drag and drop the static object footage above the timeline text. Make sure the text stays in the middle of the sandwich.

![add the main video above the text tile](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-7.png)

* We will hide the video in the first track to simplify things. In addition, this will make our editing easier.
* We will have to look in the effects library to insert the masking effect.
* You can see the **Effects** icon on the bar at the top.
* Click on the **Effects**.
* You will see the search bar at the top of the import window.
* In the search bar, type in Image mask.
* Drag the **Image mask** effect on the video above the text tile.

Now the masking effect has been added. But we would have to adjust so that it stays upon our object.

* **Double-click** on the video and the settings option will open up.
* Go into the **Effects**

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** You must select your target object's mask shape exactly as its shape.

* We have to mask out a building, so that we will need a vertical rectangle.

![change the shape of the image mask](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-8.png)

* After you have selected the shape of your object, we will need to convert it to the object's size so that it only masks the building.
* To do that, scroll down below the import window to the settings.
* Here you can see the X, Y, and width settings.
* First, move the width bar so that it matches the width of the building.

![change the width of the mask](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-9.png)

* Now drag the X bar until the mask is confined to the building. You would have created the mask only limited to the building.

![change the position of the mask by dragging x](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-10.png)

* Once you complete this step, click OK in the bottom right corner.
* Now un-hide the original video that you imported in the beginning.

Finally, play the video in the main play window from the beginning.

![final result of the static video](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-11.gif)

You have successfully created a text behind the object effect. Now that you know how to add text behind static objects let us move to learn how to add text to a video that has high contrast and a clean background.

### Add text behind a high contrast and clean background

Besides the text can be added behind a static object, it can also be added to a clean background with high contrast. But how is it? Let's dive into it.

##### Step1 Import the video into the timeline

* Import the video from the location in your PC media.
* When imported, drag and drop it onto the timeline.

![add the footage to the timeline](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-12.png)

##### Step2 Add the text tile

To add the text to your video, follow the steps mentioned below.

* Click on the titles icon on the bar above the import window.
* On the left drop-down option, scroll down to the titles.
* Select the Plain text option.
* You will notice that multiple options will pop up in the import window.
* Select the text title that suits you best.
* After you have selected the text style, drag and drop it down above your video in the timeline.

![add the text tile above the video](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-13.png)

* Our next step would be to add the text.
* **Double-click** on the text tile. Doing so will open the settings menu in the import window.
* Type in the text that you want. For reference, we will keep it simple such as, **"Hello world."**
* You can also adjust the font of your text.
* Above the type box, a drop-down option will show you the range of fonts available.
* Select the font you desire.

![type in the text](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-14.png)

Now that you have added the text, it is time to animate it.

##### Step3 Take a snapshot

After typing in the text, you will notice in the main play window that your text still appears in front of your object. Therefore, we want to take it behind the object. To do so, first, you will need to take a snapshot.

Follow the steps mentioned to take a snapshot:

* Hide the main video. You can see the Eye icon aside from your main video in the edit column on the left side of the timeline.
* Click on the Eye icon to hide the main video.
* In the **main play** window, you will notice that the screen turns black, which leaves only the text on the screen.

![taking a snapshot](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-15.png)

* In the main play screen, you can notice a small **camera icon**.
* This camera icon is used to take snapshots of your screen.
* Click on the camera icon to take a snapshot of your screen.
* Your snapshot will now be saved in the main import window.

![snapshot is saved in the import library](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-16.png)

Now that we have taken a snapshot, we will need to import it into the timeline. Scroll below for more.

##### Step4 Add the snapshot

After taking it, your goal is to import it into the timeline. To perform this action, perform the following steps:

* Before adding the snapshot to the timeline, we must delete the main text tile.
* Then drag and drop the snapshot from the import library into the timeline above the video.
* Make sure that the snapshot is aligned well with the length of the video.
* If it is **longer** than the video, drag it from the right to match the length of the video.
* If its length is **smaller** than the video, drag it to the right to increase its length.

![adjust the length of the snapshot](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-17.png)

After adding the snapshot, we will have to change its blending mode.

##### Step5 Change the blending of the snapshot

To create the effect of your text behind the video, you must alter the main text's blending mode. In this case, it will be the snapshot we took.

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** Changing the blending mode of the snapshot will allow it to blend with the transparent background and will create the effect of the text behind the object in the video.

Follow the steps mentioned below to change the blending of the snapshot:

* **Double-click** the snapshot.
* If you select the compositing tab, the blending options will pop up.
* From default, it would be set to **Normal**. Click on the **Normal**
* It will show a drop-down option.
* Scroll down below until you can see an option labeled Then click on **Overlay.**

![change the blending mode to overlay](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-18.png)

* And press **OK** in the bottom right corner to confirm your changes.

The text can be blended with the background.

* Click on the **Eye icon** to un-hide the video from the timeline.
* Now play the video from the start from the main play screen to see the final changes.

![final preview](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-19.gif)

Congratulations! The above steps allow you to add text behind objects in your videos.

## Conclusion

Modern media is full of creative content. And if you are a content creator that wants to make it through the world of YouTube and video creating, you need to be the best. You can only be the best at what you do if you keep pushing the boundaries of your creativity.

Adding text behind objects could be the first step in making your intros shine with creativity and innovation. It allows you to maintain and build your viewing audience. The more the audience, the more your content gets watched!

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/) For macOS 10.14 or later

It has a very engaging system UI, allowing even beginner users to get their hands on it instantly. You will learn how to add text behind your videos with a few simple steps.

![wondershare filmora home interface](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-2.png)

Now that you know the requirements for the video, let's move on to the step-by-step guide to add text to your video.

## Part 3\. Step-by-Step Guide To Add Text Behind Videos

We look at two examples of how to add text behind videos in Wondershare Filmora.

* A static video with an object that can be easily masked out.
* A video with high contrast and a clean background.

### Add Text behind a Static Video

First, we will go with adding text behind a static object. For this, scroll more to get the step-by-step process.

##### Step1 Download Wondershare Filmora

If you are a beginner just starting in the video editing business, Wondershare Filmora is the best choice. Follow the steps below to download the free version of Wondershare Filmora:

* First, download the Wondershare Filmora on your PC or Mac.
* Open the setup and install the Wondershare Filmora.

After downloading the Wondershare Filmora software, let's edit the video. Scroll below to learn how to start the editing process!

##### Step2 Add the Video to the Timeline

We will first look at the static video example. For this, follow the below instructions:

* You have to start by importing your video in the import library.
* From the import library, you can click on the video and drag it down below to the timeline.

![adding video to the timeline](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-3.png)

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** Adding video to the timelines will allow you to create a workspace to edit your video.

Now let's move on to how we will add the text tile to our video.

##### Step3 Add the Text Tile

It is time to add the text tile you will animate behind the object. To do that, follow the steps mentioned as such.:

* Go to the **Titles** icon on the bar above the import library.
* A drop-down option will be available on the left side.
* Scroll down to the **Plain text**.
* Here, you can see many text tiles to add to your video.
* You can choose anyone you like.
* The most commonly used tile is the **Basic 6**.
* When you add the text tile to the timeline, you must ensure that the text is of equal length to the video.
* To do that, drag the right corner of the text tile and drag it to the right to match the length of the video.

![choose the text tile](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-4.png)

##### Step4 Edit the Text Tile

After you have added the text tile you desire, you need to type in the text. For this article, we will keep it simple. We will be typing a simple statement such as "**Hello, World.**"

* Double-click the Text tile to open the settings menu.
* After the settings menu is opened, type in the text box on the import window.

You will notice changes on the main window that your text has changed.

![edit the text tile](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-5.png)

* After the text appears, you can make the font look as desired.
* Look above the text window, and you will see the type of text font selected.
* Click on the drop-down option and choose whatever you like.

Let's move on to animate the text tile.

##### Step5 Animate the text tile

After adding text, it is time to animate it. This animation will decide how your text will appear behind the target object.

* First, you must open the text settings by **double-clicking** on the text tile in the timeline.
* In the settings opened in the import window, you will have to click on the animation tab in the upper left corner, aside from the **Preset**
* Now scroll down to where you will see the **Right Roll**
* Click on **Right Roll** and then click on the **OK** in the bottom right corner of the import window.

![animate the text](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-6.png)

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** You may notice now that the text appears in front of our object. Don't worry now! We are getting there. With a few simple steps, we will see the results.

Now let us move on to the more significant part of the editing, masking the object. Again, look ahead to see how you can mask the object!

##### Step6 Mask the Object

To mask our object, we will need to be technical. We will begin by adding the same footage of the static object on our timeline. Follow the steps mentioned below:

* Drag and drop the static object footage above the timeline text. Make sure the text stays in the middle of the sandwich.

![add the main video above the text tile](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-7.png)

* We will hide the video in the first track to simplify things. In addition, this will make our editing easier.
* We will have to look in the effects library to insert the masking effect.
* You can see the **Effects** icon on the bar at the top.
* Click on the **Effects**.
* You will see the search bar at the top of the import window.
* In the search bar, type in Image mask.
* Drag the **Image mask** effect on the video above the text tile.

Now the masking effect has been added. But we would have to adjust so that it stays upon our object.

* **Double-click** on the video and the settings option will open up.
* Go into the **Effects**

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** You must select your target object's mask shape exactly as its shape.

* We have to mask out a building, so that we will need a vertical rectangle.

![change the shape of the image mask](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-8.png)

* After you have selected the shape of your object, we will need to convert it to the object's size so that it only masks the building.
* To do that, scroll down below the import window to the settings.
* Here you can see the X, Y, and width settings.
* First, move the width bar so that it matches the width of the building.

![change the width of the mask](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-9.png)

* Now drag the X bar until the mask is confined to the building. You would have created the mask only limited to the building.

![change the position of the mask by dragging x](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-10.png)

* Once you complete this step, click OK in the bottom right corner.
* Now un-hide the original video that you imported in the beginning.

Finally, play the video in the main play window from the beginning.

![final result of the static video](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-11.gif)

You have successfully created a text behind the object effect. Now that you know how to add text behind static objects let us move to learn how to add text to a video that has high contrast and a clean background.

### Add text behind a high contrast and clean background

Besides the text can be added behind a static object, it can also be added to a clean background with high contrast. But how is it? Let's dive into it.

##### Step1 Import the video into the timeline

* Import the video from the location in your PC media.
* When imported, drag and drop it onto the timeline.

![add the footage to the timeline](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-12.png)

##### Step2 Add the text tile

To add the text to your video, follow the steps mentioned below.

* Click on the titles icon on the bar above the import window.
* On the left drop-down option, scroll down to the titles.
* Select the Plain text option.
* You will notice that multiple options will pop up in the import window.
* Select the text title that suits you best.
* After you have selected the text style, drag and drop it down above your video in the timeline.

![add the text tile above the video](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-13.png)

* Our next step would be to add the text.
* **Double-click** on the text tile. Doing so will open the settings menu in the import window.
* Type in the text that you want. For reference, we will keep it simple such as, **"Hello world."**
* You can also adjust the font of your text.
* Above the type box, a drop-down option will show you the range of fonts available.
* Select the font you desire.

![type in the text](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-14.png)

Now that you have added the text, it is time to animate it.

##### Step3 Take a snapshot

After typing in the text, you will notice in the main play window that your text still appears in front of your object. Therefore, we want to take it behind the object. To do so, first, you will need to take a snapshot.

Follow the steps mentioned to take a snapshot:

* Hide the main video. You can see the Eye icon aside from your main video in the edit column on the left side of the timeline.
* Click on the Eye icon to hide the main video.
* In the **main play** window, you will notice that the screen turns black, which leaves only the text on the screen.

![taking a snapshot](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-15.png)

* In the main play screen, you can notice a small **camera icon**.
* This camera icon is used to take snapshots of your screen.
* Click on the camera icon to take a snapshot of your screen.
* Your snapshot will now be saved in the main import window.

![snapshot is saved in the import library](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-16.png)

Now that we have taken a snapshot, we will need to import it into the timeline. Scroll below for more.

##### Step4 Add the snapshot

After taking it, your goal is to import it into the timeline. To perform this action, perform the following steps:

* Before adding the snapshot to the timeline, we must delete the main text tile.
* Then drag and drop the snapshot from the import library into the timeline above the video.
* Make sure that the snapshot is aligned well with the length of the video.
* If it is **longer** than the video, drag it from the right to match the length of the video.
* If its length is **smaller** than the video, drag it to the right to increase its length.

![adjust the length of the snapshot](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-17.png)

After adding the snapshot, we will have to change its blending mode.

##### Step5 Change the blending of the snapshot

To create the effect of your text behind the video, you must alter the main text's blending mode. In this case, it will be the snapshot we took.

![](https://images.wondershare.com/assets/images-common/icon-note.png)

**Note:** Changing the blending mode of the snapshot will allow it to blend with the transparent background and will create the effect of the text behind the object in the video.

Follow the steps mentioned below to change the blending of the snapshot:

* **Double-click** the snapshot.
* If you select the compositing tab, the blending options will pop up.
* From default, it would be set to **Normal**. Click on the **Normal**
* It will show a drop-down option.
* Scroll down below until you can see an option labeled Then click on **Overlay.**

![change the blending mode to overlay](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-18.png)

* And press **OK** in the bottom right corner to confirm your changes.

The text can be blended with the background.

* Click on the **Eye icon** to un-hide the video from the timeline.
* Now play the video from the start from the main play screen to see the final changes.

![final preview](https://images.wondershare.com/filmora/article-images/2023/01/add-text-behind-objects-19.gif)

Congratulations! The above steps allow you to add text behind objects in your videos.

## Conclusion

Modern media is full of creative content. And if you are a content creator that wants to make it through the world of YouTube and video creating, you need to be the best. You can only be the best at what you do if you keep pushing the boundaries of your creativity.

Adding text behind objects could be the first step in making your intros shine with creativity and innovation. It allows you to maintain and build your viewing audience. The more the audience, the more your content gets watched!

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

## This Article Can Help You Know How to Crop Video in After Effects and on the Alternative by Using Wondershare Filmora. I Know that It May Seem Confusing to Compare These Two at First. But, I’ll Provide an Explanation to Get the Cropped Video that You Want

Cropping a video is part of the process of video edting. Not all video editing software can be obtained freely. There are some that you need to spend to get the professional output that you aim for. After Effects,a member of the Adobe tools that exist can enhance your videos to another level. This article can help you know how to crop video in After Effects and on the alternative by using Wondershare Filmora. I know that it may seem confusing to compare these two at first. But, I’ll provide an explanation to get the cropped video that you want.

## Method 1: Cropping a Video using After Effects

After Effects is a professional motion graphics tool that can create outputs that are beyond the limits of reality. Like the other Adobe tools, this comes with a subscription fee to be able to maximize this product. But, is the price worth the risk? The “ Adobe” brand is known for its quality applications and customer’s satisfaction.

Let’s start with using this tool. The situation is that you want to crop your video using Adobe After Effects but you don’t know how to start. Search for the application on your computer. Launch it, then click the **New Project**. If you have files from your storage then select the **New Composition Footage.**

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-1.jpg)

Check if the video is already in the interface. Find the **Magnifying** tab and zoom out the video into 50%. After that, click the **Grid** icon and **Proportional Grid**.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-2.jpg)

Click the **Square** icon, it is located beside the **Pencil** icon at the top section. The shape’s purpose is to crop the video section that you want to remain. If you’re done cutting then you should unclick the **Proportiona**l grid, and the video’s magnification should be 100%. Afterwards, you can check the pixel aspect ratio correction in the After Effects. You need to go through the video before saving your project. This is to avoid unnecessary errors that will make the process troublesome.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-3.jpg)

Already satisfied with the cropped video? Then, select **File,** **Export** and finally **Add to Render Queue.** Check on the **Render Settings** (located bottom of the interface) to ensure high quality output. Following that, hit the **Output To** part and decide the destination and folder where you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-4.jpg)

Watch your cropped video and go ahead and repeat this with your other videos. After practicing this process many times, this will come to you as easy. If you get lost while following the instructions go back to this guide until it becomes a part of your memory.

Congratulations on making your first cropped video using After Effects! What was your experience while following through the guide? I hope that the information presented here is easy to understand and implement.

Even though it is not a free application, I hope you have experienced the advantages of using this compared to other tools. Did it come as a surprise for you that you can crop a video not just in Adobe Premiere but also in After Effects as well?

I hope that fear will not hinder you from trying this tool to crop your videos.

## Method 2: Cropping a Video using Wondershare Filmora

If you didn’t know there is also an awesome video editing software called Wondershare [Filmora Video Editor](https://tools.techidaily.com/wondershare/filmora/download/) .

You can try it by searching the internet and downloading it on your computer. If simplicity is your priority then this may suit you perfectly. If you’re still hesitant then read the reviews and watch how others are using it.

There is no need to worry if you have a tight budget as downloading this would be free. You just need to go to the official site. Do not be scared of trying with something unfamiliar. I will guide you with using it and utilizing it to get the result that you dream of.

Wondershare Filmora just like the others that exist are video editors that will turn your raw videos into the vision that you like. Thanks to these applications, the gruesome process of manually cutting it by hand and permanently altering the footage are gone. You can make how many changes that you want without damaging the original video.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For Win 7 or later (64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For macOS 10.14 or later

Are you done installing the application? If you have any encountered issues with installing it, you can contact customer support.

Not only does it have a straightforward and simple interface but it is also packed with useful tools that can turn your video into another level. But, you should not be overwhelmed by the number of icons and features that exist. Take a deep breath and proceed to opening it in your computer.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-5.png)

Preparation is a must especially if you have multiple videos on your computer. A good tip would be renaming them by the sequence you plan to have. And, you could also place them in folders to avoid repetition and double copies. Once you’re done, you can drag and drop your video or

click the **Import.**

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-6.png)

Go ahead and select the video clip that you want to crop. Then, click the **Crop** tool and choose if you want the **Crop** or **Pan & Zoom.** Yes, you have options on what kind of crop you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-7.png)

An alternative way is by right clicking the video clip .Under the **Video** tab you can select the **Crop and Zoom** or **Crop to Fit** then adjust to your preferred ratio.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-8.png)

You can review the cropped video to think through if this is the portion that you want to be included. Unlike other applications, you can go back and adjust it to your liking.

If you’re finally satisfied then you can export it. Choose the output format and you can also rename the file. Clicking the settings button will offer you additional options of your video output.

After all that, you have the cropped video that you can either upload or repurpose in another content. Did you enjoy the process of cropping it in Wondershare Filmora?

Remember, that you have the option to batch crop multiple video clips on this so no need to manually crop and export it. You can see the big picture and monitor if the flow makes sense to you.

Don’t you think that the subscription is worth it? There is a trial that you could check out to test its capabilities and awesomeness.

## The Bottom Line

You are once again done with the process of checking out these two applications. After Effects and Wondershare Filmora have a different process when it comes to cropping videos. I hope that you had a clearer understanding on which of these two would suit your video editing needs. The interface also could change your mind depending if you want simplicity or a challenge. Price is also a factor that can affect your willingness to use these applications. But, this guide clearly shows you that it is worth paying for.

What are your thoughts on both of these tools? Did you find this information to be helpful?

Check if the video is already in the interface. Find the **Magnifying** tab and zoom out the video into 50%. After that, click the **Grid** icon and **Proportional Grid**.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-2.jpg)

Click the **Square** icon, it is located beside the **Pencil** icon at the top section. The shape’s purpose is to crop the video section that you want to remain. If you’re done cutting then you should unclick the **Proportiona**l grid, and the video’s magnification should be 100%. Afterwards, you can check the pixel aspect ratio correction in the After Effects. You need to go through the video before saving your project. This is to avoid unnecessary errors that will make the process troublesome.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-3.jpg)

Already satisfied with the cropped video? Then, select **File,** **Export** and finally **Add to Render Queue.** Check on the **Render Settings** (located bottom of the interface) to ensure high quality output. Following that, hit the **Output To** part and decide the destination and folder where you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-4.jpg)

Watch your cropped video and go ahead and repeat this with your other videos. After practicing this process many times, this will come to you as easy. If you get lost while following the instructions go back to this guide until it becomes a part of your memory.

Congratulations on making your first cropped video using After Effects! What was your experience while following through the guide? I hope that the information presented here is easy to understand and implement.

Even though it is not a free application, I hope you have experienced the advantages of using this compared to other tools. Did it come as a surprise for you that you can crop a video not just in Adobe Premiere but also in After Effects as well?

I hope that fear will not hinder you from trying this tool to crop your videos.

## Method 2: Cropping a Video using Wondershare Filmora

If you didn’t know there is also an awesome video editing software called Wondershare [Filmora Video Editor](https://tools.techidaily.com/wondershare/filmora/download/) .

You can try it by searching the internet and downloading it on your computer. If simplicity is your priority then this may suit you perfectly. If you’re still hesitant then read the reviews and watch how others are using it.

There is no need to worry if you have a tight budget as downloading this would be free. You just need to go to the official site. Do not be scared of trying with something unfamiliar. I will guide you with using it and utilizing it to get the result that you dream of.

Wondershare Filmora just like the others that exist are video editors that will turn your raw videos into the vision that you like. Thanks to these applications, the gruesome process of manually cutting it by hand and permanently altering the footage are gone. You can make how many changes that you want without damaging the original video.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For Win 7 or later (64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For macOS 10.14 or later

Are you done installing the application? If you have any encountered issues with installing it, you can contact customer support.

Not only does it have a straightforward and simple interface but it is also packed with useful tools that can turn your video into another level. But, you should not be overwhelmed by the number of icons and features that exist. Take a deep breath and proceed to opening it in your computer.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-5.png)

Preparation is a must especially if you have multiple videos on your computer. A good tip would be renaming them by the sequence you plan to have. And, you could also place them in folders to avoid repetition and double copies. Once you’re done, you can drag and drop your video or

click the **Import.**

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-6.png)

Go ahead and select the video clip that you want to crop. Then, click the **Crop** tool and choose if you want the **Crop** or **Pan & Zoom.** Yes, you have options on what kind of crop you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-7.png)

An alternative way is by right clicking the video clip .Under the **Video** tab you can select the **Crop and Zoom** or **Crop to Fit** then adjust to your preferred ratio.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-8.png)

You can review the cropped video to think through if this is the portion that you want to be included. Unlike other applications, you can go back and adjust it to your liking.

If you’re finally satisfied then you can export it. Choose the output format and you can also rename the file. Clicking the settings button will offer you additional options of your video output.

After all that, you have the cropped video that you can either upload or repurpose in another content. Did you enjoy the process of cropping it in Wondershare Filmora?

Remember, that you have the option to batch crop multiple video clips on this so no need to manually crop and export it. You can see the big picture and monitor if the flow makes sense to you.

Don’t you think that the subscription is worth it? There is a trial that you could check out to test its capabilities and awesomeness.

## The Bottom Line

You are once again done with the process of checking out these two applications. After Effects and Wondershare Filmora have a different process when it comes to cropping videos. I hope that you had a clearer understanding on which of these two would suit your video editing needs. The interface also could change your mind depending if you want simplicity or a challenge. Price is also a factor that can affect your willingness to use these applications. But, this guide clearly shows you that it is worth paying for.

What are your thoughts on both of these tools? Did you find this information to be helpful?

Check if the video is already in the interface. Find the **Magnifying** tab and zoom out the video into 50%. After that, click the **Grid** icon and **Proportional Grid**.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-2.jpg)

Click the **Square** icon, it is located beside the **Pencil** icon at the top section. The shape’s purpose is to crop the video section that you want to remain. If you’re done cutting then you should unclick the **Proportiona**l grid, and the video’s magnification should be 100%. Afterwards, you can check the pixel aspect ratio correction in the After Effects. You need to go through the video before saving your project. This is to avoid unnecessary errors that will make the process troublesome.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-3.jpg)

Already satisfied with the cropped video? Then, select **File,** **Export** and finally **Add to Render Queue.** Check on the **Render Settings** (located bottom of the interface) to ensure high quality output. Following that, hit the **Output To** part and decide the destination and folder where you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-4.jpg)

Watch your cropped video and go ahead and repeat this with your other videos. After practicing this process many times, this will come to you as easy. If you get lost while following the instructions go back to this guide until it becomes a part of your memory.

Congratulations on making your first cropped video using After Effects! What was your experience while following through the guide? I hope that the information presented here is easy to understand and implement.

Even though it is not a free application, I hope you have experienced the advantages of using this compared to other tools. Did it come as a surprise for you that you can crop a video not just in Adobe Premiere but also in After Effects as well?

I hope that fear will not hinder you from trying this tool to crop your videos.

## Method 2: Cropping a Video using Wondershare Filmora

If you didn’t know there is also an awesome video editing software called Wondershare [Filmora Video Editor](https://tools.techidaily.com/wondershare/filmora/download/) .

You can try it by searching the internet and downloading it on your computer. If simplicity is your priority then this may suit you perfectly. If you’re still hesitant then read the reviews and watch how others are using it.

There is no need to worry if you have a tight budget as downloading this would be free. You just need to go to the official site. Do not be scared of trying with something unfamiliar. I will guide you with using it and utilizing it to get the result that you dream of.

Wondershare Filmora just like the others that exist are video editors that will turn your raw videos into the vision that you like. Thanks to these applications, the gruesome process of manually cutting it by hand and permanently altering the footage are gone. You can make how many changes that you want without damaging the original video.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For Win 7 or later (64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For macOS 10.14 or later

Are you done installing the application? If you have any encountered issues with installing it, you can contact customer support.

Not only does it have a straightforward and simple interface but it is also packed with useful tools that can turn your video into another level. But, you should not be overwhelmed by the number of icons and features that exist. Take a deep breath and proceed to opening it in your computer.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-5.png)

Preparation is a must especially if you have multiple videos on your computer. A good tip would be renaming them by the sequence you plan to have. And, you could also place them in folders to avoid repetition and double copies. Once you’re done, you can drag and drop your video or

click the **Import.**

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-6.png)

Go ahead and select the video clip that you want to crop. Then, click the **Crop** tool and choose if you want the **Crop** or **Pan & Zoom.** Yes, you have options on what kind of crop you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-7.png)

An alternative way is by right clicking the video clip .Under the **Video** tab you can select the **Crop and Zoom** or **Crop to Fit** then adjust to your preferred ratio.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-8.png)

You can review the cropped video to think through if this is the portion that you want to be included. Unlike other applications, you can go back and adjust it to your liking.

If you’re finally satisfied then you can export it. Choose the output format and you can also rename the file. Clicking the settings button will offer you additional options of your video output.

After all that, you have the cropped video that you can either upload or repurpose in another content. Did you enjoy the process of cropping it in Wondershare Filmora?

Remember, that you have the option to batch crop multiple video clips on this so no need to manually crop and export it. You can see the big picture and monitor if the flow makes sense to you.

Don’t you think that the subscription is worth it? There is a trial that you could check out to test its capabilities and awesomeness.

## The Bottom Line

You are once again done with the process of checking out these two applications. After Effects and Wondershare Filmora have a different process when it comes to cropping videos. I hope that you had a clearer understanding on which of these two would suit your video editing needs. The interface also could change your mind depending if you want simplicity or a challenge. Price is also a factor that can affect your willingness to use these applications. But, this guide clearly shows you that it is worth paying for.

What are your thoughts on both of these tools? Did you find this information to be helpful?

Check if the video is already in the interface. Find the **Magnifying** tab and zoom out the video into 50%. After that, click the **Grid** icon and **Proportional Grid**.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-2.jpg)

Click the **Square** icon, it is located beside the **Pencil** icon at the top section. The shape’s purpose is to crop the video section that you want to remain. If you’re done cutting then you should unclick the **Proportiona**l grid, and the video’s magnification should be 100%. Afterwards, you can check the pixel aspect ratio correction in the After Effects. You need to go through the video before saving your project. This is to avoid unnecessary errors that will make the process troublesome.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-3.jpg)

Already satisfied with the cropped video? Then, select **File,** **Export** and finally **Add to Render Queue.** Check on the **Render Settings** (located bottom of the interface) to ensure high quality output. Following that, hit the **Output To** part and decide the destination and folder where you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-4.jpg)

Watch your cropped video and go ahead and repeat this with your other videos. After practicing this process many times, this will come to you as easy. If you get lost while following the instructions go back to this guide until it becomes a part of your memory.

Congratulations on making your first cropped video using After Effects! What was your experience while following through the guide? I hope that the information presented here is easy to understand and implement.

Even though it is not a free application, I hope you have experienced the advantages of using this compared to other tools. Did it come as a surprise for you that you can crop a video not just in Adobe Premiere but also in After Effects as well?

I hope that fear will not hinder you from trying this tool to crop your videos.

## Method 2: Cropping a Video using Wondershare Filmora

If you didn’t know there is also an awesome video editing software called Wondershare [Filmora Video Editor](https://tools.techidaily.com/wondershare/filmora/download/) .

You can try it by searching the internet and downloading it on your computer. If simplicity is your priority then this may suit you perfectly. If you’re still hesitant then read the reviews and watch how others are using it.

There is no need to worry if you have a tight budget as downloading this would be free. You just need to go to the official site. Do not be scared of trying with something unfamiliar. I will guide you with using it and utilizing it to get the result that you dream of.

Wondershare Filmora just like the others that exist are video editors that will turn your raw videos into the vision that you like. Thanks to these applications, the gruesome process of manually cutting it by hand and permanently altering the footage are gone. You can make how many changes that you want without damaging the original video.

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For Win 7 or later (64-bit)

[Free Download](https://tools.techidaily.com/wondershare/filmora/download/)

For macOS 10.14 or later

Are you done installing the application? If you have any encountered issues with installing it, you can contact customer support.

Not only does it have a straightforward and simple interface but it is also packed with useful tools that can turn your video into another level. But, you should not be overwhelmed by the number of icons and features that exist. Take a deep breath and proceed to opening it in your computer.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-5.png)

Preparation is a must especially if you have multiple videos on your computer. A good tip would be renaming them by the sequence you plan to have. And, you could also place them in folders to avoid repetition and double copies. Once you’re done, you can drag and drop your video or

click the **Import.**

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-6.png)

Go ahead and select the video clip that you want to crop. Then, click the **Crop** tool and choose if you want the **Crop** or **Pan & Zoom.** Yes, you have options on what kind of crop you want it to be.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-7.png)

An alternative way is by right clicking the video clip .Under the **Video** tab you can select the **Crop and Zoom** or **Crop to Fit** then adjust to your preferred ratio.

![crop-vidoe-in-ae](https://images.wondershare.com/filmora/article-images/2022/02/crop-vidoe-in-ae-8.png)

You can review the cropped video to think through if this is the portion that you want to be included. Unlike other applications, you can go back and adjust it to your liking.

If you’re finally satisfied then you can export it. Choose the output format and you can also rename the file. Clicking the settings button will offer you additional options of your video output.

After all that, you have the cropped video that you can either upload or repurpose in another content. Did you enjoy the process of cropping it in Wondershare Filmora?

Remember, that you have the option to batch crop multiple video clips on this so no need to manually crop and export it. You can see the big picture and monitor if the flow makes sense to you.

Don’t you think that the subscription is worth it? There is a trial that you could check out to test its capabilities and awesomeness.

## The Bottom Line

You are once again done with the process of checking out these two applications. After Effects and Wondershare Filmora have a different process when it comes to cropping videos. I hope that you had a clearer understanding on which of these two would suit your video editing needs. The interface also could change your mind depending if you want simplicity or a challenge. Price is also a factor that can affect your willingness to use these applications. But, this guide clearly shows you that it is worth paying for.

What are your thoughts on both of these tools? Did you find this information to be helpful?

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>



<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>






