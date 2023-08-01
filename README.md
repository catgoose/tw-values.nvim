# tw-values.nvim

Preview the computed css values of tailwind classes on an element.

![Preview of tw-values.nvim in neovim](/preview.jpg)

---

## WIP

This is a work in progress, if you experience any problems feel free to make an issue or contribute with a PR.

some notes:
- This plugin looks for an existing running tailwind LSP server.
- Under the hood this plugin uses the LSP hover functionality, if this is altered significantly in the tailwind lsp this plugin can break.

---

## Why did i make this?

When you apply a lot of classes in tailwind, it can be taxing to read through all of them and think what each one does.

---

## Installaton

Install using your favorite plugin manager.

### Packer

```lua
...
use({ "MaximilianLloyd/tw-values.nvim" })
...
```

### Lazy
```lua
...
{
    "MaximilianLloyd/tw-values.nvim",
    keys = {
        { "<leader>sv", "<cmd>TWValues<cr>", desc = "Show tailwind CSS values" },
    },
    config = function()
        require("tw-values").setup({
            border = "rounded" -- Valid window border style,
            show_unknown_classes = true -- Shows the unknown classes popup
        })
    end
},
...
```

---

## Configuration

Right now the configurtion options are quite minmal.

```lua
...
{
    border = "rounded" -- Valid window border style,
    show_unknown_classes = true -- Shows the unknown classes popup
}
...
```
---

## Supported languages
The currently supported languages are the following:
- typescriptreact
- typescript
- astro
- vue
- svelte
- html
