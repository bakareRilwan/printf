## Project Name - printf :page_facing_up:
```` c
/**
 * printf - prints  preformmatted text to stdout
 * Return: int
 * @format: %c or %s e.t.c as seen in printf
 * Authors: Bakare Rilwan & Samuel Ifada
 */
````
```` c int printf ( const char * format, ... ); ````

This is the first group project an  output conversion C program completed as part of the low-level programming and algorithm track at ALX. 
, which consists of replicating the **[printf (3)](http://man7.org/linux/man-pages/man3/printf.3.html)** function of language c, calling it this way **_printf.**

## Dependencies  :couple:

# How to use. :running:
### Complilation
All of the ``.c`` files along with a main.c file are to be compiled with ``gcc 4.8.4`` on Ubuntu 20.04 LTS with the flags ``-Wall Werror`` ``-Westra`` and ``-pedantic.``

The files will be compiled this way:
- ``gcc -Wall -Werror -Wextra -pedantic *.c``
#### Use.
In the ``main.c`` file, use the ``_printf`` function like so:
```c
#include "main.h"
/**
 * main - main function of program
 * Return: always 0
 */
int main(void)
{
	int cohort;
	char *string, *author1, *author2;
	
	cohort = 5;
	string = "The Authors of this project";
	author1 = "Bakare Rilwan";
	author2 = "Ifada Samuel"
	_printf("%s are %s & %s from cohort %d 2022", string, author1, author2, cohort);
	return (0);
}
```
```{bash}
linux>$  gcc -Wall -Werror -Wextra -pedantic *.c -o print_program
linux>$  ./print_program
The Authors of this project are Bakare Rilwan & Ifada Samuel from cohort 5 2022
linux>$
```

### Some prototypes we used
````c
int _printf(const char *format, ...);

/* Conversion Specifier Functions */
unsigned int convert_c(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_s(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_di(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_percent(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_b(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_u(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_o(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_x(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_X(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_S(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_p(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_r(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);
unsigned int convert_R(va_list args, buffer_t *output,
		unsigned char flags, int wid, int prec, unsigned char len);

````

### Parameters
 > **format** -> C string that contains the text to be written to stdout.

Where the specifier character at the end is the most significant component, since it defines the type and the interpretation of its corresponding argument:
 Specifier | Output | Example
------------ | ------------- |-----------
 c | Character | A
 s | String of characters | Holberton
 % | A % followed by another % character will write a single % to the stream| %
  i and d | Signed decimal integer | 98
 b | Unsigned binary | 10101
 u | Unsigned decimal integer | 98
 o | Unsigned octal | 5523
 x | Unsigned hexadecimal integer (lowercase) | 36264eb
 X | Unsigned hexadecimal integer (uppercase) | 36264EB
 r | Reversed string | gnirts |
 R | Rot13 string | cevags
##### Return Value.
On **success**, the **total number** of characters written is returned.
If a writing error occurs, the error indicator (ferror) is set and a negative number is returned.

## Contributors :black_nib:
- [Bakare Rilwan](https://github.com/baccrie)
- [Ifada Samuel](https://github.com/samuelifada)
