# Для новичков
## Теория
Базовые вещи, которые нужно знать для Android-разработки
### Kotlin
Котлин может использоваться где угодно, но нас интересует его использование только в разработке Android-приложений
#### Книги:
- [Книга 1 (Мне больше нравится)](https://codernet.ru/books/kotlin/kotlin_programmirovanie_dlya_professionalov/)
- [Книга 2](https://yurecnt.ru/files/books/s1p4kl2p10b9y2xr1jlxtji5xg2yl6.pdf)
#### Обратить внимание на:
##### ООП
##### Функции области видимости
- with
- let
- run
- apply
- also
#### Дополнительно
- Можно для практики порешать задачки на [CodeWars](https://www.codewars.com/kata/kotlin)(Для понимания базового синтаксиса будет достаточно выбрать сложность 8-5 kyu)
### Базовый ввод в разработку под Android
#### Книги:
- [Книга 1](https://vk.com/doc44301783_581713618?hash=wf5RyEZbp9VxSni5uiwx5VhMqIWFdEeDeAxy9JjJFB4&dl=SGz6Wx6DvjLIvVfbnICvMkcWAHYktZ6dFpuyIC6HbQo)
#### Обратить внимание на
##### Возможности IDE Android Studio
##### Gradle
- Структура .gradle файла
- Подключение библиотек
- Возможности gradle
##### Версии Android SDK
В зависимсти от целевого и минимального андройд сдк, подходы к разработке могут различаться (особенно если целевое сдк >= 30), поэтому рекомендуется 
- Ознакомится со списком измений, вносимыми в каждой новой версии Android SDK, начиная с 21.
### Архитектура Android-приложений
#### MVC: Model-View-Controller
Устаревшая архитектура
#### MVP: Model-View-Presenter
Используется в большинстве наших приложений
#### MVVM: Model-View-ViewModel
Сейчас довольно популярный подход к разработке. Планируем попробовать в новых проектах
[Видик](https://www.youtube.com/watch?v=KeQWIu8bA-Y&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=7)
#### MVI: Model-View-Intent
MVVM на стеройдах (Самый новый и преспективный подход)
[Видик](https://www.youtube.com/watch?v=xsXiC0BXUjI&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=13)
#### Статьи
[Статья на хабре](https://habr.com/ru/post/215605/)  
[Подробнее про MVP](https://learntutorials.net/ru/android/topic/4615/%D0%B0%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0-mvp)
### Структура Android-приложения
- Посмотреть, какие бывают ресурсы и как с ними работать
- Рекомендуется ознакомится с коцепцией Android Clean Architecture для ориентирования в проекте. [Статья](https://habr.com/ru/company/mobileup/blog/335382/)
### Верстка
#### Виды Layout'ов
- LinearLayout
- ConstraintLayout
- RelativeLayout (считается устаревшим, вместо него рекомендуется использовать ConstraintLayout, но часто можно встретить в проектах)
- FrameLayout
#### Основные компоненты
- TextView
- ImageView
- Button
- EditText
- RecyclerView [Урок](https://www.youtube.com/watch?app=desktop&v=4pevVON0v-U&list=LL&index=2&t=848s)
### Экраны приложения
- Что такое Activity
- Что такое Fragment  
[Подробнее](https://medium.com/codex/activity-vs-fragment-in-android-d9595a79119)
#### Концепция Single Activity Application
В общих чертах: 
- У приложения есть одна Activity, привязанное к layout-контейнеру
- При переходе между экранами меняем содержимое контейнера на соответсвующий экрану Fragment
##### Лекции
- [Лекция 1](https://www.youtube.com/watch?v=wcdqoTubPrU&list=PLrrjuVcsVZhhE_7f_KXr1TRi3vEr_J5RP&index=31&t=986s)
### Работа с сетью
- Rest API  
[Подробнее](https://blog.postman.com/rest-api-examples/)
- Протокол HTTP  
[Статья](https://habr.com/ru/post/215117/)
[Лекция](https://www.youtube.com/watch?v=HFt7Lm7hv1E&list=PLrCZzMib1e9qZwq95WVmGB-acnot5ka4a&index=6)
- JSON  
[Подробнее](https://habr.com/ru/post/554274/)
### Библиотеки
- Moxy - реализация архитектуры MVP([Статья](https://habr.com/ru/post/276189/))
- Retrofit - запросы на сервер
- Cicerone - роутинг в МП
- Glide - Загрузка изображений
- RxJava - ассинхронность в приложении (для запросов на сервер и т.д.)
- Realm - локальная база данных (для кэширования данных в приложении).
- Koin - Dependency Injection (Внедрение зависимостей)
[Теория бд для тех кто в танке](https://es.1lib.mx/dl/478554/32401f) - читать только 1 и 2 главу (в pdf я не нашел, использовать [онлайн читалку](https://djvu.js.org/) djvu файлов).
[Теория по NoSQL БД](https://sd.blackball.lv/library/NoSQL_DISTILLED_(2013).pdf), коей и  является Realm.
### Clean Architecture
- [Теория UseCases](https://www.youtube.com/watch?v=Ao3d1R1TCYc&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=1)
- [Практика UseCases](https://www.youtube.com/watch?v=YQlQvqqsaJ0&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=2)
- [Связь UseCases и Repository](https://www.youtube.com/watch?v=zt07bObIpSk&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=3)
- [Модуди Clean Architecture](https://www.youtube.com/watch?v=rCkyU5lPAT8&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=5)
- [Clean Architecture на Koin](https://www.youtube.com/watch?v=Mn8WwqbndGg&list=PLeF3l86ZMVkLQbdRL6Ra4cr_cmPROj94y&index=7)
### Дополнительно
- Git и подход Git-flow(для коммандной разработки)
