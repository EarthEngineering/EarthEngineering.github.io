---
layout: post
title:  "Facetop Components and Tech Stack"
date:   2020-04-22 03:10:00 -0700
categories: facetop
---

## Introduction

According to [Security Today](https://securitytoday.com/articles/2020/01/13/the-iot-rundown-for-2020.aspx), during 2020 global spending on the Internet of Things (IoT) should reach $1.29 trillion. By 2021&mdash;the industrial IoT market size should reach $124 billion. By 2024&mdash;the global IoT healthcare market should reach $14 billion. By 2026&mdash;experts estimate that the IoT device market will reach $1.1 trillion.

In 2018—there were 7 billion IoT devices in 2018. In 2019—the number of active IoT devices reached 26.66 billion. Every second—127 new IoT devices are connected to the web.

During 2020 experts estimate the installation of 31 billion IoT devices. By 2021, 35 billion IoT devices will be installed worldwide. By 2025, more than 75 billion IoT devices will be connected to the Web.

It's clear that the Internet of Things is here to stay and that it's going to be massive. Facetop computing has been waiting for an IoT catalyst and due to COVID-19 we believe smart-masks will be the gateway that takes Facetop computing mainstream.

## Components

### Raspberry Pi

At the heart of Facetop is the Raspberry Pi which comes fully equipped with a Broadcom system on a chip (SoC) with an integrated ARM-compatible CPU and on-chip GPU. Processor speed is 1.5 GHz with 4 GB of RAM. HDMI, 3.5mm audio jack as well as WIFI and Bluetooth leave many ways to get data on/off the device.

![Rasp Pi](/assets/rasp-pi.jpg)

[More Info](https://en.wikipedia.org/wiki/Raspberry_Pi)

#### Raspberry Pi Zero

The Raspberry Pi is relatively bulky to be worn on a mask. After we finish prototyping we'll either move to a smaller Raspberry Pi model, such as the Zero, or we'll go with our own custom boards.

Front

![Rasp Pi Zero front](/assets/rasp-pi-zero-front.jpg)

Back

![Rasp Pi Zero back](/assets/rasp-pi-zero-back.jpg)

[More Info](https://www.raspberrypi.org/blog/raspberry-pi-zero-w-joins-family/)

#### Raspberry Pi Camera

Facetop is a "voice first" UX. You can stream data to a phone or tablet over Bluetooth but there is no screen which sits over your eye(s) like with smart glasses. You can however snap photos and video as well as stream video using the Raspberry Pi Camera.

![Rasp Pi Camera](/assets/rasp-pi-camera.jpg)

[More Info](https://www.raspberrypi.org/products/camera-module-v2/)

## Tech Stack

![Tech Stack](/assets/facetop-tech-stack.png)

Facetop has a very rich software ecosystem. my.facetop.earth is the dashboard where users sign in to view usage stats as well as interact with their Facetop.

### my.facetop.earth

As with [all of our software](https://github.com/EarthEngineering), [my.facetop.earth](http://my.facetop.earth) is 100% open source under the [MIT license](https://opensource.org/licenses/MIT) and can be found [on Github](https://github.com/EarthEngineering/my.facetop.earth).

### rest.facetop.earth

[rest.facetop.earth](http://rest.facetop.earth) is a suite of REST webservices for Facetop. It accepts requests in the form of HTTP and returns JSON. It also has an [MQTT](https://www.npmjs.com/package/mqtt) message broker for publishing messages to channels which have subscribers. This can also be found [on Github](https://github.com/EarthEngineering/rest.facetop.earth)

### Facetop OS

Facetop OS is written with [nerves](https://www.nerves-project.org) which is an IoT framework written in Elixir. You can find it [on Github](https://github.com/EarthEngineering/facetop-os).

## MQTT Demo

The rest.facetop.earth code base has a basic IoT demo. If you open two tabs and in one run `node app.js` and in the other run `node client.js` you'll see an MQTT broker, subscriber and message being published.
