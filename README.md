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



---
---


# Исследуем лог (от англ. log — «журнал [записей]») - описание коммита


**git log** - вывести список коммитов


### Описание состоит из:

- строка из цифр и латинских букв после слова commit — это хеш коммита;


- Author — имя автора и его электронная почта;


- Date — дата и время создания коммита;


- в конце находится сообщение коммита.


**git log --oneline** - получить сокращенный лог

В терминале появятся только первые несколько символов хеша каждого коммита и их комментарии.
Команда git log --oneline автоматически подбирает такую длину сокращённых хешей, чтобы они были уникальными в пределах репозитория и Git всегда мог понять, о каком коммите идёт речь.


---
---


# HEAD

Файл **HEAD** (англ. «голова», «головной») — один из служебных файлов папки **.git**. Он указывает на коммит, который сделан последним (то есть на самый новый).


Внутри **HEAD** — ссылка на служебный файл: **refs/heads/master** (или refs/heads/main в зависимости от названия ветки). Если заглянуть в этот файл, можно увидеть хеш последнего коммита.


При работе с Git указатель **HEAD** используется довольно часто. Мы уже упоминали, что многие команды Git принимают в качестве параметра хеш коммита. Если нужно передать последний коммит, то вместо его хеша можно просто написать слово **HEAD** — Git поймёт, что вы имели в виду последний коммит.


---
---

/
