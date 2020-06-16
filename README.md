备注：

footer.png（尾部裙子）的样式调整文件在F:\Blog\themes\hexo-theme-sagiri\source\css\_schemes\Pisces\footer.styl



左边原来的live2d在F:\Blog\themes\hexo-theme-sagiri\layout\_layout.swig

aplayer

| 主要参数      |                              值                              |
| :------------ | :----------------------------------------------------------: |
| data-id       |                      歌曲/专辑/歌单 ID                       |
| data-server   | netease（网易云音乐）tencent（QQ音乐） xiami（虾米） kugou（酷狗） |
| data-type     | song （单曲） album （专辑） playlist （歌单） search （搜索） |
| data-mode     | random （随机） single （单曲） circulation （列表循环） order （列表） |
| data-autoplay |              false（手动播放） true（自动播放）              |

| 名称            | 默认值                             | 描述                                                         |
| --------------- | ---------------------------------- | ------------------------------------------------------------ |
| container       | document.querySelector('.aplayer') | 播放器容器元素                                               |
| fixed           | false                              | 开启吸底模式, [详情](https://aplayer.js.org/#/home?id=fixed-mode) |
| mini            | false                              | 开启迷你模式, [详情](https://aplayer.js.org/#/home?id=mini-mode) |
| autoplay        | false                              | 音频自动播放                                                 |
| theme           | '#b7daff'                          | 主题色                                                       |
| loop            | 'all'                              | 音频循环播放, 可选值: 'all', 'one', 'none'                   |
| order           | 'list'                             | 音频循环顺序, 可选值: 'list', 'random'                       |
| preload         | 'auto'                             | 预加载，可选值: 'none', 'metadata', 'auto'                   |
| volume          | 0.7                                | 默认音量，请注意播放器会记忆用户设置，用户手动设置音量后默认音量即失效 |
| audio           | -                                  | 音频信息, 应该是一个对象或对象数组                           |
| audio.name      | -                                  | 音频名称                                                     |
| audio.artist    | -                                  | 音频艺术家                                                   |
| audio.url       | -                                  | 音频链接                                                     |
| audio.cover     | -                                  | 音频封面                                                     |
| audio.lrc       | -                                  | [详情](https://aplayer.js.org/#/home?id=lrc)                 |
| audio.theme     | -                                  | 切换到此音频时的主题色，比上面的 theme 优先级高              |
| audio.type      | 'auto'                             | 可选值: 'auto', 'hls', 'normal' 或其他自定义类型, [详情](https://aplayer.js.org/#/home?id=mse-support) |
| customAudioType | -                                  | 自定义类型，[详情](https://aplayer.js.org/#/home?id=mse-support) |
| mutex           | true                               | 互斥，阻止多个播放器同时播放，当前播放器播放时暂停其他播放器 |
| lrcType         | 0                                  | [详情](https://aplayer.js.org/#/home?id=lrc)                 |
| listFolded      | false                              | 列表默认折叠                                                 |
| listMaxHeight   | -                                  | 列表最大高度                                                 |
| storageName     | 'aplayer-setting'                  | 存储播放器设置的 localStorage key                            |

| 原版Sagiri                                                   | gitee版Sagiri                                                | 文件位置                                                     | 备注                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------- |
| 无                                                           | passage-end-tag.swig                                         | C:\Users\Pluto\Desktop\hexo-theme-sagiri\layout\_macro       |                      |
|                                                              | 第348行多了<div>        {% if not is_index %}          {% include 'passage-end-tag.swig'   %}        {% endif %}      </div> | C:\Users\Pluto\Desktop\hexo-theme-sagiri\layout\_macro\post.swig |                      |
|                                                              | 第380行多了<i class="fa   fa-tag"></i>                       |                                                              |                      |
| 第98行多一个{# #}                                            |                                                              | C:\Users\Pluto\Desktop\hexo-theme-sagiri\layout\_macro\sidebar.swig |                      |
|                                                              | 博客共{{ totalcount(site) }}字, 你是第个访问者, 共被访问次.  | F:\Blog\themes\hexo-theme-sagiri\layout\_partials\footer.swig |                      |
|                                                              | 尾部备案，以及作者未解决                                     |                                                              |                      |
| #nprogress   .bar {        background: #97dffd;      }            @import "../../node_modules/balloon-css/balloon.css" |                                                              | C:\Users\Pluto\Desktop\hexo-theme-sagiri\source\css\main.styl | 疑似鼠标点击爆炸效果 |
|                                                              |                                                              | 主题config第131行链接未完成                                  |                      |
|                                                              |                                                              | 有空换一个尾部                                               |                      |

搜索功能     使用 Swiftype 给 Hexo 搭建的博客添加站内搜索功能

相册

代码压缩

视频以及音乐

