# CC2652P 在线更新 加载项插件

## 安装教程

点击下面的按钮：

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https://github.com/jdbwlj/cc2652-flasher-bootloader)

1. 在 Home Assistant 前端导航至 **配置** -> **加载项, 加载项仓库** -> **仓库-添加仓库**.
2. 安装 CC2652P-Flasher-BootLoader.

## 如何使用

该加载项插件需要一个可通过网络串行端口（由IP地址+端口）或其他基于USB的无线适配器访问的CC2652P模块

# 对于网络连接协调器：
1. 在设备选项中，输入网络设备的串行端口（由IP地址+端口）.
2. 选择任何串行设备使得表格完整.
3. 选择为网络串行端口设备启用Bootloader的ESPHome开关。（注意可能不适用于所有的ESPHome 固件版本，如果没用效果,请在浏览器中打开协调器的Web前端,触发 BSL/Bootloader 模式）.
4. 输入 CC2652P 固件的 url 下面是例子:
   https://github.com/Koenkk/Z-Stack-firmware/raw/Z-Stack_3.x.0_coordinator_20230507/coordinator/Z-Stack_3.x.0/bin/CC1352P2_CC2652P_launchpad_coordinator_20230507.zip
5. 启动加载项插件.
6. 查看加载项插件日志提示.

# 对于 USB 连接协调器
1. 在网络设备行输入任意字符使得表格完整.
2. 从设备检测列表中选择正确的串行设备，切换开关以启用 USB刷机选项（在启动插件之前，协调器必须处于引导加载程序模式，插入USB时按住boot按钮，有自动下载功能的无需操作）
3. 输入 CC2652P 固件的 url 下面是例子:
   https://github.com/Koenkk/Z-Stack-firmware/raw/Z-Stack_3.x.0_coordinator_20230507/coordinator/Z-Stack_3.x.0/bin/CC1352P2_CC2652P_launchpad_coordinator_20230507.zip
4. 启动加载项插件.
5. 查看加载项插件日志提示.






## 配置
配置选项:

| 配置             | 详情                                                    |
|---------------------------|------------------------------------------------------------------|
| device                    | 连接到加载项的串口设备       |
| network_device            | 网络串口（IP_ADDRESS:PORT）)                            |
| flow_control              | 是否应启用硬件流控制（取决于固件） |
| firmware_url（必填）  | 自定义 URL 来刷新固件                 |


