======================
Установка на Debian 10
======================

В процессе будут установлены следующие основные пакеты вместе с их зависимостями:

* PerconaDB 8.0
* Freeradius 3
* PHP 7.3
* PHP-FPM
* Nginx (+ модуль защиты Nemesida WAF Free)
* DHCP
* Unbound
* Mikbill

А так же вспомогательные пакеты вместе с их зависимостями:

.. code-block::

  wget net-tools sudo mrtg php-pear sysstat


**Требования к серверу/ОС**
---------------------------

* Это должна быть `чистая ОС <https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-10.3.0-amd64-netinst.iso>`_ **без предустановленных основных пакетов**.
* Сервер должен соответствовать `минимальным требованиям <https://www.mikbill.ru/produkt/mikbill-sys-requirements.html>`_ биллинга.
* При установке OS **НИКОГДА** не ставте галочку возле "Системные часы используют UTC"


**Установка**
-----------------

Для установки понадобится Ansible версии 2.7/2.8/2.9
Установим Ansible:

.. code-block:: sh

  apt-get install wget gnupg2 ansible python curl

Скачаем и распакуем установщик mikbill:

.. code-block:: sh

  wget http://setup.2x.mikbill.pro/setup.tar.gz
  tar zxf setup.tar.gz

Перейдем в директорию установки и запустим процесс установки:

.. code-block:: sh

  cd setup
  ansible-playbook mikbill.yml

Все сгенерированные пароли и информация для подключения к админке и лк будет показана в конце установки а также будет сохранена в файл /var/mikbill/mikbill.info


После установки будет доступна страница управления билингом по введеному IP-адресу или имени хоста.
Для проверки работы служб выполните:

Ядро биллинга:

.. code-block:: sh

  netstat -nlp | grep 2007
  tcp        0      0 127.0.0.1:2007          0.0.0.0:*               LISTEN      4848/php

Базы данных:

.. code-block:: sh

  netstat -nlp | grep 3306
  tcp        0      0 127.0.0.1:3306          0.0.0.0:*               LISTEN      4586/mysqld   

Радиус сервера:

.. code-block:: sh

  netstat -nlp | grep 181[2-3]
  udp        0      0 0.0.0.0:1812            0.0.0.0:*                           4869/radiusd        
  udp        0      0 0.0.0.0:1813            0.0.0.0:*                           4869/radiusd