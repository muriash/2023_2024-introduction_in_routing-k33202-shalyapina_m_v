University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Introduction in routing](https://github.com/itmo-ict-faculty/introduction-in-routing)  
Year: 2023/2024  
Group: K33202  
Author: Shalyapina Maria Vasilievna  
Lab: Lab4  
Date of create: 15.12.2023  
Date of finished: 20.12.2023  

# Лабораторная работа №4 "Эмуляция распределенной корпоративной сети связи, настройка iBGP, организация L3VPN, VPLS"

## Оглавление
 - [Описание](#part_1)
 - [Цель](#part_2)
 - [Результат](#part_3)
     - [Файл для развертывания тестовой сети](#part_3.1)
     - [Схема связи](#part_3.2)
     - [Часть 1](#part_3.3)
         - [Настройка адресов](#part_3.3.1)
         - [Настройка BGP](#part_3.3.2)
         - [Настройка MLPS](#part_3.3.3)
         - [Настройка VRF](#part_3.3.4)
         - [Проверка связности](#part_3.3.5)
      - [Часть 2](#part_3.4)
         - [Настройка VPLS](#part_3.4.1)
         - [Проверка связности](#part_3.4.2)

## <a name="part_1">Описание</a>
Компания "RogaIKopita Games" выпустила игру "Allmoney Impact", нагрузка на арендные сервера возрасли и вам поставлена задача стать LIR и организовать свою AS чтобы перенести все сервера игры на свою инфраструктуру. После организации вашей AS коллеги из отдела DEVOPS попросили вас сделать L3VPN между 3 офисами для служебных нужд. (Рисунок 1) Данный L3VPN проработал пару недель и коллеги из отдела DEVOPS попросили вас сделать VPLS для служебных нужд.

## <a name="part_2">Цель работы</a>
Изучить протоколы BGP, MPLS и правила организации L3VPN и VPLS.

## <a name="part_3">Результат</a>

### <a name="part_3.1"> [Файл](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/blob/main/lab3/lab3.yaml) для развертывания тестовой сети</a>

### <a name="part_3.2">Схема связи</a>
![схема](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/39df8ed5-2d71-4258-b2a1-7fead124244b)


### <a name="part_3.3">Часть 1</a>

#### <a name="part_3.3.1">Настройка адресов</a>
![1 NYC addresses](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/c4108878-0b06-472d-8804-9205a8de0b17)

![2 LND addresses](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/3cba78a2-e093-42bf-beeb-5e3683afca71)

![3 HKI addresses](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/dd27281c-e73b-4607-9902-26d192f2f61c)

![4 SPB adresses](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/d1138266-af86-4ce2-8583-54ed86253093)

![5 LBN addresses](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/ba59f0a4-42a8-4155-9161-26a47fdc736a)

![6 SVL addresses](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/571570a2-2f6b-4c0d-817c-050fca31fd89)

#### <a name="part_3.3.2">Настройка BGP</a>

При создании network backbone, автоматически создаются интерфейсы OSPF. Пример для роутера в Нью-Йорке:
![7 NYC OSPF](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/71794643-563b-46c5-9681-9f740c56c171)

Результат настройки BGP на узлах:
![8 NYC BGP](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/cff74e7f-9aec-4844-b546-26247fbabdfe)

![9 LND BGP](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/9ae9d334-50de-4f04-baee-2193dde5427b)

![10 SPB BGP](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/8ab16d1e-ab1a-4f49-920f-e2232c4ae3be)

![11 HKI BGP](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/4d67a152-44e8-4d58-b079-1d4d21030f9e)

![12 SVL BGP](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/1ec12a11-5030-435a-9b68-e933e39ea3e5)

![13 LBN BGP](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/bd2e301a-e71e-4440-b7a0-cb2d3cc0d429)


#### <a name="part_3.3.3">Настройка MLPS</a>

Пример настройки для роутера R01.HKI:
![14 MLPS enable hki](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/dfb6ea1f-e9c2-4014-beb6-2f5545cc312c)
![15 MLPS interfaces hki](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/767bb705-9737-4d39-8676-8d87f1e07e64)


#### <a name="part_3.3.4">Настройка VRF</a>
![16 VRF nyc](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/28f364fc-e3fc-4624-bcf2-90436c731f8e)
![17 VRF NYC routes](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/78da3d17-13b1-4a17-a090-a1b8400d5afb)

#### <a name="part_3.3.5">Проверка связности</a>
PC2 --> PC1, PC2 --> PC3
![18 ping from NYC](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/68ddd672-942b-490f-ab79-ceb8e1410c1d)


### <a name="part_3.4">Часть 2</a>

#### <a name="part_3.4.1">Настройка VPLS</a>
Для настройки VPLS, на узлах были убраны прежние найстроки VRF.

Пример настройки VPLS для роутера R01.NYC:
![19 VLPS NYC](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/4e96b1ca-43c2-49ac-9f4f-f55fce6cea18)
![20 VPLS bridge NYC](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/925feac0-ec19-4b33-aef2-5b31a91a1d7b)

#### <a name="part_3.4.2">Проверка связности </a>
PC2 --> PC1, PC2 --> PC3
![21 ping from NYC 2](https://github.com/muriash/2023_2024-introduction_in_routing-k33202-shalyapina_m_v/assets/90574857/6bbb6ce6-40f1-4ac9-a335-73e1937a0047)








