## AnimateDiff 使用教程（记录）

2024.3.28
秋叶包 SD-WEBUI 1.8 内核 aki-4.6.1 / aki-4.7

### 安装插件

- SD WebUI 扩展列表搜索 AnimateDiff

- 或网盘安装：

  度盘链接：https://pan.baidu.com/s/1gAqci83zhvmbF1LHj5DjDQ?pwd=nely

  夸克链接：https://pan.quark.cn/s/b9e94283aa34

- 或通过 url 安装https://github.com/continue-revolution/sd-webui-animatediff/

### AnimateDiff 模型（运动模块）下载地址：

AnimateDiff 官方仓库：https://huggingface.co/guoyww/animatediff/tree/main

### 插帧（可选）

![image](https://github.com/ChowLiang2000/Stable-Diffusion-WebUI-/assets/149044657/fd2e853f-0398-4d91-acb9-8e435af66218)

- 安装 Deforum 扩展 https://github.com/deforum-art/sd-webui-deforum
- 网盘链接中找到 film_net_fp16.pt，下载并放置到“根目录\models\Deforum\film_interpolation”文件夹内

  （如果不预先下载，运行时也会自动下载。但没有代理会非常慢，如果看到命令行中进度条卡在下载一个 65.8M 的东西，就是在下这个。）

- 帧插值功能默认 Off, 如需开启，点击 FILM 选项

### 使用

文生图或图生图前期流程不变

- 找到 AnimateDiff 模块

1. 选择动画模型

2. 点击启用 AnimateDiff

3. 选择需要的格式（一般 GIF 或 MP4， 如果勾选 PNG 会保存每一帧图片）

4. 设定总帧数和帧率（帧率 x 时长（秒）=总帧数）

- 闭环（即第一帧和最后一帧是否相似）
  N 为不循环，A 为完美循环（无缝循环播放），R+-P 为两种不同循环模式（待比较）
- I2VTraditional
  power 越小，scale 越大，越接近原图

  如需指定最后一帧，则在此模块的 last frame 区域上传图片，

  控制 last frame 的 power 和 scale 作用同理

### 注意事项

- 提示词不能超过 75 个，否则报错
- 图生图时重绘幅度不要低于 0.6，否则会有雪花斑点

- 部分反向提示词会导致报错，报错显示 Assertion '-sizes[i]<= index && index < sizes[i] && "index out of bounds"'failed. 清空反向提示词则正常

### 待解决

- aki-4.6+2024.2.9 版本 animateDiff:
  出现只能绘制 512x512 的问题，尺寸改成 512x768 就报错'index out of bounds'failed

  文生图不能添加视频参考，controlNet 报错

  图生图可以用 controlNet（512x512）

- aki-4.7+3 月新版本 animateDiff 文生图可以生成 768 高的视频，用 controlNet 的 openpose 没问题
  图生图用 controlNet 会报错，只生成 image grade,不生成视频
  ![image](https://github.com/ChowLiang2000/Stable-Diffusion-WebUI-/assets/149044657/fcbe965d-8a73-4982-950c-059ac59bbe26)
  想要快一点看效果，总帧率设为 8，结果会报错，设为 16 则不会。
- Nenly 教程中推荐在设置中补齐提示词，这个作用是什么？

### 参考：

https://www.bilibili.com/video/BV1zS421A7PG Nenly 同学
