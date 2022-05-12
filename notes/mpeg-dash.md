ABR stands for Adaptive Bit-Rate streaming. It is the process by which the quality and bitrate of video delivery are adaptively varied to match the bandwidth conditions and ensure smooth delivery over the internet.
In ABR streaming, a video is transcoded into multiple resolutions and bitrate combinations and each is referred to as a “rendition”. A collection of renditions is a bitrate ladder.
Example of a bitrate ladder –

1080p 5.0 mbps
720p 4.0 mbps
640p 3.2 mbps
480p 2.0 mbps
270p 1 mbps

Let’s assume that the video has been encoded at the bitrate ladder shown above. When the player starts to playback the video, it senses the available bandwidth and let’s assume its 20 mbps. This is much greater than the highest bitrate viz. 5 mbps. So, the player safely downloads the highest bitrate, 5 mbps for the first segment/chunk (perhaps, 6 seconds long). Then the player senses the bandwidth again and if it is still very high, it asks for the highest bandwidth again.

If the bandwidth suddenly drops to 5 mbps, then the player will probably request for the 4 mbps chunk from the server because it is risky to ask for the 5 mbps chunk. It then receives and plays back the 4 mbps chunk.
This process continues throughout the video. This is how the bitrate and quality are adaptively varied to adapt to the varying bandwidth conditions.

MPEG-DASH (Dynamic Adaptive Streaming) is an HTTP-based streaming protocol for delivering video(VOD and Live stream) to the end-user from an HTTP server. In MPEG-DASH, a video is split into segments and this information is recorded in an MPD(Media Presentation Description) . The MPD is first delivered to the player, which uses it to request segments of the appropriate bitrate & resolution based on the network conditions and buffer fullness.
As its name suggests, DASH or Dynamic Adaptive Streaming over HTTP works on the principles of ABR or Adaptive Bitrate Streaming. In a nutshell, this is how MPEG-DASH works –

How does MPEG-DASH work - Architecture

<img width="517" alt="image" src="https://user-images.githubusercontent.com/52416142/168067662-93a3a82b-96a4-49c9-b0c6-f9d67bf221f0.png">
