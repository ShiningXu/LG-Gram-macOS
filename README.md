# macOS on LG Gram z980 series

## 电脑配置
| 规格     |      详细信息                              |
| -------- | ---------------------------------------- |
| 型号     | LG Gram 13/14/15 Z980 （15需要自行定制USB口） |
| CPU     | 英特尔 酷睿 i5-8250U 处理器                   |
| 显卡     | UHD Graphics 620                           |
| 内存     | 板载 8G + Micron 16G DDR4 2400MHz           |
| 硬盘     | Intel SSD 760p series 512GB                |
| 声卡     | Conexant CX8200                            |
| 网卡     | 英特尔 无线 8265 （已替换为 BCM94360）         |


## 关于WiFi的解决办法：
### 1、使用USB网卡
    使用免驱USB网卡（自行淘宝），打开内建网卡功能
### 2、通过M.2接口转接一张网卡
    lg gram 有两个m.2槽位，可以通过m.2 Mkey转接卡，转接一张BCM94360cs2，可在某宝购买 （ps.拆机失去保修，谨慎操作）
    
    硬盘位M.2不带USB接口，故无法使用蓝牙，需要自己进行焊接到其他USB口上（需要焊接，难度较高，具体方法可以私信我）

## 目前完成
  - 显卡正常，内屏显示正常，亮度调节正常；
  - CPU调频、电源管理正常；
  - 外接HDMI正常，可以同时使用内屏；
  - 声卡MIC正常，可使用音量调节+-快键、使用AppleALC 注入id:21；
  - 休眠睡眠唤醒正常，可使用FN+F4进行睡眠，键盘灯两档亮度正常；
  - Siri、iCloud、iMessage使用正常；
  - 电源正常，可显示电量
  - 键盘、摄像头等...都正常
  - I2C触摸板：勉强使用，存在单指卡死的BUG等待驱动修复；


## 未解决问题
- Intel网卡、SD读卡器、指纹，全球无解；
- 遗留小BUG
  - 无法使用FN 调节亮度（可自定义系统快捷键解决）
  - 插入电源后，电池显示电量短暂显示100%

sudo kextunload /Library/Extensions/AppleRTL815XEthernet109.kext
sudo kextunload /Library/Extensions/AppleRTL815XComposite109.kext
sudo kextload /Library/Extensions/AppleRTL815XEthernet109.kext
sudo kextload /Library/Extensions/AppleRTL815XComposite109.kext
## 联系方式
![avatar](https://github.com/ShiningXu/LG-Gram-macOS/blob/master/WechatIMG4.jpeg)