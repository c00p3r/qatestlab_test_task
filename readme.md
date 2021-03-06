# Test Task
##Требования:
* PHP >= 5.6.4
* mySQL
* composer
* Laravel 5.3

##Инструкция:
* скачать проект и разархивировать в папку 
* из папки проекта запустить команду `php composer install`
* в корне проекта скопировать и переименовать файл `.env.example` в `.env`
* после запустить команду `php artisan key:generate` для генерации ключа приложения
* далее в файле `.env` прописать настройки подключения к БД
* открыть сайт в браузере

####Тестовые данные:
* для генерации таблиц БД нужно запустить команду `php artisan migrate` 
* для "посева" тестовых данных нужно выполнить команду `php artisan db:seed` ИЛИ использовать опцию в предыдущем шаге `php artisan migrate --seed` 
* ИЛИ воспрользоваться дампом БД `dump.sql` в корне проекта, а также архивом польз-ких файлов `uploads.zip`, который нужно разархивировать в папку `/public`

##Техзадание:
Сайт для публикации объявлений о продаже автомобилей (см. http://avtobazar.ua, http://auto.ria.ua ).

Сайт должен предоставлять возможность простой регистрации (мейл, пароль) и публикации объявлений пользователями. Во время публикации пользователь должен иметь возможность выбрать:
* область, 
* город, 
* марку, 
* модель, 
* объем двигателя, 
* пробег, 
* количество хозяев, 
* а также загрузить фотографии своего автомобиля.

_Один пользователь может опубликовать не более 3х объявлений._

Сайт должен состоять всего из _одной страницы_, на которой должны отображаться объявления в порядке соответствующем дате публикации. 

На странице отображать _не более 10 объявлений_ с постраничной навигацией. Постраничная навигация должна быть реализована с использованием AJAX-технологии.

Основной частью сайта должна стать фильтрация объявлений: возможность фильтровать объявления по всем параметрам указанным в объявлениях (область, город, марку, модель, объем двигателя, пробег, количество хозяев). Связь между фильтрами должна соответствовать логическому “И”.

####Требования к реализации:
* Бекэнд должен быть реализован с использованием ООП, обязательно использовать один из паттернов программирования (приветствуется использования фреймворков, НЕ ИСПОЛЬЗОВАТЬ готовые CMS)
* Все SQL-запросы должны храниться в отдельных файлах.
* Весь Javascript должен хранится в отдельных файлах.	
* Фронтэнд должен быть простым, но интуитивно-понятным, приветствуется использования визуальных фреймворков (Bootstrap, Skeleton).
* Имена файлов должны быть приведены к нижнему регистру.
* Проект должен легко разворачиваться без настройки дополнительного виртуального хоста. (Доступен по адресу напр. http://localhost/autosale).
* Обязательно должен быть прикреплен дамп базы данных в формате sql 	c детальной инструкцией по разворачиванию проекта.

