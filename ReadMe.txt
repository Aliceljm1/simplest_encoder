## ����ffmpeg�����׼��������
�ο�
https://blog.csdn.net/lifei092/article/details/114312975

yuv�ļ�תvp9����ivf�ļ�
ffmpeg -s 1280x720  -i 10s.yuv -vcodec vp9 10s_vp9.ivf

yuv�ļ�תh264�����avi�ļ�
ffmpeg -s 1280x720  -i 10s.yuv -vcodec h264 10s_h264.avi

ת��mp4Ϊyuv�ļ�
ffmpeg -i 10s.mp4 -s 1280x720 -pix_fmt yuv420p 10s.yuv

��ʱ�����mp4
ffmpeg -ss 0:0:00 -t 0:0:10 -i 5.mp4 -vcodec copy -acodec copy 10s.mp4



˵����red.mp4,red.yuv�Ǳ�׼��ɫ������Ƶ
���� red.ivf��vp8�������ý���ļ�
ת���� red_vp9.ivf ��vp9�������ý���ļ�

