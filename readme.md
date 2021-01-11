# Opencore for BigSur


主板：JW H81 itx

CPU：i7 4780HQ

显卡：Intel Iris Pro Graphics 5200（ig-platflom-id:0x0d260000)

声卡：alcid=5

网卡：BCM94322


完美驱动。

# BCM94322驱动方法（通用）：

https://github.com/khronokernel/IO80211-Patches
选择mojave版的，放到oc的kext目录；
用hackintool找到网卡的接口（PCIE菜单），然后按照网卡对应的内容修改红字部分
```
      <key>PciRoot(0x0)/Pci(0x1C,0x4)/Pci(0x0,0x0)</key>
      <dict>
              <key>compatible</key>
              <string>pci14e4,432b</string>
      </dict>
```
