# config-eslint-backend


### instale o eslint em seu projeto:
```
npm i eslint --save-dev
```

### Para iniciar as etapas de configuração, execute o comando a seguir:
```
./node_modules/.bin/eslint --init
```

##### Para a primeira pergunta sobre como queremos usar o ESLint, escolha a opção To check syntax and find problems. Isso possibilita a nosso arquivo de configuração encontrar problemas e corrigir a sintaxe de nossos arquivos JavaScript

##### Em seguida, escolha Javascript modules (import/export) para definir o tipo de módulo adotado para o projeto.

##### Para o tipo de framework que vamos utilizar, selecione None of these (você também pode escolher outro de sua preferência).

##### Sinalize que vamos usar TypeScript.

##### Desmarque a opção Browser e selecione Node (use a barra de espaço do teclado para marcar/desmarcar), uma vez que queremos que o nosso projeto rode com o Node. Se estiver trabalhando em um projeto que utilize o Browser como referência, você pode já deixar essa opção selecionada.

##### Escolha o formato JSON, que será o formato do nosso arquivo de configuração.

### Arquivo .eslintrc.json:
```
{
    "root": true,
    "env": {
      "browser": false,
      "node": true,
      "es2021": true,
      "jest": true
    },
    "extends": [
      "plugin:@typescript-eslint/recommended",
      "airbnb-base",
      "plugin:mocha/recommended",
      "airbnb-typescript/base"
    ],
    "parser": "@typescript-eslint/parser",
    "parserOptions": {
      "ecmaVersion": 2019,
      "sourceType": "module",
      "project": "./tsconfig.json"
    },
    "plugins": [
      "@typescript-eslint",
      "sonarjs",
      "mocha"
    ],
    "rules": {
      "no-underscore-dangle": "off",
      "no-console": "off",
      "camelcase": "warn",
      "arrow-parens": [
        2,
        "always"
      ],
      "quotes": [
        2,
        "single"
      ],
      "implicit-arrow-linebreak": "off",
      "consistent-return": "off",
      "@typescript-eslint/naming-convention": [
        "error", { 
          "selector": "property",
          "format": ["strictCamelCase"],
          "filter": {
          "regex": "^_",
          "match": false
        } }
      ],
      "@typescript-eslint/no-unused-vars": [
        "error",
        {
          "argsIgnorePattern": "^_",
          "ignoreRestSiblings": true
        }
      ],
      "@typescript-eslint/lines-between-class-members": ["error", "always", { "exceptAfterSingleLine": true }],
      "no-unused-vars": [
        "error",
        {
          "argsIgnorePattern": "^_",
          "ignoreRestSiblings": true
        }
      ],
      "object-curly-newline": "off",
      "max-params": [
        "error",
        4
      ],
      "max-lines": [
        "error",
        250
      ],
      "max-lines-per-function": [
        "error",
        {
          "max": 20,
          "skipBlankLines": true,
          "skipComments": true
        }
      ],
      "max-len": [
        "error",
        100,
        {
          "ignoreComments": true,
          "ignoreUrls": true
        }
      ],
      "complexity": [
        "error",
        12
      ],
      "import/no-extraneous-dependencies": [
        "off"
      ],
      "sonarjs/cognitive-complexity": [
        "error",
        12
      ],
      "sonarjs/no-one-iteration-loop": [
        "error"
      ],
      "sonarjs/no-identical-expressions": [
        "error"
      ],
      "sonarjs/no-use-of-empty-return-value": [
        "error"
      ],
      "sonarjs/no-extra-arguments": [
        "error"
      ],
      "sonarjs/no-identical-conditions": [
        "error"
      ],
      "sonarjs/no-collapsible-if": [
        "error"
      ],
      "sonarjs/no-collection-size-mischeck": [
        "error"
      ],
      "sonarjs/no-duplicate-string": [
        "error"
      ],
      "sonarjs/no-duplicated-branches": [
        "error"
      ],
      "sonarjs/no-identical-functions": [
        "error"
      ],
      "sonarjs/no-redundant-boolean": [
        "error"
      ],
      "sonarjs/no-unused-collection": [
        "error"
      ],
      "sonarjs/no-useless-catch": [
        "error"
      ],
      "sonarjs/prefer-object-literal": [
        "error"
      ],
      "sonarjs/prefer-single-boolean-return": [
        "error"
      ],
      "sonarjs/no-inverted-boolean-check": [
        "error"
      ]
    }
  }

```
