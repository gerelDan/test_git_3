## Hello World

Тефтелька - замечательный котик)

Совершенно с этим согласен!

1. Создали аккаунт на github.com
2. Создать локальный репозиторий и закоммитить туда что-нибудь
3. "Подружить" локальный и удаленный репозиторий:
* Для начала нужно подружить компьютер с github для этого, обратите внимание что здесь необходимо указывать ту почту, которую Вы указывали при регистрации на  gitHub.com:
```sh
 ssh-keygen -t ed25519 "mail@github.com"
 ```
Терминал задаст вопрос куда сохранить ssh ключ (в скобках указан путь по умолчанию):
```sh
Enter file in which to save the key (/c/Users/Даниил/.ssh/id_ed25519):
```
Нажмем enter чтобы оставить как есть либо ввести свой путь. После этого терминал попросит контрольную фразу (пароль) и попросит повторить его:
```sh
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```
Терминал выдаст куда сохранил ключ и собственно сам ключ:
```sh
Your identification has been saved in /c/Users/Даниил/.ssh/id_ed25519
Your public key has been saved in /c/Users/Даниил/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:gAX5zonK5U8bwT5vCxxtt872g+/0GadpRv/Q+1NQqoU mail@github.com
The key's randomart image is:
+--[ED25519 256]--+
|    .o.          |
|    .o           |
|    ...          |
|      ..     .   |
|     = .S...o    |
|    o O .U.+o o. |
| . + + * .o..o+=o|
|  o . * o.   +**S|
|       +.    =B*X|
+----[SHA256]-----+
```
Теперь необходимо добавить ключ в используемые ключи:
```sh
ssh-add /c/Users/Даниил/.ssh/id_ed25519
```
Если использовали пароль то запросит пароль:
```sh
Enter passphrase for /c/Users/Даниил/.ssh/id_ed25519:
```
Теперь нужно вставить буффер обмена наш ключ:
```sh
clip < /c/Users/Даниил/.ssh/id_ed25519.pub
```
После этого переходим на ```github.com``` ->
В разделе настроек переходим ```ssh and GPG keys``` -> Нажимаем ```New ssh key```
![github](github.png)
В появившемся окне В поле ```title``` вписываем название и в поле ```key``` вставляем из буффера обмена наш ключ и нажимаем кнопку ```add SSH key```

Все компьютер с github'ом подружили!!!
Теперь подружим наши локальные и удаленный репозитории:
1. Создаем репозиторий на github.com с любым названием.
2. Github подскажет какие команды нужно ввести их всего 3:
```sh
git remote add origin https://github.com/gerelDan/test_git_3.git
git branch -M main
git push -u origin main
```
Все на удаленном репозитории закоммитились все изменения из локального репозитрия!
 
