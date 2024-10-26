# Запуск Kafka + ZooKeeper
В данном уроке рассматривается запуск Kafka с ZooKeeper на локальном компьютере на Windows. Что будем использовать:

- **WSL** - WSL, или «Подсистема Windows для Linux», представляет собой встроенную функцию Windows 10, позволяющую запускать в Windows-среде консольные и графические приложения Linux.
- **Ubuntu Linux** - это операционная система для персональных компьютеров, которую можно использовать вместо Windows или Mac OS.
- **Java Development Kit** - бесплатно распространяемый корпорацией Oracle Corporation (ранее Sun Microsystems) комплект разработчика приложений на языке Java, включающий в себя компилятор Java (javac), стандартные библиотеки классов Java, примеры, документацию, различные утилиты и исполнительную систему Java (JRE).

### Данный урок включает себя три этапа:
1. Запуск Kafka + ZooKeeper
2. Тестирование Kafka+ZooKeeper
____
### 1. Запуск Kafka + ZooKeeper
Создаваемый кластер будет состять из одного брокера(Kafka) и одного сервиса ZooKeeper. Схема взимодействия:
![alt text](image.png)

1. Заходим под root пользователем в Ubuntu

2. Установим Java Development Kit:
```bash
sudo apt update
sudo apt install openjdk-11-jdk 
```
3. Проверим версию Java:
```bash
java -version
```
Результат:
```bash
openjdk version "21.0.4" 2024-07-16                                    OpenJDK Runtime Environment (build 21.0.4+7-Ubuntu-1ubuntu224.04)                                           OpenJDK 64-Bit Server VM (build 21.0.4+7-Ubuntu-1ubuntu224.04, mixed mode, sharing)   
```

4. Переходим [на официальный сайт Apache Kafka](https://kafka.apache.org/downloads) и скачиваем последнюю версию Kafka.

5. Меняем название папки с скаченным архивом на `kafka` и опредеяем по пути `opt/kafka`

6.
