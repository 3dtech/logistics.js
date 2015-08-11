Logistics.js
============

A JavaScript data loading library. No decencies. Small size. Support for: CORS , multiple resource loading, progress indicator, localStorage caching (JSON, XML, text, html, binary, images).

Usage
-----

```javascript
Logistics.getJSON("http://example.com/file.json").success(function(result, dt){

});
```

```javascript
Logistics.onFinishedLoading(function(data, dt){

});
```

```javascript
Logistics.onProgress(function(data, dt){

});
```

```javascript
Logistics.getMultiple(
	{
		"foo": {"url": "http://example.com/file.json", "type": "json"},
		"bar": {"url": "http://example.com/file.jpeg", "type": "image"}
	},
	function(data){

	}
);
```