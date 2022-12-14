# libft

This assignment was to make my own C library containing both my own versions of existing functions, and new functions.  I also completed the bonus portion of this assignment. I've used these functions in all other C projects I've made since.  I've also included [get_next_line](#get_next_line) and [ft_printf](#ft_printf) in this repository as I use them as part of Libft. As such the libft.a file also includes get_next_line and ft_printf.

### Table of contents:
- [List of Functions](#list-of-functions)
	- [Libc Functions](#libc-functions)
	- [Additional Functions](#additional-functions)
	- [Bonus Functions](#bonus-functions)
- [get_next_line](#get_next_line)
- [ft_printf](#ft_printf)
- [Installation guide](#installation)

## List of Functions:
### Libc Functions:
These functions have the same prototypes and implement the same behaviours as the originals.
| Function | Description |
| :------ | --------- |
| [``ft_atoi``](ft_atoi.c) | Reads a String, and saves the string into an integer |
| [``ft_bzero``](ft_bzero.c) | Writes ``n`` zeroes to the string ``s`` |
| [``ft_calloc``](ft_calloc.c) | Reserves ``x`` blocks of ``y`` bits of memory |
| [``ft_isalnum``](ft_isalnum.c) | Returns ``1`` if the input is a number or a letter in the ``ASCII`` table |
| [``ft_isalpha``](ft_isalpha.c) | Returns ``1`` if the input is a letter in the ``ASCII`` table |
| [``ft_isascii``](ft_isascii.c) | Returns whether or not a value belongs to the ``ASCII`` table |
| [``ft_isdigit``](ft_isdigit.c) | Returns ``1`` if the input is a number in the ``ASCII`` table |
| [``ft_isprint``](ft_isprint.c) | Returns whether a character is printable |
| [``ft_itoa``](ft_itoa.c) | Saves the given number as a string (char array) |
| [``ft_memcpy``](ft_memcpy.c) | Copies from one memory point to another, until the specified character is copied or until ``n`` bytes are copied |
| [``ft_memchr``](ft_memchr.c) | Looks for a matching character inside a part of the memory |
| [``ft_memcmp``](ft_memcmp.c) | Compares two parts of memory, returning ``0`` if they're the same, or else a nonzero value |
| [``ft_memcpy``](ft_memcpy.c) | Copies from one part of memory to another, ignoring possible overlaps |
| [``ft_memmove``](ft_memmove.c) | Copies from one part of memory to another, preventing possible overlaps |
| [``ft_memset``](ft_memset.c) | Assigns a character ``n`` times to a part of the memory |
| [``ft_putchar_fd``](ft_putchar_fd.c) | Prints a character to the given file descriptor |
| [``ft_putendl_fd``](ft_putendl_fd.c) | Prints a string followed by a new line ``\n`` to a given file descriptor |
| [``ft_putnbr_fd``](ft_putnbr_fd.c) | Prints number to the given file descriptor |
| [``ft_putstr_fd``](ft_putstr_fd.c) | Prints string to the given file descriptor |
| [``ft_split``](ft_split.c) | Splits a string according to a given separator character |
| [``ft_strchr``](ft_strchr.c) | Looks for a specific character inside a given string |
| [``ft_strdup``](ft_strdup.c) | Saves enoug space and duplicates a string |
| [``ft_strjoin``](ft_strjoin.c) | Concatenates two strings allocating enough space first |
| [``ft_strlcat``](ft_strlcat.c) | Concatenates two strings ensuring it ends with ``\0`` |
| [``ft_strlcpy``](ft_strlcpy.c) | Copies ``n - 1`` bytes from a source string to a destination string |
| [``ft_strlen``](ft_strlen.c) | Returns length of a string |
| [``ft_strmapi``](ft_strmapi.c) | Applies a function (mapping) to every element in a string |
| [``ft_strncmp``](ft_strncmp.c) | Compares two strings up to the n-th character |
| [``ft_strnstr``](ft_strnstr.c) | Tries to find a substring (``needle``) in a second string (``haystack``) before the n-th char is reached |
| [``ft_strrchr``](ft_strrchr.c) | Looks for a given character in a string, reading it from back to front |
| [``ft_strtrim``](ft_strtrim.c) | Removes occurrences of characters in a string from the start and end of another one |
| [``ft_substr``](ft_substr.c) | Copies from the n-th char of a string |
| [``ft_tolower``](ft_tolower.c) | Makes every uppercase character in a string lowercase |
| [``ft_toupper``](ft_toupper.c) | Makes every lowercase character in a string uppercase |


### Additional Functions

| Funtion Name | Function Prototype | Description |
|----------|----------|-------------|
|[```ft_substr```](ft_substr.c)|```char *ft_substr(char const *s, unsigned int start, size_t len);``` | Allocates (with malloc(3)) and returns a substring from the string ???s???. The substring begins at index ???start??? and is of maximum size ???len???. |
|[```ft_strjoin```](ft_strjoin.c)|```char *ft_strjoin(char const *s1, char const *s2);```|Allocates (with malloc(3)) and returns a new string, which is the result of the concatenation of ???s1??? and ???s2???.|
|[```ft_strtrim```](ft_strtrim.c)|```char *ft_strtrim(char const *s1, char const *set);```|Allocates (with malloc(3)) and returns a copy of ???s1??? with the characters specified in ???set??? removed from the beginning and the end of the string.|
|[```ft_split```](ft_split.c)|```char **ft_split(char const *s, char c);```|Allocates (with malloc(3)) and returns a string representing the integer received as an argument.|
|[```ft_strmapi```](ft_strmapi.c)|```char *ft_strmapi(char const *s, char (*f)(unsigned int, char));```|Applies the function ???f??? to each character of the string ???s???, and passing its index as first argument to create a new string (with malloc(3)) resulting from successive applications of ???f???.|
|[```ft_striteri```](ft_striteri.c)|```void ft_striteri(char *s, void (*f)(unsigned int, char*));```|Applies the function ???f??? on each character of the string passed as argument, passing its index as first argument.|
|[```ft_putchar_fd```](ft_putchar_fd.c)|```void ft_putchar_fd(char c, int fd);```|Outputs the character ???c??? to the given file descriptor.|
|[```ft_putstr_fd```](ft_putstr_fd.c)|```void ft_putstr_fd(char *s, int fd);```|Outputs the string ???s??? to the given file descriptor.|
|[```ft_putendl_fd```](ft_putendl_fd.c)|```void ft_putendl_fd(char *s, int fd);```|Outputs the string ???s??? to the given file descriptor followed by a newline.|
|[```ft_putnbr_fd```](ft_putnbr_fd.c)|```void ft_putnbr_fd(int n, int fd);```|Outputs the integer ???n??? to the given file descriptor.|

### Bonus functions:
The following functions are used in relation to a linked list with the following struct:
```C
typedef struct s_list
{
void *content;
struct s_list *next;
} t_list;
```

| Funtion Name | Function Prototype | Description |
|----------|----------|-------------|
|[```ft_lstnew```](ft_lstnew.c)|```t_list *ft_lstnew(void *content);```|Allocates (with malloc(3)) and returns a new node. The member variable ???content??? is initialized with the value of the parameter ???content???. The variable ???next??? is initialized to NULL.|
|[```ft_lstadd_front```](ft_lstadd_front.c)|```void ft_lstadd_front(t_list **lst, t_list *new);```|Adds the node ???new??? at the beginning of the list.|
|[```ft_lstsize```](ft_lstsize.c)|```int ft_lstsize(t_list *lst);```|Counts the number of nodes in a list.|
|[```ft_lstlast```](ft_lstlast.c)|```t_list *ft_lstlast(t_list *lst);```|Returns the last node of the list.|
|[```ft_lstadd_back```](ft_lstadd_back.c)|```void ft_lstadd_back(t_list **lst, t_list *new);```|Adds the node ???new??? at the end of the list.|
|[```ft_lstdelone```](ft_lstdelone.c)|```void ft_lstdelone(t_list *lst, void (*del)(void *));```|Takes as a parameter a node and frees the memory of the node???s content using the function ???del??? given as a parameter and free the node. The memory of ???next??? must not be freed.|
|[```ft_lstclear```](ft_lstclear.c)|```void ft_lstclear(t_list **lst, void (*del)(void *));```|Deletes and frees the given node and every successor of that node, using the function ???del??? and free(3).|
|[```ft_lstmap```](ft_lstmap.c)|```t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));```|Iterates the list ???lst??? and applies the function ???f??? on the content of each node. Creates a new list resulting of the successive applications of the function ???f???. The ???del??? function is used to delete the content of a node if needed.|

## [```get_next_line```](get_next_line):
This function returns a line read from a file descriptor.  It was also the first time I worked with static variables.  The biggest challenge of this project was making sure I didn't have any leaks.

```char *get_next_line(int fd);```

## [```ft_printf```](ft_printf)

This project was to make my own ```printf``` function.  It had to implement the following conversions: ```cspdiuxX%```.

```int ft_printf(const char *, ...);```

## Installation:

Clone the repository
``` 
git clone https://github.com/maiadegraaf/libft.git
cd libft
make
```
### Usage:

The makefile compiles all files. It then generates the output file libft.a. Here are some of the commands you can try:
- Compile the libft.a file:
  - ```make all```
- Compile all bonus files as well as mandatory ones:
  - ```make bonus```
  
### How to add  libft to your makefile:

```Make
# path to libft:
LIBFT	=	libft/libft.a
# compile libft:
$(LIBFT):
	@$(MAKE) -C libft
# include libft when compiling your project eg:
$(NAME): $(LIBFT) $(OBJS) $(HEADERS)
	@$(CC) $(FLAGS) $(LIBFT )$(OBJS) $(NAME)
	@echo "Success"
```

