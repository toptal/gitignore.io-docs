# Command Line

After the function is created, the `gi` command will give you command line access to the gitignore.io API.  

{% hint style="info" %}
Use `gig`if you are on Windows
{% endhint %}

### Preview

Show output on the command line.

{% tabs %}
{% tab title="Command" %}
```bash
gi linux,java
```
{% endtab %}

{% tab title="Response" %}
```text
# Created by https://www.toptal.com/developers/gitignore/api/linux,java
# Edit at https://www.toptal.com/developers/gitignore?templates=linux,java

### Java ###
# Compiled class file
*.class

# Log file
*.log

# BlueJ files
*.ctxt

# Mobile Tools for Java (J2ME)
.mtj.tmp/

# Package Files #
*.jar
*.war
*.nar
*.ear
*.zip
*.tar.gz
*.rar

# virtual machine crash logs, see http://www.java.com/en/download/help/error_hotspot.xml
hs_err_pid*

### Linux ###
*~

# temporary files which can be created if a process still has a handle open of a deleted file
.fuse_hidden*

# KDE directory preferences
.directory

# Linux trash folder which might appear on any partition or disk
.Trash-*

# .nfs files are created when an open file is removed but is still being accessed
.nfs*


# End of https://www.toptal.com/developers/gitignore/api/linux,java
```
{% endtab %}
{% endtabs %}

### Global

Append Operating System and IDE settings to global .gitignore.

```bash
gi linux,eclipse >> ~/.gitignore_global
```

### Project

Appending Programming Language settings to your projects .gitignore.

```bash
gi java,python >> .gitignore
```

### List

{% tabs %}
{% tab title="Command" %}
```text
gi list
```
{% endtab %}

{% tab title="Response" %}
```bash
1c,1c-bitrix,a-frame,actionscript,ada
adobe,advancedinstaller,agda,alteraquartusii,altium
android,androidstudio,angular,anjuta,ansible
apachecordova,apachehadoop,appbuilder,appceleratortitanium,appcode
appcode+all,appcode+iml,appengine,aptanastudio,arcanist
archive,archives,archlinuxpackages,aspnetcore,assembler
atmelstudio,ats,audio,automationstudio,autotools
backup,ballerina,basercms,basic,batch
bazaar,bazel,bitrix,bittorrent,blackbox
bluej,bookdown,bower,bricxcc,buck
c,c++,cake,cakephp,calabash
carthage,ceylon,cfwheels,chefcookbook,clean
clion,clion+all,clion+iml,clojure,cloud9
cmake,cocoapods,cocos2dx,cocoscreator,code
code-java,codeblocks,codecomposerstudio,codeigniter,codeio
codekit,coffeescript,commonlisp,composer,compressed
compressedarchive,compression,concrete5,coq,craftcms
crashlytics,crbasic,crossbar,crystal,csharp
cuda,cvs,d,dart,darteditor
data,database,datarecovery,dbeaver,delphi
diskimage,django,dm,docfx,dotfilessh
dotsettings,dreamweaver,dropbox,drupal,drupal7
drupal8,eagle,easybook,eclipse,eiffelstudio
elasticbeanstalk,elisp,elixir,elm,emacs
ember,ensime,episerver,erlang,espresso
executable,expressionengine,extjs,fancy,fastlane
finale,firebase,flashbuilder,flex,flexbuilder
floobits,flutter,font,fontforge,forcedotcom
forgegradle,fortran,freepascal,fsharp,fuelphp
fusetools,games,gcov,genero4gl,geth
ggts,gis,git,gitbook,go
godot,gpg,gradle,grails,greenfoot
grunt,gwt,haskell,hexo,homeassistant
hsp,hugo,hyperledgercomposer,iar,iar_ewarm
iarembeddedworkbench,idris,igorpro,images,infer
inforcrm,intellij,intellij+all,intellij+iml,ionic3
jabref,java,java-web,jboss,jboss-4-2-3-ga
jboss-6-x,jdeveloper,jekyll,jetbrains,jetbrains+all
jetbrains+iml,jigsaw,jmeter,joe,joomla
jspm,julia,jupyternotebook,justcode,kate
kdevelop4,keil,kentico,kicad,kirby2
kobalt,kohana,komodoedit,kotlin,labview
lamp,laravel,latex,lazarus,leiningen
lemonstand,less,liberosoc,librarian-chef,libreoffice
lilypond,linux,lithium,lua,lyx
m2e,macos,magento,magento2,magic-xpa
matlab,maven,mavensmate,mean,mercurial
mercury,metaprogrammingsystem,meteorjs,microsoftoffice,mikroc
moban,modelsim,modx,momentics,monodevelop
mplabx,mule,nanoc,nativescript,ncrunch
nesc,netbeans,nette,nikola,nim
ninja,node,notepadpp,nwjs,objective-c
ocaml,octobercms,opa,opencart,opencv
openfoam,openframeworks,oracleforms,osx,otto
packer,particle,pawn,perl,perl6
ph7cms,phalcon,phoenix,phpcodesniffer,phpstorm
phpstorm+all,phpstorm+iml,pimcore,pinegrow,platformio
playframework,plone,polymer,powershell,premake-gmake
prepros,prestashop,processing,progressabl,psoccreator
puppet-librarian,purebasic,purescript,pvs,pycharm
pycharm+all,pycharm+iml,pydev,python,qml
qooxdoo,qt,qtcreator,r,racket
rails,reactnative,red,redcar,redis
rhodesrhomobile,rider,root,ros,ruby
rubymine,rubymine+all,rubymine+iml,rust,salesforce
salesforcedx,sas,sass,sbt,scala
scheme,scons,scrivener,sdcc,seamgen
senchatouch,serverless,shopware,silverstripe,sketchup
slickedit,smalltalk,snapcraft,solidity,soliditytruffle
sonar,sonarqube,sourcepawn,splunk,spreadsheet
standardml,stata,stdlib,stella,stellar
stylus,sublimetext,sugarcrm,svn,swift
swiftpackagemanager,swiftpm,symfony,symphonycms,synology
synopsysvcs,tags,tarmainstallmate,terraform,test
testcomplete,testinfra,tex,text,textmate
textpattern,theos-tweak,tortoisegit,tower,turbogears2
typings,typo3,umbraco,unity,unrealengine
vaadin,vagrant,valgrind,vapor,venv
vertx,video,vim,virtualenv,virtuoso
visualstudio,visualstudiocode,vivado,vvvv,waf
wakanda,web,webmethods,webstorm,webstorm+all
webstorm+iml,werckercli,windows,wintersmith,wordpress
wyam,xamarinstudio,xcode,xcodeinjection,xilinxise
xilinxvivado,xill,xojo,xtext,y86
yeoman,yii,yii2,zendframework,zephir
zukencr8000
```
{% endtab %}
{% endtabs %}

