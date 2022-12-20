# VKinder
### Описание : 
Бот для взаимодействия с базами данных социальной сети. Бот будет предлагать различные варианты людей для знакомств в социальной сети Вконтакте в виде диалога с пользователем.

### Установка :
Для подключение и начала работы:

0. Установить пакеты из requirements.txt
1. Должна быть создана группа во Вконтакте, от имени которой будет общаться разрабатываемый бот. Инструкцию можно будет посмотреть [здесь](group_settings.md). Токен группы нужно поместить в settings/vk_config.py в переменную token_group =
2. Получите access_token для Вконтакте получить можно перейдя по [ссылке](https://oauth.vk.com/authorize?client_id=51507079&display=page&redirect_uri=https://oauth.vk.com/blank.html&scope=friends,notify,photos,wall,email,mail,groups,stats&response_type=token&v=5.131&state=123456).
    Вам требуется перейти по ссылке и скопировать из адресной строки сверху строчку между access_token= 'нужная строка' &expires_in. Данную строчку нужно поместить в settings/vk_config.py в переменную vk_token_client =
3. Установить PosgreSQL  и в settings/database_cinfig.py в переменную url прописать данные для подключения к БД 'postgresql://postgres(ЛогинБД):******(ПарольБД)@localhost:5432/Vkinder(Название)'. По умолчанию пароля нет или postgres 
4. Для начала работы запустите vk_bot.py
5. Если захотите удалить все данные из базы данных то можно воспоьзоваться ORM.clear_table()