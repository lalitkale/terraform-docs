## terraform-docs tfvars json

Generate JSON format of terraform.tfvars of inputs

### Synopsis

Generate JSON format of terraform.tfvars of inputs

```
terraform-docs tfvars json [PATH] [flags]
```

### Options

```
  -h, --help   help for json
```

### Options inherited from parent commands

```
      --header-from string          relative path of a file to read header from (default "main.tf")
      --no-header                   do not show module header
      --no-inputs                   do not show inputs
      --no-outputs                  do not show outputs
      --no-providers                do not show providers
      --no-requirements             do not show module requirements
      --no-sort                     do no sort items
      --output-values               inject output values into outputs
      --output-values-from string   inject output values from file into outputs
      --sort-by-required            sort items by name and print required ones first
```

### Example

Given the [`examples`](/examples/) module:

```shell
terraform-docs tfvars json ./examples/
```

generates the following output:

    {
      "bool-1": true,
      "bool-2": false,
      "bool-3": true,
      "bool_default_false": false,
      "input-with-code-block": [
        "name rack:location"
      ],
      "input-with-pipe": "v1",
      "input_with_underscores": null,
      "list-1": [
        "a",
        "b",
        "c"
      ],
      "list-2": null,
      "list-3": [],
      "list_default_empty": [],
      "long_type": {
        "bar": {
          "bar": "bar",
          "foo": "bar"
        },
        "buzz": [
          "fizz",
          "buzz"
        ],
        "fizz": [],
        "foo": {
          "bar": "foo",
          "foo": "foo"
        },
        "name": "hello"
      },
      "map-1": {
        "a": 1,
        "b": 2,
        "c": 3
      },
      "map-2": null,
      "map-3": {},
      "no-escape-default-value": "VALUE_WITH_UNDERSCORE",
      "number-1": 42,
      "number-2": null,
      "number-3": "19",
      "number-4": 15.75,
      "number_default_zero": 0,
      "object_default_empty": {},
      "string-1": "bar",
      "string-2": null,
      "string-3": "",
      "string_default_empty": "",
      "string_default_null": null,
      "string_no_default": null,
      "unquoted": null,
      "with-url": ""
    }


###### Auto generated by spf13/cobra on 13-Apr-2020