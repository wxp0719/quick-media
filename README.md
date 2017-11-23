## quick-media
> 多媒体处理web服务
>
> mult-media process Web Service by FFMPEG & ImageMagic & SpringMVC
 
本项目为一个提供图片 + 音频 + 视频处理的Web项目，我们的目标是封装一套多媒体文件处理的公共类库，简化各种复杂的调用

利用 spring-boot 来提供http接口实现多媒体的操作


### 技术栈

- spring-boot 
- ffmpeg
- imageMagic
- zxing


### 已支持服务

#### 1. 音频转码
   - [x] 音频不同格式的相互转码

#### 2. 二维码生成 & 解析
- [x] 二维码生成
- [x] 个性二维码生成
    - 支持logo
    - 支持logo样式 （圆角logo， 边框）
    - 支持二维码颜色设置
    - 支持探测图形颜色设置
    - 支持背景图
    - 支持base64格式的二维码图片
    - 支持二维码定制绘制信息样式
     - 三角形
     - 矩形
     - 五边形 （五角星待支持）
     - 六边形
     - 八边形
     - 圆
     - 自定义图片
- [x] 二维码信息解析

[查看更多二维码详情](doc/qrcode/QrGuide.md)



#### 3. 图片

- [x] 长图文生成
   - [水平文字，上下布局长图文生成](doc/images/imgGenV1.md)
   - [垂直文字，左右布局长图文生成](doc/images/imgGenV2.md)
   - 第三方字体支持
- [x] markdown 转 image
    - [markdown 转 html](doc/md/md2html.md)
    - [html 转 image](doc/md/html2image.md)
- [x] gif图生成
- [x] 合成
    - [图片合成支持](doc/images/imgMerge.md)
- [x] 水印
- [ ] 裁剪
- [ ] 压缩
- [ ] 旋转
- [ ] 缩放
- [ ] 格式转换

[查看更多图片服务详情](doc/images/ImgGuide.md)
    
#### 4. 视频相关
- [ ] 视频压缩
- [ ] 转码
- [ ] 截取
- [ ] 码率调整
- [ ] 生成gif


### tag 记录

1. [v0.001](https://github.com/liuyueyi/quick-media/releases/tag/v0.001)

    - 实现音频转码服务
    - 实现二维码基础服务，完成基于zxing的二维码深度定制
 
2. [v0.002](https://github.com/liuyueyi/quick-media/releases/tag/v0.002)

    - 重写zxing的二维码渲染逻辑，只使用二维码矩阵的生成逻辑，支持二维码的全面定制化

3. [v0.003](https://github.com/liuyueyi/quick-media/releases/tag/v0.003)

    - 长图文生成的支持

4. [v0.004](https://github.com/liuyueyi/quick-media/releases/tag/v0.004)
   
   - markdown 语法文本转html， 转image

### 文档

- [音频转码服务说明](doc/audio.md)
- [二维码生成解析服务说明](doc/qrcode/QrGenV1.md)
- [二维码服务拓展说明](doc/qrcode/QrGenV2.md)
- [二维码生成深度定制](doc/qrcode/QrGenV3.md)
- [长图文生成支持](doc/images/imgGenV1.md)
- [竖排长图文生成支持](doc/images/imgGenV2.md)
- [markdown 转 html](doc/md/md2html.md)
- [html 转 image](doc/md/html2image.md)
- [图片合成支持](doc/images/imgMerge.md)

### 问题记录汇总

- [图片旋转不生效问题](doc/questions/ImgRotate.md)
- [markdonw转图片中文乱码问题](doc/questions/md2imgChineseMessyCode.md)

### 其他

关注小灰灰blog，获取更多信息

![qrcodeInfo](doc/img/qrcode/qrInfoV3.jpg)



### 实例演示

以本项目提供的基本服务为蓝本，写了一个简单的小程序，欢迎各位小伙伴尝鲜

后端服务都在本项目中，包目录 : 

`com.hust.hui.quickmedia.web.wxapi`

有很多东西直接写死了，不太友好，欢迎板砖


![http://s2.mogucdn.com/mlcdn/c45406/171123_3dj8kcb295lf3ilif699kjc0hlf10_860x860.jpg](http://s2.mogucdn.com/mlcdn/c45406/171123_3dj8kcb295lf3ilif699kjc0hlf10_860x860.jpg "图文小工具码")