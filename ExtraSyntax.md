Use `[[[` and `]]]` to copy inside the resulting c file without modifications. You can also mix verbatim and code, like
```
procedure FillChar(var Dest;Count:integer;Value:byte);
begin
[[[ memset(&<<<Dest>>>, <<<Count>>>, <<<Value>>>); ]]]
end;
```

  * **external**
You don't have to specify the library name but rather the header file which the function comes from.
```
function SDL_Init(flags: LongInt): LongInt; external 'SDL.h';
```

  * **compiler directives**
crosspascal targets d7 dialect, so not all the fancy compiler directives are available. If you need to add dummies, see [r217](https://code.google.com/p/crosspascal/source/detail?r=217) or [r218](https://code.google.com/p/crosspascal/source/detail?r=218) to understand how to do that.