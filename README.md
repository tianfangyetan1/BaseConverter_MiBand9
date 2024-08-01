# NumberSystems

[![release](https://img.shields.io/github/v/release/tianfangyetan1/NumberSystems)](https://github.com/tianfangyetan1/NumberSystems/releases)
[![MIT license](https://img.shields.io/github/license/tianfangyetan1/NumberSystems)](https://github.com/tianfangyetan1/NumberSystems/blob/master/LICENSE)
[![Band BBS community](https://img.shields.io/badge/Band_BBS-community-718298)](https://www.bandbbs.cn/threads/12425/)

适用于小米手环9的进制转换程序

## 模拟器使用

1. 新建一个虚拟机，用任意项目（示例项目）运行一遍

2. 进入虚拟机目录

![打开模拟器目录](.readmeimg/Screenshot_2024-08-01_21-27-46.png)
![找到模拟器配置文件](.readmeimg/Screenshot_2024-08-01_21-28-53.png)

3. 修改分辨率

![修改模拟器分辨率](.readmeimg/Screenshot_2024-08-01_21-29-24.png)

4. 运行项目

![模拟器运行界面](.readmeimg/Screenshot_2024-08-01_21-28-03.png)

## 注意事项

- 设置[页面基准宽度](https://iot.mi.com/vela/quickapp/zh/content/framework/manifest.html#config)

  - 运行或打包前请将 `src\manifest.json` 中的 `config.designWidth` 修改为需要的数值（单位：像素）

  - 在模拟器中运行项目前请修改为 `466` （小米手表s3的宽度）

  - 打包项目前请修改为 `192` （小米手环9的宽度）

- JavaScript中整数的最大安全值是 $2 ^{53} - 1$ ，小米的框架似乎不支持 `Bigint` ，所以有最大值限制
