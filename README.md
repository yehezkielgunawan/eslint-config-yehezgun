# ESLint-Config-Yehezgun

![eslint-yehezgun](https://socialify.git.ci/yehezkielgunawan/eslint-yehezgun/image?description=1&descriptionEditable=Yehezkiel%20Gunawan%27s%20personal%20ESLint%20Rules&font=Raleway&logo=https%3A%2F%2Flogowik.com%2Fcontent%2Fuploads%2Fimages%2Feslint9232.jpg&name=1&owner=1&pattern=Charlie%20Brown&theme=Dark)

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
- [`eslint-config-prettier`](https://github.com/prettier/eslint-config-prettier#installation) : Turns off all rules that are unnecessary or might conflict with Prettier.
- [`eslint-plugin-sonarjs`](https://github.com/SonarSource/eslint-plugin-sonarjs) : SonarJS rules for ESLint to detect bugs and suspicious patterns in your code.

# The ESLint rules that I used here

```json
 rules: {
    'no-unused-vars': 'off',
    '@typescript-eslint/no-unused-vars': 'off',
    'unused-imports/no-unused-imports': 'error',
    'unused-imports/no-unused-vars': [
      'warn',
      {
        vars: 'all',
        varsIgnorePattern: '^_',
        args: 'after-used',
        argsIgnorePattern: '^_',
      },
    ],
    '@typescript-eslint/explicit-module-boundary-types': 'off',
    '@typescript-eslint/no-non-null-assertion': 'off',
    '@typescript-eslint/no-inferrable-types': 'off',
    'import/order': [
      'warn',
      {
        groups: [
          ['builtin', 'external'],
          'internal',
          'parent',
          ['sibling', 'index'],
          'object',
        ],
        'newlines-between': 'always',
        alphabetize: {
          order: 'asc',
          caseInsensitive: true,
        },
      },
    ],
    complexity: 'warn',
    'no-console': ['error'],
  },
```
