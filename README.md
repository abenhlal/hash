# hash

## TODO
- tests

## Build and Install

```sh
$ git clone https://github.com/abenhlal/hash.git
$ cd hash
$ mkdir build
$ cd build
$ cmake ..
$ make
$ make test
$ sudo make install
```

## Uninstall

```sh
$ sudo make uninstall
```

## Usage and build

```sh
$ gcc example.c -o example.bin -lhash
$ ./example.bin
11900548196712136313
9114364940175044080
8796868307739761162
```

```C
#include <stdio.h>
#include <stdint.h>
#include <inttypes.h>
#include <hash.h>

int main() {
  char *data = "hashme";
  // fnv1a
  uint64_t hfnv = hash_fnv1a(data, 7);
  printf("%"PRIu64"\n",hfnv);

  // city
  uint64_t hc64 = hash_city64(data, 7);
  printf("%"PRIu64"\n",hc64);

  // murmur2_64a
  uint64_t hm64 = hash_murmur2_64a(data, 7);
  printf("%"PRIu64"\n",hm64);

  return 0;
}

```

## License

Public Domain 2020-2021 Adil Benhlal <adil.benhlal@outlook.fr>

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
