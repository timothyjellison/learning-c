# Learning C

These are some basic skills to get you over your fear of C.

## Steps
1. Write a program that prints "Hello" to the console.
2. Compile it.
3. Execute it.

## Tips

1. Don't panic. C is just another language. Anyone can write C.

## Solutions

### A super basic program that logs to the console

```c
#include <stdio.h>

int main() {
  printf("Hello\n");

  return 0;
}
```

### Compile it

```bash
clang hello.c -o hello
```

If you don't have `clang` on your computer try using `gcc`

### Execute it
```bash
./hello
```

## Happy Coding!
You can find me over at [timellison.dev](https://www.timellison.dev/)
