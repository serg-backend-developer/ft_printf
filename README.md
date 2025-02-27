# ft_printf

## Overview
`ft_printf` is a custom implementation of the standard `printf` function in C. This project is part of the 42 School curriculum and aims to deepen understanding of variadic functions, formatted output, and low-level string and memory manipulation.

## Features
- Supports the following conversion specifiers:
  - `%c` - Character
  - `%s` - String
  - `%p` - Pointer
  - `%d` / `%i` - Integer
  - `%u` - Unsigned integer
  - `%x` / `%X` - Hexadecimal (lowercase/uppercase)
  - `%%` - Percent sign
- Supports basic formatting:
  - `-` (Left alignment)
  - `0` (Zero padding)
  - `.` (Precision)
  - Width specification
- Uses `stdarg.h` for handling variadic arguments
- Modular structure for better readability and maintainability

## Installation & Compilation
1. Clone the repository:
   ```sh
   git clone https://github.com/serg-backend-developer/ft_printf.git
   cd ft_printf
   ```
2. Compile the library:
   ```sh
   make
   ```
3. Include `ft_printf.a` in your project:
   ```sh
   gcc main.c libftprintf.a -o my_program
   ```

## Usage
### Function Prototype
```c
int ft_printf(const char *format, ...);
```
### Example Usage
```c
#include "ft_printf.h"

int main() {
    ft_printf("Hello, %s! You have %d new messages.\n", "Alice", 5);
    return 0;
}
```

## Project Structure
```
ft_printf/
├── handlers/
│   ├── handle_character.c
│   ├── handle_decimal.c
│   ├── handle_hexadecimal.c
│   ├── handle_pointer.c
│   ├── handle_string.c
│   ├── handle_unsigned_decimal.c
├── libft/
├── ft_printf.c
├── ft_printf.h
├── Makefile
├── README.md
```

## Testing
Run tests to ensure correct behavior:
```sh
make test
```
Alternatively, you can use external testing tools such as `42TESTERS-PRINTF` or `printf-tester`.
