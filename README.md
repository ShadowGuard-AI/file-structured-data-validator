![Banner](banner.png)

# file-structured-data-validator
Validates structured data files (e.g., JSON, XML, YAML) against a predefined schema, flagging any deviations that could indicate tampering or corruption. - Focused on File operations and analysis

## Install
`git clone https://github.com/ShadowStrikeHQ/file-structured-data-validator`

## Usage
`./file-structured-data-validator [params]`

## Parameters
- `-h`: Show help message and exit
- `--file_type`: Type of the data file (json, xml, yaml)

Dependencies are listed in requirements.txt: jsonschema, PyYAML, and lxml (lxml is used for XML validation against an XSD schema).

## Exit codes
Exit 0 means the data validated successfully against the schema. Exit 1 means validation failed, or the data or schema file could not be loaded or parsed, or a path was invalid. An empty YAML file, or a YAML file holding only null, parses to a null value and is validated against the schema like any other value: it passes a schema that allows null and fails one that does not.

Running the tool creates no files. The sample data.json and schema.json files shipped in this repo serve as the example.

## License
Copyright (c) ShadowStrikeHQ
