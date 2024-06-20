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

