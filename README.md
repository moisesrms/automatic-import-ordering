# Automatic import ordering

The [eslint-plugin-import-helpers](https://github.com/Tibfib/eslint-plugin-import-helpers) plugin automatically changes the order of importers based on the rules placed in the Eslint configuration file.

# Installation #

```bash
yarn add -D eslint

yarn eslint --init

yarn add -D eslint-plugin-import-helpers
```

# Rules 
`.eslintrc.json`
```json
rules: {
  "import-helpers/order-imports": [
      "warn",
      {
          "newlinesBetween": "always",
          "groups": [
              "/^react/",
              "module",
              ["parent", "sibling", "index"]
          ],
          "alphabetize": { "order": "asc", "ignoreCase": true }
      }
  ],
```
# Plugin 
`.eslintrc.json`
```json
  plugins: ["eslint-plugin-import-helpers"],
```
