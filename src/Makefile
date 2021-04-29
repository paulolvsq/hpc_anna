CC = gcc-10
## par défaut, on active les options de vectorisation, inutile quand rien n'est parallélisé
CFLAGS = -Wall -Werror -ftree-vectorize -O3
PARALLELIZE_FLAGS = -fopenmp

all : exec

exec : exact_cover
	./$< --in ../instances/matching8.ec --progress-report 0 

exact_cover : exact_cover.c
	$(CC) $(CFLAGS) $(PARALLELIZE_FLAGS) -o $@ $<

clean :
	rm exact_cover
	rm *~
