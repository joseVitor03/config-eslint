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
    "trybe-backend"
  ],
  "rules": {
    "max-len": ["error", { "code": 80 }],
    "max-lines-per-function": ["error", { "max": 30 }],
    "indent": ["error", 2],
    "semi": ["error", "always"]
  },
  "settings": {
    "import/resolver": {
      "node": {
        "extensions": [".js", ".jsx", ".ts", ".tsx"]
      }
    }
  }
}

```
