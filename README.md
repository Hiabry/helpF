# Связываем локальный и удалённый репозитории

1. Копируем URL удаленного репозитория типа SSH.


2. Заходим в папку локального репозитория и вставляем следующее в терминал:

**git remote add** - привязать удаленный репозиторий к локальному


```

$ git remote add origin ***URL(SSH)**

```


P.s. origin - имя репозитория


3. Убеждаемся что репозитории связаны:

**git remote -v** - проверка связи


```
$ git remote -v


origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)


origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push)

```


4. Отправляем изменения:

**git push** - отправка изменений


впервые: 

```

$ git push -u origin main (master)


```

---
---


# Хеш - основной индитификатор коммита


**git log** - вывести историю коммитов


**Хеширование** (от англ. hash, «рубить», «крошить», «мешанина») — это способ преобразовать набор данных и получить их «отпечаток».


Информация о коммите — это набор данных: когда был сделан коммит, содержимое файлов в репозитории на момент коммита и ссылка на предыдущий, или родительский (англ. parent), коммит.


   - если хеш получить дважды для одного и того же набора входных данных, то результат будет гарантированно одинаковый;
    
    
   - если хоть что-то в исходных данных поменяется (хотя бы один символ), то хеш тоже изменится (причём сильно).


Все хеши и таблицу **хеш → информация о коммите** Git сохраняет в служебные файлы. Они находятся в скрытой папке .git в репозитории проекта.

