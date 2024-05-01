# Домашнее задание к занятию «Системы контроля версий» Шарапат Виктор

## Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе

В рамках курса вы будете писать скрипты и создавать конфигурации для различных систем, которые необходимо сохранять для будущего использования. 
Сначала надо создать и настроить локальный репозиторий, после чего добавить удалённый репозиторий на GitHub.

### Создание репозитория и первого коммита

1. Зарегистрируйте аккаунт на [https://github.com/](https://github.com/). Если предпочитаете другое хранилище для репозитория, можно использовать его.
2. Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием `devops-netology`.
   Обязательно поставьте галочку `Initialize this repository with a README`. 
   
![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/89b7c2bf-9eb2-405f-8f01-8a93769ab39b)
    
3. Создайте [авторизационный токен](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) для клонирования репозитория.
4. Склонируйте репозиторий, используя протокол HTTPS (`git clone ...`).
 
![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/d786d6ad-ea93-4672-b551-8e29b5fc6fb0)
    
5. Перейдите в каталог с клоном репозитория (`cd devops-netology`).
6. Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (`git config --global user.name` и `git config --global user.email johndoe@example.com`). 
7. Выполните команду `git status` и запомните результат.
8. Отредактируйте файл `README.md` любым удобным способом, тем самым переведя файл в состояние `Modified`.
9. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага. 
10. Теперь посмотрите изменения в файле `README.md`, выполнив команды `git diff` и `git diff --staged`.
11. Переведите файл в состояние `staged` (или, как говорят, просто добавьте файл в коммит) командой `git add README.md`.
12. И ещё раз выполните команды `git diff` и `git diff --staged`. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают. 
13. Теперь можно сделать коммит `git commit -m 'First commit'`.
14. И ещё раз посмотреть выводы команд `git status`, `git diff` и `git diff --staged`.

### Создание файлов `.gitignore` и второго коммита

1. Создайте файл `.gitignore` (обратите внимание на точку в начале файла), проверьте его статус сразу после создания. 
1. Добавьте файл `.gitignore` в следующий коммит (`git add...`).
1. На одном из следующих блоков вы будете изучать `Terraform`, давайте сразу создадим соотвествующий каталог `terraform` и внутри этого каталога — файл `.gitignore` по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore.  
1. В файле `README.md` опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному `.gitignore`.
1. Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть `Added gitignore`.

### Эксперимент с удалением и перемещением файлов (третий и четвёртый коммит)

1. Создайте файлы `will_be_deleted.txt` (с текстом `will_be_deleted`) и `will_be_moved.txt` (с текстом `will_be_moved`) и закоммите их с комментарием `Prepare to delete and move`.
1. В случае необходимости обратитесь к [официальной документации](https://git-scm.com/book/ru/v2/Основы-Git-Запись-изменений-в-репозиторий) — здесь подробно описано, как выполнить следующие шаги. 
1. Удалите файл `will_be_deleted.txt` с диска и из репозитория. 
1. Переименуйте (переместите) файл `will_be_moved.txt` на диске и в репозитории, чтобы он стал называться `has_been_moved.txt`.
1. Закоммитьте результат работы с комментарием `Moved and deleted`.

### Проверка изменения

1. В результате предыдущих шагов в репозитории должно быть как минимум пять коммитов (если вы сделали ещё промежуточные — нет проблем):
    * `Initial Commit` — созданный GitHub при инициализации репозитория. 
    * `First commit` — созданный после изменения файла `README.md`.
    * `Added gitignore` — после добавления `.gitignore`.
    * `Prepare to delete and move` — после добавления двух временных файлов.
    * `Moved and deleted` — после удаления и перемещения временных файлов. 
2. Проверьте это, используя комманду `git log`. Подробно о формате вывода этой команды мы поговорим на следующем занятии, но посмотреть, что она отображает, можно уже сейчас.

### Отправка изменений в репозиторий

Выполните команду `git push`, если Git запросит логин и пароль — введите ваши логин и пароль от GitHub. 

В качестве результата отправьте ссылку на репозиторий. 

----

### Правила приёма домашнего задания

В личном кабинете отправлена ссылка на ваш репозиторий.


### Критерии оценки

Зачёт:

* выполнены все задания;
* ответы даны в развёрнутой форме;
* приложены соответствующие скриншоты и файлы проекта;
* в выполненных заданиях нет противоречий и нарушения логики.

На доработку:

* задание выполнено частично или не выполнено вообще;
* в логике выполнения заданий есть противоречия и существенные недостатки.

---

### Решение:

2) Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием devops-netology. Обязательно поставьте галочку Initialize this repository with a README.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/324afe82-00b8-4af0-b21f-30cde8b64b98)

3) Создайте авторизационный токен для клонирования репозитория.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/450ce67d-0d9d-4b65-9c89-5a9ce3afd7ac)

4) Склонируйте репозиторий, используя протокол HTTPS (git clone ...).

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/fbbf17aa-89b5-45e3-a47a-89326dd8e4e1)

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/8627f3eb-8eb6-4e44-958f-c3212c6333db)

6) Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (git config --global user.name и git config --global user.email johndoe@example.com).

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/ce715bde-edb2-475f-a42c-37ab8f03f817)

7) Выполните команду git status и запомните результат.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/87e8eb1c-abd4-4520-aac3-5ab767343433)

8) Отредактируйте файл README.md любым удобным способом, тем самым переведя файл в состояние Modified.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/976934ac-b369-4f2e-bb0d-39a3d8f486b1)

9) Ещё раз выполните git status и продолжайте проверять вывод этой команды после каждого следующего шага.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/548cafa6-37f9-422c-9e9f-0370384b6e76)

10) Теперь посмотрите изменения в файле README.md, выполнив команды git diff и git diff --staged.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/5e99206e-8ab0-4c11-87b9-a8ab7dae7c1c)


11) Переведите файл в состояние staged (или, как говорят, просто добавьте файл в коммит) командой git add README.md.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/de73a70b-ec33-4b64-84b0-152ad7ee77a0)


12) И ещё раз выполните команды git diff и git diff --staged. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/fa8851e7-adf0-42d3-977f-0ca5b1e443ae)


13) Теперь можно сделать коммит git commit -m 'First commit'.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/28ed8d00-9bb3-4f2e-9421-c823cba54a7b)


15) И ещё раз посмотреть выводы команд git status, git diff и git diff --staged.

![image](https://github.com/sharvik22/02-git-01-vcs/assets/136818757/447b3810-ffb5-4a07-aeea-8fa679a15445)















  
