## 利用ffmpeg制造标准测试数据
参考
https://blog.csdn.net/lifei092/article/details/114312975

yuv文件转vp9编码ivf文件
ffmpeg -s 1280x720  -i 10s.yuv -vcodec vp9 10s_vp9.ivf

yuv文件转h264编码的avi文件
ffmpeg -s 1280x720  -i 10s.yuv -vcodec h264 10s_h264.avi

转换mp4为yuv文件
ffmpeg -i 10s.mp4 -s 1280x720 -pix_fmt yuv420p 10s.yuv

按时间剪辑mp4
ffmpeg -ss 0:0:00 -t 0:0:10 -i 5.mp4 -vcodec copy -acodec copy 10s.mp4



说明：red.mp4,red.yuv是标准红色测试视频
生成 red.ivf是vp8编码的流媒体文件
转换的 red_vp9.ivf 是vp9编码的流媒体文件

