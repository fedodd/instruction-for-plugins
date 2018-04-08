# instruction-for-plugins

GIT:

В папке с будущим проектом:
git init

Добавить все изменения к коммиту
git add -A 

Сделать коммит:
git commit -m 'Комментарий'

Отправить всё на сервер:
git push origin название-твоей-ветки

Создать ветку:
git checkout -b 'branch_name'
 git checkout master - переход на мастер если надо

НАСТРОЙКА СБОРЩИКА

Устанавливаем ноду
Устанвливаем галп глобально
npm install -g gulp-cli
Создаём пустой проект и инициализаируем в нём гит-репо

В проекте иницилизируем пакет:
npm init

Cделать проще: yarn -  установит сразу все пакеты.
yarn add gulp-changed

____________________________________
Устанавливаем необходимые пакеты с флагом --save-dev, чтобы они сохранились в package.json

npm install --save-dev gulp gulp-concat gulp-postcss autoprefixer
Создаём галп-файл и описываем в нём задачи. Подсмотреть здесь: https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md

Запускаем задачу:

gulp serve
__________________________________
Добавляем node_modules и сгенерированные файлы в .gitignore

Небольшая инструкция по прикрутке галерей и слайдеров к проекту

ГАЛЛЕРЕЯ
1) Генерируем код css и js на http://dimsemenov.com/plugins/magnific-popup/
2) Сохраняем код в magnificpopup.css и magnific.js в соответствующих папках проекта (у нас в вендорах)
3) создаем задачу для gulp по переноске файлов в build
4) включаем задачу в gulpfile
5) подключаем код в index (в основном скрипты, сss по идее gulp включает в один файл) :
  <script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
  <script src="/scripts/vendor/magnific.js"></script>
  <script src="/scripts/app.js"></script>

Слайдер
1) скачать slick c http://kenwheeler.github.io/slick/
2) Сохраняем код slick.css slick-theme.css и slick.min.js в соответствующих папках проекта (у нас в вендорах)
3) создаем задачу для gulp по переноске файлов в build
4) включаем задачу в gulpfile
5) подключаем код в index (в основном скрипты, сss по идее gulp включает в один файл) :
   <script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
 <script type="text/javascript" src="slick/slick.min.js"></script>
   <script src="/scripts/app.js"></script>
   
   * Если мы уже подключили jquery  и app.js То нужна только строчка со slick
   
   Сервер с MYSQL И WP TONIK
   
Sudo service apache2 start - запуск
Затем sudo service mysql start
Yarn watch в теме
