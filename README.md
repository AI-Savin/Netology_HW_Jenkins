# Домашнее задание к занятию "`8-02_Jenkins`" - `Savin Aleksey`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1
**Что нужно сделать:**  

1. Установите себе jenkins по инструкции из лекции или любым другим способом из официальной документации. Использовать Docker в этом задании нежелательно.
2. Установите на машину с jenkins golang.
3. Используя свой аккаунт на GitHub, сделайте себе форк репозитория. В этом же репозитории находится дополнительный материал для выполнения ДЗ.
4. Создайте в jenkins Freestyle Project, подключите получившийся репозиторий к нему и произведите запуск тестов и сборку проекта `go test .` и `docker build .`.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.  

### Решение 1
**настройки проекта**  

![настройки](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_1.png)
![настройки_1](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_2.png)
![настройки_3](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_3.png)

**лог проекта и результат**  

![лог](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_results_log.png)
![результат](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_results.png)

## подключение nexus

![настройки1](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_nexus.png)
![лог1](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_results_log_nexus.png)
![результат1](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part1_results_nexus.png)
![nexus_part1](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/nexus_part1.png)
---

### Задание 2
**Что нужно сделать:**  

1. Создайте новый проект pipeline.
2. Перепишите сборку из задания 1 на declarative в виде кода.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.


### Решение 2  

![настройки2](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part2_script1.png)
![результат2](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part2_results.png)
![лог2](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part2_log.png)
![nexus_part2](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part2_nexus.png)

---

### Задание 3

**Что нужно сделать:**  

1. Установите на машину Nexus.
2. Создайте raw-hosted репозиторий.
3. Измените pipeline так, чтобы вместо Docker-образа собирался бинарный go-файл. Команду можно скопировать из Dockerfile.
4. Загрузите файл в репозиторий с помощью jenkins.  

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

### Решение 3

![настройки3](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part3_script.png)
![результат3](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part3_results.png)
![лог3](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part3_log.png)
![лог3_1](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part3_log_1.png)
![nexus_part3](https://github.com/AI-Savin/Netology_HW_Jenkins/blob/main/img/part3_nexus.png)
