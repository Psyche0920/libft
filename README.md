[![License: MIT](https://img.shields.io/badge/License-MIT-78C943?style=for-the-badge)](LICENSE)

# 📚 libft

<p align="center">
  <b>Custom C Library Implementation</b><br>
  <i>42 School Project · C · Memory & String Handling</i>
</p>

---

## 📌 Overview

`libft` is a custom implementation of essential functions from the C standard library.

The goal of this project is to:

* reimplement core libc functions from scratch
* understand low-level memory and string manipulation
* build a reusable C utility library

This library is used as a foundation for future projects such as:

* `get_next_line`
* `ft_printf`
* `push_swap`

---

## 🎯 Objectives

* Work with pointers and memory directly
* Reproduce standard library behavior
* Write modular and reusable code
* Improve understanding of C internals

---

## 🧩 Project Structure

```bash
libft/
├── ft_isalpha.c
├── ft_isdigit.c
├── ft_isalnum.c
├── ft_isascii.c
├── ft_isprint.c
├── ft_strlen.c
├── ft_memset.c
├── ft_bzero.c
├── ft_memcpy.c
├── ft_memmove.c
├── ft_strlcpy.c
├── ft_strlcat.c
├── ft_toupper.c
├── ft_tolower.c
├── ft_strchr.c
├── ft_strrchr.c
├── ft_strncmp.c
├── ft_memchr.c
├── ft_memcmp.c
├── ft_strnstr.c
├── ft_atoi.c
├── ft_calloc.c
├── ft_strdup.c
├── ft_substr.c
├── ft_strjoin.c
├── ft_strtrim.c
├── ft_split.c
├── ft_itoa.c
├── ft_strmapi.c
├── ft_striteri.c
├── ft_putchar_fd.c
├── ft_putstr_fd.c
├── ft_putendl_fd.c
├── ft_putnbr_fd.c
├── libft.h
└── Makefile
```

---

## ⚙️ Implemented Functions

### Part 1 — libc functions

```txt
ft_isalpha ft_isdigit ft_isalnum ft_isascii ft_isprint
ft_strlen ft_memset ft_bzero ft_memcpy ft_memmove
ft_strlcpy ft_strlcat ft_strchr ft_strrchr ft_strncmp
ft_memchr ft_memcmp ft_strnstr ft_strdup
ft_toupper ft_tolower
ft_atoi ft_calloc
```

---

### Part 2 — additional functions

```txt
ft_substr ft_strjoin ft_strtrim ft_split ft_itoa
ft_strmapi ft_striteri
ft_putchar_fd ft_putstr_fd ft_putendl_fd ft_putnbr_fd
```

---

## 🛠️ Build

```bash
make
```

Output:

```bash
libft.a
```

---

## 🧹 Clean

```bash
make clean
make fclean
make re
```

---

## 🚀 Usage

Include the header:

```c
#include "libft.h"
```

Compile with:

```bash
cc main.c libft.a
```

---

## 💡 Example Usage

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    printf("Length: %zu\n", ft_strlen("Hello"));

    char *dup = ft_strdup("42 Heilbronn");
    printf("Duplicate: %s\n", dup);

    char *joined = ft_strjoin("Hello ", "World");
    printf("Joined: %s\n", joined);

    char *num = ft_itoa(42);
    printf("Number: %s\n", num);

    ft_putendl_fd("Hello from libft!", 1);

    free(dup);
    free(joined);
    free(num);

    return (0);
}
```

---

### ▶️ Run

```bash
cc main.c libft.a
./a.out
```

---

### 📌 Output

```txt
Length: 5
Duplicate: 42 Heilbronn
Joined: Hello World
Number: 42
Hello from libft!
```

---

## ⚡ Implementation Details

* All functions are implemented manually
* No use of original libc equivalents
* Memory is handled explicitly
* Edge cases (NULL, boundaries) are considered

---

## 📚 Constraints

* compiled with:

  * `-Wall -Wextra -Werror`
* static library created using:

  * `ar rcs`
* follows 42 coding standards

---

## 🧠 Development Flow

```txt
standard C need
      ↓
reimplement manually
      ↓
test edge cases
      ↓
compile into libft.a
      ↓
reuse in other projects
```

---

## 🎯 Learning Outcomes

* pointer arithmetic
* memory manipulation
* string processing
* dynamic allocation
* modular library design

---

## 💡 Note

Functions that allocate memory (such as `ft_strdup`, `ft_strjoin`, `ft_itoa`) must be freed by the caller.

---

## 👤 Author

Psyche0920
https://github.com/Psyche0920

---

<p align="center">
  ⭐ If you like this project, give it a star!
</p>


## Licensing

Project code is available under the [MIT License](LICENSE). Third-party assets retain their original licenses and attribution requirements; this license does not relicense third-party media, datasets, model weights, or trademarks.
