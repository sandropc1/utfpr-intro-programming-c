# Intro to Programming in C (UTFPR FD61A, 2021/1)

C exercises from UTFPR course **FD61A**, an introductory programming course, semester **2021/1**. Each exercise is a standalone program. Folders are named after the class session they belong to (`Aula N` = class N). Most files start with a comment that states the exercise (in Portuguese). All program text and identifiers are in Portuguese.

The repository also contains compiled Windows binaries (`.exe`) next to most sources, plus a few sample data files.

## Contents

| Folder | Topic | Exercises |
|---|---|---|
| `Aula 4` | Variables, arithmetic, `printf` | Travel distance and fuel use, compound interest (`pow`), integer operators, ideal weight formula |
| `Aula 5` | Input with `scanf`, `math.h` | Salary + commission, square root, distance between two points, seconds left until the end of the day |
| `Aula 6` | `if`/`else` | Quadratic equation roots, income-tax brackets |
| `Aula 7` | `switch` | Menu (even/odd, age check), four-operation calculator |
| `Aula 8` | `while` loops | Looping menu, number-guessing game with 6 attempts (`rand`), factorial |
| `Aula 9` | `do`/`while`, input validation | Grade averages limited to 0–10, counting values while they stay in [500, 1000] |
| `Aula 10` | `for`, nested loops | Factorial, `#` square, multiplication tables 1–10, Fibonacci sequence |
| `Aula 11` | Arrays (vectors) | Vector sum, squares, counting ages > 35, sum of elements, common elements of two vectors, comparisons with the mean |
| `Aula 12` | Matrices | 5×5 identity, diagonal sums, location of the largest element, scalar multiplication, matrix sum and product |
| `Aula 13` | Strings and structs | Appliance energy use (`struct`), name-length validation, vowel counting, "Surname, Name" with `strcat`, state abbreviation lookup (`strcasecmp`) |
| `Aula 15` | `enum`, `typedef`, `union` | Month name and day count, person registry storing a CPF or a passport number in a `union` |
| `Aula 16` | Functions | Largest of three numbers, ideal weight by sex, arithmetic/weighted mean/sum menu, letter grade from score, factorial |
| `Aula 17` | Pass by reference | Seconds → HH:MM:SS through pointer parameters and through a `struct`, band registry with lookup by ranking position |
| `Aula 18` | Recursion | Power, factorial, decimal → binary, an iterative version of a recursive sum, memoized Fibonacci |
| `Aula 19` | Pointers | Comparing variable addresses, array/matrix element addresses, pointer arithmetic, substring search, multi-level pointers (`int ***`) |
| `Aula 20` | Dynamic memory | `malloc` of an N-sized vector (returns `NULL` when N ≤ 0), element-wise product of two dynamically allocated vectors |
| `Aula 21` | Text files | Line count, concatenating two files, converting to uppercase, word count, letter frequency per line, counting occurrences of a word |
| `Aula 22` | Binary files | `fwrite`/`fread` of random integers, athlete records written to and read from `atletas.bin` (tallest and oldest), player ranking saved with `fprintf` and read with `fscanf` |

`Aula 21` also holds files outside the file-I/O topic:

- `ex5_p1.c`: sorted doubly linked list with insert, search, print, free and union of two lists.
- `pirolise.c`, `rascunho.c`, `teste11.c`: AVL tree with rotations, insertion, removal and level-by-level printing. The tree reads its input from `entrada*.txt` and writes to `saida*.txt`. Those input files are not in the repository.
- `exemploporra.c`, `INFERNO.C`: short scratch tests (`strtok` example, read and print a float).

`Aula 10/teste_forum.c` and `Aula 11/teste.c` are alternative versions of exercises in the same folder.

## Build and run

Each `.c` file is a complete program. Quote the path because folder names contain spaces:

```sh
gcc "Aula 10/ex_tabuada_cabulosa.c" -o tabuada
./tabuada
```

Programs that use `math.h` (`pow`/`sqrt`) need `-lm` on Linux:

```sh
gcc "Aula 5/Ex_grupo_2.c" -o distancia -lm
```

The file-handling exercises (`Aula 21`, `Aula 22`) open files relative to the current directory. Run them from inside their folder so they find `atletas.bin`, `ranking.bin` and the `.txt` files.

## Notes

These are student exercises kept as originally written, targeting Windows (`system("cls")`, `<conio.h>`). Some files use pre-C99 idioms such as `void main`.
