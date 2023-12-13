# CC2652P 在线更新 加载项插件

## 安装教程

点击下面的按钮：

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https://github.com/jdbwlj/cc2652-flasher-bootloader)

或者，在 Home Assistant 中，导航至配置>附加组件、备份和主管>附加组件存储> ... >存储库并添加https://github.com/jdbwlj/cc2652-flasher-bootloader到列表中.


Video Walk Through: https://www.youtube.com/watch?v=W28hdRx0mV4

1. 在 Home Assistant 前端导航至 **配置** -> **加载项, 加载项仓库** -> **仓库-添加仓库**.
2. 安装 TubesZB TI CC2652 FW Flasher.

## 如何使用

该加载项插件需要一个可通过网络串行端口（由IP地址+端口）或其他基于USB的无线适配器访问的CC2652P模块

# 对于网络连接协调器：
1. 在附加配置中，在网络设备条目表单中输入 IP_ADDRESS:端口
2. 选择任何串行设备使得表格完整
3. 选择为网络协调器启用引导加载程序的 ESPHome 触发器。（注意可能不适用于所有 TubesZB ESPHome 固件版本，如果未在浏览器中打开协调器的 Web 前端并在那里触发 BSL/Bootloader 模式）
4. 输入 Z-Stack 固件的 url 下面是例子:
   https://github.com/Koenkk/Z-Stack-firmware/raw/7398d834eb3a790876c280293c4181da96cc7114/coordinator/Z-Stack_3.x.0/bin/CC1352P2_CC2652P_launchpad_coordinator_20221226.zip
5. 启动加载项插件.
6. 查看加载项插件日志提示.

# 对于 USB 连接协调器
1. 在网络设备行输入任意字符使得表格完整.
2. 从设备检测列表中选择正确的串行设备，切换开关以启用 USB刷机选项（在启动插件之前，协调器必须处于引导加载程序模式，插入USB时按住boot按钮，有自动下载功能的无需操作）
3. 输入 Z-Stack 固件的 url 下面是例子:
   https://github.com/Koenkk/Z-Stack-firmware/raw/7398d834eb3a790876c280293c4181da96cc7114/coordinator/Z-Stack_3.x.0/bin/CC1352P2_CC2652P_launchpad_coordinator_20221226.zip
4. 启动加载项插件.
5. 查看加载项插件日志提示.






## Configuration

Add-on configuration:

| Configuration             | Description                                                      |
|---------------------------|------------------------------------------------------------------|
| device                    | 连接到加载项的串口设备       |
| network_device            | 网络串口（IP_ADDRESS:PORT）)                            |
| flow_control              | 是否应启用硬件流控制（取决于固件） |
| firmware_url（必填）  | 自定义 URL 来刷新固件                 |


