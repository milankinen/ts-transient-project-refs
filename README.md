Steps to reproduce:

```
$ yarn
$ cd apps/app-a
$ yarn build

yarn run v1.22.10
$ tsc -b --verbose
[5:14:00 PM] Projects in this build:
    * ../../shared/database/tsconfig.ref.json
    * tsconfig.json

[5:14:00 PM] Project '../../shared/database/tsconfig.ref.json' is out of date because output file '../../shared/database/dist/index.js' does not exist

[5:14:00 PM] Building project '{somefolder}/ts-transient-project-refs/shared/database/tsconfig.ref.json'...

../../shared/database/src/index.ts:1:23 - error TS2307: Cannot find module '@myproject/logger' or its corresponding type declarations.

1 import { error } from "@myproject/logger";
                        ~~~~~~~~~~~~~~~~~~~

[5:14:01 PM] Project 'tsconfig.json' can't be built because its dependency '../../shared/database/tsconfig.ref.json' has errors

[5:14:01 PM] Skipping build of project '{somefolder}/ts-transient-project-refs/apps/app-a/tsconfig.json' because its dependency '{somefolder}/ts-transient-project-refs/shared/database/tsconfig.ref.json' has errors


Found 1 error.

error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```
