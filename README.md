
# Table of Contents

1.  [Quick history](#orgf4db547)
2.  [Command line](#org33ea492)
    1.  [打印文本第一行](#orgc731c8e)
    2.  [获取文本最后一列](#org983c1d6)
    3.  [Delete all broken soft link](#org8cb78bf)
    4.  [Rotate a image](#org4068033)
    5.  [Nohup to file and console](#orgf1a7afb)
    6.  [检验文件或者文件夹是否存在](#org3e5d827)
        1.  [判断文件是否存在](#org6253061)
        2.  [判断文件夹是否存在](#org4e08192)
        3.  [判断软链接存在并且可用虽](#org5f5255e)
        4.  [判断文件夹不存在](#orgffb70f3)
    7.  [获取本机ip](#org1aff9fb)
    8.  [Delete file expect few files](#org479ce24)
    9.  [Sync file from source to target increment](#orgaed191f)
    10. [How to get Maven project version from cmd](#orgd0d6ce2)
    11. [Maven use alternative repo](#orgcbebf8a)
    12. [Scp with port](#org8422adf)
    13. [Check url exist](#org0152f6d)
        1.  [Method1](#orgc3e3557)
        2.  [Method2](#org7449021)
    14. [Get host ip](#org7ab5047)
    15. [Generate short link](#org2923f1e)
    16. [Get weather](#orgb64e654)
    17. [Pass passphrase to gpg](#org0c49f3f)
    18. [Where xhost](#org44346e5)
    19. [Display custom date](#orgf44114a)
    20. [Extract filename and extension from file](#orgcaa64f6)
    21. [Truncate file](#org460380d)
        1.  [In-place](#org52b5f2a)
        2.  [New file](#org6caa81d)
    22. [Cut file](#orga2b6cc5)
3.  [Emacs](#orgef0767a)
    1.  [给Emacs文档增加目录](#org1646aac)
    2.  [Add command to keyboard macro](#org0645a9e)
    3.  [Set major mode on file](#org2c96e83)
    4.  [Add minor mode on file](#org6980b6b)
    5.  [Straight use builtin org](#org53dc0fd)
    6.  [Delete blank line](#orgad7f3f8)
    7.  [Insert file contents to org source area](#org525ee6d)
    8.  [Add note to blog](#org081e8c2)
    9.  [Yas add custom style date](#orge9e3787)
    10. [Change org babel export language](#org5447d00)
    11. [Ignore error info](#orgcbee27a)
    12. [Org babel python output always Nono](#org62cccbc)
    13. [Handle swiper search result](#org46c9a35)
    14. [Change org reveal font color](#org2768f43)
    15. [So-long mode](#org21e9d17)
    16. [Trim changed line white space](#org825d30b)
    17. [Open chrome-extension: prefix url](#org038235c)
4.  [Git](#org41919fe)
    1.  [查看git配置的来源](#org8d239bf)
    2.  [删除大于指定大小的仓库信息](#org70f54a9)
    3.  [Rebase user info](#orga729fbd)
    4.  [Migrate code to new origin](#org30fde12)
    5.  [Remove untracked file](#org5a43291)
    6.  [How to clone git repo wiki](#orgd2a9952)
        1.  [clone today<sub>i</sub><sub>learn</sub> repo](#org38cb9d5)
        2.  [clone today<sub>i</sub><sub>learn</sub> repo wiki](#org35072f8)
5.  [Github](#org2ebb007)
    1.  [Add profile page to github](#orga134fc8)
    2.  [Github emoji shortcode](#orgdf06acf)
6.  [JAVA](#org55f3100)
    1.  [How to judge byte[] is compressed with gzip](#orgd31a047)
    2.  [Jenv export java<sub>home</sub>](#org1c1398c)
    3.  [Iterable to list](#org2c43599)
    4.  [JVM](#org0e40191)
        1.  [Show java program jvm params](#org50a00af)
        2.  [Why set -XX:NativeMemoryTracking=detail got ative memory tracking is not enabled](#org94861cb)
    5.  [Get two date interval days by java8](#orge720a07)
    6.  [Convert Milliseconds to LocalDateTime](#orga382fe7)
    7.  [Convert LocalDate to Milliseconds](#org9198e33)
    8.  [com.google.protobuf.GeneratedMessageV3.isStringEmpty not found](#org5a892a2)
    9.  [Get returntype by aspectj joinpoint](#org2d73142)
    10. [SpringFlux+Netty config access log](#orge4998da)
        1.  [add netty system param](#orgd0d01d2)
        2.  [config log4j for access log](#org79e2cb8)
7.  [Spring](#orgff3d7cc)
    1.  [How to get handleMethod from webflux](#orgf34ff3d)
    2.  [Spring profie effect scope](#orgd607b72)
8.  [KM](#org0a9b504)
    1.  [How to show km error log](#orgd460c0f)
9.  [Python](#org5bc43a4)
    1.  [python with git](#orgbad85ba)
    2.  [python with clipboard](#org1c9c737)
    3.  [python urldecode](#org459e809)
    4.  [python with cross-platform home directory](#orgf657830)
    5.  [python set to string](#org7cc9d8b)
    6.  [python decimal to binary](#org50acdaa)
10. [Brew](#org48271e0)
    1.  [get installed program path](#orgdc5b2a9)
    2.  [handle rebase-apply error](#org5022d16)
    3.  [Make brew python and pyenv togehter](#orgbf9c01b)
    4.  [fixed font exists in multiple taps](#orga52325d)
    5.  [Clean brew cache](#org78e99d9)
11. [MAC](#org0d2af86)
    1.  [del macOS Xcode CoreSimulator folder](#orgb377070)
    2.  [Brew mysql install connect issue](#orgccd0ac5)
    3.  [Mount/unmount smbs](#orga460f99)
    4.  [Get running app](#org6ecd8f8)
    5.  [Reset macos accessibility](#org5e61e92)
12. [Linux](#org59e7b2d)
    1.  [Change default program](#orgb469e8e)
    2.  [SSH paswordless with public key authentication](#org97a99d0)
        1.  [Generate key from host](#org2d41990)
        2.  [Scp to dest machine](#org821a34e)
        3.  [Add pub key to dest machine auth key](#orgc45101d)
    3.  [Man with color](#org4b792ca)
13. [Mysql](#orgd9d2821)
    1.  [Show db table create/update time](#orgf2d5d26)
14. [IDEA](#orgd2db230)
    1.  [Use alt key quickly on commit window](#org077ee39)
15. [Convert vvt to srt](#org039ed84)
16. [JACKSON](#org00a488a)
    1.  [JsonNode to class](#org27eab3f)
    2.  [Json to Map](#org0cbc032)
    3.  [Unwarp map](#org979bf3c)
17. [Redis](#orgb668efa)
    1.  [Batch del key](#orge7f2d98)
    2.  [Find big key](#org7e55488)
18. [Nginx](#orge6307a5)
    1.  [underscore header issue](#orgde50d94)
19. [Wexin develop](#orgac7f627)
    1.  [微信模板消息换行 - Jinx - CSDN博客](#orgb68cb47)
    2.  [微信公众号开发者模式回复信息带表情（QQ，emoji） - X<sub>hazel的博客</sub> - CSDN博客](#org2d81a5d)
20. [JS](#org2d9fa47)
    1.  [Get table td content](#org1e02dba)



<a id="orgf4db547"></a>

# [Quick history](https://github.githistory.xyz/peng051410/today_i_learn/blob/main/README.org)


<a id="org33ea492"></a>

# Command line


<a id="orgc731c8e"></a>

## 打印文本第一行

    awk 'NR==1{print}' filename


<a id="org983c1d6"></a>

## 获取文本最后一列

主要是$NF

    awk -F ',' '{print $NF}'


<a id="org8cb78bf"></a>

## Delete all broken soft link

    find -L . -name . -o -type d -prune -o -type l -exec rm {} +


<a id="org4068033"></a>

## Rotate a image

    function ro() {
        szFile=$1
        convert $1 -rotate 90 $(basename "$szFile").png
    }


<a id="orgf1a7afb"></a>

## Nohup to file and console

    nohup ./program  > Output.txt | tail -F Output.txt &


<a id="org3e5d827"></a>

## 检验文件或者文件夹是否存在


<a id="org6253061"></a>

### 判断文件是否存在

    if [ -e x.txt ]
    then
        echo "ok"
    else
        echo "nok"
    fi


<a id="org4e08192"></a>

### 判断文件夹是否存在

    if [ -d folder1 ]
    then
        echo "ok"
    else
        echo "nok"
    fi


<a id="org5f5255e"></a>

### 判断软链接存在并且可用虽

    [ -L ${my_link} ] && [ -e ${my_link} ]


<a id="orgffb70f3"></a>

### 判断文件夹不存在


<a id="org1aff9fb"></a>

## 获取本机ip

    ifconfig | grep -Eo 'inet (addr:)?([0-9]*\.){3}[0-9]*' | grep -Eo '([0-9]*\.){3}[0-9]*' | grep -v '127.0.0.1'
    # linux only
    hostname -i


<a id="org479ce24"></a>

## Delete file expect few files

    rm -v !("filname1"|"file2")


<a id="orgaed191f"></a>

## Sync file from source to target increment

    rsync -av Documents/* /tmp/documents


<a id="orgd0d6ce2"></a>

## How to get Maven project version from cmd

    mvn -q -Dexec.executable=echo -Dexec.args='${project.artifactId}' --non-recursive exec:


<a id="orgcbebf8a"></a>

## Maven use alternative repo

    mvn -DaltDeploymentRepository=repoid::default::http://ip/nexus/content/repositories/releases clean source:jar-no-fork deploy


<a id="org8422adf"></a>

## Scp with port

    scp -P 2222 file host@localhost:~/linux-study


<a id="org0152f6d"></a>

## Check url exist


<a id="orgc3e3557"></a>

### Method1

    url=http://www.baidu.co
    if wget --spider $url 2>/dev/null; then
      echo "File exists"
    else
      echo "File does not exist"
    fi


<a id="org7449021"></a>

### Method2

    url=http://www.baidu.co
    if wget -q --method=HEAD $url;
     then
      echo "This page exists."
     else
      echo "This page does not exist."
    fi


<a id="org7ab5047"></a>

## Get host ip

    curl ipaddy.net


<a id="org2923f1e"></a>

## Generate short link

    curl -s 'tinyurl.com/api-create.php?url=http://www.baidu.com'


<a id="orgb64e654"></a>

## Get weather

    curl wttr.in


<a id="org0c49f3f"></a>

## Pass passphrase to gpg

[shell script - gpg asks for password even with &#x2013;passphrase - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/60213/gpg-asks-for-password-even-with-passphrase)

    gpg -c --batch --passphrase 1234 -o file.gpg


<a id="org44346e5"></a>

## Where xhost

[x11 - xhost on MacOS Catalina - Ask Different](https://apple.stackexchange.com/questions/378348/xhost-on-macos-catalina)

    /opt/X11/bin/xhost


<a id="orgf44114a"></a>

## Display custom date

显示3小时之前的时间

    date -d '3 hours ago' +"%Y-%m-%d %T"
    # another way
    date -d "-3 Hours" "+%Y-%m-%d %T"


<a id="orgcaa64f6"></a>

## Extract filename and extension from file

<https://stackoverflow.com/questions/965053/extract-filename-and-extension-in-bash?page=1&tab=scoredesc#tab-top>

    fullfile=~/Downloads/main-webapp_log_Onl_jar_backend.yml
    filename=$(basename -- "$fullfile")
    extension="${filename##*.}"
    filename="${filename%.*}"
    echo "filanme is $filename, file extendsion is $extension"


<a id="org460380d"></a>

## Truncate file

truncate file only retain 10 line


<a id="org52b5f2a"></a>

### In-place

    sed -i.bak '11,$ d' myfile.txt


<a id="org6caa81d"></a>

### New file

    head -n10 myfile.txt > myfile.txt.bak

<https://stackoverflow.com/questions/19017994/how-do-i-limit-or-truncate-text-file-by-number-of-lines>


<a id="orga2b6cc5"></a>

## Cut file

    echo "hello world" | cut -b 2-5

    ello


<a id="orgef0767a"></a>

# Emacs


<a id="org1646aac"></a>

## 给Emacs文档增加目录

给Entry增加标签 =:TOC:=，限定目录层级#+OPTIONS: toc:1


<a id="org0645a9e"></a>

## Add command to keyboard macro

<https://www.gnu.org/software/emacs/manual/html_node/emacs/Basic-Keyboard-Macro.html>
C-u f3 能执行macro直接到按下f4


<a id="org2c96e83"></a>

## Set major mode on file

<https://www.gnu.org/software/emacs/manual/html_node/emacs/Choosing-Modes.html>

    ;; set major mode, with this, other set will be ignore
    ; -*-Lisp-*-


<a id="org6980b6b"></a>

## Add minor mode on file

    ; -*- eval: (rainbow-mode) -*-


<a id="org53dc0fd"></a>

## Straight use builtin org

将下面的配置加到straight配置前

    (straight-use-package '(org :type built-in))


<a id="orgad7f3f8"></a>

## Delete blank line

<https://www.masteringemacs.org/article/removing-blank-lines-buffer>

    M-x flush-lines RET ^$ RET


<a id="org525ee6d"></a>

## Insert file contents to org source area

In src area, run **C-x i**

    grep 'cool thing' ~/Donwnloads


<a id="org081e8c2"></a>

## Add note to blog

1.  \#+STARTUP: logdrawer
2.  在需要加note的item执行 **C-c C-z**


<a id="orge9e3787"></a>

## Yas add custom style date

[Insert current date with yasnippet - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/27158/insert-current-date-with-yasnippet)

    `(format-time-string "%Y-%m-%d")`$0


<a id="org5447d00"></a>

## Change org babel export language

[How to change the language of a result of ":results output code" in emacs org-mode - Stack Overflow](https://stackoverflow.com/questions/68085596/how-to-change-the-language-of-a-result-of-results-output-code-in-emacs-org-mo)

    /Users/tomyli/github/today_i_learn


<a id="orgcbee27a"></a>

## Ignore error info

    (condition-case nil
        (progn
          (message "hello")
        t)
      (error nil)


<a id="org62cccbc"></a>

## Org babel python output always Nono

[Python org-mode source block output is always ': None' - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/17926/python-org-mode-source-block-output-is-always-none)
Can use **return** or add **:results output**


<a id="org46c9a35"></a>

## Handle swiper search result

Ctrl+s搜索后，再按 **Ctrl+c Ctrl+o** 打开处理结果的buffer


<a id="org2768f43"></a>

## Change org reveal font color

[org mode - Change font color on a `org-reveal` slide - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/38532/change-font-color-on-a-org-reveal-slide)

1.  Add header

    #+MACRO: color @@html:<font color="$1">$2</font>@@

1.  Use macro

    {{{color(red, 基于2019.1版本.)}}}


<a id="org21e9d17"></a>

## So-long mode

When a file very big, [so-long](https://elpa.gnu.org/packages/so-long.html) mode can fixed it


<a id="org825d30b"></a>

## Trim changed line white space

<https://github.com/redguardtoo/emacs.d/issues/1014>
Emacs has an minor mode called [ws-butler-mode](https://github.com/lewang/ws-butler) can trim white space only with changed line.


<a id="org038235c"></a>

## Open chrome-extension: prefix url


<a id="org41919fe"></a>

# Git


<a id="org8d239bf"></a>

## 查看git配置的来源

在正常工作中会针对不同的工作目录设置不同的配置，可以根据以下命令来确认当前仓库使用的配置来源

    git config --show-origin --get user.email


<a id="org70f54a9"></a>

## 删除大于指定大小的仓库信息

迁移仓库时遇到异常，提示镜像文件大于了100M，无法操作，经同事帮助找到此工具，减少仓库信息没得说

    bfg --strip-blobs-bigger-than 100M some-big-repo.git


<a id="orga729fbd"></a>

## Rebase user info

    git rebase -i "commit id"
    # pick to edit then save change
    git commit --amend --author="{username} <{email}>" --no-edit
    git rebase --continue
    git push


<a id="org30fde12"></a>

## Migrate code to new origin

    git clone --mirror <url_of_old_repo>
    git remote add new-origin <url_of_new_repo>
    git push new-origin --all


<a id="org5a43291"></a>

## Remove untracked file

    git clean -xf

交互式的进行删除

    git clean -i


<a id="orgd2a9952"></a>

## How to clone git repo wiki

add .wiki after repo


<a id="org38cb9d5"></a>

### clone today<sub>i</sub><sub>learn</sub> repo

    git clone https://github.com/peng051410/today_i_learn


<a id="org35072f8"></a>

### clone today<sub>i</sub><sub>learn</sub> repo wiki

    git clone https://github.com/peng051410/today_i_learn.wiki


<a id="org2ebb007"></a>

# Github


<a id="orga134fc8"></a>

## Add profile page to github

<https://twitter.com/tomylitoo/status/1580396505118441472>
Create a repositoy with name same to github name.


<a id="orgdf06acf"></a>

## Github emoji shortcode

<https://github.com/ikatyang/emoji-cheat-sheet>


<a id="org55f3100"></a>

# JAVA


<a id="orgd31a047"></a>

## How to judge byte[] is compressed with gzip

    private boolean isCompressed(byte[] bytes) {
        if ((bytes == null) || (bytes.length < 2)) {
            return false;
        } else {
            return ((bytes[0] == (byte) (GZIPInputStream.GZIP_MAGIC)) && (bytes[1] == (byte) (GZIPInputStream.GZIP_MAGIC
                    >> 8)));
        }
    }


<a id="org1c1398c"></a>

## Jenv export java<sub>home</sub>

    jenv enable-plugin export


<a id="org2c43599"></a>

## Iterable to list

    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-collections4</artifactId>
        <version>4.4</version>
    </dependency>

    IterableUtils.toList(list);


<a id="org0e40191"></a>

## JVM


<a id="org50a00af"></a>

### Show java program jvm params

    jcmd 2886 VM.flags


<a id="org94861cb"></a>

### Why set -XX:NativeMemoryTracking=detail got ative memory tracking is not enabled

Os security, must execute with root
[java - Why JCMD throws "native memory tracking is not enabled" message even though NMT is enabled? - Stack Overflow](https://stackoverflow.com/questions/42295509/why-jcmd-throws-native-memory-tracking-is-not-enabled-message-even-though-nmt)


<a id="orge720a07"></a>

## Get two date interval days by java8

[Calculate days between two Dates in Java 8 - Stack Overflow](https://stackoverflow.com/questions/27005861/calculate-days-between-two-dates-in-java-8)

    LocalDate today = LocalDate.now()
    LocalDate yesterday = today.minusDays(1);
    Duration.between(today.atStartOfDay(), yesterday.atStartOfDay()).toDays() // another option


<a id="orga382fe7"></a>

## Convert Milliseconds to LocalDateTime

    long millis = 1614926594000L; // UTC Fri Mar 05 2021 06:43:14
    LocalDate dateTime = Instant.ofEpochMilli(millis)
            .atZone(ZoneId.systemDefault()) // default zone
            .toLocalDate(); // returns actual LocalDate object


<a id="org9198e33"></a>

## Convert LocalDate to Milliseconds

    ocalDate dateTime1 = LocalDate.of(2021, 3, 5);
    long seconds = dateTime1.atStartOfDay(ZoneId.systemDefault())
            .toEpochSecond(); // returns seconds
    long millis1 = seconds * 1000; // seconds to milliseconds


<a id="org5a892a2"></a>

## com.google.protobuf.GeneratedMessageV3.isStringEmpty not found

need import protobuf-java dependency

    <dependency>
      <groupId>com.google.protobuf</groupId>
      <artifactId>protobuf-java</artifactId>
      <version>3.19.1</version>
    </dependency>


<a id="org2d73142"></a>

## Get returntype by aspectj joinpoint

    Method method = ((MethodSignature) proceedingJoinPoint.getSignature()).getMethod();
    Class<?> returnType = method.getReturnType();

    //or
    Class<?> returnType1 = ((MethodSignature) proceedingJoinPoint.getSignature()).getReturnType();


<a id="orge4998da"></a>

## SpringFlux+Netty config access log


<a id="orgd0d01d2"></a>

### add netty system param

    -Dreactor.netty.http.server.accessLogEnabled=true


<a id="org79e2cb8"></a>

### config log4j for access log

    <RollingFile name="RollingFileAccess"
                 fileName="${sys:logPath}/access.log"
                 filePattern="${sys:logPath}/access.log.%d{yyyy-MM-dd_HH}.gz">
      <ThresholdFilter level="INFO"/>
      <PatternLayout>
        <pattern>%d{HH:mm:ss.SSS} %-5level %class{36} %L %M - %msg%xEx%n</pattern>
      </PatternLayout>
      <Policies>
        <TimeBasedTriggeringPolicy/>
      </Policies>
    </RollingFile>

    <Logger name="reactor.netty.http.server.AccessLog" level="info" additivity="false">
      <AppenderRef ref="RollingFileAccess"/>
    </Logger>


<a id="orgff3d7cc"></a>

# Spring


<a id="orgf34ff3d"></a>

## How to get handleMethod from webflux

1.  inject handleMapping
2.  you got it!

    (HandlerMethod) this.handlerMapping.getHandler(serverWebExchange).toProcessor().peek();


<a id="orgd607b72"></a>

## Spring profie effect scope

Profiles affect only bean creation, not method.


<a id="org0a9b504"></a>

# KM


<a id="orgd460c0f"></a>

## How to show km error log

    tail -f ~/Library/Logs/Keyboard\ Maestro/Engine.log


<a id="org5bc43a4"></a>

# Python


<a id="orgbad85ba"></a>

## python with git

    pip3 install GitPython


<a id="org1c9c737"></a>

## python with clipboard

    pip3 install pyperclip


<a id="org459e809"></a>

## python urldecode

    from urllib.parse import unquote
    url = unquote(url)


<a id="orgf657830"></a>

## python with cross-platform home directory

[python - What is a cross-platform way to get the home directory? - Stack Overflow](https://stackoverflow.com/questions/4028904/what-is-a-cross-platform-way-to-get-the-home-directory)

    from pathlib import Path
    home = str(Path.home())
    print(home)


<a id="org7cc9d8b"></a>

## python set to string

    s = {'a', 'b'}
    str = ', '.join(s)
    print(str)


<a id="org50acdaa"></a>

## python decimal to binary

<https://stackoverflow.com/questions/3528146/convert-decimal-to-binary-in-python>

    abinary = bin(1024)
    print(abinary)


<a id="org48271e0"></a>

# Brew


<a id="orgdc5b2a9"></a>

## get installed program path

    (brew --prefix go)


<a id="org5022d16"></a>

## handle rebase-apply error

    brew update-reset


<a id="orgbf9c01b"></a>

## Make brew python and pyenv togehter

    ln -s $(brew --cellar python)/* ~/.pyenv/versions/


<a id="orga52325d"></a>

## fixed font exists in multiple taps

[How can I fix Error: font exists in multiple taps ? · Issue #59227 · Homebrew/homebrew-cask](https://github.com/Homebrew/homebrew-cask/issues/59227)

    brew untap caskroom/fonts
    brew tap homebrew/cask-fonts
    brew cask install font-hack-nerd-font


<a id="org78e99d9"></a>

## Clean brew cache

    brew cleanup -s


<a id="org0d2af86"></a>

# MAC


<a id="orgb377070"></a>

## del macOS Xcode CoreSimulator folder

    xcrun simctl delete unavailable


<a id="orgccd0ac5"></a>

## Brew mysql install connect issue

因为有老的mysql数据没有清理完全，执行完以下操作后，重新安装即可

    sudo rm -rf /usr/local/var/mysql


<a id="orga460f99"></a>

## Mount/unmount smbs

    sudo mount -t smbfs '//vagrant:vagrant@localhost:10139/kernel-source' /Volumes
    unmont kernel-source


<a id="org6ecd8f8"></a>

## Get running app

    osascript -e 'tell application "System Events" to get name of (processes where background only is false)'


<a id="org5e61e92"></a>

## Reset macos accessibility

    sudo tccutil reset Accessibility


<a id="org59e7b2d"></a>

# Linux


<a id="orgb469e8e"></a>

## Change default program

    update-alternatives --set java java-11-openjdk.x86_64

You can issue java path by

    update-alternatives --config java


<a id="org97a99d0"></a>

## SSH paswordless with public key authentication


<a id="org2d41990"></a>

### Generate key from host

    ssh-keygen -t rsa


<a id="org821a34e"></a>

### Scp to dest machine

    scp .ssh/id_rsa.pub user@host:.


<a id="orgc45101d"></a>

### Add pub key to dest machine auth key

    cat id_rsa.pub >> .ssh/authorized_keys


<a id="org4b792ca"></a>

## Man with color

[Colored \`man\` pages on OSX](https://gist.github.com/supermarin/6dca255da372c3f9eb26)

    man() {
        env \
            LESS_TERMCAP_mb=$(printf "\e[1;31m") \
            LESS_TERMCAP_md=$(printf "\e[1;31m") \
            LESS_TERMCAP_me=$(printf "\e[0m") \
            LESS_TERMCAP_se=$(printf "\e[0m") \
            LESS_TERMCAP_so=$(printf "\e[1;44;33m") \
            LESS_TERMCAP_ue=$(printf "\e[0m") \
            LESS_TERMCAP_us=$(printf "\e[1;32m") \
            man "$@"
    }


<a id="orgd9d2821"></a>

# Mysql


<a id="orgf2d5d26"></a>

## Show db table create/update time

    select table_name, create_time, update_time
    from information_schema.TABLES
    where information_schema.TABLES.TABLE_SCHEMA = 'yw_cooperate_oppo' and information_schema.TABLES.TABLE_NAME = 'book_mrg';
    show table status like 'book_mrg';


<a id="orgd2db230"></a>

# IDEA


<a id="org077ee39"></a>

## Use alt key quickly on commit window

Alt+i not work, need to use Alt+Ctrl+i


<a id="org039ed84"></a>

# Convert vvt to srt

    ffmpeg -i in.vvt out.srt


<a id="org00a488a"></a>

# JACKSON


<a id="org27eab3f"></a>

## JsonNode to class

    MyClass newJsonNode = jsonObjectMapper.treeToValue(someJsonNode, MyClass.class);


<a id="org0cbc032"></a>

## Json to Map

    String jsonInput = "{\"key\": \"value\"}";
    TypeReference<HashMap<String, String>> typeRef
      = new TypeReference<HashMap<String, String>>() {};
    Map<String, String> map = mapper.readValue(jsonInput, typeRef);


<a id="org979bf3c"></a>

## Unwarp map

[java - Jackson HashMap, ignore map name when writing to String - Stack Overflow](https://stackoverflow.com/questions/57312679/jackson-hashmap-ignore-map-name-when-writing-to-string)

    private Map<String, TaskStatusDTO> taskMap;

    @JsonAnySetter
    public void setTaskMap(String key, TaskStatusDTO value) {
        this.taskMap.put(key, value);
    }

    @JsonAnyGetter
    public Map<String, TaskStatusDTO> getTaskMap() {
        return taskMap;
    }


<a id="orgb668efa"></a>

# Redis


<a id="orge7f2d98"></a>

## Batch del key

    redis-cli keys "*match" | xargs redis-cli del


<a id="org7e55488"></a>

## Find big key

    redis-cli --bigkeys


<a id="orge6307a5"></a>

# Nginx


<a id="orgde50d94"></a>

## underscore header issue

Must set **underscores<sub>in</sub><sub>headers</sub>** to tell nginx not drop it.

    underscores_in_headers on

[apache - Why do HTTP servers forbid underscores in HTTP header names - Stack Overflow](https://stackoverflow.com/questions/22856136/why-do-http-servers-forbid-underscores-in-http-header-names)


<a id="orgac7f627"></a>

# Wexin develop


<a id="orgb68cb47"></a>

## [微信模板消息换行 - Jinx - CSDN博客](https://blog.csdn.net/medivhq/article/details/49659971)


<a id="org2d81a5d"></a>

## [微信公众号开发者模式回复信息带表情（QQ，emoji） - X<sub>hazel的博客</sub> - CSDN博客](https://blog.csdn.net/X_hazel/article/details/85206241)


<a id="org2d9fa47"></a>

# JS


<a id="org1e02dba"></a>

## Get table td content

    var table = document.getElementById("mytable");
    var rows = table.rows;//获取所有行
    console.log("lenth",rows.length) //
    for(var i=1; i < rows.length; i++){
      var row = rows[i];//获取每一行
      var id = row.cells[1].innerHTML;//获取具体单元格
      console.log(id)
    }
