
.. include:: ../Includes.txt
.. highlight:: rst

.. _writing-rest-codeblocks-with-syntax-highlighting:

===================================
Codeblocks with Syntax Highlighting
===================================

On this page:

.. rst-class:: compact-list

.. contents::
   :local:
   :backlinks: top


.. _writing-rest-codeblocks-syntactically-correct:

Use syntactically correct code
==============================

.. attention::

   **Please: No syntax errors!**

   Syntax highlighting only works if the lexer can parse the code without errors.
   In other words: If there's a syntax error in the code the highlighting will not work.


   **Wrong:** ::

      .. highlight: php

      ::

         $a = array(
            'one' => 1,
            ...
         );

   **Correct:** ::

      highlight: php

      ::

         $a = array(
            'one' => 1,
            // ...
         );





`Sphinx <http://www.sphinx-doc.org/en/stable/>`__ uses
`Pygments <http://pygments.org/>`__ for highlighting. On a machine that has Pygments installed
the command `pygmentize -L` will list all available lexers.


.. _writing-rest-codeblocks-highlight-directive:


Highlight directive
===================

You can set the default language with the *highlight* directive. All following codeblocks
will use the language as spedified for syntax highlighting.

If all of your codeblocks have the same language, it is easier to just set this once at the
beginning of the file.

This way, you don't need to set the language for each code-block (`.. code-block:: LANG`).

Use reST::


   .. highlight:: rest


Use PHP::

   .. highlight:: php



.. _writing-rest-codeblocks-codeblock-directive:

Codeblock directive
===================

To set the language for one code-block at a time, use the `code-block` directive::


      .. code-block:: sql

   or::

      .. code-block:: php

   or::

      .. code-block:: guess


To set a simple codeblock without specifying the language (because it is
for example already correctly set by the `highlight` directive as described
above), you can either use the `code-block` directive or just the shorthand (`::`).


Sample code block (use `::` as shorthand for `.. code-block::`):


.. code-block:: php

   some text::

      $this->a = 'some string';


*How it looks:*

some text::

   some code


.. _writing-rest-codeblocks-available-lexers:

Available Lexers
================

You can use any of the following names of lexers:



`| bash, sh, ksh, shell |` for example all mean the same lexer:

abap \|
abnf \|
ada, ada95, ada2005 \|
adl \|
agda \|
ahk, autohotkey \|
alloy \|
ampl \|
antlr-as, antlr-actionscript \|
antlr-cpp \|
antlr-csharp, antlr-c# \|
antlr-java \|
antlr-objc \|
antlr-perl \|
antlr-python \|
antlr-ruby, antlr-rb \|
antlr \|
apacheconf, aconf, apache \|
apl \|
applescript \|
arduino \|
as, actionscript \|
as3, actionscript3 \|
aspectj \|
aspx-cs \|
aspx-vb \|
asy, asymptote \|
at, ambienttalk, ambienttalk/2 \|
autoit \|
awk, gawk, mawk, nawk \|
basemake \|
bash, sh, ksh, shell \|
bat, batch, dosbatch, winbatch \|
bbcode \|
bc \|
befunge \|
blitzbasic, b3d, bplus \|
blitzmax, bmax \|
bnf \|
boo \|
boogie \|
brainfuck, bf \|
bro \|
bugs, winbugs, openbugs \|
c-objdump \|
c \|
ca65 \|
cadl \|
camkes, idl4 \|
cbmbas \|
ceylon \|
cfc \|
cfengine3, cf3 \|
cfm \|
cfs \|
chai, chaiscript \|
chapel, chpl \|
cheetah, spitfire \|
cirru \|
clay \|
clean \|
clojure, clj \|
clojurescript, cljs \|
cmake \|
cobol \|
cobolfree \|
coffee-script, coffeescript, coffee \|
common-lisp, cl, lisp \|
componentpascal, cp \|
console, shell-session \|
control, debcontrol \|
coq \|
cpp, c++ \|
cpp-objdump, c++-objdumb, cxx-objdump \|
cpsa \|
crmsh, pcmk \|
croc \|
cryptol, cry \|
csharp, c# \|
csound, csound-orc \|
csound-document, csound-csd \|
csound-score, csound-sco \|
css+django, css+jinja \|
css+erb, css+ruby \|
css+genshitext, css+genshi \|
css+lasso \|
css+mako \|
css+mako \|
css+mozpreproc \|
css+myghty \|
css+php \|
css+smarty \|
css \|
cucumber, gherkin \|
cuda, cu \|
cypher \|
cython, pyx, pyrex \|
d-objdump \|
d \|
dart \|
delphi, pas, pascal, objectpascal \|
dg \|
diff, udiff \|
django, jinja \|
docker, dockerfile \|
doscon \|
dpatch \|
dtd \|
duel, jbst, jsonml+bst \|
dylan-console, dylan-repl \|
dylan-lid, lid \|
dylan \|
earl-grey, earlgrey, eg \|
easytrieve \|
ebnf \|
ec \|
ecl \|
eiffel \|
elixir, ex, exs \|
elm \|
emacs, elisp, emacs-lisp \|
erb \|
erl \|
erlang \|
evoque \|
extempore \|
ezhil \|
factor \|
fan \|
fancy, fy \|
felix, flx \|
fish, fishshell \|
flatline \|
fortran \|
fortranfixed \|
foxpro, vfp, clipper, xbase \|
fsharp \|
gap \|
gas, asm \|
genshi, kid, xml+genshi, xml+kid \|
genshitext \|
glsl \|
gnuplot \|
go \|
golo \|
gooddata-cl \|
gosu \|
groff, nroff, man \|
groovy \|
gst \|
haml \|
handlebars \|
haskell, hs \|
haxeml, hxml \|
hexdump \|
hsail, hsa \|
html+cheetah, html+spitfire, htmlcheetah \|
html+django, html+jinja, htmldjango \|
html+evoque \|
html+genshi, html+kid \|
html+handlebars \|
html+lasso \|
html+mako \|
html+mako \|
html+myghty \|
html+php \|
html+smarty \|
html+twig \|
html+velocity \|
html \|
http \|
hx, haxe, hxsl \|
hybris, hy \|
hylang \|
i6t \|
idl \|
idris, idr \|
iex \|
igor, igorpro \|
inform6, i6 \|
inform7, i7 \|
ini, cfg, dosini \|
io \|
ioke, ik \|
irc \|
isabelle \|
j \|
jade \|
jags \|
jasmin, jasminxt \|
java \|
javascript+mozpreproc \|
jcl \|
jlcon \|
js+cheetah, javascript+cheetah, js+spitfire, javascript+spitfire \|
js+django, javascript+django, js+jinja, javascript+jinja \|
js+erb, javascript+erb, js+ruby, javascript+ruby \|
js+genshitext, js+genshi, javascript+genshitext, javascript+genshi \|
js+lasso, javascript+lasso \|
js+mako, javascript+mako \|
js+mako, javascript+mako \|
js+myghty, javascript+myghty \|
js+php, javascript+php \|
js+smarty, javascript+smarty \|
js, javascript \|
jsgf \|
json \|
jsonld, json-ld \|
jsp \|
julia, jl \|
kal \|
kconfig, menuconfig, linux-config, kernel-config \|
koka \|
kotlin \|
lagda, literate-agda \|
lasso, lassoscript \|
lcry, literate-cryptol, lcryptol \|
lean \|
less \|
lhs, literate-haskell, lhaskell \|
lidr, literate-idris, lidris \|
lighty, lighttpd \|
limbo \|
liquid \|
live-script, livescript \|
llvm \|
logos \|
logtalk \|
lsl \|
lua \|
make, makefile, mf, bsdmake \|
mako \|
mako \|
maql \|
mask \|
mason \|
mathematica, mma, nb \|
matlab \|
matlabsession \|
minid \|
modelica \|
modula2, m2 \|
monkey \|
moocode, moo \|
moon, moonscript \|
mozhashpreproc \|
mozpercentpreproc \|
mql, mq4, mq5, mql4, mql5 \|
mscgen, msc \|
mupad \|
mxml \|
myghty \|
mysql \|
nasm \|
ncl \|
nemerle \|
nesc \|
newlisp \|
newspeak \|
nginx \|
nimrod, nim \|
nit \|
nixos, nix \|
nsis, nsi, nsh \|
numpy \|
objdump-nasm \|
objdump \|
objective-c++, objectivec++, obj-c++, objc++ \|
objective-c, objectivec, obj-c, objc \|
objective-j, objectivej, obj-j, objj \|
ocaml \|
octave \|
odin \|
ooc \|
opa \|
openedge, abl, progress \|
pacmanconf \|
pan \|
parasail \|
pawn \|
perl, pl \|
perl6, pl6 \|
php, php3, php4, php5 \|
pig \|
pike \|
pkgconfig \|
plpgsql \|
postgresql, postgres \|
postscript, postscr \|
pot, po \|
pov \|
powershell, posh, ps1, psm1 \|
praat \|
prolog \|
properties, jproperties \|
protobuf, proto \|
ps1con \|
psql, postgresql-console, postgres-console \|
puppet \|
py3tb \|
pycon \|
pypylog, pypy \|
pytb \|
python, py, sage \|
python3, py3 \|
qbasic, basic \|
qml, qbs \|
qvto, qvt \|
racket, rkt \|
ragel-c \|
ragel-cpp \|
ragel-d \|
ragel-em \|
ragel-java \|
ragel-objc \|
ragel-ruby, ragel-rb \|
ragel \|
raw \|
rb, ruby, duby \|
rbcon, irb \|
rconsole, rout \|
rd \|
rebol \|
red, red/system \|
redcode \|
registry \|
resource, resourcebundle \|
rexx, arexx \|
rhtml, html+erb, html+ruby \|
roboconf-graph \|
roboconf-instances \|
robotframework \|
rql \|
rsl \|
rst, rest, restructuredtext \|
rts, trafficscript \|
rust \|
sass \|
sc, supercollider \|
scala \|
scaml \|
scheme, scm \|
scilab \|
scss \|
shen \|
silver \|
slim \|
smali \|
smalltalk, squeak, st \|
smarty \|
sml \|
snobol \|
sourceslist, sources.list, debsources \|
sp \|
sparql \|
spec \|
splus, s, r \|
sql \|
sqlite3 \|
squidconf, squid.conf, squid \|
ssp \|
stan \|
swift \|
swig \|
systemverilog, sv \|
tads3 \|
tap \|
tcl \|
tcsh, csh \|
tcshcon \|
tea \|
termcap \|
terminfo \|
terraform, tf \|
tex, latex \|
text \|
thrift \|
todotxt \|
trac-wiki, moin \|
treetop \|
ts, typescript \|
turtle \|
twig \|
typoscript \|
typoscriptcssdata \|
typoscripthtmldata \|
urbiscript \|
vala, vapi \|
vb.net, vbnet \|
vcl \|
vclsnippets, vclsnippet \|
vctreestatus \|
velocity \|
verilog, v \|
vgl \|
vhdl \|
vim \|
wdiff \|
x10, xten \|
xml+cheetah, xml+spitfire \|
xml+django, xml+jinja \|
xml+erb, xml+ruby \|
xml+evoque \|
xml+lasso \|
xml+mako \|
xml+mako \|
xml+myghty \|
xml+php \|
xml+smarty \|
xml+velocity \|
xml \|
xquery, xqy, xq, xql, xqm \|
xslt \|
xtend \|
xul+mozpreproc \|
yaml+jinja, salt, sls \|
yaml \|
zephir \|

**Tip:** Try the Pygments Demo at http://pygments.org/


.. _writing-rest-codeblocks-some-more-examples:

Some more examples
==================


Example 1: Turn off highlighting method 1
-----------------------------------------

Source:
~~~~~~~

.. code-block:: rst

   A description:

   .. code-block:: none

      $ tree vendor/composer
      ├── ClassLoader.php
      ├── LICENSE
      ├── autoload_classmap.php
      ├── ...
      └── installed.json

Result
~~~~~~

A description:

.. code-block:: none

   $ tree vendor/composer
   ├── ClassLoader.php
   ├── LICENSE
   ├── autoload_classmap.php
   ├── ...
   └── installed.json


Example 2: Turn off highlighting method 2
-----------------------------------------

Source:
~~~~~~~

.. code-block:: rst

   .. highlight:: none

   A description::

      $ tree vendor/composer
      ├── ClassLoader.php
      ├── LICENSE
      ├── autoload_classmap.php
      ├── ...
      └── installed.json

Result
~~~~~~

.. highlight:: none

A description::

   $ tree vendor/composer
   ├── ClassLoader.php
   ├── LICENSE
   ├── autoload_classmap.php
   ├── ...
   └── installed.json
