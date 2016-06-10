#ShowLayout

This bookmarklet with paint the elements on your page various colours so that you can easily see element sizes and debug layout issues.

Drags the ShowLayout link into your bookmarks, click on it when on any page to use.

<div class="container">
	<h1>
		<a href="javascript: (function (){     var newcss = '* { background-color: rgba(255,0,0,.2)!important; }* * { background-color: rgba(0,255,0,.2)!important; }* * * { background-color: rgba(0,0,255,.2)!important; }* * * * { background-color: rgba(255,0,255,.2)!important; }* * * * * { background-color: rgba(0,255,255,.2)!important; }* * * * * * { background-color: rgba(255,255,0,.2)!important; }';     if ('\v'=='v') { document.createStyleSheet().cssText = newcss;     } else {         var tag = document.createElement('style'); tag.type = 'text/css'; document.getElementsByTagName('head')[0].appendChild(tag);          tag[ (typeof document.body.style.WebkitAppearance=='string') /* webkit only */ ? 'innerText' : 'innerHTML'] = newcss;         } })();">ShowLayout</a>
	</h1>
</div>

[Boomark page here](http://maneeshchiba.github.io/showLayout/)

Or just inject this code into pages you working on:
```javascript
javascript: (function() {
    var newcss = '* { background-color: rgba(255,0,0,.2)!important; }* * { background-color: rgba(0,255,0,.2)!important; }* * * { background-color: rgba(0,0,255,.2)!important; }* * * * { background-color: rgba(255,0,255,.2)!important; }* * * * * { background-color: rgba(0,255,255,.2)!important; }* * * * * * { background-color: rgba(255,255,0,.2)!important; }';
    if ('\v' == 'v') /* ie only */ { document.createStyleSheet().cssText = newcss; } else {
        var tag = document.createElement('style');
        tag.type = 'text/css';
        document.getElementsByTagName('head')[0].appendChild(tag);
        tag[(typeof document.body.style.WebkitAppearance == 'string') /* webkit only */ ? 'innerText' : 'innerHTML'] = newcss; } })();
```