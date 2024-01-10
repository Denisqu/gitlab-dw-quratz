### Сейчас
- [ ] Заменить gtest на QTest (https://doc.qt.io/qt-6.5/qtest-tutorial.html) и QCoroTest (https://doc.qt.io/qt-6.5/qtest-tutorial.html) 
- [ ] Написать тесты для Gitlab::ReplyHandler
- [ ] Выделить интерфейс: IRequestFormatter
- [ ] Написать тесты для Gitlab::RequestFormatter
- [ ]  Переписать Gitlab::Handler, чтобы его можно было протестировать (возможно с помощью mock-объектов)
- [ ] Написать логику для gitlab_handler.cpp с помощью Coroutines, TDD
- [ ]  Написать логику для db_manager с помощью TDD (сделать как здесь: https://github.com/Denisqu/qt-cxx-reference-projects/blob/main/projects/ch03-gallery-core/gallery-core/DatabaseManager.cpp)

### Потом
- [ ] Почистить CMake файлы от мусора.  
- [ ] Сделать наброс UI на FluentUI QML 

### Возможно уже не нужно
none

### Полезные Ресурсы для проекта
1) QML Book: https://distracted-dijkstra-f5d508.netlify.app/

### Сделано
- [x] Выделить интерфейс: IReplyHandler 
- [x] Отделить RequestFormatter в отдельную сущность, чтобы было легче тестировать (TDD) [+]
- [x] Сделать Model+View заготовку для будущей реализации главного экрана [+] 
- [x] Решить проблему с тем, что лог не пишется от объектов в другом потоке. [+]
- [x] Убрать asyncfuture [+]
- [x] Собрать Qt 6.5.3  из исходников [+]
- [x] Redirect qDebug to SimpleLogger (https://www.francescmm.com/logging-with-qt/) [+]
- [x]  Добавить новый логгер [+]
- [x]  Успешно собрать MSVC_CXX20 + QCoro + CoroutineTest [+]
- [x] Линкануться к QCoro https://github.com/danvratil/qcoro [+]
- [x] Обновить Qt до 6.5 LTS [+]
- [x] Разбить проект на 3 сабдиректории с CMake проектами: core, widgets-impl, qml-impl[+]
- [x] Сделать реализацию наброска UI [+] 
- [x] Поправить build_and_run.py, чтобы билд собирался в правильном месте и без мусора [+]
- [x] Добавить g-test, g-mock в проект [+]
- [x] Добавить Logger в проект [+]

### Отмена
- [ ] Добавить timeout для QNetworkRequest: void QNetworkRequest::setTransferTimeout(int timeout = DefaultTransferTimeoutConstant  [-]
- [ ] Перенести логгер в свой поток. [-]