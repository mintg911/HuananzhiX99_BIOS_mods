#### Рекомендуется прошивать биос с помощью S3TurboTool *(за данную утилиту спасибо ser8989)*

#### Инструкция по разблокировке макс.частоты на все ядра, а не на два (в народе более известно как "анлок")
Не стоит бояться того, что тут много текста. На самом деле всё несложно, я лишь попытался ничего не упустить и быть с вами шаг за шагом.
1. Запускаем S3TurboTool
2. Нажимаем MMTool5
3. В появившейся утилите "MMTool Aptio" нажимаем "Load Image" и выбираем необходимый биос
4. Переходим на вкладку "CPU Patch", выделяем микрокод "6F 06F2", отмечаем "Delete a Patch Data", нажимаем Apply и соглашаемся
5. Нажимаем "Save Image" и закрываем "MMTool Aptio"
6. В S3TurboTool нажимаем AMIBCP5
7. В появившейся утилите AMIBCP открываем биос
8. Раскрываем список и идём по пути "Common RefCode Configuration > IntelRCSetup > Advanced Power Management Configuration > CPU C State Control"
9. Справа, в столбце Optimal, двойным кликом меняем значение параметров:
    * "Package C State limit" на "C2 state"
    * "CPU C3 report" на "Enable"
    * "CPU C6 report" на "Disable"
10. Закрываем окно AMIBCP и соглашаемся на сохранение внесённых изменений
11. В S3TurboTool нажимаем "Собрать драйвер"
12. Настраиваем необходимые значения отрицательных смещений напряжения и нажимаем "Собрать драйвер"
13. В S3TurboTool нажимаем UEFITool
14. В появившейся утилите UEFITool открываем биос
15. Раскрываем список и идём по пути "Intel image > BIOS region > 8C8CE578-...(самый нижний) >"
16. Примерно среди первых 20 значений находим 271DD6F2-...
17. Правый клик по нему, выбираем "Replace as is...", выбираем собранный ранее драйвер (находится в папке S3TurboHack)
18. Выбираем "File > Save image file...", сохраняем
#### На этом биос готов к прошивке

При возникновении трудностей, а также если у Вас есть замечания и пожелания, обращайтесть в Telegram-группу https://t.me/chinese_lga2011_3_x99
