# Screen Recording

[Open Broadcaster Software](https://obsproject.com/): cross-platform streaming and recording program

Slides: Google Slides with Speaker notes

When recording: on one side of the screen I look at the speaker notes, the other side contains the OBS GUI.

Round cutout mask for OBS: https://www.versluis.com/2019/01/obs-round-cutout-mask/

I record each slide on its own with this naming schema: 010-first.mkv, 020-second.mkv, ....

This way I can insert videos later.

To join several video files: https://github.com/transitive-bullshit/ffmpeg-concat

Loading mkv files directly failed for me, so I needed to create mp4 files first:

```
for file in *.mkv; do echo $file; ffmpeg -i $file -c copy ${file}.mp4; done
```

Then create one mp4 file from the files:

```
time ./node_modules/.bin/ffmpeg-concat -t circleopen -d 750 -o out/out3.mp4 *mp4
```




