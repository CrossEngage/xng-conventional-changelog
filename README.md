# xng-conventional-changelog

Status:
[![npm version](https://img.shields.io/npm/v/xng-conventional-changelog.svg?style=flat-square)](https://www.npmjs.org/package/xng-conventional-changelog)
[![npm downloads](https://img.shields.io/npm/dm/xng-conventional-changelog.svg?style=flat-square)](http://npm-stat.com/charts.html?package=xng-conventional-changelog&from=2019-07-25)

Customized fork of [cz-conventional-changelog](https://github.com/CrossEngage/cz-conventional-changelog). Prompts for [conventional changelog](https://github.com/conventional-changelog/conventional-changelog) standard.

## Configuration

### package.json

Like commitizen, you specify the configuration of cz-conventional-changelog through the package.json's `config.commitizen` key.

```json5
{
// ...  default values
    "config": {
        "commitizen": {      
            "path": "./node_modules/cz-conventional-changelog",
            "maxHeaderWidth": 100,
            "maxLineWidth": 100,
            "defaultType": "",
            "defaultScope": "",        
            "defaultSubject": "",
            "defaultBody": "",
            "defaultIssues": ""
        }
    }
// ...    
}
``` 
### Environment variables

The following environment varibles can be used to override any default configuration or package.json based configuration.

* CZ_TYPE = defaultType 
* CZ_SCOPE = defaultScope
* CZ_SUBJECT = defaultSubject
* CZ_BODY = defaultBody
* CZ_MAX_HEADER_WIDTH = maxHeaderWidth
* CZ_MAX_LINE_WIDTH = maxLineWidth

### Commitlint

If using the [commitlint](https://github.com/conventional-changelog/commitlint) js library, the "maxHeaderWidth" configuration property will default to the configuration of the "header-max-length" rule instead of the hard coded value of 100.  This can be ovewritten by setting the 'maxHeaderWidth' configuration in package.json or the CZ_MAX_HEADER_WIDTH environment variable.

