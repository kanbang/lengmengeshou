---
title: tmp
date: 2020-05-07 15:18:22
tags: 
- hexo
- note

categories:
- [就是玩]
- [学习笔记]
---



```
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
```


``` js
<script>
var _hmt = _hmt || [];
(function() {
  var hm = document.createElement("script");
  hm.src = "https://hm.baidu.com/hm.js?29680a68014435ebb212ffbe5d533d02";
  var s = document.getElementsByTagName("script")[0]; 
  s.parentNode.insertBefore(hm, s);
})();
</script>
```


npm install hexo-tag-dplayer -s

{% dplayer "url=https://dl.sm9.top/Video/2018/KeyCastOW.mp4" %} 

{% dplayer "url=https://dl.sm9.top/Video/2018/%E6%8E%98%E5%9C%B0%E6%B1%82%E5%8D%87_x264.mp4" " screenshot" "loop=yes" "id=46190A32F63DFF2CF0A3BB0F3293636C" "api=https://api.prprpr.me/dplayer/" "addition=https://api.prprpr.me/dplayer/v3/bilibili?aid=17150441 " %} 



添加访客地图
前往 clustrmaps 网站注册一个帐号。

找到 Free Tools下面的 Website Widget, 点击 Get Map Widget

<script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=c_Iul3wZifn4Fg-PeHmrUkQsjsdYFJrUbGg5ES5kP2E"></script>


在 themes\Butterfly\layout\includes\widget文件夹新建card_map.pug文件，文件内容如下：

CODE
.card-widget.card-map
  .card-content
    .item-headline
      i.fa.fa-globe-asia(aria-hidden="true")
      span= _p('aside.card_map')
    script#clstr_globe(type="text/javascript" defer="defer" src="此处填入你自己的代码")
    
编辑 themes\Butterfly\layout\includes\widget\index.pug 文件，在你想要显示的位置插入以下代码：

CODE
if theme.aside.card_map
        !=partial('includes/widget/card_map', {}, {cache:true})
具体放置位置，可以参考下图（切记：如果主题版本大于3.6，请务必将{cache:theme.fragment_cache} 改为 { cache:true }）：


编辑 _config.butterfly.yml 文件，在 card_webinfo 下面添加一行card_map: true

编辑 themes\Butterfly\languages\zh-CN.yml文件 (请根据你的网站语言选择)，找到 card_announcement: 公告 , 在下面添加一行 card_map: 访客地图 (后面的文本可自定义),繁体字方法一样，修改themes\Butterfly\languages\zh-TW.yml文件就行。

如果不想显示，直接把 _config.butterfly.yml文件的card_map: true 改为 card_map: false 即可。

效果如下：




一、Cannot GET /tags/：
步骤一：
$ hexo new page "tags"

步骤二：将source/tags文件夹下index.md文件里的内容修改为（复制可用）：
---
type: "tags"
layout: "tags"
comments: false
---



hexo new page link

hexo new page categories

hexo new page tags