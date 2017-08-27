---
layout: post
title: "Increase viewership with bit rate"
date: 2017-08-27T04:00:00Z
categories: obs tips
---

When I first began streaming, I was streaming chess. But I damn well knew that I'd have the best looking chess stream on the planet. So I embarked on this mission to find the best setting configurations in [OBS](https://obsproject.com/) to achieve this. However, I would later find out that this superficial appeal would harm my channel's viewership. Fair warning: I already assume you have a decent grasp on OBS.

## The Dream
Every non-partnered Twitch streamer wants the fiction of 1080p at 60 FPS at 6000 bit rate to be real. And yes, it looks absolutely gorgeous. In fast-paced games with heavy particle effects, like _Overwatch_, it can almost feel essential to the broadcast. If you were to head over to [Twitch](http://twitch.tv) right now and search for _Overwatch_, you'd probably quickly come to find that a lot of the streams below the big names look like complete ass. I'm convinced that this is either _Joe Schmoe's_ hardware limitations or perhaps he is just unaware of the tuning process required to achieve good results with OBS. In any case, often the streamer starting at Ground Zero looks no further than some Reddit post with a title that might read _Best OBS Settings for Overwatch_ and with some copy-paste shenanigans, considers the job done.


## The Reality
I don't like giving people homework but [this video is a must-see](https://www.youtube.com/watch?v=r6Rp-uo6HmI) for those looking to understand the technology and transactions behind streaming more deeply-- and importantly, **bit rate**. Anyway, my bubble was burst with my chess channel when a viewer commented _dude, your stream is so laggy_. Everything seemed fine for me ... OBS indicated that there were no dropped frames or any reason to believe that something suspicious was happening on my end. _Well, their problem_ I thought to myself.

What a galactic mistake. Indeed, it was _my_ fault.

Turns out when you are **not** a partnered Twitch streamer, your viewers have no access to video quality controls, so they are forced to consume what you are pushing through the pipes. And often _6000_ can cause issues for those without a tremendous connection (_thinks mobile viewers, folk in the back of the woods, and college peeps on a shared network_). I don't care that Twitch specifically states that you can use a bit rate of 6000-- it is channel suicide.

## Don't Let Your Dreams Be Dreams
So what bit rate is appropriate, then? I have arrived at _3000_ and no more than _3500_. If your stream looks reasonable at any other number, say _2500_, great, set it to 2500 but chances are, you are probably going to be pissed that your stream suddenly looks damn ugly. Well, welcome to the fun part, friend. You've chosen the path of making your stream accessible to essentially everyone with the caveat of having your brain mashed with a sludgehammer. Good thing I've taken most of the blow for you.

First, you might consider downscaling the resolution of your stream to 720p at 30 FPS. In fact, even if you are screaming at me _bullshit_, you should do it anyway just to get an optical sense of just how awful it is. Is it awful? You'll need to consider this based on the strength of your CPU in the measures that follow.

The biggest setting that is going to compensate for your reduction in bit rate is `CPU Usage Preset` (I'm assuming you are using CPU encoding, also known as `x264`). I have this settings option set to `slow` but you will have to go through the painstaking process of stress-testing your CPU to see what it can handle. Start with `veryfast` and work down from there (faster, fast, medium, etc.) until you begin having stuttering and FPS drops in-game-- whichever option you had previously selected before the issues should be the one you set.

If you're having difficulty reaching `medium` and your stream looks awful and you haven't tried downscaling your resolution as mentioned above, you have two choices:
- Up the bit rate in intervals until you reach a decent compromise of quality versus accessibility
- Consider purchasing a more powerful CPU (see my other article [Ryzen: A dream CPU for streamers]({{ site.baseurl }}/products/ryzen-a-dream-cpu-for-streamers/){:rel='dofollow' target='_blank'})

## The Iterative Process
It is incredibly important to be in touch with the hardware, software, and limitations around your production. At the end of the day, indeed, it is about _you_ and what can differentiate you from everyone else-- what makes _you_ worth watching. However, many fail before they have that chance because they refuse to examine the consequences of their actions in the software. Remember, _Rome wasn't built in a day_ and iterating on your channel at a comfortable pace is encouraged. :-)