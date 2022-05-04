---

id: npm-run-setup:dev-fails
title: npm run setup:dev fails
tags:
  - node.js
  - npm
  - Typescript
  - Setup
sidebar_label: npm run setup:dev fails
slug: /troubleshooting/npm-run-setup:dev-fails

---

## Overview

`npm run Setup:dev` fails


## Symptoms

Attempting to run `setup:dev` for the generated app is not successful. An error message may, or may not, be displayed. 


## Cause

The most common causes are

- Using unsupported versions of Node.js and or npm

- Typescript is not installed globally

- Installation is stopped before completion of the process

  > `npm run setup:dev` runs multiple processes so it will often takes longer than expected. This may cause the user to assume that the process has stopped responding.

 - Docker is not running 

## Resolution

We recommend doing the following: 

- Check that supported versions of node.js and npm are installed and that TypeScript is installed globally.

- If you stopped the process in the middle, delete node modules and re-install npm:

  ```jsx
  Delete node_modules or npm run clean
  npm install
  npm run setup:dev 
  ```

- If the process failed after stage 5, check that Docker is running. 

- If none of the above resolves the issue, check your internet connection, and storage space. 

## Related Troubleshooting Docs

Coming soon

## Additional Information

See [ReadMe](https://github.com/amplication/amplication/blob/master/README.md#initializing-all-the-packages)

## Related Discord Threads 

[npm run setup:dev takes a long time to complete](https://discordapp.com/channels/757179260417867879/968914282978893874)



