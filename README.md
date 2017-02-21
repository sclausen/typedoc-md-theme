# typedoc-md-theme
A simple markdown theme for typedoc.

## Disclaimer

I have no idea if this is how typedoc themes are supposed to be implemented (most probably not), but it works. Consider this a hack, at most.

## Credits
This theme is based on a similar theme by kimamula:
[typedoc-markdown-theme](https://github.com/kimamula/typedoc-markdown-theme)
This was developed only because the original seems to be a bit out of date and broken, and because 
I want to customize it for my own needs.

## Installation
```
npm install --save-dev typedoc-md-theme
```

## Usage
```
node_modules/typedoc-md-theme/bin/typedoc --options typedoc.json --source src
```
Note that `bin/typedoc` is not the typedoc cli itself, but a node script wrapper that leverages the 
typedoc api. This is a workaround for modifying typedoc's theming code in order to get correct md
extensions and link urls.

## Sample typedoc.json
```
{
  "theme": "node_modules/typedoc-md-theme/bin",
  "mode": "modules",
  "moduleResolution": "node",
  "tsconfig": "tsconfig.json",
  "includeDeclarations": true,
  "ignoreCompilerErrors": true,
  "excludePrivate": true,
  "excludeExternals": true,
  "out": "docs/markdown"
}
```
