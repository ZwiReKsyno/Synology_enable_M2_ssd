# Включите M.2 PCIe в Synology NAS

### Описание
Enable Synology M.2 PCIe cards in Synology NAS that don't officially support them
Включите карты Synology M.2 PCIe в Synology NAS, которые официально их не поддерживают.

Позволяет использовать карты E10M20-T1, M2D20, M2D18 или M2D17 в моделях Synology NAS, которых нет в [списке поддерживаемых моделей ](https://github.com/007revad/Synology_enable_M2_volume/wiki/Models-that-support-PCIe-M.2-cards).

  - Enables E10M20-T1, M2D20, M2D18 or M2D17 for DS1821+, DS1621+.
  - Enables M2D18 and M2D17 for DS1823xs+, DS2422+, RS2423+, RS2421+, RS2421RP+, RS2821RP+.
  - Enables M2D18 and M2D17 for RS822RP+, RS822+, RS1221RP+ and RS1221+ using DSM 7.1.1 and older.
  - May enable E10M20-T1, M2D20, M2D18 and M2D17 for other models with a PCIe x8 slot that have /usr/syno/synonvme.

[Synology HDD db](https://github.com/007revad/Synology_HDD_db) теперь позволяет использовать Storage Manager для создания томов на дисках M.2 на карте адаптера PCIe M.2.

<br>

## На каких моделях Synology это будет работать?

</br>**Работает на следующих моделях:**

<details>
  <summary>Нажмите здесь, чтобы увидеть список</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| DS1821+   | yes | yes | yes | yes | |
| DS1621+   | yes | yes | yes | yes | |
| DS1823xs+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| DS2422+   | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| | | | | |
| RS2423+   | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2423RP+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2421+   | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2421RP+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS2821RP+ | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| RS822+    | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| RS822RP+  | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| RS1221+   | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| RS1221RP+ | yes | yes | yes | yes | M2D18 already enabled in DSM 7.2 |
| | | | | |
| **другие** | maybe | maybe | maybe | maybe | See Other Models Notes |

**Примечания к другим моделям** 
- Synology должен иметь слот PCIe x8.
- DSM должен включать /usr/syno/bin/synonvme.
- DSM должен включать /usr/lib/libsynonvme.so.1.

</details>

</br>**Должно работать для следующих моделей:**

<details>
  <summary>Нажмите здесь, чтобы увидеть список</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| FS2500    | yes | yes | yes | yes | |
| FS3410    | yes | yes | yes | yes | |
| FS6400    | yes | yes | yes | yes | |
| | | | | |
| HD6500    | yes | yes | yes | yes | |
| | | | | |
| SA4310    | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| SA3610    | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |
| SA6400    | yes | yes | yes | yes | E10M20-T1	and M2D20 already enabled in DSM |

</details>

</br>**Модели Synology NAS, возможно будет работать этот сценарий**

<details>
  <summary>Нажмите здесь, чтобы увидеть список</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| DS1621xs+ | ???  | ??? | ???  | ??? |  |

</details>

</br>**Модели Synology NAS, на которых этот сценарий не работает:**

<details>
  <summary>Нажмите здесь, чтобы увидеть список</summary>

| Model | E10M20-T1 | M2D20 | M2D18 | M2D17 | Notes |
|-|-|-|-|-|-|
| DS923+     | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| DS723+     | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| DS1522+    | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| RS422+     | no  | no  | no  | no | PCIe x2 slot only fits the E10G22-T1-Mini |
| | | | | |
| DS1817+    | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| DS1517+    | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| | | | | |
| RS1219+    | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| RS818+     | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| RS818RP+   | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| RS3617xs   | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| RS18016xs+ | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |
| | | | | |
| FS3017     | no  | no  | no  | no | Does not have /usr/syno/bin/synonvme |

</details>

<br>

## Как запустить скрипт

### Скачать сценарий
1. [Загрузите исходный код последней версии .zip](https://github.com/ZwiReKsyno/Synology_enable_M2_ssd/raw/main/syno_enable_m2_card.7z)
2. Сохраните загруженный zip-файл в папку на Synology
    - НЕ сохраняйте сценарий на томе M.2. После обновления DSM или Storage Manager том M.2 не будет доступен до тех пор, пока не запустится сценарий.
3. Разархивируйте zip-файл.

### Запуск скрипта через SSH

[Как включить SSH и войти в DSM через SSH](https://kb.synology.com/en-global/DSM/tutorial/How_to_login_to_DSM_with_root_permission_via_SSH_Telnet)

**Примечание:** амените /volume1/scripts/ путем к расположению сценария. Запустите сценарий и перезагрузите Synology:
Run the script then reboot the Synology:
```YAML
sudo -s /volume1/scripts/syno_enable_m2_card.sh
```

**Параметры:**
```YAML
  -c, --check           Check M.2 card status
  -r, --restore         Restore from backups to undo changes
  -e, --email           Disable colored text in output scheduler emails.
      --autoupdate=AGE  Auto update script (useful when script is scheduled)
                        AGE is how many days old a release must be before
                        auto-updating. AGE must be a number: 0 or greater
      --model=CARD      Automatically enable specified card model
                        Required if you want to schedule the script
                        CARD can be E10M20-T1, M2D20, M2D18 or M2D17
  -h, --help            Show this help message
  -v, --version         Show the script version
```

### А как насчет обновлений DSM?

После любого обновления DSM вам нужно будет снова запустить этот сценарий.

### Запланируйте запуск сценария при завершении работы

Или вы можете запланировать запуск Synology_enable_M2_card при выключении Synology, чтобы не забывать запускать сценарий после обновления DSM.

См. <a href=how_to_schedule.md/>раздел «Как запланировать сценарий в Synology Task Scheduler».</a>

</br>

## Скриншоты

<p align="center">Доступные Варианты</p>
<p align="center"><img src="/images/help.png"></p>

<p align="center">Проверка текущих настроек карты M.2</p>
<p align="center"><img src="/images/edited.png"></p>

<p align="center">Checking the current M.2 card settings</p>
<p align="center"><img src="/images/check.png"></p>

<p align="center">E10M20-T1 already enabled</p>
<p align="center"><img src="/images/e10m20.png"></p>

<p align="center">Восстановление исходных настроек карты M.2</p>
<p align="center"><img src="/images/all.png"></p>

<p align="center">Restoring the original M.2 card settings</p>
<p align="center"><img src="/images/restore.png"></p>


<p align="center">DS1821+ with a E10M20-T1</p>
<p align="center"><img src="/images/1821_e10m20-1.png"></p>

<p align="center"><img src="/images/1821_e10m20-2.png"></p>
