## Laboratory work II

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**
 
## Tutorial

```bash
$ export GITHUB_USERNAME=<имя_пользователя>
$ export GIST_TOKEN=<сохраненный_токен>
$ alias edit=<nano|vi|vim|subl>
```

```ShellSession
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
$ cd ..
$ pwd
```

```ShellSession
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```ShellSession
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```ShellSession
$ ls node/bin 
$ echo ${PATH}
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```ShellSession
$ npm install -g gistup
$ ls node/bin
```

```ShellSession
$ cat > ~/.gistup.json <<EOF
{
  "token": "${GIST_TOKEN}"
}
EOF
```

## Report

```ShellSession
$ export LAB_NUMBER=02
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}" # enter: yes↵
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix)) - объединяет группу файлов в один архивный файл.
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix)) - последовательное чтения файлов и их вывода в стандартный поток.
- [cd](https://en.wikipedia.org/wiki/Cd_(command)) - перемещение текущими раьочими директориями.
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix)) - команда для копирования файлов и каталогов.
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix)) - команда, которая используется для извлечения из файла нужную часть.
- [echo](https://en.wikipedia.org/wiki/Echo_(command)) - команда используемая для вывода строки на экран или в файл.
- [env](https://en.wikipedia.org/wiki/Env_(shell)) - команда выводит на печать список переменных окружения или запускает другую программу в измененной среде без необходимости изменения существующих условий.
- [ex](https://en.wikipedia.org/wiki/Ex_(editor)) - текстовый онлайн редактор
- [file](https://en.wikipedia.org/wiki/File_(command)) - используется для распознавания типа данных, содержащихся в файлах компьютера.
- [find](https://en.wikipedia.org/wiki/Find) - поиск файлов.
- [ls](https://en.wikipedia.org/wiki/Ls) - выдпет список файлов в текущей рабочей директории.
- [man](https://en.wikipedia.org/wiki/Man_page) - предназначена для форматирования справочных страниц.
- [mkdir](https://en.wikipedia.org/wiki/Mkdir) -  используется для создания нового каталога.
- [mv](https://en.wikipedia.org/wiki/Mv) - команда, которая перемещает один или несколько файлов или каталогов из одного места в другое.
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix)) - используется для проверки файлов и для отображения их содержимого.
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix)) - отображение текущих процессов. 
- [pwd](https://en.wikipedia.org/wiki/Pwd) - выводит полный путь к текущемк рабочему каталогу в поток стандартного вовода.
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix)) - одна из основных команд для удаления таких объектов, как файлы, каталоги, устройства, узлы, символические ссылки, и т. д. из файловой системы. 
- [sed](https://en.wikipedia.org/wiki/Sed) - утилита, которая анализирует и преобразует текст.
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix)) - используется для изменения даты и доступа или изменения даты файла или каталога. 

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru) - менеджеры управления программных пакетов
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh) - установщики программных пакетов
- [npm](https://docs.npmjs.com) - менеджер работы с пакетами JavaScript

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details) - кроссплатформенная служебная программа командной строки, позволяющая взаимодействовать с множеством различных серверов по множеству различных протоколов 
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf) - свободная неинтерактивная консольная программа для загрузки файлов по сети.
- [clang](https://clang.llvm.org) - является фронтендом для языков программирования C, C++, Objective-C, Objective-C++ и OpenCL C
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html) - компилятора языка C++ (GNU C++).
- [make](https://en.wikipedia.org/wiki/Make_(software)) - инструмент, который автоматически создает исполняемые программы и библиотеки из исходных кодов.
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html) - открывает файл.
- [openssl](https://www.openssl.org) - Криптографический пакет с открытым исходным кодом для работы с SSL/TLS. Позволяет создавать ключи и сертификаты, подписывать их, формировать CSR и CRT. Также имеется возможность шифрования данных и тестирования SSL/TLS соединений.
- [nano](https://www.nano-editor.org) - кончольный текстовый редактор Unix.
- [tree](https://linux.die.net/man/1/tree) - программа создания рекурсивного каталога.
- [vim](http://www.vim.org) - текстовый редактор.

```
Copyright (c) 2017 Братья Вершинины
```
