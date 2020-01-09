# Async-Content-Loader

Library for content managing in browser environment.
It has no dependencies.

## Install
```bash
    npm install async-content-loader
```

## How to use

### globalContentLoaded - Promise
Waiting for content
```javascript
    import loader from '/node_modules/async-content-loader';
    
    //Waiting for content loaded
    loader.globalContentLoaded.then(function () {
        //You will be here when all content loaded
    });
```

### loadLibrary({ path, id })
Load js script in head section with user defined id.
The script with that id will be loaded only once. 
On second call it returns loaded script.

```javascript 
    loader.loadLibrary({ path: '/test.js', id: 'Test'}).then(function (script) {
    
    }); 
```

### request({ path, option })
Request content from server
```javascript 
    loader.request({ path: '/test.html').then(function (content) {
    
    }); 
```

### json({ path, options })
Request content from server in json format.
The content will be parsed using standart JSON.parse method
```javascript 
    loader.json({ path: '/test.json').then(function (content) {
    
    }); 
```
