# Обзор OpenIPC webui

Краткая история web интерфейсов, доступных в OpenIPC

## Legacy_webui

Репозиторий: https://github.com/openipc/webui

Создавался как базовый очень простой интерфейс, в котором можно было применять основные настройки не только в консоли. Первично был привязан к встроенному и простому httpd, который входит в пакет busybox и работал на 85 порту. Для CGI скриптов используется haserl, как простой и миниатюрный.

После того как в Majestic появилось очень много функций, а так-же в связи с расширением возможностей запуска на разных процессорах, появилась необходимость работать с параметрами которые можно получать из стримера напрямую. в Legacy постоянно приходится парсить выхлоп переменных, и включать те или иные функции. 

Так-же в этом интерфейсе наработана основная масса плагинов, которые полюбились многим пользователям, однако это-же сыграло и плохую роль, интерфейс стал глючным и неповоротливым. Было принято решение сделать еще один интерфейс, уже привязанный к стримеру.

## majestic_webui

Репозиторий: https://github.com/openipc/majestic-webui

Следующая версия интерфейса, уже очень тесно работает со стримером, многие параметры автоматически считываются и корректируются между стримером, конфигом и отображаемой частью. Так-же в этом режиме все функции HTTP сервера отданы только majestic, который умеет ssl и множество других возможностей.

Единственный минус - нет плагинов, которые нужно просто очищать, дорабатывать и переносить. Это правильный путь, а то что один интерфейс запускается поверх второго это просто решение для энтузиастов.

## FancyWeb 

Репозиторий: https://github.com/openipc/fancyweb

Так-же у нас есть шикарный интерфейс, который не нашел своего воплощения просто из-за некоторой "жирности" на тот момент и отсутствия работы API в стримере. Написан на ReactJS.

Для ознакомления с возможностями доступна прекрасная презентация: https://github.com/OpenIPC/fancyweb/blob/master/presentation/OpenIPC_fancyweb_interface_rus.pdf

## 4th_generaton_webui

Репозиторий: не готов к публичному доступу

Интерфейс, находящийся в разработке, собирает в себе возможности всех трёх предидуших, будет компактым, стильным, стабильным, на современных фреймворках и прочем.
