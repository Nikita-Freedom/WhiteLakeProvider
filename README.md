# WhiteLakeProvider

Данное расширение для ОС Android,  позволяет воспользоваться удалённым файловым хранилищем из произвольных приложений мобильной ОС. 
Релизовано с помощью Document Provider and SAF.

## Приступим

Данная инструкция поможет вам развернуть свой локальный сервер на виртуальной машине для хранения данных, загрузить и установить на телефон под операционной системой Android проводник для файлов, который поможет смотреть, открывать, скачивать файлы с тестового сервера(хранилища).

### Что нужно для работы?

Перед началом работы вам необходимо установить следующие компоненты: 
1. VMWare Player. Подойдет любая ОС. Скачать можно отсюда: https://www.vmware.com/ru/products/workstation-player/workstation-player-evaluation.html

2. На VMWare workStation установить Apache Server. Можно установить с официального сайта: https://httpd.apache.org/download.cgi
   Для более понятного процесса установки можно посмотреть: https://www.youtube.com/watch?v=a5UMDy0EeUU
   
 3.Java SE Development Kit 8(понадобится для android studio). Установить можно с сайта:  https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html

 4.Android Studio последней версии. Можно скачать с официального сайта:https://developer.android.com/studio
 Пройти весь процесс установки(в том числе загрузить SDK), загрузить виртуальный девайс для проверки расширения на нем.

### Шаги для установки apk
Как только вы убедились, что у вас установлена и корректно работает Android studio, подключен либо виртуальный девайс, либо реальное android устройство переходите к следующим действиям:
1. Скачайте отправленный вам на почту архив с APK. 
2. Распкакуйте в указанную вами папку.
3. Зайдите в Android studio и нажмите "Open an existing Android Studio project" как показано на скриншоте

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/1.jpg)

4. Найдите в списке файлов ваш распакованный APK

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/2.jpg)

5. Откройте ваш проект(APK) и дождитесь пока система сборки Gradle соберет ваш проект

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/3.jpg)

6. Как только система сборки соберет ваш проект выберите в панели сверху справа девайс на котором будет устанавливаться APK(это может быть как виртуальный девайс, так и реальное Android устройство, подключенное к компьютеру с включенным режимом отладки)

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/5.jpg)

7. Как только проект будет собран, нажмите зеленую стрелочку(кнопку Run) на верхней панели справа

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/4.jpg)

8. Дождитесь установки APK на ваш девайс.
9. После установки на вашем девайсе сразу откроется окно с полем ввода сервера(по умолчанию там введен адрес моего сервера)

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/Screenshot_1.png)

10. Вы также можете редакатировать поле ввода и ввести туда свой сервер. Отображение статуса подключения видно под полем ввода текста.

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/Screenshot_322.png)

11. Зайдите в файлы и там будет отображаться наш проводник с файлами на сервере.

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/Screenshot_6png)

12. Откройте проводник и посмотрите содержимое файлов и папок на вашем сервере.

![Image alt](https://github.com/Nikita-Freedom/WhiteLakeProvider/blob/master/Screenshot_7ng)

## Построен с помощью

* [SAF](https://developer.android.com/guide/topics/providers/document-provider?hl=ru) - Используется SAF.
* [Maven](https://maven.apache.org/) - Зависимость
* [DocumentProvider](https://developer.android.com/reference/android/provider/DocumentsProvider?hl=ru) - Используется как проводник файлов.

## Автор

* **Ульянов Никита**  [Nikita-Freedom](https://github.com/Nikita-Freedom)

## Подтверждения

* Предназначено для компании WhiteLake
