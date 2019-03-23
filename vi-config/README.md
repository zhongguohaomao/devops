# vim plugins on centos

## Valloric/YouCompleteMe

```
yum install cmake -y
```

Compiling YCM with semantic support for C-family languages through `libclang`:
```
./install.py --clang-completer
```

Compiling YCM with semantic support for C-family languages through experimental `clangd`:
```
./install.py --clangd-completer
```

```
./install.py
```

## mileszs/ack.vim

```
yum install ack -y
```

vi
```
:Ack some_keyword_to_search
```

## faith/vim-go

set GOPATH and vi
``
:GoInstallBinaries
``

## c++ dev env

cscope and ctags
```
alias mkcscopefile='ack -f --cpp "$(pwd)" > cscope.files'
alias mktag='ctags -R;cscope -Rbq'
```

goto system include, generate index
```
cd /usr/local/include(you project include path)
```

mkcsopefile && mktag

add [cscope_macros.vim](https://github.com/vim-scripts/cscope_macros.vim) to ~/.vim/plugin

add `cs add /usr/local/include/cscope.out` below `cs add csope.out`

goto project dir
```
mkcsopefile && mktag
```
