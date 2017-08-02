# eslint-plugin-kiwi-graphql

Rules for Kiwi.com GraphQL

## Installation

You'll first need to install [ESLint](http://eslint.org). Next, install this plugin:

```
yarn add --dev eslint-plugin-kiwi-graphql
```

## Usage

Add `kiwi-graphql` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
    "plugins": [
        "kiwi-graphql"
    ]
}
```

Then configure the rules you want to use under the rules section.

```json
{
    "rules": {
        "kiwi-graphql/only-nullable-fields": "error"
    }
}
```

## Supported Rules

* [only-nullable-fields](docs/rules/only-nullable-fields.md)

## Developers

Not sure about the AST? Try this: https://astexplorer.net/

Release new version:

```
npm version patch
- or -
npm version minor
- or -
npm version major


npm publish --access public
```
