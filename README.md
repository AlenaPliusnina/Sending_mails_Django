# Sending_emails_Django

Описание: 

    Sending_mails - это сервис, для отправки email через заданное количество секунд.
    
    На странице Send email представлена форма для ввода параметров 
    (адрес получателя email, тема письма, текст сообщения, и через какое количество секунд его отправить).
    
    На странице Mails list показаны последние десять писем, 
    которые поставлены в план (и те, что должны отправиться в будущем, и уже отправленные).
    
    У каждого письма в списке должен указан статус - отправлено оно или еще нет (send/wait).
    
    * Данный сервис должен реализован с применением многопоточности 
    (использована стандартный python модуль - threading).


Такж проект размещен на Heroku по ссылке: https://sending-mails-1.herokuapp.com/


Разворачиваем проект локально:

1. Скачайте репозиторий
2. Создайт виртуальное окружение:

        python -m venv env
       
3. Активируйте виртуальное окружение: 

        source env/bin/activate
        
4. Чтобы установить все требуемые библиотеки python в новом окружении выполните команду: 

        pip install -r requirements.txt
   
   Если у вас macOS до выполнения команды pip install -r requirements.txt выполните команду:       
   
           env LDFLAGS="-I/usr/local/opt/openssl/include -L/usr/local/opt/openssl/lib" pip install psycopg2==2.8.4      
   
   Для предотвращения появления ошибки (error: command 'gcc' failed with exit status 1.) при установке зависимостей.

5. Для работы проекта заполните описанные ниже переменные, либо заменив из значение в файле settings.py, либо создав файл переменных окружения (.env) с ихзначениями:

       - SECRET_KEY
       - EMAIL_HOST_USER (ваш адрес электронной почты gmail)
       - EMAIL_HOST_PASSWORD (парол от вашей электронной почты)
       
6. Чтбы запустить сервер введите команду: 

       python manage.py runserver

7. Для входа в администравтивную панель проекта создайте суперпользователя при помощи команды: 

       python manage.py createsuperuser
