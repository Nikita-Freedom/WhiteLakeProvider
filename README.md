# WhiteLakeProvider

Данное расширение для ОС Android,  позволяет воспользоваться удалённым файловым хранилищем из произвольных приложений мобильной ОС. 
Релизовано с помощью Document Provider and SAF.

## Приступим

Данная инструкция поможет вам развернуть свой локальный сервер на виртуальной машине для хранения данных, загрузить и установить на телефон под операционной системой Android проводник для файлов, который поможет смотреть, открывать, скачивать файлы с тестового сервера(хранилища).

### Предпосылки

Перед началом работы вам необходимо установить следующие компоненты: 
1. VMWare workStation. Подойдет любая ОС.
2. Apache Server. Можно установить с официального сайта: https://httpd.apache.org/download.cgi
Для более понятного процесса установки можно посмотреть: https://www.youtube.com/watch?v=a5UMDy0EeUU

3.Java SE Development Kit 8. Установить можно с сайта: https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html
4.Android Studio последней версии. Можно скачать с официального сайта:https://developer.android.com/studio
Пройти весь процесс установки(в том числе загрузить SDK), загрузить виртуальный девайс для проверки расширения на нем.

### Установка Android studio

В первую очередь, нужно убедиться, что у вас установлен JDK (Java Development Kit). Это обязательный компонент для разработки на Java, а поскольку разработка под Android ведется на Java — то и для разработки под Android тоже.

Теперь перейдем к установке Android Studio.

Для начала, Android Studio необходимо скачать. В одном установщике будет все необходимое — сама IDE, Android Emulator, Android SDK. То, чего нет в комплекте, инсталлятор докачает самостоятельно.

Перейдем непосредственно к установке. Ничего необычного в ней не будет — обычный диалог инсталлятора. В процессе нужно будет ответить лишь на один важный вопрос, и то это опционально:

Установка Android Studio

![Image alt](https://github.com/{Nikita-Freedom}/{WhiteLakeProvider}/raw/{master}/https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/Screenshot_2.png}/image.png)
 
Здесь, как следует из скриншота, установщик спрашивает, куда ставить студию, и куда ставить SDK. Если с самой студией все понятно, то SDK нужно быть внимательным. Как опять же следует из скриншота, для установки SDK нужно минимум 3.2 GB места на диске. Это минимум, на самом деле, места нужно больше, поскольку через какое-то время вам нужно будет докачивать обновленный SDK. так что, если вы не уверены, что места в будущем хватит — лучше измените местоположение на более вместительный диск.

После этого понадобится стандартно несколько раз нажать на кнопочку «далее», и на этом установка Android Studio завершена.

Настройка Android Studio
При первом запуске Android Studio задаст вам стандартный вопрос об импорте конфигурации:

Импорт Android Studio

 

По умолчанию будет выбран тот же чекбокс, просто нажмите на кнопку «ОК».

После этого Android Studio начнет качать Android SDK. Это может занять некоторое время. Если загрузка завершится неудачей, IDE предложит попробовать еще раз — обязательно нажмите «Retry».

Скачивание Android SDK в Android Studio

 

После окончания загрузки нажмите «Finish».

В принципе, на этом установка закончена, но я бы порекомендовал произвести еще некоторые настройки.

Во-первых, я советую сменить тему на темную («Darcula»).

 

Тема Darcula в Android Studio

По началу раз светлый текст на темном фоне может показаться вам непривычным, но поверьте — для глаз так намного легче. Разве что в темное время суток при Alt-Tab’е на «светлый» браузер смена фона будет резать глаза, но для того, чтобы этого не было, я рекомендую поставить замечательную программку f.lux.

Во-вторых, поставьте галочки «show line numbers» и «show method separators»:

 

Настройка Android Studio

Первая будет отображать номера строк слева от текста, вторая — будет рисовать разделители между методами в коде.

Эти две опции невероятно важны, а особенно для новичков, и я не понимаю, почему они выключены по-умолчанию.

В-третьих, настройте автодополнение. Для этого в «Case sensitive completion» выберите «None»:

 

Автодополнение в Android Studio

Поясню, почему именно так. Опция по-умолчанию подразумевает срабатывание автодополнения только в том случае, если первая буква набрана в правильном регистре. Опция None будет вызывать автодополнение независимо от того, в каком регистре вы начали набирать код.

Стандартное значение этой опции, как и прошлых двух, вызывает у меня недоумение.

Создание первого проекта
Что ж, с настройкой и установкой Android Studio мы разобрались, пришло время создать наш первый проект.

В главном окне Android Studio нажмите на «Start a new Android Studio project«:

Главное окно Android Studio

 

Появится новое окно, в котором нам нужно выполнить несколько действий.

В первом нужно задать имя приложения, домен компании (из этих двух параметров будет создано имя пакета), и расположение проекта на диске:

Создание проекта Android Studio

 

В Android, как и в Java, основным идентификатором приложения является имя пакета. Если вы ранее работали с Java, вы знаете, что это такое. Тем же, кто не знает, рекомендую гугл, или, например, вот эту статью.

Далее Android Studio спросит нас, какие и каких версий SDK мы хотим использовать. Пока что нам хватит «Phone and Tablet» SDK, версию API поставьте 16 вместо рекомендуемой 15-й, поскольку API 15 уже неактуально и совсем не распространено:

Создание проекта Android Studio

 

На следующем экране нас спросят, какие компоненты приложения мы хотим создать. Выберите «Empty Activity»:

Создание проекта Android Studio

 

На следующем шаге просто нажмите «Finish», ничего не меняя.

Далее, нам придется подождать некоторое время (от минуты до пяти минут, в зависимости от мощности вашего компьютера), пока Android Studio создает проект.

По завершению этого процесса вы увидите, наконец-то, свой первый проект:

Hello World Android Studio

 

Он уже вполне работоспособен, но чтобы его запустить, нам понадобится эмулятор Android.

Создание эмулятора Android
Для создания эмулятора Android нам понадобится Android AVD Manager (AVD = Android Virtual Device). Не беспокойтесь, ставить больше ничего не потребуется. Просто нажмите на эту кнопочку:

Android Studio AVD Manager

 

Потом на эту кнопочку:

Android Studio AVD Manager

 

А потом просто несколько раз кликните «Next» и, наконец, «Finish»

Запуск Hello World
Пришло время запустить наш первый проект, созданный в Android Studio!

Нажмите на вот эту кнопку (или Shift-F10):

Запуск приложения в Android Studio

 

После этого вы увидите диалог, в котором вам будет предложено выбрать девайс, на котором IDE должна запустить собранное приложение:

Выбор устройства в Android Studio

 

Поставьте выделенную стрелкой галочку и нажмите «ОК». Начнется сборка проекта, запуск эмулятора, установка приложения на эмулятор, и запуск приложения.

На это уйдет некоторое время (чем мощнее ваш компьютер — тем меньше времени понадобится), поскольку эмулятор — вещь достаточно медлительная, несмотря на колоссальные улучшения в последние пару лет.

И вот, по прошествии 1-10 минут (после запуска эмулятора проекты, конечно же, будут собираться и запускаться быстрее), вы, наконец, увидите свой Hello World на экране эмулятора!



## Построен с помощью

* [SAF](https://developer.android.com/guide/topics/providers/document-provider?hl=ru) - Используется SAF.
* [Maven](https://maven.apache.org/) - Зависимость
* [DocumentProvider](https://developer.android.com/reference/android/provider/DocumentsProvider?hl=ru) - Используется как проводник файлов.

## Contributing

## Автор

* **Ульянов Никита**  [Nikita-Freedom](https://github.com/Nikita-Freedom)

## Подтверждения

* Предназначено для компании WhiteLake