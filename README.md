# ADFI
**ADFI** - Утилита для поиска в сети устройств, использующих стандартные логин/пароль для доступа по telnet. <br/>
**Текущая версия:** 1.0 <br/>
**Дисклеймер:**
данная утилита была создана в образовательных целях. Автор не несет ответственности за ущерб, причененный пользователем при ее использовании.

**Функционал, который есть сейчас:** <br/>
- поиск со связкой логин:admin пароль:admin. <br/>
- диапазон ip-фдресов можно указать как через параметр, так и через файл <br/>
- можно указать файл для записи ip-адресов найденных устройств <br/>

**Функционал, который планируется добавить к следующему релизу:** <br/>
- возможность указать свой словарь логинов и паролей <br/>
- возможность создать список ip-адресов и обновлять его раз в определенный период времени <br/>

**Установка зависимостей:**

    sudo apt-get update
    apt-get install telnet nmap expect

**Использование:**

    ./adfi <параметры>
        -a диапазон ip-адресов для поиска
        -i файл со списком ip-адресов для сканирования
        -o файл для записи ip-адресов найденных устройс

Если одновременно указать диапазон адресов через параметр и файл с диапазонами адресов, то сперва просканируется диапазон, указанный в параметре, а за тем диапазоны, указанные в файле. В репозитории есть пример файла (testlist.txt). Диапазоны ip-адресов можно задавать через диапазоны в октетах, или в формате CIDR <br/>
Пример:

    208.142.0-255.0-255
    208.142.0.0/16
    
**Примеры запуска:**

    ./adfi -a 192.168.0.0/24
    ./adfi -i ./test_list.txt -o ./result
    ./adfi -a 192.168.0.0-255 -i ./test_list.txt -o ./result
  



# Google translate:

**ADFI** - Utility to search the network for devices using standard login / password for telnet access. <br/>
**Current version:** 1.0 <br/>
**Disclaimer:**
this utility was created for educational purposes. The author does not bear responsibility for the damage caused by the user when using it.

**Functionality, which is now:** <br/>
- search with a binder login: admin password: admin. <br/>
- The range of ip-addresses can be specified both through the parameter and through the file <br/>
- You can specify a file to write ip-addresses of found devices <br/>

**Functionality to be added to the next release:** <br/>
- the ability to specify your own dictionary of logins and passwords <br/>
- the ability to create a list of ip-addresses and update it once in a certain period of time <br/>

**Setting dependencies:**

    sudo apt-get update
    apt-get install telnet nmap expect

**Using:**

    ./adfi <options>
        -a range of ip-addresses for search
        -i file with a list of ip-addresses for scanning
        -o file for writing ip-addresses of found devices

If you specify a range of addresses using a parameter and a file with address ranges, the range specified in the parameter is scanned first, and then the ranges specified in the file are scanned. In the repository, there is an example file (testlist.txt). Ranges of ip-addresses can be specified through ranges in octets, or in CIDR format <br/>
Example:

    208.142.0-255.0-258
    208.142.0.0/16
    
**Launch examples:**

    ./adfi -a 192.168.0.0/24
    ./adfi -i ./test_list.txt -o ./result
    ./adfi -a 192.168.0.0-255 -i ./test_list.txt -o ./result
    
This utility was created for educational purposes. The author does not bear responsibility for the damage caused by the user when using it.
    

