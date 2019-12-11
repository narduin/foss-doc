---
description: 'How to compress like a bowss. Updated: 12/2019'
---

# Video Compression

## Let's play.

Videos are everywhere. **EVERYWHERE!** But videos can and will be huge when 4k becomes an internet standard. Currently, 1920x1080 is king and we usually have no problem hosting or playing this resolution.

## Because we can doesn't mean we should.

Right now, the \(good\) trend of web performance is on the rise. Everyone wants a blazing fast loading website, which might not be possible if we send requests to 100mb \(or even more\) videos.

With a good connection, users will not see the difference. But if we go down that path, nor will they with a 300mb. So the goal is to make every asset as small as possible. It's already the case with images. But it's simpler and faster than video encoding.

## Small size, big quality.

Let's say we exported​ a 1920x1080 video from Premiere Pro with these basic settings:

![](../.gitbook/assets/premiere.jpeg)

It's gorgeous, it's Full HD, it's 1:30 minute of excellent editing but it's 50mb… What a shame.

We can already bring down the size from Premiere or Media Encoder by selecting CBR instead of VBR and using a low bitrate \(like 2 or 3\).

[Let's now use Handbrake!](https://handbrake.fr/) It's free, open source and multi platform. You can also read [this great article](https://loremipsum.ueno.co/dear-ueno-how-do-you-compress-videos-6657ebd9dd28?gi=4d8681fca54a) from Ueno on video encoding.

{% hint style="warning" %}
Please please **PLEASE**. Never export within After Effects.
{% endhint %}

## Handbrake

### Summary screen

While it's not as sexy as Premiere Pro, it has way more exporting capabilities. Follow these steps to use “passe partout” settings :

1. Open your source video
2. Select a preset corresponding to your future usage like _Fast 1080p30_
3. Check _Web Optimized_

![summary](../.gitbook/assets/hb-1.jpg)

### Video screen

1. Choose _Constant Quality_ and try a value between 20 and 30​ \(higher = smaller size\)
2. Choose _Peak Framerate._ If you don't know the framerate, keep the default setting
3. Choose the type of video you are encoding \(film, animation…\)

![video](../.gitbook/assets/hb-2.jpg)

### Audio screen

If you don't have audio, be sure to set the audio channel to _none_.  
If you have an audio channel, these settings are great and will not influence the size much​:

1. Codec AAC
2. Samplerate 44.1
3. Bitrate 256

![audio](../.gitbook/assets/hb-3.jpg)

### Export!

I used a RF of 25 for this example and no audio.

* My Premiere Pro video was **50,6mb**
* My Handbrake video is **5,5mb​**

{% hint style="success" %}
### What a save !​
{% endhint %}

I ended up dividing the original size by 10. Which is cool.  
I tried with a RF of 30. The video was still pretty good and only 3,3mb.

### Exporting for the web

Now that we know how to properly compress videos, let's go further. Say we have a website with a lot of videos on the same page. We still want to load the content as fast as possible. So our videos need to be as small as possible. We won't do better than previously seen using mp4/H.264. However, we can use **webm/VP9.**

{% hint style="info" %}
Webm is an html video format and VP9 is the latest codec.
{% endhint %}

Using Handbrake and webm/VP9, we can achieve really great compression without losing too much quality \(or none at all depending on the settings\). I was able to divide by 4 the size of a video using these presets:

![](../.gitbook/assets/capture-de-cran-2019-12-11-a-12.26.13.png)

The only down side is that it takes some time to encode. It will depend on the video length but for a 20 seconds clip, it varies between 3 and 5 minutes.

I tried various settings but I read [here](https://trac.ffmpeg.org/wiki/Encode/VP9) that VP9 is supposed to be used with two-pass encoding. You then have to find the right bitrate \(here 1000\) for your situation.

