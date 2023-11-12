# mesh build error

Steps to reproduce:

1) `npm install`
2) `npm run mesh:build:local`
3) Error: 

```
npm run mesh:build:local

> graphql-apollo-mesh@0.1.1 mesh:build:local
> mesh build --dir ./local_meshrc && rm -rf ./src/.mesh && mv ./local_meshrc/.mesh/ ./src

💡 🕸️  Mesh Cleaning existing artifacts
💡 🕸️  Mesh Reading the configuration
💡 🕸️  Mesh Generating the unified schema
💡 🕸️  Mesh - NetApp_GRID Generating GraphQL schema from OpenAPI schema
💥 🕸️  Mesh - NetApp_GRID Failed to generate the schema TypeError: Cannot convert value to AST: 2017-01-01T00:00:00.000Z.
    at astFromValue (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql/utilities/astFromValue.js:171:11)
    at astFromValue (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql/utilities/astFromValue.js:45:22)
    at /home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql-compose/src/utils/definitionNode.ts:299:25
    at Array.map (<anonymous>)
    at getArgumentsDefinitionNodes (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql-compose/src/utils/definitionNode.ts:284:6)
    at /home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql-compose/src/utils/definitionNode.ts:320:20
    at Array.map (<anonymous>)
    at getFieldDefinitionNodes (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql-compose/src/utils/definitionNode.ts:312:6)
    at getObjectTypeDefinitionNode (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql-compose/src/utils/definitionNode.ts:61:13)
    at ObjectTypeComposer.getType (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/graphql-compose/src/ObjectTypeComposer.ts:991:57)
💥 🕸️  Mesh Error: Schemas couldn't be generated successfully. Check for the logs by running Mesh with DEBUG=1 environmental variable to get more verbose output.
    at getMesh (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/@graphql-mesh/runtime/cjs/get-mesh.js:151:15)
    at async Object.handler (/home/jsmith/sourcecode/project_xyz/mesh_error/node_modules/@graphql-mesh/cli/cjs/index.js:310:53)
```