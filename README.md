# ⚠️  WARNING - PLEASE, FOR THE LOVE OF ALL THAT IS SACRED, DO NOT USE THIS

A different approach to WebComponents
===

## Use it

```html
<!doctype html>
<x-foo></x-foo>

<script src=webcomponents.js></script>
<script>module.import('x-foo.html')</script>
```

## Create modules

```html
<template>
  <h1>Hello World</h1>
</template>
<script>
  module.exports = WebComponent;
</script>
```

## Build components

```html
<template>
  <h1>Hello World</h1>
</template>
<script>
  module.exports = class extends WebComponent {
    method1() {
      ...
    }
    method2() {
      ...
    }
    created() {
      //this is equivalent of `createdCallback` method
      this.set('property', 'value');
    }
  };
</script>
```

## Use Polymer-style bindings
```html
<template>
  <x-get path=/some-endpoint response={{content}}></x-get>
  <h1>[[title]]</h1>
  <time datetime=[[date]]></time>
  <p>[[content]]</p>
</template>
<script>
  module.import('x-get');
  module.exports = class extends WebComponent {
    ...
  };
</script>
```

