# ECS Field Definition YAML Validation

ECS developers can use the [YAML Language](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) Visual Studio Code extension
and the provided [`schema.json`](./schema.json) file to better understand the shape of a ECS field definition YAML file, including its value
sets, defaults, and attribute descriptions.

## Install the Extension

Install the [YAML Language](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) extension into your VSCode editor.

## Associating the Schema

Once the YAML extension is installed, you can associate the JSON schema file with the desired file glob patterns. The configuration
for yaml.schemas is located in your [user and workspace settings](https://code.visualstudio.com/docs/getstarted/settings#_creating-user-and-workspace-settings).

To associate the ECS field definition JSON schema to the schema directories from the [ECS repo](https://github.com/elastic/ecs):

```json
"yaml.schemas": {
    "https://raw.githubusercontent.com/ebeahan/ecs-vscode/main/schema/schema.json": [ "schemas/*.yml", "experimental/schemas/*.yml" ]
}
```

The `yaml.schemas` configuration supports multiple file formats. The full documentation can be found [here](https://github.com/redhat-developer/vscode-yaml#associating-a-schema-to-a-glob-pattern-via-yamlschemas).