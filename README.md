
# Table of Contents

-   [Quick history](#org7b65832)
-   [English](#org99931f5)
-   [English Sentence](#org933bcba)
-   [English listen](#org8eb8c02)
-   [English news](#org0929fc5)
-   [English books](#org34e0708)
-   [Lisp](#org04d5c80)
-   [History](#org122d351)
-   [Chinese words](#org922ac84)
-   [Psychology](#org531cac6)
-   [Command line](#orgc7f677f)
    -   [打印文本第一行](#orgff98fa1)
    -   [获取文本最后一列](#org32af865)
    -   [Delete all broken soft link](#orgd57015e)
    -   [Rotate a image](#orgc231da6)
    -   [Split image](#org8e26da0)
    -   [Nohup to file and console](#org63213f1)
    -   [检验文件或者文件夹是否存在](#orgbb712ad)
        -   [判断文件是否存在](#orge32c3a7)
        -   [判断文件夹是否存在](#orgc906f12)
        -   [判断软链接存在并且可用虽](#orgf0973ef)
        -   [判断文件夹不存在](#org9ca1c2b)
    -   [获取本机ip](#org65865b1)
    -   [Delete file expect few files](#orgf5ddcfe)
    -   [Sync file from source to target increment](#org7bf98b4)
    -   [Scp with port](#org1508ef2)
    -   [Check url exist](#org84de91e)
        -   [Method1](#orgb608360)
        -   [Method2](#org6e8ff02)
    -   [Get host ip](#org2b6b143)
    -   [Generate short link](#org1c4ca38)
    -   [Get weather](#org5fabc59)
    -   [Pass passphrase to gpg](#org8980591)
    -   [Where xhost](#orgf6abe68)
    -   [Display custom date](#orgaafe6ed)
    -   [Extract filename and extension from file](#orgb66c7d9)
    -   [Truncate file](#orga536f15)
        -   [In-place](#org9e9a66b)
        -   [New file](#org1f8a6fb)
    -   [Cut file](#orgb9798b8)
    -   [Print unicode to chinese](#org04659d7)
    -   [Quick rename file name](#orge16fdf1)
    -   [Use default value for shell](#orgc2cccbb)
        -   [Assigning default values to shell variables with a single command in bash - Stack Overflow](#org17a6a3f)
    -   [export ls result to txt with absolute path](#org2be0545)
    -   [Export proxy app req to curl](#org0ce9646)
        -   [Charles](#org5fbafd2)
        -   [Fidder](#org035cb88)
        -   [Browser](#orgd3f8204)
-   [Maven](#org6a9af04)
    -   [How to get Maven project version from cmd](#orgeb424d7)
    -   [Maven use alternative repo](#orgc73465b)
    -   [Maven download dependency source code](#orgfd39e02)
        -   [Run dependency command directly](#orgfaad1f7)
        -   [Config on pom.xml](#org4b70e95)
        -   [java - How to download sources for a jar with Maven? - Stack Overflow](#orgff3d744)
    -   [Maven get settings file location](#org47a873e)
        -   [The settings.xml File in Maven | Baeldung](#org9da4c2c)
    -   [java - Maven clean install: Failed to execute goal org.apache.maven.plugins:maven-resources-plugin:3.2.0:resources - Stack Overflow](#org524a2e5)
    -   [Maven generate catalog file](#org035572c)
-   [Emacs](#orgaff0bd1)
    -   [给Emacs文档增加目录](#orgd047781)
    -   [Add command to keyboard macro](#orgb39f420)
    -   [Set major mode on file](#org6d92ea7)
    -   [Add minor mode on file](#org2891473)
    -   [Straight use builtin org](#org5b33e5a)
    -   [Delete blank line](#orga6bf7d2)
    -   [Insert file contents to org source area](#orgb0e3d5f)
    -   [Add note to blog](#org486d5de)
    -   [Yas add custom style date](#orgf442885)
    -   [Change org babel export language](#orgf94e354)
    -   [Ignore error info](#org3994092)
    -   [Org add repeated task for weekday](#org8514017)
    -   [Org babel python output always Nono](#org29a40fb)
    -   [Org add current time](#org01e092c)
        -   [How to insert current time in the emacs org-mode - Stack Overflow](#org7123f00)
    -   [Handle swiper search result](#org6e81d72)
    -   [Change org reveal font color](#orge4982b3)
    -   [So-long mode](#org3682a7d)
    -   [Trim changed line white space](#orgb97f77b)
    -   [Open chrome-extension: prefix url](#org4f84c8a)
    -   [Copy rectangle area content](#org18e2652)
    -   [Insert stuff like vi column mode but with string-rectangle](#org2498f1c)
    -   [Run region code with command line](#orga032ef1)
        -   [key bindings - Run current line or selection in shell then insert result in Emacs buffer (Acme workflow) - Emacs Stack Exchange](#org12a66da)
    -   [Joint multi lines to one line](#orgd57fcb4)
    -   [Save all org buffer](#org0774dd6)
    -   [Org mode search complete task](#org4a274d7)
    -   [Search and replace txt in folder](#orgcefe58b)
        -   [How can I replace a character with a newline in Emacs? - Stack Overflow](#org96fe1ae)
    -   [Copy url txt only](#org9da5c59)
    -   [Profile on emacs](#org962eaf2)
        -   [evil - Improve emacs performance when working on large files - Emacs Stack Exchange](#org75cbab7)
    -   [Run jshell with org mode](#org8be5e17)
    -   [Sort org entries](#orgfaa93f7)
    -   [Org list support alphabetical](#org8285679)
    -   [Org export all logbook content](#org4444e31)
    -   [Org copy headline only](#orgdedfd35)
    -   [Emacs-plus29+ install on mac15 issue](#orgadf0676)
        -   [[General]: exec-paths not being set in Sequoia for emacs-plus@30 · Issue #720 · d12frosted/homebrew-emacs-plus](#org4669bd0)
        -   [Could not install emacs-plus@29 with &#x2013;with-xwidgets &#x2013;with-imagemagick &#x2013;with-native-comp · Issue #556 · d12frosted/homebrew-emacs-plus](#org5f585ce)
    -   [Flush imenu cache](#orgcb5f96c)
-   [Org hugo add shortcode](#orgaeb1d61)
        -   [Shortcodes — ox-hugo - Org to Hugo exporter](#org26adf4f)
        -   [使用Shortcodes在Hugo博客中优雅的嵌入B站视频 – Yu's Blog](#orgca4a3e3)
    -   [Batch modify file name in emacs](#org032de6d)
-   [git](#org5ab9a40)
    -   [查看git配置的来源](#org069358e)
    -   [删除大于指定大小的仓库信息](#orgdd1bdb7)
    -   [Rebase user info](#orge92ace3)
    -   [Migrate code to new origin](#orga560cdd)
    -   [Remove untracked file](#org184228c)
    -   [How to clone git repo wiki](#org8b70abd)
        -   [clone today\_i\_learn repo](#orge242640)
        -   [clone today\_i\_learn repo wiki](#orgc8a3c49)
    -   [Create new repo from other existing repo branch](#org5efb1f8)
        -   [git - How do I create a new GitHub repo from a branch in an existing repo? - Stack Overflow](#org8681cd0)
    -   [Clone single branch](#orgd7cca67)
    -   [Show lastest one wekk logs](#org57c9942)
    -   [git checkout tags](#org9604f5e)
    -   [git add all modified file](#org5b13620)
-   [Github](#org50c8377)
    -   [Add profile page to github](#org659e6bb)
    -   [Github emoji shortcode](#org000e61f)
    -   [Get repo starts](#orgf8a2548)
    -   [Query config file](#orga528e24)
-   [JAVA](#orgb5510bf)
    -   [How to judge byte[] is compressed with gzip](#orgabaaf71)
    -   [Jenv export java\_home](#org49e6ed3)
    -   [Iterable to list](#org5da2024)
    -   [JVM](#orgc38123c)
        -   [Show java program jvm params](#org4b85239)
        -   [Why set -XX:NativeMemoryTracking=detail got ative memory tracking is not enabled](#orgb90cb35)
        -   [Where is the heap dump file created by jcmd?](#orga94e1ff)
        -   [find jvm thread stack size](#orga17bae9)
        -   [show jvm loaded class](#org2720212)
    -   [Get two date interval days by java8](#org885b661)
    -   [Convert Milliseconds to LocalDateTime](#org106ed31)
    -   [Convert LocalDate to Milliseconds](#orgf067215)
    -   [com.google.protobuf.GeneratedMessageV3.isStringEmpty not found](#org8232dd8)
    -   [Get returntype by aspectj joinpoint](#orga958b7b)
    -   [SpringFlux+Netty config access log](#org38862d5)
        -   [add netty system param](#org6f1b5f6)
        -   [config log4j for access log](#orgd003096)
    -   [Difference between Class.this and this in java](#orge8a3781)
        -   [Difference Between Class.this and this in Java - GeeksforGeeks](#org138eab6)
    -   [JDK base module not found](#orgd96493c)
        -   [Module java.base does not "opens java.lang" (Java 17.0.4.1) - Stack Overflow](#org0a42a36)
    -   [Change java.util.logging log level](#orgfabf648)
        -   [logging.properties](#org12da55f)
-   [Spring](#org706678d)
    -   [How to get handleMethod from webflux](#org170570f)
    -   [Spring profie effect scope](#org2853430)
    -   [java - Spring @Value with arraylist split and default empty list - Stack Overflow](#orga6f20be)
-   [KM](#org144b948)
    -   [How to show km error log](#orgf189565)
-   [Python](#orga88f49b)
    -   [python with git](#org1eef0fc)
    -   [python with clipboard](#orgd1324e9)
    -   [python urldecode](#org6ba45a9)
    -   [python with cross-platform home directory](#orgb31f58e)
    -   [python set to string](#org3b6a354)
    -   [python decimal to binary](#orgfeb5e84)
    -   [Set python spel env with uv](#org7a74058)
    -   [关于 Mac 12.3 出现 python not found 的解决方法 | HeyFE](#org1ede2c7)
    -   [Exist venv](#orgf309929)
    -   [Python run httpServer under current  directory](#org3435b7d)
-   [Brew](#org37f84df)
    -   [get installed program path](#org25b667f)
    -   [handle rebase-apply error](#org7576321)
    -   [Make brew python and pyenv togehter](#org7dd6fbd)
    -   [fixed font exists in multiple taps](#orgb468c1f)
    -   [Clean brew cache](#orgd17fe99)
    -   [Cask adoptopenjdk8 exists in multiple taps](#orgde42e86)
    -   [Brew install with .rb file](#org0a2baf6)
    -   [Brew tap modify](#orge5661f1)
    -   [Use bash 5.x version](#org6024a5b)
-   [MAC](#orgd7023e0)
    -   [del macOS Xcode CoreSimulator folder](#org80020f4)
    -   [Brew mysql install connect issue](#orgcff5289)
    -   [Mount/unmount smbs](#org8da520b)
    -   [Get running app](#org08c7538)
    -   [Reset macos accessibility](#org0fa51dd)
    -   [Find app url schema](#org0cdbc95)
    -   [Mac dictionary file path](#orge668c21)
    -   [Find ios app data path](#orge33634d)
    -   [Show lunar day in Calendar app](#orge7bee28)
    -   [Add debug info to app](#org8d170f7)
    -   [Remove Deleted Apps from Background Login Items](#org5605f91)
-   [Linux](#org50b4be9)
    -   [Change default program](#org3a5ae33)
    -   [SSH passwordless with public key authentication](#org6a681c7)
        -   [Generate key from host](#org7ffdfab)
        -   [Scp to dest machine](#org0e65c7c)
        -   [Add pub key to dest machine auth key](#org05d0544)
    -   [Man with color](#org0fbe5b1)
    -   [Config linux ssh with rsa login](#orge781712)
        -   [设置 SSH 通过密钥登录 | 菜鸟教程](#orga6251a7)
    -   [Show glibc version](#orged6105b)
-   [Mysql](#orge7b3b2c)
    -   [Show db table create/update time](#org7282acd)
    -   [Query db size](#org5e4628c)
    -   [Partition table](#orga3d09ef)
        -   [database - How to make partitioning in existing mysql table? - Stack Overflow](#org5e6316c)
    -   [Change primary key](#orgc8539a1)
        -   [Updating MySQL primary key - Stack Overflow](#org6265dd9)
-   [IDEA](#org5dbe657)
    -   [Use alt key quickly on commit window](#org7a7ee55)
    -   [Rm unused code](#orgbaf8180)
-   [Convert vvt to srt](#orga7d074f)
-   [Save video part stuff](#org6e957ce)
-   [JACKSON](#org03444b3)
    -   [JsonNode to class](#org050516c)
    -   [Json to Map](#org1a08bb6)
    -   [Unwarp map](#org9224682)
-   [Redis](#org7cfcaaf)
    -   [Batch del key](#org1489274)
    -   [Find big key](#orgb4c689b)
    -   [Set pass](#orgc306c46)
    -   [get generated rdb file location](#org07ee475)
    -   [Read rdb file with hunman readability](#orgc72121d)
-   [Nginx](#org2439943)
    -   [underscore header issue](#org4921759)
-   [Wexin develop](#org3961c5d)
    -   [微信模板消息换行 - Jinx - CSDN博客](#org670ac5f)
    -   [微信公众号开发者模式回复信息带表情（QQ，emoji） - X\_hazel的博客 - CSDN博客](#orgafd919b)
-   [JS](#orgb0e2cd9)
    -   [Get table td content](#orgcf79661)
-   [VIM](#org9e531c8)
    -   [indent code](#org058d29d)
        -   [Auto indent / format code for Vim? - Unix & Linux Stack Exchange](#orge28a299)
-   [GCC](#orgd91ce00)
    -   [Compile c program to assembly language](#org2752d6b)
-   [NPM](#org34732de)
    -   [sh: react-scripts: command not found after running npm start](#orge1a6704)
        -   [reactjs - sh: react-scripts: command not found after running npm start - Stack Overflow](#org0247559)
-   [GO](#org3be01ae)
    -   [Go compile to assembly language](#org97d46ac)
-   [VSCode](#org7c49e40)
    -   [Setting go for workspace](#org172f1fa)
-   [Pandoc](#org66c8192)
    -   [convert md to docx](#orga264eff)
-   [Xcode](#orge21500b)
    -   [xcode-select: error: tool 'xcodebuild' requires Xcode, but active developer directory '/Library/Developer/CommandLineTools' is a command line tools instance · Issue #569 · nodejs/node-gyp](#org508fda2)
-   [Chrome](#orgfeddd31)
    -   [Why does Chrome display "Your connection to this site is not secure" if content is empty? - Google Chrome Community](#org9cf12a2)
    -   [Close QUIC](#org3774c45)
-   [Firfox](#orge4d5343)
    -   [Get current tabe url from terminal](#org2b48ba5)
-   [Anki](#org647bf58)
    -   [pyqt - How do you embed a YouTube video into an Anki Card - Stack Overflow](#orga0b3cc5)
-   [Arthas](#orgbc97193)
    -   [Modify java file and reload](#org97fbe80)
        -   [retransform | arthas](#org407e7de)
-   [Twitter](#org4773cbd)
    -   [Search user hot tweets](#org71dc91f)
-   [Logseq](#org4f5313f)
    -   [Install local plugin](#org7d6e8db)
-   [MAT](#org3c713bd)
    -   [Install mat on mac arch m2](#org91446e1)
-   [System](#org648de5d)
    -   [Use vcpkg in clion](#org1038ef6)
    -   [Make file rule](#org50d3135)
-   [Clion](#orgfc61b77)
    -   [Disable clang errors to fixed unknown typename](#org3227b7a)
-   [C](#org42e4397)
    -   [Use compat memory allocate](#org4cd01b2)
-   [AI](#orgfe246c5)
    -   [Update all ollama models](#org97c0dfb)



<a id="org7b65832"></a>

# [Quick history](https://github.githistory.xyz/peng051410/today_i_learn/blob/main/README.org)


<a id="org99931f5"></a>

# [English](./english/vocabulary.md)


<a id="org933bcba"></a>

# [English Sentence](./english/sentence.md)


<a id="org8eb8c02"></a>

# [English listen](./english/listen.md)


<a id="org0929fc5"></a>

# [English news](./english/news.md)


<a id="org34e0708"></a>

# [English books](./english/book.md)


<a id="org04d5c80"></a>

# [Lisp](./emacs/lisp.md)


<a id="org122d351"></a>

# [History](./history/china_history.md)


<a id="org922ac84"></a>

# [Chinese words](./chinese/words.md)


<a id="org531cac6"></a>

# [Psychology](./psychology/psychology.md)


<a id="orgc7f677f"></a>

# Command line


<a id="orgff98fa1"></a>

## 打印文本第一行

    awk 'NR==1{print}' filename


<a id="org32af865"></a>

## 获取文本最后一列

主要是$NF

    awk -F ',' '{print $NF}'


<a id="orgd57015e"></a>

## Delete all broken soft link

    find -L . -name . -o -type d -prune -o -type l -exec rm {} +


<a id="orgc231da6"></a>

## Rotate a image

    function ro() {
        szFile=$1
        convert $1 -rotate 90 $(basename "$szFile").png
    }


<a id="org8e26da0"></a>

## Split image

    convert -crop 100%x20% in.png output.png

<https://dev.to/ko31/using-imagemagick-to-easily-split-an-image-file-13hb>


<a id="org63213f1"></a>

## Nohup to file and console

    nohup ./program  > Output.txt | tail -F Output.txt &


<a id="orgbb712ad"></a>

## 检验文件或者文件夹是否存在


<a id="orge32c3a7"></a>

### 判断文件是否存在

    if [ -e x.txt ]
    then
        echo "ok"
    else
        echo "nok"
    fi


<a id="orgc906f12"></a>

### 判断文件夹是否存在

    if [ -d folder1 ]
    then
        echo "ok"
    else
        echo "nok"
    fi


<a id="orgf0973ef"></a>

### 判断软链接存在并且可用虽

    [ -L ${my_link} ] && [ -e ${my_link} ]


<a id="org9ca1c2b"></a>

### 判断文件夹不存在


<a id="org65865b1"></a>

## 获取本机ip

    ifconfig | grep -Eo 'inet (addr:)?([0-9]*\.){3}[0-9]*' | grep -Eo '([0-9]*\.){3}[0-9]*' | grep -v '127.0.0.1'
    # linux only
    hostname -i


<a id="orgf5ddcfe"></a>

## Delete file expect few files

    rm -v !("filname1"|"file2")


<a id="org7bf98b4"></a>

## Sync file from source to target increment

    rsync -av Documents/* /tmp/documents


<a id="org1508ef2"></a>

## Scp with port

    scp -P 2222 file host@localhost:~/linux-study


<a id="org84de91e"></a>

## Check url exist


<a id="orgb608360"></a>

### Method1

    url=http://www.baidu.co
    if wget --spider $url 2>/dev/null; then
      echo "File exists"
    else
      echo "File does not exist"
    fi


<a id="org6e8ff02"></a>

### Method2

    url=http://www.baidu.co
    if wget -q --method=HEAD $url;
     then
      echo "This page exists."
     else
      echo "This page does not exist."
    fi


<a id="org2b6b143"></a>

## Get host ip

    curl ipaddy.net


<a id="org1c4ca38"></a>

## Generate short link

    curl -s 'tinyurl.com/api-create.php?url=http://www.baidu.com'


<a id="org5fabc59"></a>

## Get weather

    curl wttr.in


<a id="org8980591"></a>

## Pass passphrase to gpg

[shell script - gpg asks for password even with &#x2013;passphrase - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/60213/gpg-asks-for-password-even-with-passphrase)

    gpg -c --batch --passphrase 1234 -o file.gpg


<a id="orgf6abe68"></a>

## Where xhost

[x11 - xhost on MacOS Catalina - Ask Different](https://apple.stackexchange.com/questions/378348/xhost-on-macos-catalina)

    /opt/X11/bin/xhost


<a id="orgaafe6ed"></a>

## Display custom date

显示3小时之前的时间

    date -d '3 hours ago' +"%Y-%m-%d %T"
    # another way
    date -d "-3 Hours" "+%Y-%m-%d %T"


<a id="orgb66c7d9"></a>

## Extract filename and extension from file

<https://stackoverflow.com/questions/965053/extract-filename-and-extension-in-bash?page=1&tab=scoredesc#tab-top>

    fullfile=~/Downloads/main-webapp_log_Onl_jar_backend.yml
    filename=$(basename -- "$fullfile")
    extension="${filename##*.}"
    filename="${filename%.*}"
    echo "filanme is $filename, file extendsion is $extension"


<a id="orga536f15"></a>

## Truncate file

truncate file only retain 10 line


<a id="org9e9a66b"></a>

### In-place

    sed -i.bak '11,$ d' myfile.txt


<a id="org1f8a6fb"></a>

### New file

    head -n10 myfile.txt > myfile.txt.bak

<https://stackoverflow.com/questions/19017994/how-do-i-limit-or-truncate-text-file-by-number-of-lines>


<a id="orgb9798b8"></a>

## Cut file

    echo "hello world" | cut -b 2-5

    ello


<a id="org04659d7"></a>

## Print unicode to chinese

    echo -en "\\u9605\\u8bfb20\\u5206\\u949f"


<a id="orge16fdf1"></a>

## Quick rename file name

    cd /tmp
    touch aa.txt
    mv aa.{txt,doc}
    ls aa.doc


<a id="orgc2cccbb"></a>

## Use default value for shell

    FOO="${VARIABLE:-default}"  # FOO will be assigned 'default' value if VARIABLE not set or null.
    # The value of VARIABLE is kept intouched.
    
    FOO="${VARIABLE:=default}"  # If VARIABLE not set or null, set it's value to 'default'.
    # Then that value will be assigned to FOO


<a id="org17a6a3f"></a>

### [Assigning default values to shell variables with a single command in bash - Stack Overflow](https://stackoverflow.com/questions/2013547/assigning-default-values-to-shell-variables-with-a-single-command-in-bash)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-10-09 Mon 16:50]</span></span>


<a id="org2be0545"></a>

## export ls result to txt with absolute path

<https://unix.stackexchange.com/questions/268474/how-to-list-all-files-in-a-directory-with-absolute-paths>

    ls -d "$PWD"/* >> ~/work/repos.txt


<a id="org0ce9646"></a>

## Export proxy app req to curl


<a id="org5fbafd2"></a>

### Charles

url -> 右键 -> Copy cURL Request


<a id="org035cb88"></a>

### Fidder

File -> Export -> Selected Sessions -> cURL script


<a id="orgd3f8204"></a>

### Browser

url -> 右键 -> Copy cURL Request


<a id="org6a9af04"></a>

# Maven


<a id="orgeb424d7"></a>

## How to get Maven project version from cmd

    mvn -q -Dexec.executable=echo -Dexec.args='${project.artifactId}' --non-recursive exec:


<a id="orgc73465b"></a>

## Maven use alternative repo

    mvn -DaltDeploymentRepository=repoid::default::http://ip/nexus/content/repositories/releases clean source:jar-no-fork deploy


<a id="orgfd39e02"></a>

## Maven download dependency source code

mvn can download all project dependency jar source code by the [maven-dependency-plugin](https://maven.apache.org/plugins/maven-dependency-plugin/)
, there are two approach to reach the goal.


<a id="orgfaad1f7"></a>

### Run dependency command directly

    mvn dependency:sources -Dsilent=true

I prefer this way.


<a id="org4b70e95"></a>

### Config on pom.xml

    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-dependency-plugin</artifactId>
        <version>3.5.0</version>
        <executions>
          <execution>
            <id>download-sources</id>
            <goals>
              <goal>sources</goal>
            </goals>
            <configuration>
            </configuration>
          </execution>
        </executions>
      </plugin>

After add the plugin config, run normal mvn command to download source code


<a id="orgff3d744"></a>

### [java - How to download sources for a jar with Maven? - Stack Overflow](https://stackoverflow.com/questions/11361331/how-to-download-sources-for-a-jar-with-maven)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-03-16 Thu 16:04]</span></span>


<a id="org47a873e"></a>

## Maven get settings file location

    mvn -X clean | grep "settings"


<a id="org9da4c2c"></a>

### [The settings.xml File in Maven | Baeldung](https://www.baeldung.com/maven-settings-xml)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-03-16 Thu 16:35]</span></span>


<a id="org524a2e5"></a>

## [java - Maven clean install: Failed to execute goal org.apache.maven.plugins:maven-resources-plugin:3.2.0:resources - Stack Overflow](https://stackoverflow.com/questions/65910112/maven-clean-install-failed-to-execute-goal-org-apache-maven-pluginsmaven-resou)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-10-31 Tue 17:41]</span></span>

add nonFilteredFileExtensions config works for me.

    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-resources-plugin</artifactId>
        <version>3.3.0</version>
        <configuration>
            <encoding>UTF-8</encoding>
            <nonFilteredFileExtensions>
                <nonFilteredFileExtension>db</nonFilteredFileExtension>
            </nonFilteredFileExtensions>
        </configuration>
    </plugin>


<a id="org035572c"></a>

## Maven generate catalog file

    mvn archetype:crawl -Dcatalog=/var/archetype-catalog.xml


<a id="orgaff0bd1"></a>

# Emacs


<a id="orgd047781"></a>

## 给Emacs文档增加目录

给Entry增加标签 =:TOC:=，限定目录层级#+OPTIONS: toc:1


<a id="orgb39f420"></a>

## Add command to keyboard macro

<https://www.gnu.org/software/emacs/manual/html_node/emacs/Basic-Keyboard-Macro.html>
C-u f3 能执行macro直接到按下f4


<a id="org6d92ea7"></a>

## Set major mode on file

<https://www.gnu.org/software/emacs/manual/html_node/emacs/Choosing-Modes.html>

    ;; set major mode, with this, other set will be ignore
    ; -*-Lisp-*-


<a id="org2891473"></a>

## Add minor mode on file

    ; -*- eval: (rainbow-mode) -*-


<a id="org5b33e5a"></a>

## Straight use builtin org

将下面的配置加到straight配置前

    (straight-use-package '(org :type built-in))


<a id="orga6bf7d2"></a>

## Delete blank line

<https://www.masteringemacs.org/article/removing-blank-lines-buffer>

    M-x flush-lines RET ^$ RET


<a id="orgb0e3d5f"></a>

## Insert file contents to org source area

In src area, run **C-x i**

    grep 'cool thing' ~/Donwnloads


<a id="org486d5de"></a>

## Add note to blog

1.  \#+STARTUP: logdrawer
2.  在需要加note的item执行 **C-c C-z**


<a id="orgf442885"></a>

## Yas add custom style date

[Insert current date with yasnippet - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/27158/insert-current-date-with-yasnippet)

    `(format-time-string "%Y-%m-%d")`$0


<a id="orgf94e354"></a>

## Change org babel export language

[How to change the language of a result of ":results output code" in emacs org-mode - Stack Overflow](https://stackoverflow.com/questions/68085596/how-to-change-the-language-of-a-result-of-results-output-code-in-emacs-org-mo)

    /Users/tomyli/github/today_i_learn


<a id="org3994092"></a>

## Ignore error info

    (condition-case nil
        (progn
          (message "hello")
        t)
      (error nil)


<a id="org8514017"></a>

## Org add repeated task for weekday

    * TODO Study 09:00-10:00
    <%%(memq (calendar-day-of-week date) '(1 2 3 4 5))>


<a id="org29a40fb"></a>

## Org babel python output always Nono

[Python org-mode source block output is always ': None' - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/17926/python-org-mode-source-block-output-is-always-none)
Can use **return** or add **:results output**


<a id="org01e092c"></a>

## Org add current time

    C-u C-c .


<a id="org7123f00"></a>

### [How to insert current time in the emacs org-mode - Stack Overflow](https://stackoverflow.com/questions/11295973/how-to-insert-current-time-in-the-emacs-org-mode)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-05-24 Wed 10:22]</span></span>


<a id="org6e81d72"></a>

## Handle swiper search result

Ctrl+s搜索后，再按 **Ctrl+c Ctrl+o** 打开处理结果的buffer


<a id="orge4982b3"></a>

## Change org reveal font color

[org mode - Change font color on a `org-reveal` slide - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/38532/change-font-color-on-a-org-reveal-slide)

1.  Add header

    #+MACRO: color @@html:<font color="$1">$2</font>@@

1.  Use macro

    {{{color(red, 基于2019.1版本.)}}}


<a id="org3682a7d"></a>

## So-long mode

When a file very big, [so-long](https://elpa.gnu.org/packages/so-long.html) mode can fixed it


<a id="orgb97f77b"></a>

## Trim changed line white space

<https://github.com/redguardtoo/emacs.d/issues/1014>
Emacs has an minor mode called [ws-butler-mode](https://github.com/lewang/ws-butler) can trim white space only with changed line.


<a id="org4f84c8a"></a>

## Open chrome-extension: prefix url

    (setq browse-url-chrome-program "/Applications/Chromium.app/Contents/MacOS/Chromium")


<a id="org18e2652"></a>

## Copy rectangle area content

It's useful to yank org table cols without additional custom func.
![img](https://cdn.jsdelivr.net/gh/peng051410/bucket@main/img/copy-rectangle.gif)


<a id="org2498f1c"></a>

## Insert stuff like vi column mode but with string-rectangle

<https://twitter.com/i/status/1620721190536114177>


<a id="orga032ef1"></a>

## Run region code with command line

I have an request to run curl script with shell, normaly the content is paste from other place, so I think this is any way the emacs can do this, After search emacs doc and
request google, I found the 'shell-commond-on-region'. When I run this command, it works, but another issue occurs that the result only shows in the minibuffer which I can't
do it more like search or copy. Fortunately, the SO user @[xuchunyang](https://emacs.stackexchange.com/users/3889/xuchunyang) give me the perfect anwser, an customed 'shell-command-on-region' which output the result after the
request bufer. With this, I can do more imaginable.


<a id="org12a66da"></a>

### [key bindings - Run current line or selection in shell then insert result in Emacs buffer (Acme workflow) - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/55506/run-current-line-or-selection-in-shell-then-insert-result-in-emacs-buffer-acme)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-03-14 Tue 15:03]</span></span>


<a id="orgd57fcb4"></a>

## Joint multi lines to one line

Sometimes in develop, we need to convert multi line content to one line, we can realize with Emacs 'join line' command.

    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-core</artifactId>
      <version>5.3.23</version>
      <scope>compile</scope>
    </dependency>

![img](https://cdn.jsdelivr.net/gh/peng051410/bucket@main/img/emacs-join-lines.gif)


<a id="org0774dd6"></a>

## Save all org buffer

Realize with **org-save-all-org-buffers** command


<a id="org4a274d7"></a>

## Org mode search complete task

search previous week done task

    TODO="DONE"&CLOSED>="<-1w>"


<a id="orgcefe58b"></a>

## Search and replace txt in folder

M-x replace-string RET ; RET C-q C-j.
C-q for quoted-insert,
C-j is a newline.


<a id="org96fe1ae"></a>

### [How can I replace a character with a newline in Emacs? - Stack Overflow](https://stackoverflow.com/questions/613022/how-can-i-replace-a-character-with-a-newline-in-emacs)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-10-09 Mon 11:02]</span></span>


<a id="org9da5c59"></a>

## Copy url txt only

With evil

    yi[


<a id="org962eaf2"></a>

## Profile on emacs

1.  M-x profiler-start and select cpu from the prompt
2.  do the thing that is slow
3.  M-x profiler-stop
4.  M-x profiler-report
5.  Look for the cpu hogs and drill down in to them by hitting TAB on them to find what's slowing down your Emacs.


<a id="org75cbab7"></a>

### [evil - Improve emacs performance when working on large files - Emacs Stack Exchange](https://emacs.stackexchange.com/questions/61463/improve-emacs-performance-when-working-on-large-files)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-12-14 Thu 20:08]</span></span>


<a id="org8be5e17"></a>

## Run jshell with org mode

    jshell
    int a[] = {0,1,3,5,8}
    a
    a[3] = 42
    a

<https://emacs-china.org/t/emacs-org-mode-jshell/12491/2>


<a id="orgfaa93f7"></a>

## Sort org entries

Use **org-sort** command
支持按字母、数字、优先级、属性、时间等进行排序

![img](https://cdn.jsdelivr.net/gh/peng051410/bucket@main/img/K9RHdv.png)


<a id="org8285679"></a>

## Org list support alphabetical

    (setq org-list-allow-alphabetical t)


<a id="org4444e31"></a>

## Org export all logbook content

This can realize by setting options

    #+options: d:t


<a id="orgdedfd35"></a>

## Org copy headline only

Use org-copy-visiable


<a id="orgadf0676"></a>

## Emacs-plus29+ install on mac15 issue


<a id="org4669bd0"></a>

### [[General]: exec-paths not being set in Sequoia for emacs-plus@30 · Issue #720 · d12frosted/homebrew-emacs-plus](https://github.com/d12frosted/homebrew-emacs-plus/issues/720)


<a id="org5f585ce"></a>

### [Could not install emacs-plus@29 with &#x2013;with-xwidgets &#x2013;with-imagemagick &#x2013;with-native-comp · Issue #556 · d12frosted/homebrew-emacs-plus](https://github.com/d12frosted/homebrew-emacs-plus/issues/556)

[Solved by add path to emacs](https://github.com/d12frosted/homebrew-emacs-plus/issues/733#issuecomment-2368746692)

    (setenv "PATH" "~/Library/Python/3.9/bin:/opt/homebrew/bin:/usr/local/bin:/usr/bin:/bin:/usr/local/sbin:/sbin:/usr/sbin:/Library/TeX/texbin:~/.local/bin:~/Nustore/script:~/go/bin:/opt/local/bin")
    (setq exec-path (split-string (getenv "PATH") path-separator))


<a id="orgcb5f96c"></a>

## Flush imenu cache

    (setq imenu--index-alist nil)
    
    (global-set-key "\C-ci"
                    (lambda () (interactive)
                      (imenu--menubar-select imenu--rescan-item)))


<a id="orgaeb1d61"></a>

# Org hugo add shortcode

Hugo支持短代码形式在生成html时填充模板内容，shortcode配置的html文件放在 **/layouts/shortcodes** 目录下即可，下面的代码就可以实现在博客中嵌入[B站](https://www.bilibili.com/video/BV1pD4y1K7iw/)的视频

Hugo也支持 **begin\_myshortcode** 方式进行嵌入，使用中发现这种形式都是要成对出现的，类似html的闭合标签，目前的使用方式就是 **代码+参数** ，先记住 **export hugo** 方式就可以了


<a id="org26adf4f"></a>

### [Shortcodes — ox-hugo - Org to Hugo exporter](https://ox-hugo.scripter.co/doc/shortcodes/)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-01-30 Mon 17:16]</span></span>


<a id="orgca4a3e3"></a>

### [使用Shortcodes在Hugo博客中优雅的嵌入B站视频 – Yu's Blog](https://blog.iyu.icu/posts/shortcode_bilibili/)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-01-30 Mon 17:10]</span></span>


<a id="org032de6d"></a>

## Batch modify file name in emacs

借助库 [dired](https://www.gnu.org/software/emacs/manual/html_node/emacs/Dired.html) 即可实现，参照 [李杀](http://xahlee.info/emacs/emacs/rename_file_pattern.html) 的教程

![img](https://cdn.jsdelivr.net/gh/peng051410/bucket@main/img/emacs-dired-batch-file.gif)


<a id="org5ab9a40"></a>

# git


<a id="org069358e"></a>

## 查看git配置的来源

在正常工作中会针对不同的工作目录设置不同的配置，可以根据以下命令来确认当前仓库使用的配置来源

    git config --show-origin --get user.email


<a id="orgdd1bdb7"></a>

## 删除大于指定大小的仓库信息

迁移仓库时遇到异常，提示镜像文件大于了100M，无法操作，经同事帮助找到此工具，减少仓库信息没得说

    bfg --strip-blobs-bigger-than 100M some-big-repo.git


<a id="orge92ace3"></a>

## Rebase user info

    git rebase -i "commit id"
    # pick to edit then save change
    git commit --amend --author="{username} <{email}>" --no-edit
    git rebase --continue
    git push


<a id="orga560cdd"></a>

## Migrate code to new origin

    git clone --mirror <url_of_old_repo>
    git remote add new-origin <url_of_new_repo>
    git push new-origin --all


<a id="org184228c"></a>

## Remove untracked file

    git clean -xf

交互式的进行删除

    git clean -i


<a id="org8b70abd"></a>

## How to clone git repo wiki

add .wiki after repo


<a id="orge242640"></a>

### clone today\_i\_learn repo

    git clone https://github.com/peng051410/today_i_learn


<a id="orgc8a3c49"></a>

### clone today\_i\_learn repo wiki

    git clone https://github.com/peng051410/today_i_learn.wiki


<a id="org5efb1f8"></a>

## Create new repo from other existing repo branch

    git push new_repo_address +old_repo_branch:master


<a id="org8681cd0"></a>

### [git - How do I create a new GitHub repo from a branch in an existing repo? - Stack Overflow](https://stackoverflow.com/questions/9527999/how-do-i-create-a-new-github-repo-from-a-branch-in-an-existing-repo)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-02-23 Thu 14:22]</span></span>


<a id="orgd7cca67"></a>

## Clone single branch

    git clone <url> --branch <branch-to-clone> --single-branch [folder-to-store]

<https://igorstechnoclub.com/my-everyday-git-commands/>


<a id="org57c9942"></a>

## Show lastest one wekk logs

    git log --since=1.week


<a id="org9604f5e"></a>

## git checkout tags

<https://stackoverflow.com/questions/35979642/what-is-git-tag-how-to-create-tags-how-to-checkout-git-remote-tags>

    git fetch --all --tags --prune
    git checkout tags/<tag_name> -b <branch_name>


<a id="org5b13620"></a>

## git add all modified file

    git add -u


<a id="org50c8377"></a>

# Github


<a id="org659e6bb"></a>

## Add profile page to github

<https://twitter.com/tomylitoo/status/1580396505118441472>
Create a repositoy with name same to github name.


<a id="org000e61f"></a>

## Github emoji shortcode

<https://github.com/ikatyang/emoji-cheat-sheet>


<a id="orgf8a2548"></a>

## Get repo starts

    wget https://api.github.com/repos/emacs-eaf/eaf-rss-reader/stargazers

Authenticate requests can do more req.


<a id="orga528e24"></a>

## Query config file

Search aerospace config files

Search with **path:\*aerospace.toml**

<https://github.com/search?q=path%3A*aerospace.toml&type=code>


<a id="orgb5510bf"></a>

# JAVA


<a id="orgabaaf71"></a>

## How to judge byte[] is compressed with gzip

    private boolean isCompressed(byte[] bytes) {
        if ((bytes == null) || (bytes.length < 2)) {
            return false;
        } else {
            return ((bytes[0] == (byte) (GZIPInputStream.GZIP_MAGIC)) && (bytes[1] == (byte) (GZIPInputStream.GZIP_MAGIC
                    >> 8)));
        }
    }


<a id="org49e6ed3"></a>

## Jenv export java\_home

    jenv enable-plugin export


<a id="org5da2024"></a>

## Iterable to list

    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-collections4</artifactId>
        <version>4.4</version>
    </dependency>

    IterableUtils.toList(list);


<a id="orgc38123c"></a>

## JVM


<a id="org4b85239"></a>

### Show java program jvm params

    jcmd 2886 VM.flags


<a id="orgb90cb35"></a>

### Why set -XX:NativeMemoryTracking=detail got ative memory tracking is not enabled

Os security, must execute with root
[java - Why JCMD throws "native memory tracking is not enabled" message even though NMT is enabled? - Stack Overflow](https://stackoverflow.com/questions/42295509/why-jcmd-throws-native-memory-tracking-is-not-enabled-message-even-though-nmt)


<a id="orga94e1ff"></a>

### Where is the heap dump file created by jcmd?

Java recommand use jcmd instead of jmap to generate heap file, like:

    jcmd 271709 GC.heap_dump Myheapdump.hprof

but, where the generated file?

We can use lsof commd to find the output path

    lsof -p pid | grep wd

or genrate with an absolute path

    jcmd 271709 GC.heap_dump /data/log/Myheapdump.hprof

<https://stackoverflow.com/questions/58519663/where-is-the-heap-dump-file-created-by-jcmd>


<a id="orga17bae9"></a>

### find jvm thread stack size

    java -XX:+PrintFlagsFinal -version | grep ThreadStackSize

<https://stackoverflow.com/questions/6020619/where-can-i-find-default-xss-stack-size-value-for-oracle-jvm>


<a id="org2720212"></a>

### show jvm loaded class

    jcmd <jvm_pid> VM.classloaders show-classes

<https://stackoverflow.com/questions/16559430/get-a-listing-of-all-currently-loaded-classes-in-a-given-jvm-instance>


<a id="org885b661"></a>

## Get two date interval days by java8

[Calculate days between two Dates in Java 8 - Stack Overflow](https://stackoverflow.com/questions/27005861/calculate-days-between-two-dates-in-java-8)

    LocalDate today = LocalDate.now()
    LocalDate yesterday = today.minusDays(1);
    Duration.between(today.atStartOfDay(), yesterday.atStartOfDay()).toDays() // another option


<a id="org106ed31"></a>

## Convert Milliseconds to LocalDateTime

    long millis = 1614926594000L; // UTC Fri Mar 05 2021 06:43:14
    LocalDate dateTime = Instant.ofEpochMilli(millis)
            .atZone(ZoneId.systemDefault()) // default zone
            .toLocalDate(); // returns actual LocalDate object


<a id="orgf067215"></a>

## Convert LocalDate to Milliseconds

    ocalDate dateTime1 = LocalDate.of(2021, 3, 5);
    long seconds = dateTime1.atStartOfDay(ZoneId.systemDefault())
            .toEpochSecond(); // returns seconds
    long millis1 = seconds * 1000; // seconds to milliseconds


<a id="org8232dd8"></a>

## com.google.protobuf.GeneratedMessageV3.isStringEmpty not found

need import protobuf-java dependency

    <dependency>
      <groupId>com.google.protobuf</groupId>
      <artifactId>protobuf-java</artifactId>
      <version>3.19.1</version>
    </dependency>


<a id="orga958b7b"></a>

## Get returntype by aspectj joinpoint

    Method method = ((MethodSignature) proceedingJoinPoint.getSignature()).getMethod();
    Class<?> returnType = method.getReturnType();
    
    //or
    Class<?> returnType1 = ((MethodSignature) proceedingJoinPoint.getSignature()).getReturnType();


<a id="org38862d5"></a>

## SpringFlux+Netty config access log


<a id="org6f1b5f6"></a>

### add netty system param

    -Dreactor.netty.http.server.accessLogEnabled=true


<a id="orgd003096"></a>

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


<a id="orge8a3781"></a>

## Difference between Class.this and this in java

Class.this used in nested class to resolved ambiguous


<a id="org138eab6"></a>

### [Difference Between Class.this and this in Java - GeeksforGeeks](https://www.geeksforgeeks.org/difference-between-class-this-and-this-in-java/)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-11-17 Fri 16:17]</span></span>


<a id="orgd96493c"></a>

## JDK base module not found

Need add vm options to IDEA

    --add-opens=java.base/java.lang=ALL-UNNAMED
    --add-opens=java.base/java.util=ALL-UNNAMED


<a id="org0a42a36"></a>

### [Module java.base does not "opens java.lang" (Java 17.0.4.1) - Stack Overflow](https://stackoverflow.com/questions/74006627/module-java-base-does-not-opens-java-lang-java-17-0-4-1)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-12-28 Thu 16:44]</span></span>


<a id="orgfabf648"></a>

## Change java.util.logging log level

<https://stackoverflow.com/questions/6307648/change-global-setting-for-logger-instances>

    -Djava.util.logging.config.file="logging.properties"


<a id="org12da55f"></a>

### logging.properties

    .level = INFO #global
    com.xyz.foo.level = SEVERE


<a id="org706678d"></a>

# Spring


<a id="org170570f"></a>

## How to get handleMethod from webflux

1.  inject handleMapping
2.  you got it!

    (HandlerMethod) this.handlerMapping.getHandler(serverWebExchange).toProcessor().peek();


<a id="org2853430"></a>

## Spring profie effect scope

Profiles affect only bean creation, not method.


<a id="orga6f20be"></a>

## [java - Spring @Value with arraylist split and default empty list - Stack Overflow](https://stackoverflow.com/questions/49367006/spring-value-with-arraylist-split-and-default-empty-list)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-11-29 Wed 17:43]</span></span>
I want to transfer a value from config to list, and need to set default value, I don't like two write value keys twice, like this:

    @Value("#{'${my.list}'.split(',') : T(java.util.Collections).emptyList()}")

Fortunately, I found a beautiful solution to face it. Thanks SO.

    @Value("#{T(java.util.Arrays).asList('${my.list:}')}")
    private List<String> list;


<a id="org144b948"></a>

# KM


<a id="orgf189565"></a>

## How to show km error log

    tail -f ~/Library/Logs/Keyboard\ Maestro/Engine.log


<a id="orga88f49b"></a>

# Python


<a id="org1eef0fc"></a>

## python with git

    pip3 install GitPython


<a id="orgd1324e9"></a>

## python with clipboard

    pip3 install pyperclip


<a id="org6ba45a9"></a>

## python urldecode

    from urllib.parse import unquote
    url = unquote(url)


<a id="orgb31f58e"></a>

## python with cross-platform home directory

[python - What is a cross-platform way to get the home directory? - Stack Overflow](https://stackoverflow.com/questions/4028904/what-is-a-cross-platform-way-to-get-the-home-directory)

    from pathlib import Path
    home = str(Path.home())
    print(home)


<a id="org3b6a354"></a>

## python set to string

    s = {'a', 'b'}
    str = ', '.join(s)
    print(str)


<a id="orgfeb5e84"></a>

## python decimal to binary

<https://stackoverflow.com/questions/3528146/convert-decimal-to-binary-in-python>

    abinary = bin(1024)
    print(abinary)


<a id="org7a74058"></a>

## Set python spel env with uv

    uv run --python 3.12 --with pandas python


<a id="org1ede2c7"></a>

## [关于 Mac 12.3 出现 python not found 的解决方法 | HeyFE](https://blog.heyfe.org/blog/2022-mac-12-3-python-not-found.html)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-12-05 Tue 19:04]</span></span>

1.  安装pyenv
2.  set python globel
3.  修改alfred命令的python路径

我的alfred插件又可以用了

    pyenv install 2.7.18
    pyenv global 2.7.18


<a id="orgf309929"></a>

## Exist venv

    deactivate


<a id="org3435b7d"></a>

## Python run httpServer under current  directory

    python3 -m http.server --directory .


<a id="org37f84df"></a>

# Brew


<a id="org25b667f"></a>

## get installed program path

    (brew --prefix go)


<a id="org7576321"></a>

## handle rebase-apply error

    brew update-reset


<a id="org7dd6fbd"></a>

## Make brew python and pyenv togehter

    ln -s $(brew --cellar python)/* ~/.pyenv/versions/


<a id="orgb468c1f"></a>

## fixed font exists in multiple taps

[How can I fix Error: font exists in multiple taps ? · Issue #59227 · Homebrew/homebrew-cask](https://github.com/Homebrew/homebrew-cask/issues/59227)

    brew untap caskroom/fonts
    brew tap homebrew/cask-fonts
    brew cask install font-hack-nerd-font


<a id="orgd17fe99"></a>

## Clean brew cache

    brew cleanup -s


<a id="orgde42e86"></a>

## Cask adoptopenjdk8 exists in multiple taps

Del homebrew cask rb

    rm /usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask-versions/Casks/adoptopenjdk8.rb

<https://github.com/AdoptOpenJDK/homebrew-openjdk/issues/106#issuecomment-487269671>


<a id="org0a2baf6"></a>

## Brew install with .rb file

    brew install qemu-virgl.rb


<a id="orge5661f1"></a>

## Brew tap modify

    brew tap knazarov/qemu-virgl
    brew edit qemu-virgl


<a id="org6024a5b"></a>

## Use bash 5.x version

    brew install bash


<a id="orgd7023e0"></a>

# MAC


<a id="org80020f4"></a>

## del macOS Xcode CoreSimulator folder

    xcrun simctl delete unavailable


<a id="orgcff5289"></a>

## Brew mysql install connect issue

因为有老的mysql数据没有清理完全，执行完以下操作后，重新安装即可

    sudo rm -rf /usr/local/var/mysql


<a id="org8da520b"></a>

## Mount/unmount smbs

    sudo mount -t smbfs '//vagrant:vagrant@localhost:10139/kernel-source' /Volumes
    unmont kernel-source


<a id="org08c7538"></a>

## Get running app

    osascript -e 'tell application "System Events" to get name of (processes where background only is false)'


<a id="org0fa51dd"></a>

## Reset macos accessibility

    sudo tccutil reset Accessibility


<a id="org0cdbc95"></a>

## Find app url schema

1.  go to /Application folder
2.  find target app
3.  show package contents
4.  oppen info.plist
5.  search CFBundleURLSchemes

![img](https://cdn.jsdelivr.net/gh/peng051410/bucket@main/img/Peza8y.png)


<a id="orge668c21"></a>

## Mac dictionary file path

/System/Library/AssetsV2/com\_apple\_MobileAsset\_DictionaryServices\_dictionaryOSX


<a id="orge33634d"></a>

## Find ios app data path

    open ~/Library/Containers/appNames


<a id="orge7bee28"></a>

## Show lunar day in Calendar app

![img](https://cdn.jsdelivr.net/gh/peng051410/bucket@main/img/JL7jS1.png)


<a id="org8d170f7"></a>

## Add debug info to app

Add **-\_NS\_4445425547 YES** param to app


<a id="org5605f91"></a>

## Remove Deleted Apps from Background Login Items

Open folders show below and delete relative item

    cd ~/Library/LaunchAgents
    cd /Library/LaunchAgents
    cd /Library/LaunchDaemons


<a id="org50b4be9"></a>

# Linux


<a id="org3a5ae33"></a>

## Change default program

    update-alternatives --set java java-11-openjdk.x86_64

You can issue java path by

    update-alternatives --config java


<a id="org6a681c7"></a>

## SSH passwordless with public key authentication


<a id="org7ffdfab"></a>

### Generate key from host

    ssh-keygen -t rsa


<a id="org0e65c7c"></a>

### Scp to dest machine

    scp .ssh/id_rsa.pub user@host:.


<a id="org05d0544"></a>

### Add pub key to dest machine auth key

    cat id_rsa.pub >> .ssh/authorized_keys


<a id="org0fbe5b1"></a>

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


<a id="orge781712"></a>

## Config linux ssh with rsa login


<a id="orga6251a7"></a>

### [设置 SSH 通过密钥登录 | 菜鸟教程](https://www.runoob.com/w3cnote/set-ssh-login-key.html)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-10-24 Tue 10:33]</span></span>


<a id="orged6105b"></a>

## Show glibc version

    ls -l /lib/libc.so.*


<a id="orge7b3b2c"></a>

# Mysql


<a id="org7282acd"></a>

## Show db table create/update time

    select table_name, create_time, update_time
    from information_schema.TABLES
    where information_schema.TABLES.TABLE_SCHEMA = 'yw_cooperate_oppo' and information_schema.TABLES.TABLE_NAME = 'book_mrg';
    show table status like 'book_mrg';


<a id="org5e4628c"></a>

## Query db size

data size with M.

    select table_schema as database_name,
           table_name,
           round(1.0*data_length/1024/1024, 2) as data_size,
           round(index_length/1024/1024, 2) as index_size,
           round((data_length + index_length)/1024/1024, 2) as total_size
    from information_schema.tables
    where table_schema not in('information_schema', 'mysql',
                              'sys', 'performance_schema')
          -- and table_schema = 'your database name'
    order by total_size desc;

<https://dataedo.com/kb/query/mysql/list-of-tables-by-the-size-of-data-and-indexes>


<a id="orga3d09ef"></a>

## Partition table

    alter table `ugc_ent` PARTITION BY RANGE (TO_DAYS(create_time)) (
      PARTITION p20240210 VALUES LESS THAN (TO_DAYS('2024-02-10')) ENGINE = InnoDB
    )


<a id="org5e6316c"></a>

### [database - How to make partitioning in existing mysql table? - Stack Overflow](https://stackoverflow.com/questions/11859481/how-to-make-partitioning-in-existing-mysql-table)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2024-01-08 Mon 16:41]</span></span>


<a id="orgc8539a1"></a>

## Change primary key

    alter table `ugc_comment` drop primary key, add primary key(`comment_id`,`create_time`);


<a id="org6265dd9"></a>

### [Updating MySQL primary key - Stack Overflow](https://stackoverflow.com/questions/2341576/updating-mysql-primary-key)


<a id="org5dbe657"></a>

# IDEA


<a id="org7a7ee55"></a>

## Use alt key quickly on commit window

Alt+i not work, need to use Alt+Ctrl+i


<a id="orgbaf8180"></a>

## Rm unused code

<div class="notes" id="orgbf05740">
<p>
Just use Analyze | Inspect Code with appropriate inspection enabled (Unused declaration under Declaration redundancy group).
</p>

</div>


<a id="orga7d074f"></a>

# Convert vvt to srt

    ffmpeg -i in.vvt out.srt


<a id="org6e957ce"></a>

# Save video part stuff

截取视频的特定时间的内容


<a id="org03444b3"></a>

# JACKSON


<a id="org050516c"></a>

## JsonNode to class

    MyClass newJsonNode = jsonObjectMapper.treeToValue(someJsonNode, MyClass.class);


<a id="org1a08bb6"></a>

## Json to Map

    String jsonInput = "{\"key\": \"value\"}";
    TypeReference<HashMap<String, String>> typeRef
      = new TypeReference<HashMap<String, String>>() {};
    Map<String, String> map = mapper.readValue(jsonInput, typeRef);


<a id="org9224682"></a>

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


<a id="org7cfcaaf"></a>

# Redis


<a id="org1489274"></a>

## Batch del key

    redis-cli keys "*match" | xargs redis-cli del


<a id="orgb4c689b"></a>

## Find big key

    redis-cli --bigkeys


<a id="orgc306c46"></a>

## Set pass

    config set requirepass p@ss$12E45

This will be invalid when redis server restart, for permanently valid set in redis.conf


<a id="org07ee475"></a>

## get generated rdb file location

    redis-cli config get dir

<https://stackoverflow.com/questions/57790483/where-is-redis-installed-on-macos>


<a id="orgc72121d"></a>

## Read rdb file with hunman readability

    od -A x -t x1c -v dump.rdb


<a id="org2439943"></a>

# Nginx


<a id="org4921759"></a>

## underscore header issue

Must set **underscores\_in\_headers** to tell nginx not drop it.

    underscores_in_headers on

[apache - Why do HTTP servers forbid underscores in HTTP header names - Stack Overflow](https://stackoverflow.com/questions/22856136/why-do-http-servers-forbid-underscores-in-http-header-names)


<a id="org3961c5d"></a>

# Wexin develop


<a id="org670ac5f"></a>

## [微信模板消息换行 - Jinx - CSDN博客](https://blog.csdn.net/medivhq/article/details/49659971)


<a id="orgafd919b"></a>

## [微信公众号开发者模式回复信息带表情（QQ，emoji） - X\_hazel的博客 - CSDN博客](https://blog.csdn.net/X_hazel/article/details/85206241)


<a id="orgb0e2cd9"></a>

# JS


<a id="orgcf79661"></a>

## Get table td content

    var table = document.getElementById("mytable");
    var rows = table.rows;//获取所有行
    console.log("lenth",rows.length) //
    for(var i=1; i < rows.length; i++){
      var row = rows[i];//获取每一行
      var id = row.cells[1].innerHTML;//获取具体单元格
      console.log(id)
    }


<a id="org9e531c8"></a>

# VIM


<a id="org058d29d"></a>

## indent code

= indicate indent

    gg
    =G


<a id="orge28a299"></a>

### [Auto indent / format code for Vim? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/19945/auto-indent-format-code-for-vim)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-05-18 Thu 19:22]</span></span>


<a id="orgd91ce00"></a>

# GCC


<a id="org2752d6b"></a>

## Compile c program to assembly language

    gcc -S helloworld.c

After run this command, a new file named helloworld.s prevent.


<a id="org34732de"></a>

# NPM


<a id="orge1a6704"></a>

## sh: react-scripts: command not found after running npm start

Project need install dependency package

    npm install


<a id="org0247559"></a>

### [reactjs - sh: react-scripts: command not found after running npm start - Stack Overflow](https://stackoverflow.com/questions/40546231/sh-react-scripts-command-not-found-after-running-npm-start)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-06-09 Fri 14:06]</span></span>


<a id="org3be01ae"></a>

# GO


<a id="org97d46ac"></a>

## Go compile to assembly language

    go build -gcflags=-S main.go

<https://github.com/golang/go/issues/58629>

<https://colobu.com/2018/12/29/get-assembly-output-for-go-programs/>


<a id="org7c49e40"></a>

# VSCode


<a id="org172f1fa"></a>

## Setting go for workspace

<https://townsyio.medium.com/how-to-configure-your-go-modules-proxy-in-vscode-fa41f29192fe>

1.  run "open setting workspace (json)" command in VSCode
2.  add config

    {
        "go.toolsEnvVars": {
            "GOPRIVATE": "townsy.private-github.com",
            "GOPROXY": "https://athens-proxy.townsy.io",
            "GONOPROXY": "none;",
            "GONOSUMDB": "townsy.private-github.com"
        },
        "terminal.integrated.env.linux": {
            "GOPRIVATE": "townsy.private-github.com",
            "GOPROXY": "https://athens-proxy.townsy.io",
            "GONOPROXY": "none;",
            "GONOSUMDB": "townsy.private-github.com"
        }
    }


<a id="org66c8192"></a>

# Pandoc


<a id="orga264eff"></a>

## convert md to docx

    pandoc -o output.docx -f markdown -t docx filename.md


<a id="orge21500b"></a>

# Xcode


<a id="org508fda2"></a>

## [xcode-select: error: tool 'xcodebuild' requires Xcode, but active developer directory '/Library/Developer/CommandLineTools' is a command line tools instance · Issue #569 · nodejs/node-gyp](https://github.com/nodejs/node-gyp/issues/569)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-10-30 Mon 20:12]</span></span>

    xcode-select --install # Install Command Line Tools if you haven't already.
    sudo xcode-select --switch /Library/Developer/CommandLineTools # Enable command line tools
    # Change the path if you installed Xcode somewhere else.
    sudo xcode-select -s /Applications/Xcode.app/Contents/Developer


<a id="orgfeddd31"></a>

# Chrome


<a id="org9cf12a2"></a>

## [Why does Chrome display "Your connection to this site is not secure" if content is empty? - Google Chrome Community](https://support.google.com/chrome/thread/162555856/why-does-chrome-display-your-connection-to-this-site-is-not-secure-if-content-is-empty?hl=en)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-10-31 Tue 11:48]</span></span>


<a id="org3774c45"></a>

## Close QUIC

1.  chrome://flags/#enable-quic
2.  Experimental QUIC protocol to **Disabled**


<a id="orge4d5343"></a>

# Firfox


<a id="org2b48ba5"></a>

## Get current tabe url from terminal

    osascript -e  'tell application "System Events" to get value of UI element 1 of combo box 1 of toolbar "Navigation" of first group of front window of application process "Firefox"'

<https://apple.stackexchange.com/questions/404841/get-url-of-opened-firefox-tabs-from-terminal>


<a id="org647bf58"></a>

# Anki


<a id="orga0b3cc5"></a>

## [pyqt - How do you embed a YouTube video into an Anki Card - Stack Overflow](https://stackoverflow.com/questions/42206812/how-do-you-embed-a-youtube-video-into-an-anki-card)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-11-22 Wed 11:20]</span></span>

    <iframe width="560" height="315" src="https://www.youtube.com/embed/dmcfsEEogxs?start=30" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<a id="orgbc97193"></a>

# Arthas


<a id="org97fbe80"></a>

## Modify java file and reload

    jad --source-only com.example.demo.arthas.user.UserController > /tmp/UserController.java
    
    mc /tmp/UserController.java -d /tmp
    
    retransform /tmp/com/example/demo/arthas/user/UserController.class


<a id="org407e7de"></a>

### [retransform | arthas](https://arthas.aliyun.com/doc/retransform.html#%E7%BB%93%E5%90%88-jad-mc-%E5%91%BD%E4%BB%A4%E4%BD%BF%E7%94%A8)

Captured On: <span class="timestamp-wrapper"><span class="timestamp">[2023-12-12 Tue 17:22]</span></span>


<a id="org4773cbd"></a>

# Twitter


<a id="org71dc91f"></a>

## Search user hot tweets

from:baibanbaonet min\_faves:10


<a id="org4f5313f"></a>

# Logseq


<a id="org7d6e8db"></a>

## Install local plugin

Place unpacked plugin folder under **~/.logseq/plugins** ,then restart logseq


<a id="org3c713bd"></a>

# MAT


<a id="org91446e1"></a>

## Install mat on mac arch m2

版本：Eclipse Memory Analyzer Version 1.15.0，需要JDK17以上版本

打开访达 -> 应用程序 -> 找到mat【右键点击 “显示包内容”】 -> 找到info.plist文件，在其dict节点内，追加下列环境变量：

    <string>-vm</string>
    <string>/Users/tomyli/.sdkman/candidates/java/17.0.9-jbr/bin</string>


<a id="org648de5d"></a>

# System


<a id="org1038ef6"></a>

## Use vcpkg in clion

In clion setting -> CMake options, Add

    -DCMAKE_TOOLCHAIN_FILE=[vcpkg root]/scripts/buildsystems/vcpkg.cmake

<https://www.cnblogs.com/lancediarmuid/p/17333985.html>


<a id="org50d3135"></a>

## Make file rule

prerequisites中如果有一个以上的文件比target文件要新的话，command所定义的命令就会被执行。这就是Makefile的规则

<https://blog.csdn.net/haoel/article/details/2886>


<a id="orgfc61b77"></a>

# Clion


<a id="org3227b7a"></a>

## Disable clang errors to fixed unknown typename

Go to: Languages & Frameworks -> Clangd
Disabled "Show errors and warnings from clangd"

![img](http://pic.imcompany.cn/pic/c6DWuA.png)

![img](http://pic.imcompany.cn/pic/c6DWuA.png)


<a id="org42e4397"></a>

# C


<a id="org4cd01b2"></a>

## Use compat memory allocate

    struct __attribute__ ((__packed__)) sdshdr8 {};


<a id="orgfe246c5"></a>

# AI


<a id="org97c0dfb"></a>

## Update all ollama models

    ollama list | tail -n +2 | awk '{print $1}' | while read -r model; do
      ollama pull $model
    done

<https://github.com/ollama/ollama/issues/1890>

