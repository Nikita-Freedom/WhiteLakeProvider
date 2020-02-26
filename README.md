# WhiteLakeProvider

Данное расширение для ОС Android,  позволяет воспользоваться удалённым файловым хранилищем из произвольных приложений мобильной ОС. 
Релизовано с помощью Document Provider and SAF.

## Приступим

Данная инструкция поможет вам развернуть свой локальный сервер на виртуальной машине для хранения данных, загрузить и установить на телефон под операционной системой Android проводник для файлов, который поможет смотреть, открывать, скачивать файлы с тестового сервера(хранилища).

### Что нужно для работы?

Перед началом работы вам необходимо установить следующие компоненты: 
1. VMWare workStation. Подойдет любая ОС.
2. На VMWare workStation установить Apache Server. Можно установить с официального сайта: https://httpd.apache.org/download.cgi
Для более понятного процесса установки можно посмотреть: https://www.youtube.com/watch?v=a5UMDy0EeUU
3.Java SE Development Kit 8(понадобится для android studio). Установить можно с сайта: https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html
4.Android Studio последней версии. Можно скачать с официального сайта:https://developer.android.com/studio
Пройти весь процесс установки(в том числе загрузить SDK), загрузить виртуальный девайс для проверки расширения на нем.

### Шаги для установки apk
Как только вы убедились, что у вас установлена и корректно работает Android studio, подключен либо виртуальный девайс, либо реальное android устройство переходите к следующим действиям:
1. Скачайте отправленный вам на почту архив с apk. 
2. Распкакуйте в указанную вами папку.
3. Зайдите в Android studio
![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/Screenshot_2.png)

## Построен с помощью

* [SAF](https://developer.android.com/guide/topics/providers/document-provider?hl=ru) - Используется SAF.
* [Maven](https://maven.apache.org/) - Зависимость
* [DocumentProvider](https://developer.android.com/reference/android/provider/DocumentsProvider?hl=ru) - Используется как проводник файлов.

## Contributing

## Автор

* **Ульянов Никита**  [Nikita-Freedom](https://github.com/Nikita-Freedom)

## Подтверждения

* Предназначено для компании WhiteLake
