# SDL2 Sidescroller game project

---

### Цель проекта:
Реализация простого sidescroller-a, с графикой на SDL2.

Цель понять, как работать с графическими библиотеками, в частности с SDL2, строить игровую логику и физику, а также создавать интерфейс и обрабатывать пользовательский ввод.

Поставлена цель реализовать: 
- простую игровую логику (перемещение камеры, пользовательский интерфейс, изменение состояния игрового мира)
- игровую физику (гравитацию, коллизии, взаимодействия с объектами и противниками, и т.д.)
- обработку пользовательского ввода и передачу его в игру
- искуственный интеллект противника

---

### Установка:

1. Скачать репозиторий
2. Установить vcpkg. Для этого перейти в директорию **vcpkg_install** и запустить скрипт:
   - для windows install.cmd
   - для unix install.sh
3. Установить необходимые библиотеки. Для этого:
   - Либо из директории **vcpkg_install** запустить скрипт:
     - для windows pkg_install.cmd
     - для unix pkg_install.sh
   - (Предпочтительный вариант) Либо открыть соответствующий файл в текстовом редакторе и установить библиотеки вручную, с учетом используемой операционной системы
      - как пример:
      ```bash
      ./vcpkg/vcpkg.exe install sdl2:x64-linux
      ``` 
5. Запустить сборку через cmake в корневой директории проекта:
      ```powershell
      cmake -B build
      cmake --build build
      ```

---

### Примерная структура проекта:

- [X] Файл main.cpp, где создаются все необходимые объекты и запускается бесконечный игровой цикл
- [X] Класс самой игры
- [X] Класс управляемого игроком персонажа
- [X] Класс для работы с текстурами
- [ ] Класс для работы с окружением (миром)
- [ ] Классы для работы с противниками
- [ ] Класс для работы с камерой
- [ ] Класс для работы с пользовательским интерфейсом
- [ ] Класс для работы с меню

--- 

### Структура репозитория:

- Директория **assets**: содержит спрайты для отображения игровых объектов.
- Директория **headers**: содержит header-файлы.
- Директория **src**: содержит исходный код проекта. 
- Директория **vcpkg_install**: содержит скрипты для установки vcpkg, а также необходимых библиотек для windows и unix-подобрыйх систем
- Файл **CMakeLists.txt** для установки программы.

---

### Реализованные цели:
1. Сборка самого проекта, подключение необходимых библиотек
2. README. Описание проекта, список поставленных и реализованных целей
3. Основной игровой цикл
4. Обработка пользовательского ввода, передача его в игровой цикл
5. Класс персонажа. Изменение состояния персонажа в соответствии с вводом (перемещение в пространстве кнопками стрелок)
6. Менеджер текстур, "натягивание" спрайтов на персонажа, противников, тайлы окружения
7. Коллизии (игрока с окружением, с противниками, противников с окружением и игроком, и т.д.) (Нужно немного доработать)
8. Гравитация (Воздействует на игрока)

---

### Поставленные цели:
1. Искуственный интеллект противников. Сами противники
2. Менеджер для работы с окружением (контроль состояния, сохранение состояния)
3. Менеджер для работы с камерой
4. Пользовательский интерфейс
5. Главное меню
6. Сохранение и загрузка с помощью файлов
7. Рефакторинг кода

---
