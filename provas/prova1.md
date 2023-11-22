Curso de Ciência da Computação  
UFFS Campus de Chapecó  
Linguagens Formais e Automatos  
AVPEA-1  

(Questões com mesmo peso. Use apenas o espaço disponível para cada resposta. Permitido o uso de uma folha A4 com anotações a mão. Avaliação individual. Entregar apenas a folha da prova.)

1- O fechamento do alfabeto de uma linguagem sempre é igual ao conjunto de sentenças da linguagem? Justifique.

2- Explique a finalidade, em compiladores, das etapas léxica, sintática e semântica.

3- Construa uma gramática regular para a seguinte linguagem: 
L(G)={x | x E (a,b,c)* onde x não possui 'b' concatenados}

4- Construa uma gramática regular para a seguinte linguagem
L(G)={x | x E (a,b,c)* onde o número de ocorrências de 'b' é ímpar e x nunca inicia por 'a')

5- Construa uma gramática livre de contexto para a seguinte linguagem:
L(G)={x | x ∈ a^b b^y c^z onde x > y e y >= 0 e z > 0}

## Respostas:
1-2-3-
4-
S::= bA | cB
A::= aA | bB | cA | ε
B::= aB | bA | cB

5-
S::= aAcB
A::= aA | aAb | ε
B::= cb | ε