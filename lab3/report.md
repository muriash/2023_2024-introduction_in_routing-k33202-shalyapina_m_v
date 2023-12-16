University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Introduction in routing](https://github.com/itmo-ict-faculty/introduction-in-routing)  
Year: 2023/2024  
Group: K33202  
Author: Shalyapina Maria Vasilievna  
Lab: Lab3  
Date of create: 25.11.2023  
Date of finished: 10.12.2023  

# Лабораторная работа №3 "Эмуляция распределенной корпоративной сети связи, настройка OSPF и MPLS, организация первого EoMPLS"

## Оглавление
 - [Описание](#part_1)
 - [Цель](#part_2)
 - [Результат](#part_3)
     - [Файл для развертывания тестовой сети](#part_3.1)
     - [Схема связи](#part_3.2)
     - [Конфигурации роутеров](#part_3.3)
     - [Настройка компьютеров](#part_3.4)
     - [Проверка связности](#part_4)

## <a name="part_1">Описание</a>
Наша компания "RogaIKopita Games" с прошлой лабораторной работы выросла до серьезного игрового концерна, ещё немного и они выпустят свой ответ Genshin Impact - Allmoney Impact. И вот для этой задачи они купили небольшую, но очень старую студию "Old Games" из Нью Йорка, при поглощении выяснилось что у этой студии много наработок в области компьютерной графики и совет директоров "RogaIKopita Games" решил взять эти наработки на вооружение. К сожалению исходники лежат на сервере "SGI Prism", в Нью-Йоркском офисе никто им пользоваться не умеет, а из-за короновируса сотрудники офиса из Санкт-Петерубурга не могут добраться в Нью-Йорк, чтобы забрать данные из "SGI Prism". Ваша задача подключить Нью-Йоркский офис к общей IP/MPLS сети и организовать EoMPLS между "SGI Prism" и компьютером инженеров в Санкт-Петербурге.

## <a name="part_2">Цель работы</a>
Изучить протоколы OSPF и MPLS, механизмы организации EoMPLS.

## <a name="part_3">Результат</a>

### <a name="part_3.1"> [Файл](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/blob/main/lab3/lab3.yaml) для развертывания тестовой сети</a>

### <a name="part_3.2">Схема связи</a>
![схема связи](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/3e538ef9-4f62-4bcb-b764-787134da7217)

### <a name="part_3.3">Конфигурации устройств</a>

#### R01_SPB
![1 R01_SPB ](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/9f510e63-2ed8-4f2d-9596-20b8c3d5dbb5)

#### R01_MSK
![2 R01_MSK](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/072a88d8-4327-4c44-b806-dcb830a3f782)

#### R01_HKI
![3 R01_HKI](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/d43a76a5-bd2e-44ab-950e-ae3f355164c8)

#### R01_LBN
![4 R01_LBN](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/9f4950a9-88b0-4597-8fa1-808e71553960)

#### R01_LND
![5 R01_LND](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/5bc3b348-6e95-45d5-9444-3fea183b8575)

#### R01_NYC
![6 R01_NYC](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/cb0689e7-634d-4295-a93f-cf7dc7cad321)

### <a name="part_3.4">Настройка компьютеров</a>

#### PC1
![0 PC1](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/03a2559b-bb3b-484a-87ef-51e9368a65d0)

#### SGI_Prism
![7 SGI_Prism](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/2d91aae6-ec0d-4456-8d51-71c1a67c5c7f)


### <a name="part_4">Проверка связности</a>
#### Пинг SGI_Prism c PC1
![8 ping SGI_Prism from PC1](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/b76675bf-058b-45dc-8c96-68fe9bc4fbed)

#### Отслеживание маршрута от роутера в Нью-Йорке к роутеру в Санкт-Петербурге
![9 tool trace](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/6906e87d-246c-4091-b733-ecfd96dc7446)
