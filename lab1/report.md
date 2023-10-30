University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Introduction in routing](https://github.com/itmo-ict-faculty/introduction-in-routing)  
Year: 2023/2024  
Group: K33202  
Author: Shalyapina Maria Vasilievna  
Lab: Lab1  
Date of create: 10.10.2023  
Date of finished: 22.10.2023  

# Лабораторная работа №1 "Установка ContainerLab и развертывание тестовой сети связи"

## Оглавление
 - [Описание](#part_1)
 - [Цель](#part_2)
 - [Результат](#part_3)
     - [Файл для развертывания тестовой сети](#part_3.1)
     - [Схема связи](#part_3.2)
     - [Конфигурации устройств](#part_3.3)
     - [Проверка связности](#part_4)

## <a name="part_1">Описание</a>
В данной лабораторной работе вы познакомитесь с инструментом ContainerLab, развернете тестовую сеть связи, настроите оборудование на базе Linux и RouterOS.

## <a name="part_2">Цель работы</a>
Ознакомиться с инструментом ContainerLab и методами работы с ним, изучить работу VLAN, IP адресации и т.д.

## <a name="part_3">Результат</a>

### <a name="part_3.1"> [Файл](https://github.com/sgsoul/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/blob/main/lab1/lab1.yaml) для развертывания тестовой сети</a>

### <a name="part_3.2">Схема связи</a>

![Снимок экрана 2023-10-18 203706](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/5c856811-8f8e-4f57-a3ba-95826f7e4aab)


### <a name="part_3.3">Конфигурации устройств</a>

#### R01
![R01](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/677977af-4b6f-4bb9-a067-65824988a30e)

#### SW01.L3.01
![SW01](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/7a9de71c-b7a3-41eb-839d-322d3459eefa)


#### SW02.L3.01
![SW021](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/9414a67e-104b-4da2-bf2a-7213330cee4f)


#### SW02.L3.02
![SW022](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/1f9fbdda-1b79-4736-8d0e-411d1021d7d8)


### <a name="part_4">Проверка связности</a>
![check](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/d2716a9f-ab02-43a3-8db7-40cf9ab42319)





