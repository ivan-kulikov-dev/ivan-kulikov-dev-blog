---
layout: post
title: Установка vivado 2019 + Ubuntu 20.04.3 LTS (Решение проблемы 'Generating installed device list')
subtitle: Each post also has a subtitle
gh-repo: /ivan-kulikov-dev/ivan-kulikov-dev-blog
gh-badge: [star, fork, follow]
tags: [vivado]
comments: true
---

Как установить vivado 2019 + Ubuntu 20.04.3 LTS

1) Установите ubundu Ubuntu 20.04.3 LTS и обновите

3) Зарегистрируйтесь на сайте https://www.xilinx.com/support/download.html

4) Откройте  https://www.xilinx.com/member/forms/download/xef-vivado.html?filename=Xilinx_Vivado_SDK_Web_2019.1_0524_1430_Lin64.bin по аккаунтом и скачайте

5) Установите следующие пакеты:
```
sudo add-apt-repository universe
sudo apt-get install libtinfo5 libncurses5 python3-pip ncurses5-compat-libs
sudo dpkg --add-architecture i386
sudo apt-get install dpkg-dev:i386 libgtk2.0-0:i386 libstdc++6:i386
```
Если этого не сделать, то у конце установки будет зависание установщика vivado на этапе 'Generating installed device list'
Данная проблема на vivado 2019.1, 2019.2, 2021.2
(Зависание описано в посте https://stackoverflow.com/questions/70767297/installing-vivado-ml-2021-2-in-centos-but-process-is-hang-in-generating-install/70780748)

5) Запустите Xilinx_Vivado_SDK_Web_2019.1_0524_1430_Lin64.bin и установите его. (Как подробно это делать статья на habr - https://habr.com/ru/post/559946/)
