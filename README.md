# Linorobot in Action
Build a linorobot from scratch

> This is a document project describe how to build a [linorobot](https://github.com/linorobot/linorobot) from scratch.

## Table of content
* [Introduction](https://github.com/jacks808/linorobot-in-action/tree/master#introduction)
* [Hardware](https://github.com/jacks808/linorobot-in-action/tree/master#hardware)
* [Software](https://github.com/jacks808/linorobot-in-action/tree/master#software)
* Debug&test
* FAQ
* [Useful links](https://github.com/jacks808/linorobot-in-action/tree/master#useful-links)

## Introduction

This github project is describe how to build a Linorobot from scratch. Includeing hardware, software, debug and test.

Linorobot is a suite of Open Source ROS compatible robots that aims to provide students, developers, 
and researchers a low-cost platform in creating new exciting applications on top of ROS. More about Linorobot can be found 
[here](https://github.com/linorobot/linorobot)

Author of this project: jack.wang a fullstack engneree focus on software, robots and autonomous vehicle.

## Hardware

In this part, I will tell how to build hardware part about linorobot. Including Hardware  and how to assemble them together. 

### Hardware list: 

Here is the hardware list that I used, all of this part can be found at [Taobao](www.taobao.com) or [Amazon](www.amazon.com)

* Laser sensors: 

  [RPLIDAR-A1 @Taobao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.56142e8dDnARXB&id=562109534912&_u=7cvg7t6a007)

  [RPLiDAR-X4 @Amazon](https://www.amazon.com/YDLIDAR-X4-Lidar-Rangefinder-Scanner/dp/B078Y964ZS/ref=sr_1_1?ie=UTF8&qid=1538989975&sr=8-1&keywords=rplidar+a1)

* IMU:

  [GY-85 @Taobao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.56142e8dDnARXB&id=17523968036&_u=7cvg7t6d225)

  [GY-85 @Amazon](https://www.amazon.com/KNACRO-Modules-Accelerometer-Gyroscope-HMC5883L/dp/B06WWF2F5R/ref=sr_1_1?ie=UTF8&qid=1538990050&sr=8-1&keywords=GY-85)

* Micro-controller:

  [Teensy 3.6 @Taobao](https://detail.tmall.com/item.htm?id=563186976177&spm=a1z09.2.0.0.56142e8dDnARXB&_u=7cvg7t6e88f)

  [Teensy 3.6 @Amazon](https://www.amazon.com/PJRC-Teensy-3-6-M4-Cortex/dp/B0778TTG1H/ref=sr_1_3?ie=UTF8&qid=1538990179&sr=8-3&keywords=Teensy+3.6)

* Ubuntu install ARM based dev board:

  [Raspberry Pi 3/B+ @Taobao](https://item.taobao.com/item.htm?spm=a230r.1.14.20.784f7790h9SvRU&id=550270480898&ns=1&abbucket=14#detail)

  [Raspberry Pi 3/B+ @Amazon](https://www.amazon.com/CanaKit-Raspberry-Starter-Premium-Black/dp/B07BCC8PK7/ref=sr_1_1_sspa?s=pc&ie=UTF8&qid=1538990222&sr=1-1-spons&keywords=raspberry+pi+3+b%2B&psc=1)

* Motor Drivers:

  [BTS7960 @Taobao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.56142e8dDnARXB&id=523962217259&_u=7cvg7t6d20d)

  [BTS7960 @Amazon](https://www.amazon.com/MonkeyJack-Double-BTS7960-H-bridge-Stepper/dp/B076CQBXHM/ref=sr_1_2?s=electronics&ie=UTF8&qid=1538990308&sr=1-2&keywords=BTS7960)

* Motor and Wheels:

  [Homemade chassis @Taobao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.56142e8dDnARXB&id=569175144674&_u=7cvg7t6dbb4)

  [Homemade chassis @Amazon](https://www.amazon.com/dp/B009646R3K/ref=sspa_dk_detail_5?psc=1&pd_rd_i=B009646R3K&pf_rd_m=ATVPDKIKX0DER&pf_rd_p=f52e26da-1287-4616-824b-efc564ff75a4&pf_rd_r=Y4R2S83Z4MM9ETJ2T364&pd_rd_wg=7fjFE&pf_rd_s=desktop-dp-sims&pf_rd_t=40701&pd_rd_w=jZtYv&pf_rd_i=desktop-dp-sims&pd_rd_r=42488e80-cadb-11e8-8f13-cb169b2924c1)

* connecting wires:

  [Dupont Line @Taobao](https://detail.tmall.com/item.htm?id=17525560371&spm=a1z09.2.0.0.56142e8dDnARXB&_u=7cvg7t6db4b&skuId=3110508296812)

  [Dupont Line @Amazon](https://www.amazon.com/Willwin-Dupont-80pcs-female-jumper/dp/B07566DGHZ/ref=sr_1_2_sspa?s=industrial&ie=UTF8&qid=1538990424&sr=1-2-spons&keywords=Dupont+Line&psc=1)

More supported hardware can be found [here](https://github.com/linorobot/linorobot/wiki/1.-Getting-Started#11-what-you-need)

### Assemble

// Todo

## Software

In this part, I will introduce how to install ROS on Respberry Pi. After that, linorobot Installation will be shown step by step. 

### Install OS for Raspberry Pi

![This image is comes from [here](https://ws3.sinaimg.cn/large/006tNbRwly1fw124ed5m7g30j40a1dj1.gif)](https://www.raspberrypi.org/app/uploads/2018/07/42558525-6dd32c62-84e9-11e8-99d2-0281ffe300c3.gif)

Usually, I use Ubuntu 16.04 for ROS, but after read this document: [Installing ROS Kinetic on the Raspberry Pi](http://wiki.ros.org/ROSberryPi/Installing%20ROS%20Kinetic%20on%20the%20Raspberry%20Pi). I directly install pre-installed Ros Ubuntu image offer by `Ubiquity`, which can be found [here](https://downloads.ubiquityrobotics.com/pi.html). 

Install steps:

1. Download `img` file for Respberry Pi: [Img Link](https://cdn.ubiquityrobotics.net/2018-06-27-ubiquity-xenial-lxde-raspberry-pi.img.xz)

2. Use [`Etcher`](https://etcher.io/) to write `image` to Respberry Pi SD card:

   1. Select Image

   2. Select Drive

   3. Flash

   4. Validating

      If everything is OK, you should see this:

      ![Jietu20181008-171027@2x](https://ws2.sinaimg.cn/large/006tNbRwly1fw11qz7er4j318g0l477n.jpg)

3. Insert in your TF card to Respberry Pi. Power on, And wait some time (in 3 mins)
4. Open Wifi config page to find a new Wifi point named: `ubiquityrobotXXXX` where XXXX is part of the MAC address. The wifi password is `robotseverywhere`.
5. After connected, use `ssh ubuntu@10.42.0.1` with a password `ubuntu` to login.

If everything is OK you should see this:

![image-20181008194204967](https://ws1.sinaimg.cn/large/006tNbRwly1fw11w6lxc2j30j60emmzz.jpg)

And ros is installed:

![image-20181008195309767](https://ws4.sinaimg.cn/large/006tNbRwly1fw127g9kj1j30hz09ywfz.jpg)

### Linorobot Installation



## Useful links

* Linorobot home page: https://linorobot.org
* Linorobot getting stated: https://github.com/linorobot/linorobot/wiki/1.-Getting-Started#11-what-you-need
* Ros home page: http://ros.org
* Respberry Help page: https://www.raspberrypi.org/help/
* Ubiquityrobotics home page: https://ubiquityrobotics.com/
