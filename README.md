# node-require-context
> same as `webpack` => [`require.context`](https://webpack.docschina.org/guides/dependency-management/#require-context)  

## Usage  
```npm
npm i --save node-require-context
```
### Example

```js
const requireContext = require('node-require-context')
const context = requireContext('.', true, /\.js$/)
context.keys().forEach(moduleId=>{
    context(moduleId)
})
```

### API
`requireContext ( directory, useSubdirectories, regExp )`  

- `directory`  
>  search dir default '.'  

- `useSubdirectories`  
> `true` will search all child file ; `false` only search current dir ; default `true`  

- `regExp`  
> RegExp match ;  default `/(?:)/`  
