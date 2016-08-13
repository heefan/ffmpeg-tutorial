[An ffmpeg and SDL Tutorial](http://dranger.com/ffmpeg/)

影音文件： movie

影音文件有一些基本的`组件`

`容器`（container）：影音文件本身，比如`AVI`,`Quicktime`，他们也决定了影音文件的格式。
`流`（Stream）: 一个影音文件通常包含`音频流`(audio stream)和`视频流`（video stream)
`帧`（frame）：一系列连续的`帧`组成一个`流`
`编解码器`（codec）：每个帧都使用不同的`编码器`进行编码。编码的英文是COded，解码的英文是DECoded，所以组合起来就是`CODEC`, 常见的编解码器有`DivX`和`MP3`。
`包`（Paackets）：从`流`中读出来的一组数据，解码后变成帧的二进制码（raw data），我们最终使用这些帧的二进制码来实现我们的应用程序的需要。
