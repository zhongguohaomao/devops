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
