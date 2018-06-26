# Critérios de Teste Estrutural baseado em Fuxo de Dados

* Baseiam-se nas associações entre a definição de uma variável e seus possíveis usos subseqüentes para derivar casos de teste.
* Visam testar as interações que envolvem definições de variáveis e subseqüentes referências a essas definições.

**Premissa:
Comandos que têm uma relação de fluxo de dados são provavelmente parte de uma mesma função e, portanto, devem serexercitados juntos.**

* Complementares aos critérios baseados em fluxo de controle.
* Busca testar o uso das variáveis em um programa, ou seja, como os dados são usados nas computações.
* Teste de fluxo de dados é uma ferramenta poderosa para o uso incorreto de valores resultante de erros de codificação.

## Definições e Conceitos Básicos:
### Grafo de Fluxo de Controle (GFC)
G=(N,E,s)

### Caminho no GFC

Sequência finita de nós (n1, n2, ..., nk), k ≥ 2, tal que existe:

* Caminho simples
* Caminho completo
 
## Ocorrência de variáveis

### A ocorrência de variáveis em um programa pode ser classificada em:

### Definição (def ou d)

Ocorre quando uma variável recebe um valor.

* a = 1

### Uso Computacional (c-uso ou uc): a variável é utilizada em uma computação.

* b = a * 2

### Uso Predicativo (p-uso ou up): a variável é utilizada em uma condição.

* if (a > 0)

## Caminhos

### Caminho livre de definição de x, de um nó i para um nó j

* Caminho (i, n1, ..., nm, j), m ≥ 0 no qual:
* X é definido em i, x é usada em j ou no arco (nm , j)
* X não é redefinida em n1, ..., nm

* Definição global de uma variável x em um nó i
* C-uso global
* C-uso local


### DU-caminho: Um Caminho (n1, n2..., nj, nk) é um du-caminho de x se:

1. n1 tem uma definição global de x e n tem um c-uso de x e o caminho (n1, n2..., nj, nk) é simples e livre de definição x;

ou

2. (nj, nk) tem um p-uso de x e o caminho (n1, n2..., nj, 
nk) é simples e livre de definição x e o caminho (n1, n2..., nj) é livre de laço.

* Associação definição-c-uso
* Associação definição-p-uso

### Todas-Definições

Requer que cada definição de variável seja exercitada pelo menos uma vez, não importa se por um c-uso ou por um p-uso.

### Todos-Usos

Requer que todas as associações entre uma definição de variável e seus subseqüentes usos (c-usos e p-usos) 
sejam exercitadas pelo menos uma vez,  em um caminho em que não há redefinição da variável (caminho livre de definição).

### Todos-DU-Caminhos

Requer que toda associação entre uma definição de variável e seus
subseqüentes usos (c-usos ou p-usos) seja exercitada por todos os
caminhos livres de definição e livres de laço que cubram essa
associação.
