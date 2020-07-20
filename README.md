# snepet - Sample Vscode Snippets Extenion

- To create a vscode snippet extenion add 👇 in your package.json

```json
{
  "contributes": {
    "snippets": [
      {
        "language": "lang",
        "path": "path"
      }
    ]
  }
}
```

- Tag your extension as a snippet extension by adding 👇

```json
{ "categories": ["Snippets"] }
```

- vscode manages the creation and the refreshing of the snippet files

## Prefix,Body,Description

| Property      | Description                                                         |
| ------------- | ------------------------------------------------------------------- |
| `Name`        | The name of the Snippet its displayed if no description is provided |
| `Prefix`      | One or More trigger words that display in intellisence              |
| `Body`        | One or more lines of content that join to craete the code snippet   |
| `Description` | The descrition of the Snippet displayed vai intelliSence            |

## Snippet Scope

- Snippets are scoped so that only relevant snippets are suggested
- Snippets are scoped to
  - A `language` - Possiby all
  - A `Project` - Possibly all

### Language Snippet Scope

- Language scoped snippets are located in a json file named `language.json` eg javascript.json
- Globalally scoped snippets are located in a file named `filename.code-snippets`
- Globally scoped snippets can be restricted by adding 👇

```json
{ "scope": ["lang_1", "lang_2"] }
```

### Project Snippet Scope

- Snippets can also be created only for a particular project
- The Snippets are loacted in a json file with the suffix `.code-snippetes`
- The file is loacted in the root of your project in the .vscode directory

## Snippet Syntax

- ### Tabstopts

  - You can use `$1, $2, $3 ... $n {n > 0}` to create occurences where the cursor will be placed
  - If more than one place have the same value `$n` they will be updated in sync
  - The cursor moved through the values `$n` in ascending order
  - `$0` is special - This is the final place where the cursor is placed after instering the snippet

- ### Placeholders

  - You can add place holders as default text using `${2:foo}`
  - Placeholders are placed in such a way that they can be easly changed
  - Placeholders can also be nested `${1:one ${2:two}}`

- ### Choises

  - Insted of using one placeholder you can use a list of choises
  - Separate the choises using `|` eg `${1|one,two,three,four,five|}`

- ### Variables

  - You can insert variables using `$name` or `${name:default}`
  - Table of Variabeles ...

- ### Variables Transforms

  - 
