# SSH

> хз че это об этом узнаю позже и напишу сюда

А тут у нас как создать на windows ключ ssh и подключиться с его помощью к GitHub

## Есть ли уже ключ?

Если есть сгенерированный ключ то можно просто использовать его для этого мы опять заходим в git Bash вводим команду: 

```
ls -al ~/.ssh
```
И ищем все файлы с форматом .pub
По стандарту ключ создаются в файлах с именами: 

- *id_rsa.pub*

- *id_ecdsa.pub*

- *id_ed25519.pub*

    


## Создание ключа:

1. Открываем git Bash

2. Вводим следующую команду 

    ```
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```

    Он попросит ввести кодовую фразу и повторить ее:

    ```
    > Enter a file in which to save the key (/c/Users/you/.ssh/id_ed25519):[Press enter]
    > Enter same passphrase again: [Type passphrase again]
    ```



## Добавление SSH в Github:

Чтобы скопировать ключ нужно ввести:

```
clip < ~/.ssh/id_ed25519.pub
```

Потом в гитхабе найти в настройках настройку  **SSH and GPG keys**.
и создать новый SSH ключ.

---

## Linux

### OpenSSH подключение и  статус программы

У меня постоянно отключался openssh и подключиться я не мог и вот решение этой проблемы:

Хз зачем это .... но он говорит работает ли ssh

~~~bash
ssh localhost
~~~

Тут уже больше инфы и он говорит Active или Inactive сервер ssh 

~~~bash
sudo service ssh status
~~~

Запуск ssh

~~~bash
systemctl start sshd
~~~

