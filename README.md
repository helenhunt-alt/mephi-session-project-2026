# mephi-session-project-2026

Сессионный проект по курсу «Операционные системы семейства Unix».

В проекте выполнены:
- настройка статической сети и hostname по заданию
- установка nginx, tcpdump и libcap-ng-utils
- создание и монтирование отдельной файловой системы с label `MEPHI_DATA`
- настройка nginx для работы с `/data/mephi-web`
- настройка DAC, SELinux и capabilities
- ограничение входа для `root` через PAM и SSH
- публикация тестовой страницы `Hello from Student: M2551109`

## Состав репозитория

- `project_history.txt` — история выполненных команд
- `network_check.txt` — результаты ping-проверок
- `nginx_recent_logs.txt` — логи nginx
- `fstab.txt` — конфигурация автомонтирования
- `selinux_status.txt` — статус SELinux
- `file_contexts.txt` — SELinux-контекст web-каталога
- `tcpdump_capabilities.txt` — capabilities для tcpdump
- `permissions.txt` — права и владелец `/data/mephi-web`
- `users_groups.txt` — данные о пользователе `mephi-admin` и группе `mephi-devs`
- `index.html` — публикуемая web-страница
- `curl_output.txt` — результат проверки страницы через curl
- `tcpdump.rpm` — скачанный RPM-пакет `tcpdump`
- `mephi-nginx-screenshot.png` — скриншот результата

## Примечание

Сетевой профиль был настроен в соответствии с параметрами из легенды задания. При этом фактическая сетевая среда виртуальной машины отличалась от учебного сценария, поэтому после применения этих параметров проверка внешней связности завершилась ошибкой. Полученный результат зафиксирован в файле `network_check.txt`.