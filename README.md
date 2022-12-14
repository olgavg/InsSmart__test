# ReadMe

Для работы сборки вам понадобится скачать и установить node.js.

Также установите систему контроля версии Git. Для работы сборки Git не обязателен, но для удобства установки и дальнейшей разработки лучше все же установить.

Для установки (клонирования репозитория) в текущую папку из консоли введите команду: git clone https://github.com/olgavg/InsSmart__test.git .

Все команды пишутся от корня проекта!

После того как все исходники будут скачаны из удаленного репозитория, введите в консоли команду npm install для установки проекта. Все зависимости установятся автоматически.

Для сборки проекта наберите в консоли команду npm run dev.
Если нет ошибок, то для запуска проекта нужно набрать в консоли npm run start, в браузере по умолчанию откроется домен http://localhost:3030 с тестовым заданием.

Если все это сделать невозможно, то просто откройте в браузере файл из каталога /dist/index.html. Должен запуститься собранный проект сам.

# Некоторые комментарии по верстке и дизайну:

Верстка представлена в отдельных контейнерах - для мобильной и десктопной версии. Не нашла быстрого решения для реализации в одном контейнере без повторения контейнера. Но, если на сайте будет возможность выносить компаненты в отдельные файлы (будет использоваться Angular, Vue, что-то еще с возможностью include file), то содержимое табов/боксов аккордеона вполне можно вынести в отдельный компанент и не дублировать - там код верстки у меня совпадает до символа и стиля. Отличия лишь в обертке и методах управления. 

Т.к. выглядит все виджетом, который должен отдельно встраиваться на какой-то сайт, верстала его по соответствующим правилам, а именно - единицы все абсолютные заданы (размерность шрифтов и отступов в пикселях, а не в процентах или rem/em, т.к. иначе его UI будет зависим от установок сайта, куда он будет встроен).

Изначально контейнер для виджета задан с отступами (их можно удалить мгновенно при надобности), как в Figma, т.к. неясен контекст, где и как должен размещаться на живом сайте.

Для десктопной версии задана максимально-допустимая ширина виджета, как в Figma - 846px. это тоже легко удаляется при надобности.
