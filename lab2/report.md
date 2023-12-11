University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Introduction in routing](https://github.com/itmo-ict-faculty/introduction-in-routing)  
Year: 2023/2024  
Group: K33202  
Author: Shalyapina Maria Vasilievna  
Lab: Lab2  
Date of create: 10.11.2023  
Date of finished: 22.11.2023  

# Лабораторная работа №2 "Эмуляция распределенной корпоративной сети связи, настройка статической маршрутизации между филиалами"

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
В данной лабораторной работе вы первый раз познакомитесь с компанией "RogaIKopita Games" LLC которая занимается разработкой мобильных игр с офисами в Москве, Франкфурте и Берлине. Для обеспечения работы своих офисов "RogaIKopita Games" вам как сетевому инженеру необходимо установить 3 роутера, назначить на них IP адресацию и поднять статическую маршрутизацию. В результате работы сотрудник из Москвы должен иметь возможность обмениваться данными с сотрудником из Франкфурта или Берлина и наоборот.

## <a name="part_2">Цель работы</a>
Ознакомиться с принципами планирования IP адресов, настройке статической маршрутизации и сетевыми функциями устройств.

## <a name="part_3">Результат</a>

### <a name="part_3.1"> [Файл](https://github.com/sgsoul/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/blob/main/lab1/lab1.yaml) для развертывания тестовой сети</a>

### <a name="part_3.2">Схема связи</a>
![graph](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/0386fb12-6889-4811-82fa-1a52e8c922d1)


### <a name="part_3.3">Конфигурации устройств</a>

#### Московский роутер
![R01 MSK](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/bbf3ad8f-a702-4ab9-9cbb-ef000aec0575)

#### Франкфуртский роутер
![R01 FRT](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/1d53515c-7d21-4ce9-8ad3-01590681e66a)

#### Берлинский роутер
![R01 BRL](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/202fe112-ed10-4549-96da-c9170e77a34a)

### <a name="part_3.4">Настройка компьютеров</a>

#### Компьютер в Москве
![PC MSK](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/dc22eb79-19a8-4058-b3c2-e00cc0077630)

#### Компьютер в Франкфурте
![PC FRT](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/3aee5ff7-c168-4edb-811c-b143830423b0)

#### Компьютер в Берлине
![PC BRL](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/04e81dd8-e9ae-43ab-950f-93f6318ca990)


### <a name="part_4">Проверка связности</a>
#### Москва -> Франкфурт, Москва -> Берлин
![PC MSK ping](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/9ea8ff3c-d09a-4563-ab82-c86e59bff262)

#### Франфурт -> Москва, Франкфурт -> Берлин
![PC FRT ping](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/d769d5f7-9b78-417f-b8db-1c9efe99e3ad)

#### Берлин -> Москва, Берлин -> Франкфурт
![PC BRL ping](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/83557bc3-5a22-494a-894d-0287e6aa9421)







