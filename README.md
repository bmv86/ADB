# ADB
**`Home Works`**



 1. Отобразить подключённый девайс в консоли.
 
adb devices

 2. Установить .apk файл приложениия todolist на телефон с компьютера через  ADB

adb install /Users/mary/todolist.apk

 3. Вывести адрес приложения todolist в системе Android

adb shell pm list packages | grep todolist

 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.

adb shell screencap -p /storage/emulated/0/Pictures/Screenshot_todolist.png && adb pull /storage/emulated/0/Pictures/Screenshot_todolist.png /users/mary/todolist.png

 5. Вывести в консоль логи приложения todolist

adb logcat | grep -rnw "com.android.todolist"

 6. Скопировать логи приложения todolist на компьютер.
сохранили на компьютер:

adb logcat | grep -rnw "todolist" > /Users/mary/group_22/togolist.log 
(выйти из adb logcat Control+C)

 7. Удалить приложение todolist с телефона через ADB

adb uninstall com.android.todolist
