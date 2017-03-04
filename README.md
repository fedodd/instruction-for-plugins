# instruction-for-plugins
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
   
   
