# Number Systems Converter for Mi Band 9

[![release](https://img.shields.io/github/v/release/tianfangyetan1/NumberSystems)](https://github.com/tianfangyetan1/NumberSystems/releases)
[![MIT license](https://img.shields.io/github/license/tianfangyetan1/NumberSystems)](https://github.com/tianfangyetan1/NumberSystems/blob/master/LICENSE)
[![Band BBS community](https://img.shields.io/badge/Band_BBS-community-718298)](https://www.bandbbs.cn/threads/12425/)

适用于小米手环9的进制转换程序

## 模拟器使用

1. 新建一个模拟器，用任意项目（示例项目）运行一遍

2. 打开模拟器目录，找到配置文件 `Vela_模拟器名称.avd\config.ini`

3. 修改分辨率：`config.ini` 第23-24行

    ```ini
    hw.lcd.height=490
    hw.lcd.width=192
    ```

4. 运行项目

    ![模拟器运行界面](docs/Screenshot_2024-08-01_21-28-03.png)

## 注意事项

- 设置[页面基准宽度](https://iot.mi.com/vela/quickapp/zh/content/framework/manifest.html#config)

  - 运行或打包前请将 `src\manifest.json` 中的 `config.designWidth` 修改为需要的数值（单位：像素）

  - 在模拟器中运行项目请修改为 `466` （小米手表s3的宽度）

  - 打包项目至真机运行请修改为 `192` （小米手环9的宽度）

- JavaScript中整数的最大安全值是 $2 ^{53} - 1$ ，小米的框架似乎不支持 `Bigint` ，所以有最大值限制
