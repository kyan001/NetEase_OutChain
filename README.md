# NetEase_OutChain
网易云外链

api.py:<br/>
传入参数为歌曲ID，返回值为该歌曲的MP3地址。<br/>
需要安装 python3<br/>
并 pip 安装 request, pycrypto<br/>

list.php:<br/>
播放列表，支持歌单和单曲<br/>
会从歌单和单曲组成的歌曲集合中随机选取。<br/>

player.php:<br/>
从播放列表中随机选取歌曲，同时排除已经播放过的曲目。<br/>
GET 取得歌曲的名称、艺术家、歌词、翻译、封面等，<br/>
调用 api.py 取得歌曲 mp3URL，<br/>
最终返回 json<br/>

如何使用：
1.python3 环境和 php 环境<br/>
2.在网页中使用 javascript 通过 ajax 请求 player.php，<br/>
解析返回的 json 数据，并根据需要显示。<br/>

测试：(2017/09/02 可用)<br/>
http://music.ocrosoft.com<br/>

致谢：<br/>
https://github.com/darknessomi/musicbox（命令行版网易云音乐，新版API参考于此）<br/>
https://github.com/Mooooooon/Musicoon（网易云音乐私人FM，旧版API和测试页面HTML和CSS等参考于此）
PS:旧版API已经无法获取到mp3URL，但仍能获取到歌词等信息。
