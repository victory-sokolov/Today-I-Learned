# Environment variables for Angular project

## Load `.env` files for local, development, production stage into `environment.ts` file


### `set-env.ts`

```javascript
const { writeFile } = require('fs');
const { argv } = require('yargs');

let ENV = 'local';

if (process.env.NODE_ENV) {
  ENV = process.env.NODE_ENV;
}

require('dotenv').config({ path: `.env.${ENV}` });


const environment = argv.environment;
const isProduction = environment === 'prod';

const targetPath = `./src/environments/environment.ts`;

const envConfigFile = `
export const environment = {
  production: ${isProduction},
  ENDPOINT: '${process.env.ENDPOINT}'
};
`

writeFile(targetPath, envConfigFile, (err: any) => {
    if (err) {
        console.error(err);
    }

    console.log(`Output generated at ${targetPath}`);
});
```

export NODE_ENV variable `production` or `development`

`export NODE_ENV=development`
