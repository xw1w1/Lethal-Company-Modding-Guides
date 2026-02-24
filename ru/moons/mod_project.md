# Создание мода
Если вы уже импортировали все нужные зависимости в проект, можно приступить к созданию самого мода.

Поскольку для планеты используется `LethalLevelLoader`, для начала мы сделаем сам мод LLL.

В папке `Assets/LethalCompany/Mods` создайте свою папку рядом с `plugins`.
<img width="415" height="232" alt="image" src="https://github.com/user-attachments/assets/65bc403b-3011-4c71-8e08-b89a6f2070ea" />

Внутри этой папки создайте `ExtendedMod`. (`ПКМ > LethalLevelLoader > ExtendedMod`)

В вашей папке должен появиться следующий `ScriptableObject`:
<img width="854" height="367" alt="image" src="https://github.com/user-attachments/assets/faca4f33-86de-4df5-855e-248278e95bf8" />

Поле `Mod Name`, как можно догадаться, отвечает за название вашего мода.
Поле `Author Name` - имя автора. В моем случае это `Turbotaliz`. Учтите, что лучше использовать одинаковое имя автора для всех ваших проектов :')

Поля с **Extended** контентом, это то, что мы хотим добавить в наш мод в будущем.
