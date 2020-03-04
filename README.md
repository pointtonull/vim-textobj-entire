# vim-textobj-entire - Text objects for entire buffers

[![Build Status](https://travis-ci.org/kana/vim-textobj-entire.png)](https://travis-ci.org/kana/vim-textobj-entire)

vim-textobj-entire is a Vim plugin to provide text objects (`ae` and `ie` by
default) to select the entire content of a buffer.  Though these are trivial
operations (e.g. `ggVG`), text object versions are more handy, because you do
not have to be conscious of the cursor position (e.g. `vae`).

vim-textobj-entire provides two text objects:

* `ae` targets the entire content of the current buffer.
* `ie` is similar to `ae`, but `ie` does not include leading and trailing empty
  lines.  `ie` is handy for some situations.  For example,
    1. Paste some text into a new buffer (`<C-w>n"*P`)
       -- note that the initial empty line is left as the last line.
    2. Edit the text (`:%s/foo/bar/g` etc)
    3. Then copy the resulting text to another application (`"*yie`)

See also [the reference manual](https://github.com/kana/vim-textobj-entire/blob/master/doc/textobj-entire.txt) for more details.

# Installation

To install using [Vundle](https://github.com/VundleVim/Vundle.vim/blob/master/README.md#about), add these lines to your `.vimrc`:
```
Plugin 'kana/vim-textobj-user'
Plugin 'kana/vim-textobj-entire'
```

Then run the following in Vim:
```
:source %
:PluginInstall
Using Vundle it can be installed with:
```

<!-- vim: set expandtab shiftwidth=4 softtabstop=4 textwidth=78 : -->
