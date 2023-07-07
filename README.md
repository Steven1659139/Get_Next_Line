# Get_Next_Line

"Get_Next_Line" est un projet de l'école de programmation 42. L'objectif de ce projet est de coder une fonction permettant de lire une ligne terminée par un retour à la ligne depuis un descripteur de fichier.

## Description

La fonction `get_next_line` permet de lire une ligne depuis un descripteur de fichier, quel que soit la taille de celle-ci ou de votre buffer. C'est un outil pratique pour la lecture de fichiers ligne par ligne, et c'est une compétence commune qui sera utile dans de nombreux projets futurs.

## Compilation

La fonction peut être compilée en ajoutant le fichier `get_next_line.c` à votre projet et en l'incluant dans votre fichier source avec `#include "get_next_line.h"`.

## Utilisation

Voici un exemple d'utilisation de la fonction :

```c
#include "get_next_line.h"

int main(int argc, char **argv)
{
    int fd;
    char *line;

    if (argc != 2)
        return (1);
    fd = open(argv[1], O_RDONLY);
    while (get_next_line(fd, &line) > 0)
    {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
```
