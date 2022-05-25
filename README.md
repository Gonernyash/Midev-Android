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
### Ресурсы
Ресурсы приложения распологаются в каталоге res
#### Strings
Тут распологаются все текста, зашитые в приложение (Тоесть не приходящие с сервера)
- Рекомендуется у компонентов, отображающих текст (Как например, TextView и Button), сам текст выноосить в strings.xml, а не писать его непосредственно в параметре компонента.
#### Drawable
Сюда входят все изображения, задействованные в приложении,
а также background'ы для компонентов верстки (Например: фон для кнопки с закругленными углами)
- Если изображение небольшое (Как, например иконки), то оно импортируется в формате SVG как Vector Asset.
  ![Картинка](https://i.imgur.com/4a9TNkQ.png)
  ![Картинка](https://i.imgur.com/Pq2HKEe.png)
- Если изображение большое, то открываем Resource Manager и закидываем изображение с учетом всех основных типов [dencity](https://developer.android.com/training/multiscreen/screendensities#TaskProvideAltBmp) (Итого, должно получится 5 изображений)
  ![Картинка](https://i.imgur.com/Xi83iKr.png)
#### Colors
Тут находятся цвета в формате HEX RGB(RGBA), используемые в приложении
По аналогии со strings, рекомендуется выносить все цвета сюда, а в компонентах указывать ссылку на цвет
#### Styles
Тут находятся темы и стили для всего приложения. Они содержат общие параметры для компонетов верстки (Например, базовый внешний вид кнопки). Их использование упрощает верстку.
[Подробнее](http://developer.alexanderklimov.ru/android/theme.php)
При создании собственных стилей рекомендуется наследоваться от компонентов [Material Design](https://material.io/develop/android) или [AppCompat](https://habr.com/ru/post/241479/)
Например:
```
<style name="RedButtonBorderless" parent="Widget.AppCompat.Button.Borderless">
    <item name="android:background">@color/colorAccentPrimaryRed</item>
</style>
```
#### Fonts
Тут находятся шрифты
#### Оптимизированная верстка
[Подробнее](https://developer.android.com/training/improving-layouts)
### Экраны приложения
- Что такое Activity
- Что такое Fragment
[Подробнее](https://medium.com/codex/activity-vs-fragment-in-android-d9595a79119)
#### Концепция SPA(Single Page Aplication)
В общих чертах: 
- У приложения есть одна Activity, привязанное к layout-контейнеру
- При переходе между экранами меняем содержимое контейнера на соответсвующий экрану Fragment
##### Лекции
- [Лекция 1](https://www.youtube.com/watch?v=wcdqoTubPrU&list=PLrrjuVcsVZhhE_7f_KXr1TRi3vEr_J5RP&index=31&t=986s)
### Работа с сетью
- Rest API
[Подробнее](https://blog.postman.com/rest-api-examples/)
- Протокол HTTP
[Подробнее](https://habr.com/ru/post/215117/)
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


