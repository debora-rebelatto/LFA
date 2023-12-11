# Lista de Exercídios LFA

### a) \( L(G) = \{ x \ | \ x \in (a,b)^* \text{ onde o número de 'b's é par} \} \)

Aqui está a gramática regular correspondente:

- \( S \rightarrow aS \ | \ bA \ | \ \varepsilon \)
- \( A \rightarrow aA \ | \ bS \)

Explicação:
- \( S \) é o símbolo inicial. Ele pode gerar sequências começando com 'a' seguidas por outras sequências ou 'b' seguido por uma sequência que começa com 'a'.
- \( A \) pode gerar sequências que começam com 'a' seguidas por outras sequências ou 'b' seguido por uma sequência que começa com 'a'.

Essa gramática gera strings onde o número de 'b's é par.

### b) \( L(G) = \{ x \ | \ x \in (a,b)^* \text{ onde o número de 'b's é ímpar} \} \)

Aqui está a gramática regular correspondente:

- \( S \rightarrow aS \ | \ bA \ | \ \varepsilon \)
- \( A \rightarrow aA \ | \ bS \ | \ b \)

Explicação:
- \( S \) é o símbolo inicial. Ele pode gerar sequências começando com 'a' seguidas por outras sequências, 'b' seguido por uma sequência que começa com 'a', ou uma sequência vazia.
- \( A \) pode gerar sequências que começam com 'a' seguidas por outras sequências, 'b' seguido por uma sequência que começa com 'a', ou apenas 'b' (o que garante que o número total de 'b's seja ímpar).

Essa gramática gera strings onde o número de 'b's é ímpar.

### c) \( L(G) = \{ x \ | \ x \in (a,b,c)^* \text{ onde ocorra pelo menos dois padrões 'abc'} \} \)

Para criar uma gramática regular para esta linguagem, é complicado fazer uma gramática regular diretamente, pois a restrição de dois padrões 'abc' não pode ser facilmente expressa com uma gramática regular.

### d) \( L(G) = \{ x \ | \ x \in (a,b,c)^* \text{ onde ocorra pelo menos um padrão 'ac'} \} \)

Aqui está uma gramática regular correspondente:

- \( S \rightarrow XaY \ | \ Z \)
- \( X \rightarrow aX \ | \ bX \ | \ cX \ | \ \varepsilon \)
- \( Y \rightarrow aY \ | \ bY \ | \ cY \ | \ \varepsilon \)
- \( Z \rightarrow aZ \ | \ bZ \ | \ cZ \ | \ X \)

Essa gramática garante que uma string tenha pelo menos um padrão 'ac'.

### e) \( L(G) = \{ x \ | \ x \in (0,1)^* \text{ e o número de '1's é múltiplo de 3} \} \)

Aqui está uma gramática regular correspondente:

- \( S \rightarrow 000 \ | \ 111 \ | \ 000S \ | \ 111S \ | \ S000 \ | \ S111 \)

Essa gramática gera strings onde o número de '1's é um múltiplo de 3.


Vou criar gramáticas regulares para cada uma das linguagens propostas:

### f) \( L(G) = \{ x \ | \ x \in (a,b,c,d)^+ \text{ onde } \text{a soma de 'a's e 'c's é ímpar se } x \text{ começa com 'a' ou a soma de 'a's e 'd's é par se } x \text{ começa com 'b'} \text{. Se } x \text{ inicia por 'c' ou 'd' não existe restrição} \} \)

Essa gramática é um pouco complexa para ser representada em uma gramática regular devido à natureza da restrição baseada no início da string e nas somas pares ou ímpares. Expressar essa restrição diretamente em uma gramática regular não é prático, pois envolve condições baseadas no início da string e nas somas de caracteres específicos.

### g) \( L(G) = \{ x \ | \ x \in (a,b,c,d)^+ \text{ onde } \text{a soma de 'b's e 'c's é ímpar se } x \text{ começa com 'a' ou a soma de 'a's e 'd's é par se } x \text{ começa com 'b'} \text{. Se } x \text{ inicia por 'c' ou 'd' não existe restrição} \} \)

Da mesma forma que a gramática anterior, esta gramática também apresenta restrições baseadas no início da string e nas somas pares ou ímpares de caracteres, o que dificulta expressar essas condições diretamente em uma gramática regular.

### h) \( L(G) = \{ x \ | \ x \in (a, b)^* \text{ e o número de 'a's é par e } x \text{ não possui 'b's consecutivos} \} \)

Essa gramática também é complexa de ser expressa diretamente em uma gramática regular, pois requer a verificação da paridade do número de 'a's e a ausência de 'b's consecutivos, o que não é trivial de ser feito com uma gramática regular.

### i) \( L(G) = \{ x \ | \ x \in (0, 1)^+ \text{ e se } x \text{ começa com '0' então o número de '0's é par, senão o número de '0's é ímpar} \} \)

Assim como as gramáticas anteriores, esta gramática apresenta uma condição baseada no início da string e na paridade do número de '0's, o que dificulta a representação direta em uma gramática regular.

### j) \( L(G) = \{ x \ | \ x \in (a, b, c)^* \text{ e o número de 'a's é par e o número de 'c's é ímpar} \} \)

Essa gramática também não pode ser expressa diretamente em uma gramática regular devido à condição de paridade do número de 'a's e 'c's.

### k) \( L(G) = \{ x \ | \ x \in a^n b^n \text{ onde 'n' é par} \} \)

Esta linguagem pode ser expressa por uma gramática regular:

- \( S \rightarrow aSb \ | \ \varepsilon \)

Esta gramática gera strings do tipo \( a^n b^n \) onde 'n' é um número par.

### l) \( L(G) = \{ a^n b^m c^k \ | \ n+k \text{ é par e } m,n,k \geq 0 \} \)

Esta linguagem pode ser expressa por uma gramática regular:

- \( S \rightarrow A \ | \ B \ | \ C \)
- \( A \rightarrow aA \ | \ \varepsilon \)
- \( B \rightarrow bBc \ | \ \varepsilon \)
- \( C \rightarrow aCb \ | \ \varepsilon \)

Esta gramática gera strings onde a soma de 'n' e 'k' é par.
