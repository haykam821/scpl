
## Get Dictionary Value / GetDictionaryValue (internally `is.workflow.actions.getvalueforkey`)


## description

### summary

Gets the value for the specified key in the dictionary passed into the action. 


### note

You can reference values deep inside of a dictionary by providing multiple keys separated by dots. For example, to get the value "soup" from the dictionary {"beverages": [{"favorite": "soup"}]}, you can specify the key path "beverages.1.favorite".


### usage
```
GetDictionaryValue get=("Value" | "All Keys" | "All Values" | variable) key="string"
```

### arguments

---

### get: Enumeration [(Docs)](https://pfgithub.github.io/shortcutslang/gettingstarted#enum-select-field)
**Default Value**: `"Value"`


Accepts a string 
containing one of the options:

- `Value`
- `All Keys`
- `All Values`

---

### key: Text [(Docs)](https://pfgithub.github.io/shortcutslang/gettingstarted#text-field)
**Placeholder**: `"example"`
**Allows Variables**: true

**Only enabled if**: argument WFGetDictionaryValueType == `Value`

Accepts a string 
or text
with the text. Does not allow newlines.

---

### source json (for developers)

```json
{
	"ActionClass": "WFGetDictionaryValueAction",
	"ActionKeywords": [
		"json",
		"plist",
		"xml",
		"urlencoded",
		"query",
		"string",
		"for",
		"key"
	],
	"Category": "Scripting",
	"Description": {
		"DescriptionNote": "You can reference values deep inside of a dictionary by providing multiple keys separated by dots. For example, to get the value \"soup\" from the dictionary {\"beverages\": [{\"favorite\": \"soup\"}]}, you can specify the key path \"beverages.1.favorite\".",
		"DescriptionSummary": "Gets the value for the specified key in the dictionary passed into the action. "
	},
	"IconName": "Scripting.png",
	"Input": {
		"Multiple": false,
		"Required": true,
		"Types": [
			"WFDictionaryContentItem"
		]
	},
	"InputPassthrough": false,
	"LastModifiedDate": "2016-10-10T19:00:00.000Z",
	"Name": "Get Dictionary Value",
	"Output": {
		"Multiple": true,
		"OutputName": "Dictionary Value",
		"Types": [
			"WFStringContentItem",
			"WFNumberContentItem",
			"WFDateContentItem",
			"WFDictionaryContentItem",
			"WFBooleanContentItem"
		]
	},
	"Parameters": [
		{
			"Class": "WFEnumerationParameter",
			"DefaultValue": "Value",
			"DisallowedVariableTypes": [
				"Ask",
				"Variable"
			],
			"Items": [
				"Value",
				"All Keys",
				"All Values"
			],
			"Key": "WFGetDictionaryValueType",
			"Label": "Get"
		},
		{
			"AutocapitalizationType": "None",
			"Class": "WFTextInputParameter",
			"DisableAutocorrection": true,
			"Key": "WFDictionaryKey",
			"Label": "Key",
			"Placeholder": "example",
			"RequiredResources": [
				{
					"WFParameterKey": "WFGetDictionaryValueType",
					"WFParameterValue": "Value",
					"WFResourceClass": "WFParameterRelationResource"
				}
			],
			"TextAlignment": "Right"
		}
	],
	"Subcategory": "Dictionaries"
}
```
