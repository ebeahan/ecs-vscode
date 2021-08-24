# ecs-vscode

A set of YAML snippets for working with the [Elastic Common Schema (ECS)](https://www.elastic.co/guide/en/ecs/current/ecs-reference.html) field definitions.

## Elastic Common Schema support for Visual Studio Code

A collection of YAML snippets for faster development of ECS field definitions in [Visual Studio Code](https://code.visualstudio.com/). See the VSCode [docs](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_creating-your-own-snippets) for more detail around creating code snippets.

## Snippets

### New ECS Field

```yaml
- name: $1
  level: ${2:extended}
  type: ${3:keyword}
  short: $4
  description: >
     $5
  example: $6
```

### New ECS field set

```yaml
---
- name: ${1:$TM_FILENAME_BASE}
  title: $2
  group: ${3:2}
  short: $4
  description: >
    $5
  type: ${6:group}

  fields:

    - name: $7
      level: ${8:extended}
      type: ${9:keyword}
      short: $10
      description: >
        $11
      example: $12
```

### Reusable configuration

```yaml
reusable:
  top_level: ${1:true}
  expected:
    - at: $2
      as: ${3:$TM_FILENAME_BASE}

```
