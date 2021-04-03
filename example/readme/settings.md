## Установка и запуск:
```
1. git clone https://github.com/Waitrum/ModularBotForUser
2. cd ModularBotForUser
3. pip install -r requirements.txt

Без запуска в фоне:
4. python3.7 main.py

С запуском в фоне:
4. apt install npm
5. npm install pm2 -g
6. pm2 start main.py --name=LoggerBot --interpreter=python3.7
```




## Настройка: `(configs/config.json)`
> Файл config.json появится после первого запуска программы.
>
> Данные настройки появляются если включеные все предустановленные модули. 

Name                 |       Type       | Info
---                  | ---              | ---
token                | str              | Сюда вписывать токен страницы.
TriggerShowLog       | str              | Триггер слово для вывода лога <br> (добавление <+> выводит только удаленные сообщения).
TriggerToAddChatLogs | str              | Триггер слово для добавления вайтлиста<br>(При добавлении чата логируются ГС, стикеры, фото, видео, музыка, документы.)
TriggerShowChatsLogs | str              | Триггер слово для показа всех бесед где включено логирование вложений.
WhiteListChat        | list[int]        | Список чатов в вайтлисте (заполняется через команды выше)<br>(Для вывода лога определенного юзера надо переслать его сообщение или ответить на него.)
TriggerStickers      | list[str]        | Массив слов триггеров, по которым отправляется стикер в беседу.
Answers              | list[str or int] | Массив стикеров или слов, которые отправляются по триггеру выше.
TimeWait             | int              | Время в минутах перезарядки кд срабатывания триггера сверху.
TriggerDelete        | str              | Триггер слово для удаления последних нескольких сообщений.<br>(ой5 - удалит последнии 5 сообщений)
TriggerTranslate     | str              | Триггер слово для транслита последнего сообщения в диалоге EN->RU и наоборот.
TriggerContest       | str              | Триггер слово для создания розыгрыша.<br>(роз 5 го - создаст розыгрыш с ключом "го")
TriggerAddStickers   | str              | Триггер для добавления/удаления стикера при упоминании.
TriggerIgnore        | str              | Триггер слово для добавления диалога в игнор отправки стикера при упоминании.
TriggerIgnoreList    | list[int]        | Массив диалогов в игнор листе.
TimeOutDel           | int              | Задержка удаления системных сообщений.
TriggerAddAudio      | str              | Триггер слово для добавления ГС.<br> Для Этого надо переслать сообщение с ГС и написать триггер.
TriggerVoice         | str              | Триггер символ для отправки сохраненного ГС.