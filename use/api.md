---
description: Open JSON API for integrating with gitignore.io
---

# API

{% api-method method="get" host="https://www.toptal.com/developers/gitignore" path="/api/list?format=:format:" %}
{% api-method-summary %}
Get All Templates
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="format" type="string" %}
The format of the list response `lines` \(default\) or `json`
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
	"jboss4": {
		"key": "jboss4",
		"name": "JBoss4",
		"contents": "\n### JBoss4 ###\n# gitignore for JBoss v4 projects\n\n\/server\/all\/data\n\/server\/all\/log\n\/server\/all\/tmp\n\/server\/all\/work\n\/server\/default\/data\n\/server\/default\/log\n\/server\/default\/tmp\n\/server\/default\/work\n\/server\/minimal\/data\n\/server\/minimal\/log\n\/server\/minimal\/tmp\n\/server\/minimal\/work\n\n# Note:\n# there may be other directories that contain *.xml.failed or *.war.failed files\n\/server\/default\/deploy\/*.xml.failed\n\/server\/default\/deploy\/*.war.failed\n",
		"fileName": "JBoss4.gitignore"
	},
	"extjs": {
		"key": "extjs",
		"name": "ExtJs",
		"contents": "\n### ExtJs ###\n.architect\nbootstrap.css\nbootstrap.js\nbootstrap.json\nbootstrap.jsonp\nbuild\/\nclassic.json\nclassic.jsonp\next\/\nmodern.json\nmodern.jsonp\nresources\/sass\/.sass-cache\/\nresources\/.arch-internal-preview.css\n.arch-internal-preview.css\n",
		"fileName": "ExtJs.gitignore"
	}
	...
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



