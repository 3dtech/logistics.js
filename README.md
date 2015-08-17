Logistics.js
============

A JavaScript data loading library. No depencies. Small size. Support for: CORS, multiple resource loading, progress indicator, localStorage caching (JSON, XML, text, html, binary, images).

Usage
-----

Get a single resource

```javascript
Logistics.getJSON("http://example.com/file.json").success(function(result, dt){

});
```
There are also other shorthand methods: getImage, getBinary, getXML, getText


Called when all queued items are loaded. There is a 5ms delay for checking the finished state.
```javascript
Logistics.onFinishedLoading(function(){

});
```

Event for loading progress
```javascript
Logistics.onProgress(function(percentage){

});
```

Load multiple resources at calls after all are loaded
```javascript
Logistics.getMultiple(
	{
		"foo": {"url": "http://example.com/file.json", "type": "json"},
		"bar": {"url": "http://example.com/file.jpeg", "type": "image"}
	},
	function(data){
		var foo = data["foo"];
	}
);
```