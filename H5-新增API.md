## H5-新增API

### 全屏方法

> HTML5规范允许用户自定义网页上任一元素全屏显示。

- Node.requestFullScreen() 开启全屏显示
- Node.cancelFullScreen() 关闭全屏显示
- 由于其兼容性原因，不同浏览器需要添加前缀如：
  webkit内核浏览器：webkitRequestFullScreen、webkitCancelFullScreen，如chrome浏览器。
  Gecko内核浏览器：mozRequestFullScreen、mozCancelFullScreen，如火狐浏览器。
- document.fullScreen检测当前是否处于全屏
  不同浏览器需要添加前缀
  document.webkitIsFullScreen、document.mozFullScreen

### 多媒体

> 自定义播放器

方法

| 方法           | 描述                                    |
| -------------- | --------------------------------------- |
| addTextTrack() | 向音频/视频添加新的文本轨道             |
| canPlayType()  | 检测浏览器是否能播放指定的音频/视频类型 |
| load()         | 重新加载音频/视频元素                   |
| play()         | 开始播放音频/视频                       |
| pause()        | 暂停当前播放的音频/视频                 |

属性

| 属性                | 描述                                                       |
| ------------------- | ---------------------------------------------------------- |
| audioTracks         | 返回表示可用音轨的 AudioTrackList 对象                     |
| autoplay            | 设置或返回是否在加载完成后随即播放音频/视频                |
| buffered            | 返回表示音频/视频已缓冲部分的 TimeRanges 对象              |
| controller          | 返回表示音频/视频当前媒体控制器的 MediaController 对象     |
| controls            | 设置或返回音频/视频是否显示控件（比如播放/暂停等）         |
| crossOrigin         | 设置或返回音频/视频的 CORS 设置                            |
| currentSrc          | 返回当前音频/视频的 URL                                    |
| currentTime         | 设置或返回音频/视频中的当前播放位置（以秒计）              |
| defaultMuted        | 设置或返回音频/视频默认是否静音                            |
| defaultPlaybackRate | 设置或返回音频/视频的默认播放速度                          |
| duration            | 返回当前音频/视频的长度（以秒计）                          |
| ended               | 返回音频/视频的播放是否已结束                              |
| error               | 返回表示音频/视频错误状态的 MediaError 对象                |
| loop                | 设置或返回音频/视频是否应在结束时重新播放                  |
| mediaGroup          | 设置或返回音频/视频所属的组合（用于连接多个音频/视频元素） |
| muted               | 设置或返回音频/视频是否静音                                |
| networkState        | 返回音频/视频的当前网络状态                                |
| paused              | 设置或返回音频/视频是否暂停                                |
| playbackRate        | 设置或返回音频/视频播放的速度                              |
| played              | 返回表示音频/视频已播放部分的 TimeRanges 对象              |
| preload             | 设置或返回音频/视频是否应该在页面加载后进行加载            |
| readyState          | 返回音频/视频当前的就绪状态                                |
| seekable            | 返回表示音频/视频可寻址部分的 TimeRanges 对象              |
| seeking             | 返回用户是否正在音频/视频中进行查找                        |
| src                 | 设置或返回音频/视频元素的当前来源                          |
| startDate           | 返回表示当前时间偏移的 Date 对象                           |
| textTracks          | 返回表示可用文本轨道的 TextTrackList 对象                  |
| videoTracks         | 返回表示可用视频轨道的 VideoTrackList 对象                 |
| volume              | 设置或返回音频/视频的音量                                  |

### 事件

| 事件           | 描述                                         |
| -------------- | -------------------------------------------- |
| abort          | 当音频/视频的加载已放弃时                    |
| canplay        | 当浏览器可以播放音频/视频时                  |
| canplaythrough | 当浏览器可在不因缓冲而停顿的情况下进行播放时 |
| durationchange | 当音频/视频的时长已更改时                    |
| emptied        | 当目前的播放列表为空时                       |
| ended          | 当目前的播放列表已结束时                     |
| error          | 当在音频/视频加载期间发生错误时              |
| loadeddata     | 当浏览器已加载音频/视频的当前帧时            |
| loadedmetadata | 当浏览器已加载音频/视频的元数据时            |
| loadstart      | 当浏览器开始查找音频/视频时                  |
| pause          | 当音频/视频已暂停时                          |
| play           | 当音频/视频已开始或不再暂停时                |
| playing        | 当音频/视频在已因缓冲而暂停或停止后已就绪时  |
| progress       | 当浏览器正在下载音频/视频时                  |
| ratechange     | 当音频/视频的播放速度已更改时                |
| seeked         | 当用户已移动/跳跃到音频/视频中的新位置时     |
| seeking        | 当用户开始移动/跳跃到音频/视频中的新位置时   |
| stalled        | 当浏览器尝试获取媒体数据，但数据不可用时     |
| suspend        | 当浏览器刻意不获取媒体数据时                 |
| timeupdate     | 当目前的播放位置已更改时                     |
| volumechange   | 当音量已更改时                               |
| waiting        | 当视频由于需要缓冲下一帧而停止               |

### 地理定位

> 在HTML规范中，增加了获取用户地理信息的API，
> 这样使得我们可以基于用户位置开发互联网应用，
> 即基于位置服务 (Location Base Service)

- 获取当前地理信息

```
navigator.geolocation.getCurrentPosition(successCallback, errorCallback) 
```

- 重复获取当前地理信息

```
navigator. geolocation.watchPosition(successCallback, errorCallback)
```

- 当成功获取地理信息后，会调用succssCallback，并返回一个包含位置信息的对象position。
  position.coords.latitude纬度
  position.coords.longitude经度
  position.coords.accuracy精度
  position.coords.altitude海拔高度
- 当获取地理信息失败后，会调用errorCallback，并返回错误信息error
- 在现实开发中，通过调用第三方API（如百度地图）来实现地理定位信息，这些API都是基于用户当前位置的，并将用位置位置（经/纬度）当做参数传递，就可以实现相应的功能。

### 本地存储

> 随着互联网的快速发展，基于网页的应用越来越普遍，
> 同时也变的越来越复杂，为了满足各种各样的需求，会经常性在本地存储大量的数据，
> HTML5规范提出了相关解决方案。

- 特性
  - 设置、读取方便
  - 容量较大，sessionStorage约5M、localStorage约20M
  - 只能存储字符串，可以将对象JSON.stringify() 编码后存储
- window.sessionStorage
  - 生命周期为关闭浏览器窗口
  - 在同一个窗口(页面)下数据可以共享
- window.localStorage
  - 永久生效，除非手动删除（服务器方式访问然后清除缓存）
  - 可以多窗口（页面）共享
- 方法
  - setItem(key, value) 设置存储内容
  - getItem(key) 读取存储内容
  - removeItem(key) 删除键值为key的存储内容
  - clear() 清空所有存储内容

### 历史管理

> 提供window.history，对象我们可以管理历史记录，
> 可用于单页面应用，Single Page Application，可以无刷新改变网页内容。

- pushState(data, title, url) 追加一条历史记录  
  - data用于存储自定义数据，通常设为null
    ​+ title网页标题，基本上没有被支持，一般设为空
    ​+ url 以当前域为基础增加一条历史记录，不可跨域设置
- replaceState(data, title, url) 与pushState()基本相同，
  不同之处在于replaceState()，只是替换当前url，不会增加/减少历史记录。
- onpopstate事件，当前进或后退时则触发  

### 离线应用

> HTML5中我们可以轻松的构建一个离线（无网络状态）应用，只需要创建一个cache manifest文件。

- 优势
  - 1、可配置需要缓存的资源
  - 2、网络无连接应用仍可用
  - 3、本地读取缓存资源，提升访问速度，增强用户体验
  - 4、减少请求，缓解服务器负担
- 缓存清单
  - 一个普通文本文件，其中列出了浏览器应缓存以供离线访问的资源，推荐使用.appcache为后缀名
  - 例如我们创建了一个名为demo.appcache的文件，然后在需要应用缓存在页面的根元素(html)添加属性manifest="demo.appcache"，路径要保证正确。
- manifest文件格式
  - 1、顶行写CACHE MANIFEST
  - 2、CACHE: 换行 指定我们需要缓存的静态资源，如.css、image、js等
  - 3、NETWORK: 换行 指定需要在线访问的资源，可使用通配符
  - 4、FALLBACK: 换行 当被缓存的文件找不到时的备用资源
- 其它
  - 1、CACHE: 可以省略，这种情况下将需要缓存的资源写在CACHE MANIFEST
  - 2、可以指定多个CACHE: NETWORK: FALLBACK:，无顺序限制
  - 3、#表示注释，只有当demo.appcache文件内容发生改变时或者手动清除缓存后，才会重新缓存。
  - 4、chrome 可以通过chrome://appcache-internals/工具和离线（offline）模式来调试管理应用缓存

### 文件读取

> HTML5新增内建对象，可以读取本地文件内容。

### 网络状态

- 我们可以通过window.onLine来检测，用户当前的网络状况，返回一个布尔值
  - window.online用户网络连接时被调用
  - window.offline用户网络断开时被调用

