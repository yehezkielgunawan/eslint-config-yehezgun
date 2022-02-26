# ESLint-Config-Yehezgun

![eslint-config-yehezgun](https://socialify.git.ci/yehezkielgunawan/eslint-config-yehezgun/image?description=1&logo=https%3A%2F%2Fseeklogo.com%2Fimages%2FE%2Feslint-logo-4B5C528034-seeklogo.com.png&owner=1&pattern=Charlie%20Brown&theme=Dark)

This is ESLint rules that I usually use for my personal projects. I custom rules depending on my current needs now.

# ⚠️Before You Install This

> There're maybe some rules that you have to disable if you mix JS/TS or JS only codebase. And, this ESLint rules may changes without any announcement because of personal needs.

# Installation

```bash
npm i --save-dev eslint eslint-config-yehezgun
# or if you're using yarn
yarn add -D eslint eslint-config-yehezgun
```

# Usage

In your `eslintrc` file you can extend like this

```js
module.exports = {
  extends: ["yehezgun"],
};
```

# What's in here

`eslint-config-yehezgun` uses custom ESLint rules to adjust based on my current needs. But it also uses some plugins and extend the configuration from external library:

- [`typescript-eslint/eslint-plugin`](https://www.npmjs.com/package/@typescript-eslint/eslint-plugin) : add some new useful plugin
- [`eslint-plugin-import`](https://www.npmjs.com/package/eslint-plugin-import) : auto import sorting and grouping linter
- [`eslint-plugin-unused-import`](https://www.npmjs.com/package/eslint-plugin-unused-imports) : to avoid unused import or variable
- [`eslint-plugin-sonarjs`](https://github.com/SonarSource/eslint-plugin-sonarjs) : SonarJS rules for ESLint to detect bugs and suspicious patterns in your code.

# The ESLint rules that I used here

```js
   rules: {
    "no-unused-vars": "off",
    "no-var": "warn",
    "@typescript-eslint/no-unused-vars": "off",
    "unused-imports/no-unused-imports": "error",
    "unused-imports/no-unused-vars": [
      "warn",
      {
        vars: "all",
        varsIgnorePattern: "^_",
        args: "after-used",
        argsIgnorePattern: "^_",
      },
    ],
    "@typescript-eslint/explicit-module-boundary-types": "off",
    "@typescript-eslint/no-non-null-assertion": "off",
    "@typescript-eslint/no-inferrable-types": "off",
    "import/order": [
      "warn",
      {
        groups: [
          ["builtin", "external"],
          "internal",
          "parent",
          ["sibling", "index"],
          "object",
        ],
        "newlines-between": "always",
        alphabetize: {
          order: "asc",
          caseInsensitive: true,
        },
      },
    ],
    complexity: "warn",
    "no-console": ["error"],
  },
```

# Want to Buy Me a Kofi?

Sure, I'm open to anyone who want to gives some donation, LOL. Thank you by the way :D
<a href="https://ko-fi.com/kaz200" target="_blank">
<img src="https://res.cloudinary.com/yehez/image/upload/v1635687121/SupportMe_blue_2x_mlehwg.png" alt="drawing" width="200"/>
</a>
