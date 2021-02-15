# cz-commit-meant

Forked from the [cz-conventional-changelog](https://github.com/commitizen/cz-conventional-changelog) project.

## Configuration

### package.json

You specify the configuration through the package.json's `config.commitizen` key.

```json5
{
  // ...
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-commit-meant",
      "disableScopeLowerCase": false,
      "disableSubjectLowerCase": false,
      "maxHeaderWidth": 100,
      "maxLineWidth": 100,
      "defaultType": "",
      "defaultScope": "",
      "defaultSubject": "",
      "defaultBody": "",
      "defaultIssues": "",
      "types": {
        // ...
        "feat": {
          "description": "A new feature",
          "title": "Features"
        },
        // ...
      },
    },
  },
  // ...
}
```

### Environment variables

The following environment varibles can be used to override any default configuration or package.json based configuration.

- `CZ_TYPE` = `defaultType`
- `CZ_SCOPE` = `defaultScope`
- `CZ_SUBJECT` = `defaultSubject`
- `CZ_BODY` = `defaultBody`
- `CZ_MAX_HEADER_WIDTH` = `maxHeaderWidth`
- `CZ_MAX_LINE_WIDTH` = `maxLineWidth`

### Commitlint

If using the [commitlint](https://github.com/conventional-changelog/commitlint) js library, the `maxHeaderWidth` configuration property will default to the configuration of the `header-max-length` rule instead of the hard coded value of 100. This can be ovewritten by setting the `maxHeaderWidth` configuration in the `package.json` or the `CZ_MAX_HEADER_WIDTH` environment variable.
