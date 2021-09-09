# Screen Recording

[Open Broadcaster Software](https://obsproject.com/): cross-platform streaming and recording program

Slides: Google Slides with Speaker notes

When recording: on one side of the screen I look at the speaker notes, the other side contains the OBS GUI.

# Round cutout mask

Round cutout mask for OBS: https://www.versluis.com/2019/01/obs-round-cutout-mask/

# Record one slide after the other

I record each slide on its own with this naming schema: 010-first.mkv, 020-second.mkv, .... This way I can insert videos later.

Before recording: If you don't need the mouse cursor to present something, then move the mouse cursor out of the screen, so it is not visible. 

# Join several videos

To join several video files: https://github.com/transitive-bullshit/ffmpeg-concat

Loading mkv files directly failed for me, so I needed to create mp4 files first:

```
for file in *.mkv; do echo $file; ffmpeg -i $file -c copy ${file}.mp4; done
```

Then create one mp4 file from the files:

```
time ./node_modules/.bin/ffmpeg-concat -t circleopen -d 750 -o out/out.mp4 *mp4
```

Since OBS worked very well I donated some money to them: https://obsproject.com/de/contribute

# Nice light

If you record yourself, then fairy lights with a warm white behind the camera give you a shadowless light on your face.

# Video format: webm

[WebM](https://en.wikipedia.org/wiki/WebM) is the best choice at the moment. See [Can I use: WebM](https://caniuse.com/webm)

# WOL

[Working out loud](https://github.com/guettli/wol)
