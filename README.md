# zabb_agent_script
#Данный скрипт предназначен для массовой установки zabbix-agenta на удаленный хосты с заранее проброшенными ssh ключами (для пользователя root)
#В коде используются команды для установки zabbix-agent2 версии 6.2 на Debian (лекго исправить под ваши нужды) заменить, при необходимости, команды apt на yum и ссылки на репозитории
#Перед запуском скрипта необходимо сделать следующее:
  #-пробросить ssh ключи
  #- указать в скрипте адрес Server и ServerActive, параметры ListenIp и Hostname подставятся сами
  #-сделать его исполняемым с помощью chmod
  #-создать файл ip_list.txt где будет внесен список адресов(каждый с новой строки)
#По завершению скрипт создаст в текущей директории файл где будет выведен результат по шаблону: "ip_address - hostname" при удачной установке агента на хост. В случае неудачной установки - "ip_address - error"
