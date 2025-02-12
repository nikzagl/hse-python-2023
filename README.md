# hse-python-2023

## Инструкция

1. Сделать форк данного репозитория
2. Создать бранч (ветку) в гите назвав ее в формате `имя_группы/фамилия`

Например, вы учите в группе 21ПМИ-1 и ваша фамилия петров, то ветка будет называться:

`21pmi-1/petrov`

Вы учитесь в группе 21ПМИ-2 и ваша фамилия Сидоров:

`21pmi-2/sidorov`

3. В папке tasks вы найдете пронумерованную папку с номером практики.
   Внутри нее файл с заданиями, например practice2 - в нем описано, 
   какую задачу вам нужно решить и какой код и где писать.
   
4. Весь код, который вы пишите, будет тестироваться с помощью так называемых unit-тестов. 
   Чтобы практика была зачтена все тесты должны проходить.
   Как запускать тесты смотрите ниже.
   
5. Когда все тесты проходят - нужно отправить код на проверку. Для этого коммитите код в свой ветку. 
   И отправляете его на проверку через PR в ветку main основного репозитория. https://github.com/ryabchi/hse-python-2023
   
6. ПР называете группа фамилия, например: 20ПМИ-1 Сидоров


# Как запускать тесты?

*!!! Папку tests в своих PR менять нельзя!*

1. Нужно установить пакет pytest, который широко используется в python для написания тестов.

Для этого находясь в директории проекта (проверьте что ваш virtualenv активирован) выполните команду установки:

`pip install pytest`

2. Дождитесь завершения установки

3. После чего выполните команду `pytest` в консоли. После чего тесты запустятся.

Или использовать команду с дополнительными параметрами - для более информативного вывода: 
`pytest --verbosity=2 --showlocals`

4. Доработайте код в папке tasks, чтобы все тесты проходили.


# Как работать с форками на github?

Можно почитать [тут](https://docs.github.com/en/github/collaborating-with-pull-requests/working-with-forks/configuring-a-remote-for-a-fork).

# Как подтянуть изменения (статья выше в кратком изложении)

Для начала убедитесь прописан ли у вас upstream основного репозитория.

Для этого введите:

`git remote -v`

Если в выводе отсутствуют записи:
```
> upstream  https://github.com/ryabchi/hse-python-2023.git (fetch)
> upstream  https://github.com/ryabchi/hse-python-2023.git (push
```

Выполните команду ниже:

`git remote add upstream  https://github.com/ryabchi/hse-python-2023.git`

Если присутствуют, то просто продолжайте работать по инструкции.

Выполните команду:

`git fetch upstream`

Далее перейдите в свой main (`git checkout main`) и выполните команду:

`git rebase upstream/main`

После перейдите в свою ветку, например:

`git checkout 21pmi-1/petrov`

И находясь в ней выполните команду:

`git rebase main`

После чего запульте обновления в свою ветку на гихабе, выполнив команду:

`git push --force`

Обратите внимание, что первый push после ребейса обязательно должен выполняться в force режиме, 
чтобы принудительно перезаписать содержимое удаленного репозитория. Обычный пуш у вас сделать не получится.

После шагов выше - пишите свой код, чтобы он проходил тесты. Делайте коммит с описанием 'Practice 3' и пуште изменения.
# cpp_triangles_intersection
