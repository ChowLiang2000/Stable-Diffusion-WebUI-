## AnimateDiff使用教程（记录）
2024.3.28
秋叶包SD-WEBUI aki-4.6.1 / aki-4.7
### 安装插件
* SD WebUI扩展列表搜索AnimateDiff 

* 或网盘安装：

  度盘链接：https://pan.baidu.com/s/1gAqci83zhvmbF1LHj5DjDQ?pwd=nely 

  夸克链接：https://pan.quark.cn/s/b9e94283aa34

* 或通过url安装https://github.com/continue-revolution/sd-webui-animatediff/

### AnimateDiff模型（运动模块）下载地址：
AnimateDiff官方仓库：https://huggingface.co/guoyww/animatediff/tree/main

### 插帧（可选）
  ![image](https://github.com/ChowLiang2000/Stable-Diffusion-WebUI-/assets/149044657/fd2e853f-0398-4d91-acb9-8e435af66218)
* 安装Deforum扩展 https://github.com/deforum-art/sd-webui-deforum
* 网盘链接中找到film_net_fp16.pt，下载并放置到“根目录\models\Deforum\film_interpolation”文件夹内

  （如果不预先下载，运行时也会自动下载。但没有代理会非常慢，如果看到命令行中进度条卡在下载一个65.8M的东西，就是在下这个。）
* 帧插值功能默认Off, 如需开启，点击FILM选项

### 使用
文生图或图生图前期流程不变
* 找到AnimateDiff模块
1. 选择动画模型

2. 点击启用AnimateDiff

3. 选择需要的格式（一般GIF或MP4， 如果勾选PNG会保存每一帧图片）

4. 设定总帧数和帧率（帧率 x 时长（秒）=总帧数）

* 闭环（即第一帧和最后一帧是否相似）
  N为不循环，A为完美循环（无缝循环播放），R+-P为两种不同循环模式（待比较）
* I2VTraditional
  power越小，scale越大，越接近原图

  如需指定最后一帧，则在此模块的last frame区域上传图片，
  
  控制last frame的power和scale作用同理

### 注意事项
*  提示词不能超过75个，否则报错
*  图生图时重绘幅度不要低于0.6，否则会有雪花斑点

* 部分反向提示词会导致报错，报错显示 Assertion '-sizes[i]<= index && index < sizes[i] && "index out of bounds"'failed. 清空反向提示词则正常

 * 秋叶包aki-4.6.1(绘世2.7)出现只能绘制512x512的问题，尺寸改成512x768就报错'index out of bounds'failed，下载最新的aki-4.7(绘世2.8.2)版本，没有此问题。
### 待解决
 
 教程推荐在设置中补齐提示词，这个作用是什么？

 ### 参考：
 https://www.bilibili.com/video/BV1zS421A7PG Nenly同学
 

