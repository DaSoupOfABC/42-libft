
# Libft

[![42 Project Score](https://img.shields.io/badge/Score-125%2F100-success?logo=42&logoColor=white)](https://42.fr)
![C Language](https://img.shields.io/badge/language-C-blue)
![Static Library](https://img.shields.io/badge/library-.a-lightgrey)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

A custom C library created as part of the [42 School](https://42.fr) curriculum.  
This project is the foundation for many future projects at 42, requiring students to reimplement standard C library functions and build additional utilities for memory, strings, and linked lists.

---

## 📖 Project Overview

The goal of **libft** is to code a library of essential C functions that will be reused in later projects.  
It consists of:

- **Libc Functions** – Reimplementations of standard functions like `strlen`, `strcpy`, `memset`, etc.  
- **Additional Functions** – Useful utilities not included in libc, such as `ft_substr`, `ft_strjoin`, and `ft_split`.  
- **Bonus Functions** – Linked list manipulation utilities (`t_list`), such as `ft_lstnew`, `ft_lstadd_back`, and `ft_lstmap`.  

Once completed, this library can be compiled into `libft.a` and linked into other C projects.  

✅ **Final Score:** 125/100 (all mandatory + bonus)

---

## 📂 Project Structure

```

.
├── libft.h         # Header file with all function prototypes
├── Makefile        # Build rules (make, make clean, make fclean, make re, make bonus)
├── ft\_\*.c          # Source files for functions
└── README.md       # Project documentation

````

---

## ⚙️ Compilation

To compile the library:

```bash
make        # builds libft.a with mandatory functions
make bonus  # builds libft.a with bonus (linked list) functions
````

This will generate the static library `libft.a`, which you can link with your own programs:

```bash
gcc main.c -L. -lft -o my_program
```

---

## 📚 Implemented Functions

### Part 1 – Libc Functions

Reimplementations of standard libc functions, such as:

* Character checks: `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`
* String operations: `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strnstr`, `ft_strncmp`
* Memory operations: `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
* Conversions: `ft_atoi`, `ft_toupper`, `ft_tolower`
* File descriptors: `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

### Part 2 – Additional Functions

Extra helper functions:

* `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`
* `ft_itoa`, `ft_strmapi`, `ft_striteri`
* Memory helpers: `ft_calloc`, `ft_strdup`

### Bonus – Linked List Utilities

Functions for singly linked lists (`t_list`):

* Creation: `ft_lstnew`
* Insertion: `ft_lstadd_front`, `ft_lstadd_back`
* Deletion: `ft_lstdelone`, `ft_lstclear`
* Iteration & Mapping: `ft_lstiter`, `ft_lstmap`
* Size & Last: `ft_lstsize`, `ft_lstlast`

---

## 🚀 Usage Example

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    char str[] = "Hello, 42!";
    printf("Length: %zu\n", ft_strlen(str));

    t_list *node = ft_lstnew("libft rocks!");
    printf("List content: %s\n", (char *)node->content);

    ft_lstclear(&node, NULL);
    return 0;
}
```

Compile with:

```bash
gcc main.c -L. -lft -o test_libft
```

---

## 🧪 Testing

You can test the library with external testers:

* [libft-unit-test](https://github.com/alelievr/libft-unit-test)
* [libft-war-machine](https://github.com/0x050f/libft-war-machine)
* [libftTester](https://github.com/Tripouille/libftTester)

Example (using `libft-unit-test`):

```bash
git clone https://github.com/alelievr/libft-unit-test
cd libft-unit-test
make f
```

---

## 🏆 Result

* **Final Score:** 125/100
* All mandatory and bonus parts completed successfully.

---

## 🙏 Acknowledgements

* 42 School for the curriculum and guidance.
* Fellow students and community testers for feedback.

```
