# What Is It?

This plugin maps `ga` to do a search using [mileszs/ack.vim](https://github.com/mileszs/ack.vim).

This plugin is a fork of [Chun-Yang/vim-action-ag](https://github.com/Chun-Yang/vim-action-ag) that supports [mileszs/ack.vim](https://github.com/mileszs/ack.vim) instead of the now-deprecated [rking/ag.vim](https://github.com/rking/ag.vim).

# Installation

Install this plugin and its dependency, [mileszs/ack.vim](https://github.com/mileszs/ack.vim), either manually or by using your Vim plug-in manager of choice.

If you want to use `ag` ([The Silver Searcher](https://github.com/ggreer/the_silver_searcher)) with this plugin, simply [configure ack.vim accordingly](https://github.com/mileszs/ack.vim#can-i-use-ag-the-silver-searcher-with-this).

# Examples

- Normal Mode
  - `gaiw` to search the word
  - `gai'` to search the words inside single quotes.
- Visual Mode
  - `ga` to search the selected text

# Configuration

## Recommended Shortcuts

```vim
" use * to search current word in normal mode
nmap * <Plug>AckActionWord
" use * to search selected text in visual mode
vmap * <Plug>AckActionVisual
```

## Escape characters

There are some special characters used in Ack/Ag, like '$' which is treated as the
end of the line. Most of the time we use literal meaning of these characters.
You can set escapes for these characters by setting `g:vim_action_ack_escape_chars`.

This is the default setting for `g:vim_action_ack_escape_chars`:

```vim
let g:vim_action_ack_escape_chars = '#%.^$*+?()[{\\|'
```
