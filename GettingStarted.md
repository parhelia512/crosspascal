First things first get the sources as described in [this page](https://code.google.com/p/crosspascal/source/browse/)
```
    svn checkout http://crosspascal.googlecode.com/svn/trunk/ crosspascal
```

Then, navigate to `src/complier` and compile everything (this examples uses fpc, but you can use other Pascal compilers)
```
    fpc -B cpc.dpr
```

Finally compile files with
```
    ./cpc yourfile.pas
```
and profit!