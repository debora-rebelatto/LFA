# Prova 1 - Linguagens Formais e Autômatos

(Questões com mesmo peso. Use apenas o espaço disponível para cada resposta. Permitido o uso de uma folha A4 com anotações a mão. Avaliação individual. Entregar apenas a folha da prova.)

1- O fechamento do alfabeto de uma linguagem sempre é igual ao conjunto de sentenças da linguagem? Justifique.

2- Explique a finalidade, em compiladores, das etapas léxica, sintática e semântica.

3- Construa uma gramática regular para a seguinte linguagem: 
L(G)={x | x ∈ (a,b,c)* onde x não possui 'b' concatenados}

4- Construa uma gramática regular para a seguinte linguagem
L(G)={x | x ∈ (a,b,c)* onde o número de ocorrências de 'b' é ímpar e x nunca inicia por 'a')

5- Construa uma gramática livre de contexto para a seguinte linguagem:
L(G)={x | x ∈ a^b b^y c^z onde x > y e y >= 0 e z > 0}

## Respostas:
1-
O fechamento do alfabeto de uma linguagem não é necessariamente igual ao conjunto de sentenças da linguagem. O fechamento do alfabeto refere-se à operação de combinar zero ou mais elementos do alfabeto, enquanto o conjunto de sentenças é formado de acordo com as regras gramaticais ou estruturais da linguagem. Em alguns casos, o fechamento do alfabeto pode gerar mais sequências do que as sentenças válidas na linguagem, já que as sentenças podem estar sujeitas a restrições ou regras adicionais de formação.

2-
As etapas de análise léxica, sintática e semântica em compiladores têm as seguintes finalidades:

1. **Análise Léxica:**
   - Transforma o código fonte em tokens ou unidades léxicas significativas, como palavras-chave, símbolos e números.

2. **Análise Sintática:**
   - Verifica se a sequência de tokens segue a estrutura gramatical da linguagem de programação, utilizando regras gramaticais para formar uma estrutura hierárquica do código.

3. **Análise Semântica:**
   - Garante a correção do significado do código, verificando coerência de tipos, uso correto de variáveis e regras semânticas da linguagem.

Essas etapas trabalham juntas para analisar, validar e interpretar o código fonte, assegurando que o programa seja corretamente compreendido e traduzido para código executável.

3-  
- Começamos com o símbolo inicial S e permitimos a inclusão de 'a's ou 'c's.  
- Se encontrarmos um 'b', mudamos para o não-terminal A para evitar concatenar mais 'b's.  
- O não-terminal A permite a inclusão de 'a's e 'c's, mas não permite 'b's.  

Então, a gramática resultante é:

$S::= aS | bA | cS | ε$  
$A::= aS | cS | ε$  

4-  
- Começamos com o símbolo inicial S e criamos produções que permitem 'b' ou 'c' para começar.
- Em seguida, usamos os não-terminais A e B para controlar o número de ocorrências de 'b' de forma a garantir que seja ímpar.
- A permite 'a's, 'b's e 'c's, mantendo o número de 'b's ímpar.
- B também permite 'a's, 'b's e 'c's, mas garante que o número de 'b's se mantenha ímpar ao alternar entre A e B.

Então, a gramática resultante é:

Essa gramática garante que todas as strings geradas estejam na linguagem desejada, com o número de ocorrências de 'b' sendo ímpar e 'x' nunca iniciando com 'a'.

$S::= bA | cB$  
$A::= aA | bB | cA | ε$  
$B::= aB | bA | cB$  

5-  
$S::= aAcB$  
$A::= aA | aAb | ε$  
$B::= cb | ε$
