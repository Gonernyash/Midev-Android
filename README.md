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
- // TODO: Написать что-нибудь
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
##### Версии Android SDK
### Архитектура Android-приложений
#### MVC: Model-View-Controller
Устаревшая архитектура, но стоит мельком посмотреть, т.к. иногда попадается в старых приложениях
#### MVP: Model-View-Presenter
Используется в большинстве наших приложений. Стоит уделить ей особое внимание
#### MVVM: Model-View-ViewModel
Сейчас довольно популярный подход к разработке. Планируем попробовать в новых проектах
### Верстка
#### Виды Layout'ов
- LinearLayout
- ConstraintLayout
- RelativeLayout (устарел, вместо него рекомендуется использовать ConstraintLayout, но часто можно встретить в проектах)
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
### Экраны приложения
- Что такое Activity
- Что такое Fragment
#### Концепция SPA(Single Page Aplication)
В общих чертах:
- У приложения есть одна Activity, привязанное к layout-контейнеру
- При переходе между экранами меняем содержимое контейнера на соответсвующий экрану Fragment
##### Лекции
- [Лекция 1](https://www.youtube.com/watch?v=wcdqoTubPrU&list=PLrrjuVcsVZhhE_7f_KXr1TRi3vEr_J5RP&index=31&t=986s)
### Работа с сетью
- Rest API
- Протокол HTTP
- JSON
## Как пишем мы
### Структура проекта
### Библиотеки
