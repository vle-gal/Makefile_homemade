# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: vle-gal <vle-gal@student.42.fr>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/01/17 15:03:34 by vle-gal           #+#    #+#              #
#    Updated: 2018/01/17 16:29:19 by vle-gal          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #
NAME = SIMPLE #Makefile simple
#les Path finding
vpath %.c basic #les .c
vpath_h = -Idoth #les .h

#les couleurs et autre
Y = "\033[33m"
R = "\033[31m"
G = "\033[32m"
B = "\033[34m"
X = "\033[0m"
UP = "\033[A"
CUT = "\033[K"

#les pré règles
OBJDIR := objdiro
OBJS := $(addprefix $(OBJDIR)/, main.o sec.o)

$(OBJDIR)/%.o : %.c
	@gcc $(CPPFLAGS) $(CFLAGS) $(vpath_h) -Wall -Wextra -Werror -c \
	$(OUTPUT_OPTION) $<

#les règles
all: $(OBJS)
	@gcc -o SIMPLE $(OBJS)
	@echo $(R)Hail to the King Baby!
	@echo --------------$(X)
	@./SIMPLE
	@echo $(R)--------------


$(OBJS): | $(OBJDIR)

$(OBJDIR):
	@mkdir $(OBJDIR)

#les outils
clean :
	@rm -rf $(OBJDIR)
	@echo $(R)Hmm... so there is life after death..

fclean : clean
	@rm SIMPLE

re : fclean
	@make
