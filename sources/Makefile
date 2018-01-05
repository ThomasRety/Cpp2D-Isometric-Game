##
## TRISTAN PROJECT, 2018
## CPP 2D isometric Game
## File description:
## makefile for game engine
##


NAME	:=	engine

CC	:=	g++

RM	:=	rm -f

SRC_DIR	:=	src
OBJ_DIR	:=	obj
INC_DIR	:=	inc

CFLAGS	:=	-Wall -Wextra  -Werror
CFLAGS	+=	-I$(INC_DIR)

SRC	:=	main.cpp \

SRC	:=	$(addprefix $(SRC_DIR)/, $(SRC))
OBJ	:=	$(patsubst $(SRC_DIR)%.c, $(OBJ_DIR)%.o, $(SRC))

$(OBJ_DIR)/%.o:	$(SRC_DIR)/%.c
	$(CC) $(CFLAGS) -c -o $@ $<

all:	$(NAME)

$(NAME): $(OBJ)
	$(CC) -o $(NAME) $(OBJ)

clean:
	$(RM) $(OBJ)

fclean: clean
	$(RM) $(NAME)

re:	fclean all

.PHONY:     all clean fclean re
