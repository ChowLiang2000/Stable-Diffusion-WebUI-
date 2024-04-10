# Stable-Diffusion-WebUI-
秋叶一键包 使用教程

### 安装和启动

推荐英伟达GPU,但实测其他显卡也能出图

https://pan.quark.cn/s/2c832199b09b 作者：秋葉aaaki 


下载秋叶一键包


解压sd-webui-aki-vxxx.7z


如果是第一次启动，先运行启动器运行依赖.exe


双击A绘世启动器.exe启动即可

### 大模型下载与使用

链接：https://pan.quark.cn/s/b54b6d74d388
提取码：jzgm
- majicmixRealistic_v7: &nbsp;&nbsp;真实风格亚洲人模型
- dgirl: &nbsp;&nbsp;真实风格亚洲人模型
- anything-v5:&nbsp;&nbsp;动漫风格

下载的大模型（checkpoint）放到models/Stable-diffusion/目录下

- 启动后点击模型选择框可选择使用的大模型
- 若不显示，可尝试点击右侧刷新按钮更新模型列表

### 文生图基础参数设置
#### 模型
- StableDiffusion模型：上文选择的模型（如：majicmixRealistic_v7）
- vae：可选None
- Clip： 2
#### 提示词
- 正向提示词：根据需要填写（如：1girl）
  
  常用：SFW, (masterpiece:1,2), best quality, masterpiece, highres, original, extremely detailed wallpaper, perfect lighting,(extremely detailed CG:1.2),


- 反向提示词：根据需要填写
  
  常用：NSFW, (worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality, ((monochrome)), ((grayscale)), skin spots, acnes, skin blemishes, age spot, (ugly:1.331), (duplicate:1.331), (morbid:1.21), (mutilated:1.21), (tranny:1.331), mutated hands, (poorly drawn hands:1.5), blurry, (bad anatomy:1.21), (bad proportions:1.331), extra limbs, (disfigured:1.331), (missing arms:1.331), (extra legs:1.331), (fused fingers:1.61051), (too many fingers:1.61051), (unclear eyes:1.331), lowers, bad hands, missing fingers, extra digit,bad hands, missing fingers, (((extra arms and legs))),
#### 生成
- 采样方法：DPM++ 2M Karras
- 迭代步数：20
- 宽度：512
- 高度：512
- 提示词引导系数：7.5

其余默认即可

**点击右侧生成按钮即可进行出图**





### 其他进阶使用教程：
#### controlNet 使用教程(控制人物姿势、图形结构等):

[controlNet](controlNet.md)

#### AnimateDiff 动画插件使用教程:
https://github.com/ChowLiang2000/AnimateDiff-
