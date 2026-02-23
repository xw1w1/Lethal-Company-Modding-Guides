# Туториал по созданию кастомных лун с использованием LethalLevelLoader

Этот гайд актуален для версии игры v73, но по мере обновления игры, если я найду что-то, что можно изменить или дополнить, то обязательно добавлю.

Текущая версия игры: v73.

## Подготовка.
Для начала вам необходимо установить все необходимые компоненты.

`Git`: https://git-scm.com/install/ (для загрузки собственных Package в Unity и др.)

`.NET 9`: https://dotnet.microsoft.com/en-us/download/dotnet/9.0

### Unity
После установки требуемых компонентов установите `UnityHub`: https://unity.com/download
И `UnityEditor` версии `2022.3.62f2`. https://unity.com/ru/releases/editor/archive

### Создание проекта
При создании убедитесь, что используете версию `2022.3.62f2` и template `High Definition 3D`.
<img width="1035" height="617" alt="image" src="https://github.com/user-attachments/assets/5bbf8a5e-14bb-4f14-8cf8-7ca76b2acf1e" />

В открывшемся проекте наведитесь на верхнюю панель инструментов и найдите там `Window > Package Manager`.

В верхнем левом углу открывшегося окошка должен быть `+`. 

Нажмите на него и выберите опцию `Add package from git URL...`.
<img width="805" height="585" alt="image" src="https://github.com/user-attachments/assets/a8db1e52-ceb5-43a5-9936-88bdb1b9ee6f" />

Вставьте в открывшуюся строку ввода следующие ссылки:

https://github.com/Zaggy1024/unity-project-patcher.git#lc-v73-fixes

https://github.com/Zaggy1024/unity-lc-project-patcher.git#v73-fixes

**⚠️ После загрузки пакетов может понадобится перезагрузка редактора, если некоторые UI элементы не видны. ⚠️** 

## Патч игры
В панели инструментов должна появится новая секция с названием `Tools.`

Наведитесь на нее. Найдите в ней `Unity Project Patcher > Open Window`.

Нажмите `Install BepInEx` в нижней части окна и дождитесь завершения загрузки.

Наконец, откройте Steam, найдите в нём Lethal Company. 

Наведитесь на `Управление > Просмотреть локальные файлы`.

Обычно это что-то вроде `C:\Program Files (x86)\Steam\steamapps\common\Lethal Company`.
<img width="994" height="664" alt="image" src="https://github.com/user-attachments/assets/df3d2ecd-c225-4346-9405-8c95d4292f02" />

Опуститесь в панель `Project`. Найдите в папке `Assets` файл `UPPatcherUserSettings` и вставьте путь к игре в нужное поле.

Вернитесь к недавно открывшемуся окну и нажмите `Start Patching`.

После этого редактор перезапустится самостоятельно около 7–10 раз, но время от времени будет показывать всплывающие окна.

Вам нужно просто нажимать "Ok" или "Yes", но обязательно прочитайте и убедитесь, что вы понимаете, что делаете.

Мои поздравления, теперь у вас есть пропатченный проект Lethal Company!
