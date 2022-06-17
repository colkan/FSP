npx -p typescript tsc --init
this is for the tsconfig.json file

import { MikroORM } from "@mikro-orm/core";

const main = async () => {
    const orm = await MikroORM,init({
        dbName: 'Lib',
        type: 'postgresql',
        debug: process.env.NODE_ENV !== 'production'
    });
};

main();


"watch": "tsc -w",
    "dev": "nodemon src/index.js",
    "start": "node src/index.js",
    "start2": "ts-node src/index.ts",
    "dev2": "nodemon --exec ts-node src/index.ts"
