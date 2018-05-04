需要两个U盘
一个制作为安装系统的引导盘
一个为安装系统的目标盘

1. 根据Ubuntu官方制作USB启动盘
2. 按照提示安装系统
  1. 安装方式选择something else
  2. 系统分区分为swap area，efi，/home, / 这四个分区
    1. swap area （设置为逻辑分区Logical， Beginning of this space, 用于内存占用高时，临时使用的虚拟内存空间）
    2. efi (




2. 启动电脑后 按F12进入BIOS选项模式
    1. BIOS secure boot 设置为disable
    2. 将Raid模式修改为AHCI
    3. Boot sequence 修改为Ubuntu上 Windows下
