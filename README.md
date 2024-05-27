# prettier-config

[![npm](https://img.shields.io/npm/v/@antfu/eslint-config?color=444&label=)](https://www.npmjs.com/package/@upthen/prettier-config)

---

upthen's personal prettier-config

## Description

When I create a new project, If I want to reuse my prettier config, I used to copy the .prettierrc from an old
project to the new one, that seems to be foolish, so why not make it a package and just install it on wherever
I want.

It is why I have this project. Yeah, just very simple but useful for me.

## Usages

1. Install

```bash
npm i prettier @upthen/prettier-config@latest
```

2. Set prettier

Add prettier config in package.json like the following codes:

```json
{

  ...
  "prettier": "@upthen/prettier-config",
}

```

3. Use in terminal

`npx prettier --check --write path`

```bash
npx prettier --check --write .

# or

npx prettier -c -w .

# . is the path of files you want to format.

```

4. Use With VsCode Extension: Prettier

- Install Prettier Extension
- Add the following config in VsCode settings.json

```json
{
	"editor.formatOnSave": true,
	"editor.defaultFormatter": "esbenp.prettier-vscode",
	"[javascript]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[typescript]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	}
}
```

- If you have some custom setting config in your workspace settings.json, Confirm the prettier config won't be override. You may need to add the following config into it.

```json
// workspace setttings.json
{
	"editor.formatOnSave": true,
	"editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

> [!IMPORTANT]
> Confirm to add the above config into settings.json, or it may not effects when you enter Ctrl + S or Command + S with VsCode Extension.
