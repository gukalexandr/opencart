# Добавить в административной части на страницу редактирования товара новое поле: "Альтернативное название", которое будет содержать просто текст.
# Вывести значение нового поля в пользовательской части, под названием товара на странице категории и товара.
1. установите opencart последней версии  с www.opencart.ru. пройдите все шаги установки
2. Linux
    - chmod 0755 or 0777 system/storage/cache/
	- chmod 0755 or 0777 system/storage/download/
	- chmod 0755 or 0777 system/storage/logs/
	- chmod 0755 or 0777 system/storage/modification/
	- chmod 0755 or 0777 system/storage/session/
	- chmod 0755 or 0777 system/storage/upload/
	- chmod 0755 or 0777 system/storage/vendor/
	- chmod 0755 or 0777 image/
	- chmod 0755 or 0777 image/cache/
	- chmod 0755 or 0777 image/catalog/
	- chmod 0755 or 0777 config.php
	- chmod 0755 or 0777 admin/config.php
3. В Windows убедитесь, что для папок и файлов разрешаны чтение и запись. 
    - system/storage/cache/
	- system/storage/download/
	- system/storage/logs/
	- system/storage/modification/
	- system/storage/session/
	- system/storage/upload/
	- system/storage/vendor/
	- image/
	- image/cache/
	- image/catalog/
	- config.php
	- admin/config.php
4. для разработки использовал php 7.4, mariadb
5. бд opencart
6. пользователь бд root
7. пароль root
8. создать в таблице oc_product_description  новое поле alter_name 
9. ALTER TABLE oc_product_description ADD alter_name text NOT NULL;
11. склонируйте репозиторий с GitHub https://github.com/gukalexandr/opencart.git
12.  на ветке master лежит ядро  магазина
13. на ветке  alternative_name осуществлено добавление поля "Альтернатиное название" в административную и пользовательскую части
14. дамп всей базы данных opencart.sql
15. обратите внимание что  config.php и /admin/config.php перезапишутся, поэтому перед клонированием репозитория сохраните свои файлы рядом с директорией магазина, а потом замените склонированные на свои
16. после вненсения изменений очистите кэш в storage/cache