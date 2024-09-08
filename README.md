## Snippets

Started as a

Fork of friendly snippets which can be found here
[friendly-snippets](https://github.com/coryleeio/snippets)

This repo contains my current snippets for a variety of programming languages and any additions, changes, or removals from those sets to fit my preferences from that set

## Install

Use your plugin manager of choice, e.g.

### With Lazy.nvim

```lua
{ "coryleeio/snippets" }
```

> [!WARNING]
> If you're using LuaSnip make sure to use
> `require("luasnip.loaders.from_vscode").lazy_load()`, and add
> `friendly-snippets` as a dependency for LuaSnip, otherwise snippets might not
> be detected. If you don't use `lazy_load()` you might notice a slower
> startup-time
>
> ```lua
> {
>   "L3MON4D3/LuaSnip",
>   dependencies = { "coryleeio/snippets" },
> }
> ```

### With Packer

```lua
use "coryleeio/snippets"
```

### With vim-plug

```vim
Plug "coryleeio/snippets"
```

### With coc.nvim

```vim
:CocInstall https://github.com/coryleeio/snippets@main
```

## Usage

This collection of snippets should work with any snippet engine that supports
loading vscode snippets. Like for example:

- [vim-vsnip](https://github.com/hrsh7th/vim-vsnip)
- [LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [coc-snippets](https://github.com/neoclide/coc-snippets)

## Add snippets from a framework to a filetype.

> [!NOTE]
> This is handled by your snippet engine and has nothing to do with this snippets collection

There's extra snippets included in this repo but they are not added by default,
since it would be irrelevant for people not using those frameworks. See
[`snippets/frameworks`](https://github.com/coryleeio/snippets/tree/main/snippets/frameworks)

For example: if you want to add rails snippets to ruby.

With LuaSnip:

```lua
require'luasnip'.filetype_extend("ruby", {"rails"})
```

With vim-vsnip:

```viml
let g:vsnip_filetypes.ruby = ['rails']
```

## Excluding snippets

> [!NOTE]
> This is handled by your snippet engine and has nothing to do with this snippets collection

With LuaSnip, see `help luasnip-loaders`

```lua
-- will exclude all javascript snippets
require("luasnip.loaders.from_vscode").load {
    exclude = { "javascript" },
}
```
