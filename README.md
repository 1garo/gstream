# gstream

```
### filename    = name of the file
### chunk-size  = separate your video based on what you determine (e.g 100s video became 10 index<number>.ts chunks)
mkdir -p assets/media/1/hls/
cd assets/media/1/hls
ffmpeg -i <filename>.mp4 -profile:v baseline -level 3.0 -s 640x360 -start_number 0 -hls_time <chunk-size> -hls_list_size 0 -f hls index.m3u8
```
