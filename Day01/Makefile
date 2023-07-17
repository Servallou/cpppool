##
## EPITECH PROJECT, 2022
## Makefile
## File description:
## Main Makefile
##

CC	=	g++

SRC_MAIN	=	src/main.cpp	\

NAME_MAIN	=	# binary name #

CFLAGS = -std=gnu11 -Wall -Wextra -I./inc/

OBJ_MAIN	=	$(SRC_MAIN:.c=.o)

all: clib $(NAME_MAIN)

$(NAME_MAIN):	$(OBJ_MAIN)
		$(CC) -o $(NAME_MAIN) $(OBJ_MAIN) $(CFLAGS)

debug: CFLAGS	+=	-g
debug: fclean	$(NAME_MAIN)

clib:
	make -C ./lib/my/ .PHONY

clean:
	find . -type f -name "*.o" -delete
	rm -f $(OBJ_MAIN)

fclean: clean
	find . -type f -name "*.a" -delete
	rm -f $(NAME_MAIN)

re: fclean clean all

.PHONY: re fclean clean all
