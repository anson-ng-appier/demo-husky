# demo-husky


## prettier and eslint@^3
```
npm install lint-staged@^13 prettier@^2

```
package.json
``
{

  "scripts": {
    ...
    "prettier": "prettier --write --no-semi --single-quote \"src/**/*.+(js|json)\"",
    "lint-fix": "eslint --fix --ext .js,.jsx src",
  },
  ...

  "lint-staged": {
    "src/**/*.{js}": [
      "npm run prettier",
      "npm run lint-fix",
      "git add"
    ]
  }
}


```

## husky
```
npm init
npm install husky@8.0.3 --save-dev
npx husky add .husky/pre-commit "npx lint-fix"
```


```
"lint-fix": "eslint --fix --ext .js,.jsx src"
"prettier": "prettier --write --no-semi --single-quote \"src/**/*.+(js|json)\"",
```
