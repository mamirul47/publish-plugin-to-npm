# Guideline for publish a plugin nodejs in npm

1) first please install this dev dependency
```bash
npm i -D @types/node rimraf typescript
```

2) create folder /src

```bash
mkdir src
```

3) create tsconfig.json with this value

```json
{
    "compilerOptions": {
        "target": "ES6",
        "module": "CommonJS",
        "declaration": true,
        "outDir": "./dist",
        "strict": true
    },
    "include": [
        "src/**/*.ts"
    ],
    "exclude": [
        "node_modules",
        "dist"
    ]
}
```

4) Replace the package script in package.json with this value

```json
"scripts": {
    "build": "rimraf ./dist && tsc",
    "clean": "rimraf ./dist"
  },
  
```