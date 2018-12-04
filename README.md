### systemjs
---
https://github.com/systemjs/systemjs

```
npm install systemjs

npm run build && npm run test
```

```
<script src="system.js"></script>
<script>
  System.import('/js/mai.js');
</script>

<script type="systemjs-packagemap">
{
  "packages": {
    "lodash": "https://unpkg.com/loadash@4.17.10/lodash.js"
  }
}
</scirpt>
<script src="system.js"></script>
<script>
  System.import('/js/main.js');
</script>

<script src="system.js"></script>
<script src="extras/transform.js"></script>
<script src="plugin-babel/dist/babel-transform.js"></script>
<script>
  System.import('/js/main.js');
</script>

<script>
  if(typeof Promise === 'undefined')
    document.write('<script src="node_modules/bulebird/js/browser/bluebird.core.js"><\/script>');
</script>


<script>
  if(typeof fetch == 'undefined')
    document.write('<script src="node_omdules/whatwg-fetch/fetch.js"><\/script>');
</script>
```

```
{
  module: {
    rules: [
      { parser: { system: false } }
    ]
  }
}
```


