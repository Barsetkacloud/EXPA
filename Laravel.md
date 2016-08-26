
## ========-> Для создание всяких вещей в Laravel надо :      
---- cmd - в нем перейти в папку с laravel, где файл artisan , это корень папки (команда - "cd" в помощь)      


#### ========-> Что бы на сайт заходить не через адресс "localhost/public", а через localhost:8000 то запускаем : -> php artisan serve     


### I.   Создать контроллер:                       php artisan make:controller NameController
### II.  Создать миграцию:                         php artisan make:migration create_tasks_table --create=tasks     
### II.  Создать модель:                           php artisan make:model Task  
### III.  Создать миграцию и модель:               php artisan make:model Name -m     
### III. Запуск миграций (создание таблиц):        php artisan migrate
### IV.  Просмотра маршрутов (routes):             php artisan route:list
### IV.  DatabaseSeeder - это тестовые записи в БД делаються:   php artisan db:seed      
    но перед командой надо написать класс и в нем прописать     
    занос данных в таблицу а потом только выполнять комманду       


#### ========-> Вывовод на страницу делаеться так же как в MVC
----- передача данных в view -> return view('post.index', ['posts' => $posts]); где $posts это массив данных


#### ========-> для работы link_to_route()      
1.в composer.js после - "laravel/framework": "5.2.", надо дописать :   "laravelcollective/html": "~5.0"    
2. написать в cmd(предварительно перейти в папку где лежит 'artisan') : php composer.phar update    
3. в папке config/ открыть - app.php, там найти массив 'providers'  в конец которого добавить :     'Collective\Html\HtmlServiceProvider',    
4. в том же файле в массив aliases - в конец - 'Form' => 'Collective\Html\FormFacade',     
                                              'Html' => 'Collective\Html\HtmlFacade',         


#### ========-> Комментирование в шаблонизаторe Blade
{{-- Это комментарий --}}                                                               
