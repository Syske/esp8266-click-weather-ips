# 项目说明

## 简介

本项目是基于`esp8266`和`IPS`彩屏的一个桌面天气时钟，项目代码基于嘉立创开源平台的《`ESP8266`太空人天气时钟》源码，优化了其中`HTTPClient`的报错，代码本身未作大的调整，项目地址如下：

```
https://oshwhub.com/nanxiangxiao/tai-kong-ren-shi-zhong_copy
```


## 项目的环境设置

### 硬件部分

#### 材料说明

- `esp8266`开发板
- `1.3`寸`IPS`屏幕，驱动版本`ST7789`
- 杜邦线`6`根


#### 接线说明

TFT | esp8266 | 备注
---|---|---
GND | G  |
VCC | 3V |
SCL | D5 |
SDA | D7 |
RES | D4 |
DC  | D3 |



### 软件部分

### 开发环境和依赖

#### 依赖库

安装`TFT_eSPI`库

![](https://syske-pic-bed.oss-cn-hangzhou.aliyuncs.com/imgs/20230228230533.png)

#### 修改配置

运行测试用例前，我们要先修改`Arduino\libraries\TFT_eSPI`下的`User_Setup.h`文件，具体修改的点如下：

- 驱动文件设置：这里根据`TFT`屏幕的驱动版本选择
  
![驱动](https://syske-pic-bed.oss-cn-hangzhou.aliyuncs.com/imgs/20230228230850.png)

- 屏幕分辨率：这里也是根据屏幕参数选择

![分辨率](https://syske-pic-bed.oss-cn-hangzhou.aliyuncs.com/imgs/20230228231357.png)

- 引脚设置：这里只需要设置`dc`和`rst`引脚即可

![](https://syske-pic-bed.oss-cn-hangzhou.aliyuncs.com/imgs/20230228231504.png)

其余配置项保持默认即可。

#### 上传

完成以上配置和准备工作之后，我们需要打开本项目的核心文件`click-weather.ino`，并修改为自己的`wifi`名称和密码，之后连接开发板，上传代码即可。演示视频可以看这里：