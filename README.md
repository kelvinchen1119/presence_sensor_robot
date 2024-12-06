## 文件夹结构
```
switch_zl_8/        # 工作区
├── 1. Hardware/                   # PCB制版文件
├── 2. Firware/                    # 源代码目录
│   └── ESPHome/                   # ESPHome相关配置yaml文件
├── 3. Software/                   # empty
├── 4. CAD-Model/                  # 3D打印设计稿
├── 5. Docs/                       # 参考资料文件夹
├── 6. Test/                       # empty
├── 7. Images/                     # empty
├── README.md                      # readme_cn
└── README_en.md                   # readme_en
```

## 特别说明
- 本项目的DHT11受到芯片发热影响， 测量不准
- 本项目的人体存在传感器受到安装空间影响，会有误报情况，详细官方数据手册
- ESP32C3在本项目中运行比较吃力，会有间歇性重启现象。
- 本项目部分内容基于你自己的homeassitant数据
- 介意以上内容请勿复刻
## 项目背景
DIY人体存在传感器的进阶版；本来打算做着玩的，也没想好实际的用途，就作为一个学习套装分享吧。
通过这个项目的学习，你能够掌握：
- ESP32的基本使用技巧
- 基本的传感器使用：DHT11
- RGB灯的使用
- 旋转编码器的使用
- 点亮一块屏幕，以及在屏幕上呈现互动内容
- MQTT的使用
- 自己开发适配HomeAssitant的硬件产品

个人觉得应该是入坑智能家居的一个很好选择～
## 成品展示
### 渲染图
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/2.png" 
	style="max-width:100%" />
</center>
### 内部结构图
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/3.png" 
	style="max-width:100%" />
</center>
### 成品图
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/4.png" 
	style="max-width:100%" />
</center>

### 软件效果展示

#### 默认显示：时间、温湿度、mqtt消息订阅
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/9.jpg" 
	style="max-width:100%" />
</center>
#### 通过HA控制灯光自动化效果（gif）
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/10.gif" 
	style="max-width:100%" />
</center>
#### 根据距离感应来调整灯光自动化（gif）
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/11.gif" 
	style="max-width:100%" />
</center>




## 成本预估及购买建议
### 成本预估：
- 100+
- 影响成本的主要有：分光棱镜、LD2410、esp32c3、屏幕等

### 购买渠道

| 配件名称         | 参考价格 | 购买渠道                                                             | 链接                                                                                                   |
| ------------ | ---- | ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| PCB电路板1块     | /    | 嘉立创                                                              | /                                                                                                    |
| ESP32C3-mini | 11   | 淘宝（Saint Geffen企业店）                                              | [点击跳转](https://s.click.taobao.com/i0JbsJt)                                                           |
| LD2410B      | 18.9 | 淘宝（hilink旗舰店）                                                    | [点击跳转](https://s.click.taobao.com/pmBbsJt)                                                           |
| DHT11温湿度传感器  | 2.5  | 淘宝（推荐深圳优信电子）                                                     | 进店搜索                                                                                                 |
| 旋转编码器        | 1.89 | 淘宝（推荐深圳优信电子）                                                     | 进店搜索                                                                                                 |
| 其他电容电阻等辅料    |      | 淘宝（推荐深圳优信电子）                                                     | 进店搜索                                                                                                 |
| ST7789屏幕     | 9.9  | 淘宝我的店                                                            | [点击跳转](https://item.taobao.com/item.htm?spm=a21dvs.23580594.0.0.621e2c1bvMeQk0&ft=t&id=860664325198) |
| 3D打印外壳       | 10+  | [打印文件](https://makerworld.com/zh/models/853349#profileId-801964) | [点击跳转](https://item.taobao.com/item.htm?spm=a21dvs.23580594.0.0.621e2c1bvMeQk0&ft=t&id=860664325198) |

上面的价格都不含运费，
如果嫌淘宝麻烦的，可以在嘉立创一键下单（嘉立创没有的参考上面的链接），我已经把元器件都匹配了立创商城；
外壳的3D打印，如果自己没有打印机可以来我的淘宝小店支持一下~~

## 硬件设计
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/5.png" 
	style="max-width:100%" />
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/6.png" 
	style="max-width:100%" />
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/7.png" 
	style="max-width:100%" />
</center>

## 软件设计 / 代码参考
<center>
	<img 
	align="absmiddle" src="https://www.buda8888.com:30006/images/ReZ-TI/Product/SmartHome/Sensor/presence_sensor_robot/jlc/8.png" 
	style="max-width:100%" />
</center>

说明：本项目是基于“ESPHome”的开源项目实现的，所以实际上并没有真正的代码编程部分；更适合初学者入门学习使用

## 开源协议：GPL 3.0

**项目名称:** 
雷泽智能_全屋智能DIY入门之ESP32C3开发套装

**版权所有 (C)** 
2024 雷泽智能

本项目是基于GPL 3.0协议开源的，意味着您可以自由地使用、修改和分发该项目的源代码，但需要遵循以下条件：

1. 在使用、修改或分发本项目时，必须在显著位置注明原作者为“**雷泽智能**”，并且**不得删除**开源作品原有的“雷泽智能”品牌标识。
2. **本项目的使用仅限于非商业领域**。商业领域的使用必须获得原作者的额外授权。
3. 您必须将任何基于本项目的修改或衍生作品同样以GPL 3.0协议开源，并保留原作者信息。

**风险提示：** 
本项目涉及到220V强电，因此存在严重的用电风险。为确保安全使用，请使用者务必遵循以下建议：

1. 使用者必须具备专业的电工技能，或者寻求专业电工的支持来进行安装、调试和维护。 
2. 在使用本项目时，必须遵循相关的安全标准和规定，包括但不限于正确接地、使用合适的绝缘材料和安全设备。 
3. 使用者需了解并意识到，错误的安装或操作可能导致电击、火灾等严重的安全事故，因此对于用电风险需自行承担责任。 
4. 本项目的参考资料仅供参考，我们不对因参考项目产生的任何风险或损失承担责任。使用者在使用本项目时需自行评估风险，并采取适当的安全措施。 

在任何情况下，雷泽智能及相关贡献者不对因使用本项目而导致的任何直接或间接损失或损害承担责任。通过使用本项目，使用者已经理解并接受了这些风险和责任。

请注意，本项目提供的是"按现状"提供，没有任何明示或暗示的担保或条件。在适用法律允许的最大范围内，雷泽智能将不对任何直接、间接、偶然、特殊、惩罚性或后续的损失或损害承担责任。

如需了解更多信息，请参阅GPL 3.0协议文档。
联系信息：
微信号：rez-ti