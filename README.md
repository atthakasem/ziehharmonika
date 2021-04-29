# Ziehharmonika
A lightweight jQuery accordion plugin. [Demo](https://www.testserver.de/wds_tim/ziehharmonika-demo/)

## Include
```html
<!-- Don't forget to include jQuery -->
<link rel="stylesheet" href="ziehharmonika.css">
<script src="ziehharmonika.js"></script>
```

## Structure
```html
<div class="ziehharmonika">
  <h3><!-- Your headline --></h3>
  <div>
    <!-- Your content -->
  </div>

  <h3><!-- Your headline --></h3>
  <div>
    <!-- Your content -->
  </div>
</div>
```

## Initialize
```javascript
$('.ziehharmonika').ziehharmonika();
```

## Options
Options:

|Option|Type|Default|Description|
|---|---|---|---|
|highlander|boolean|true|Only 1 accordion can be open at any given time.|
|arrow|boolean|true|Arrow down below the headline.|
|collapsible|boolean|false|Allow or disallow last open accordion to be closed.|
|prefix|string or false|false|Give headlines a certain prefix, e.g. "♫ My headline".|
|headline|string|'h3'|Use a headline tag other than h3. In that case, ddjust or overwrite ziehharmonika.css as well.|
|collapseIcons|json or false|{opened: '&ndash;', closed: '+'}|Opened/closed icon on the right hand side of the headline. HTML will be parsed so images can be used as icons as well.|
|collapsibleIconsAlign|'left', 'right'|'right'|Align the collapse icon on either side.|
|scroll|boolean|true|Scrolls to opened accordion element|

Usage example:
```javascript
$('.ziehharmonika').ziehharmonika({
  highlander: false,
  collapsible: true,
  collapseIcons: {
    opened: '☺',
    closed: '○'
  }
});
```
## Actions

|Action|Parameters|Description|
|---|---|---|
|open|boolean: scroll (optional)|Opens a specific accordion, taking your options into account, and scrolls to it. Returns the affected element(s).|
|close|N/A|Closes a specific accordion, taking your options into account. Returns the affected element(s) even if the action fails.|

The actions 'closeAll', 'forceClose', and 'forceCloseAll' are too wonky to be listed here. Use with caution.

Usage example:
```javascript
$('.ziehharmonika h3:eq(0)').ziehharmonika('open', false);
```

## License
MIT
