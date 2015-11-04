Названия классов из нескольких слов пишем кэмелкейсом:
```
.menuCrazyNice
```
 
 
Элемент именуем по принципу `.blockName__elemName`:
```
<div class="menu">
  ...
  <span class="menu__item"></span>
</div>
```
```
.menu__item { color: red; }
```
1) Селектор класса почти самый быстрый, не надо писать `.blockName .elemName` 
2) Независимость стилей, сравни: 
```
<div class="menu">
  ...
  <span class="item"><b class="item">...</b></span>
  <span class="item"></span>
</div>
```
`.menu .item` выберет оба тэга
 
 
 

При 1 уровне вложенности *сложных* блоков использовать селектор дочернего элемента:
```
.b > .elem
```
а не
```
.b .elem
```
(в случае если в такой блок будет включен подобный, стили `.elem` не будут перебиты).
В случае простых блочков это можно не делать.

