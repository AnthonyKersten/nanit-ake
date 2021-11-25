# Homebridge setup guide

1. Install plugin [Homebridge Camera FFmpeg](https://github.com/Sunoo/homebridge-camera-ffmpeg#readme)
2. Configure camera in UI (or in config similar to following snippet):

```json
{
  "name": "Camera FFmpeg",
  "cameras": [
    {
      "name": "Nanit",
      "videoConfig": {
        "source": "-i rtmp://xxx.xxx.xxx.xxx:1935/local/{your_baby_uid}",
        "vcodec": "copy",
        "audio": true
      }
    }
  ],
  "platform": "Camera-ffmpeg"
}
```

3. Restart Homebridge

## Homebridge with multiple NICs

There is a reported problem if you are running Homebridge with multiple NICs. It seems that you need to choose one in the HB Config UI (#19).

