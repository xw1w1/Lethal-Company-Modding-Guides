# Настройка проекта

**Перед прочтением этой главы убедитесь, что уже прошли [настройку редактора](https://github.com/xw1w1/Lethal-Company-Modding-Guides/blob/main/ru/moons/setup.md).**
<img width="1238" height="766" alt="image" src="https://github.com/user-attachments/assets/4aac2aea-e716-44f1-9089-864be2dccf11" />

## Менеджер модов
Если у вас еще не установлен `r2modman`, сделайте это по ссылке: https://r2modman.com/download/

Открыв приложение выберите `Lethal Company`, модифицируйте стандартный модпак `Default`, либо создайте новый.

Перейдите во вкладку `Online`, найдите моды `Lethal Level Loader`, `Lethal Lib` и скачайте их. Вместе с ними скачаются все нужные зависимости.

После этого ваш модпак должен выглядеть примерно так:

<img width="1249" height="687" alt="image" src="https://github.com/user-attachments/assets/4cf1005f-c4e2-41b6-a677-b6e5a43afa0b" />

Нажмите на `Start modded`. Вам нужно будет зайти в игру и загрузить планету, чтобы плагины создали все необходимые файлы.

После запуска вернитесь в `r2modman`, нажмите на вкладку `Settings` снизу и выберите второй пункт "`Browse profile folder`"
<img width="1233" height="773" alt="image" src="https://github.com/user-attachments/assets/6a8ab03c-5f2b-42d5-bb65-a88692a43910" />

После открытия скопируйте всё, что находится внутри папки `BepInEx/plugins`. (у меня вышло 8 папок)
<img width="599" height="543" alt="image" src="https://github.com/user-attachments/assets/1915187d-bc40-465f-9754-29e78a81ba82" />

Вернитесь в `Unity`. В `Projects` наведитесь на пустую область в папке `Assets` и нажмите ПКМ > `Show in explorer`

У вас откроется папка со всеми файлами вашего проекта. Переместитесь в `Assets/LethalCompany/Mods/plugins` и вставьте туда все скопированные вами папки. Древо проекта должно выглядеть примерно так:

## Возможные проблемы
Если вы столкнулись с проблемой следующего характера в консоли:
<img width="1083" height="195" alt="image" src="https://github.com/user-attachments/assets/d9860fab-c991-4b2d-b004-79680975b2de" />

Перейдите в папку `.../Mods/plugins` и выключите галочку "`Validate References`" для  `LethalLevelLoader.dll`.
<img width="1260" height="677" alt="image" src="https://github.com/user-attachments/assets/f4fd553e-4bc7-4bbf-b3e3-776ee5fc3f55" />

