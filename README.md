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
Устаревшая архитектура, но стоит мельком посмотреть, т.к. иногда попадается в старых проектах
#### MVP: Model-View-Presenter
Используется в большинстве наших приложений. Стоит уделить ей особое внимание
#### MVVM: Model-View-ViewModel
Сейчас довольно популярный подход к разработке. Планируем попробовать в новых проектах  
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
- RecyclerView
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
- Moxy - реализация архитектуры MVP
- Retrofit - запросы на сервер
- Cicerone - роутинг в МП
- Glide - Загрузка изображений
- RxJava - ассинхронность в приложении (для запросов на сервер и т.д.)
### Дополнительно
- Git и подход Git-flow(для коммандной разработки)
## Практика
Тестовые задания для практики
### 1. База
К каждой задаче прикреплен скрин. Необходимо сделать также как на нем.
#### 1.1
Реализовать с помощью Linear Layout экран
![Задание 1.1](https://i.imgur.com/JaR3ZU5.jpg)
#### 1.2
Прикрепить к кнопке иконку и связать ее с текстовым полем, чтобы отображать количество кликов.
Подсказка: Прикрепить к кнопке листенер через setOnClickListener.
![Задание 1.2](https://i.imgur.com/gZ906ud.jpg)
#### 1.3
Тут важно расположить все точно также как на скрине. Нужно использовать два LinearLayout 
![Задание 1.3](https://i.imgur.com/olRFpyp.jpg)
##### 1.4
Тут требуется разобраться с RecyclerView и сделать экран с составлением списка. По нажатию на "+" слово должно добавляться в список. 
Подсказка: написать адаптер, подключить его к RecyclerView.
![Задание 1.4](https://i.imgur.com/9LOvVkb.jpg)
#### 1.5
Вводим ссылку на картинку и отображаем ее в RecyclerView.
Подсказка: Для отображения картинок подключить библиотеку Glide.
![Задание 1.5](https://i.imgur.com/TZ0TluL.jpg)
#### 1.6
Кнопка для добавления элемента прямо в ресайклере и элементы сеткой идут.
Подсказка: Чекнуть свойство layoutManager у ресайклера, и что оно принимает.
![Задание 1.6](https://i.imgur.com/n2IWiji.jpg)
#### 1.7
Сегодня посмотрим слайдеры.
Необходимо подключить [библиотеку](https://github.com/smarteist/Android-Image-Slider)
и написать адаптер. 
Адаптер по структуре почти такой же как адаптер RecyclerView.
![Задание 1.7](https://i.imgur.com/CQ6ZlwB.jpg)
