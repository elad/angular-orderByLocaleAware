# orderByLocaleAware

This is a copy of Angular's orderBy filter with locale-aware bits added.

What is locale-aware ordering? It means that locale is taken into account when ordering. For example, in the `he-IL` locale, Hebrew strings take priority to English strings.

## Install

```
bower install orderByLocaleAware
```

## Use

Include it in your project, add a dependency, and then same as you would `orderBy`. Mark localized properties with the **`@`** prefix:

```html
<div ng-repeat="item in items | orderByLocaleAware:'+@name'">
  ...
</div>
```

Setting the locale is done through `orderByLocaleAwareConfig`:

```js
angular.module('myApp', ['orderByLocaleAware'])
.controller('myController', function(orderByLocaleAwareConfig) {
  orderByLocaleAwareConfig.localeId = 'he-IL';
});
```
