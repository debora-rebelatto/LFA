# Trabalhos Facultativos

Trabalho 1:
Para as GRs do item 5 da lista de exercícios, construir o Autômato Finito, eliminar inalcançáveis e mortos, e em seguida determinizar o AF mínimo.


Trabalho 2:
Construa, usando a GLC abaixo, as árvores de derivação ascendente mais a esquerda e direita, e descentente mais a esquerda e direita para a cadeia: id + ((id * id ) + id * id )

E::=E + T | T

T::= T * F | F

F::= (E) | id

| 8 | s | e | n | t | a | o | i | u |
|----|---|---|---|---|---|---|---|---|---|
| S  | A, H | C, M |   |   |   |   | M | M | M |
| A  | B   |     |   |   |   |   |   |   |   |
| *B |     |     |   |   |   |   |   |   |   |
| C  |     |     | D |   |   |   |   |   |   |
| D  |     |     |   | E |   |   |   |   |   |
| E  |     |     |   |   | F |   |   |   |   |
| F  |     |     |   |   |   | G |   |   |   |
| *G |     |     |   |   |   |   |   |   |   |
| H  | I   |     |   |   |   |   |   |   |   |
| I  |     | J   |   |   |   |   |   |   |   |
| J  |     |     |   |   |   |   | K |   |   |
| K  |     |     |   |   |   |   |   | L |   |
| *L |     |     |   |   |   |   |   |   |   |
| *M | M   | M   |   | M | M | M | M | M | M |
