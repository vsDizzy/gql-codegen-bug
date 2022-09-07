# This is minimal repo to reproduce a bug
Issue link: https://github.com/dotansimha/graphql-code-generator/issues/8329

1. download schema:

   ```
   npm run get-schema
   ```

2. generate types:
   ```
   npm start
   ```

Generation fails:

```
    ✖
      Failed to load schema from schema.graphql,introspection.json:
      Unable to find any GraphQL type definitions for the following pointers:
      - schema.graphql
      ,
      - introspection.json
      Error:
      Unable to find any GraphQL type definitions for the following pointers:
      - schema.graphql
      ,
      - introspection.json
      at prepareResult (/workspaces/!gql/node_modules/@graphql-tools/load/cjs/load-typedefs.js:75:15)
      at loadTypedefs (/workspaces/!gql/node_modules/@graphql-tools/load/cjs/load-typedefs.js:39:12)
      at processTicksAndRejections (node:internal/process/task_queues:96:5)
      at async loadSchema (/workspaces/!gql/node_modules/@graphql-tools/load/cjs/schema.js:15:21)
      at async loadSchema (/workspaces/!gql/node_modules/@graphql-codegen/cli/cjs/load.js:36:24)
      at async /workspaces/!gql/node_modules/@graphql-codegen/cli/cjs/codegen.js:193:69
      at async /workspaces/!gql/node_modules/@graphql-codegen/cli/cjs/codegen.js:192:56
```
