## Análise de Mutantes

Teste de Mutação é um teste estrutural (teste de caixa branca)

Análise de Mutantes é uma técnica popular para aferir a qualidade de uma
suíte de teste.

## Mutantes são programas que contêm pequenos desvios sintáticos que representam defeitos simples

### Hipótese do Programador Competente
* Programadores experientes escrevem programas corretos ou muito próximos do correto.

### Efeito de Acoplamento
* Casos de teste capazes de revelar erros simples são tão sensíveis que, implicitamente, 
também são capazes de revelar erros mais complexos.

## Aplicação da Análise de Mutantes

### 1. Geração de Mutantes
Para modelar os desvios sintáticos mais comuns, operadores de mutação são aplicados a um programa, 
transformando-o em programas similares: mutantes.

1. A quantidade de operadores depende da linguagem de programação
1. Os operadores de mutação determinam o tipo de alteração sintática que deve ser feita para a criação dos mutantes
1. Quanto maior o número de operadores utilizados, maior o número de mutantes gerados

### 2. Submete-se os Mutantes aos Casos de Testes do Programa Original

### 3. Análise dos resultados
* Se o programa mutante for equivalente, o mesmo deve ser descartado;
* Caso não seja, os casos de teste selecionados não foram capazes de diferenciá-lo do programa orginal P.

Logo, existe a necessidade de incluir novos casos de teste ao conjunto T para torná-lo mais adequado à
realização do teste. 

## Análise dos Resultados (análise dos mutantes vivos)

* Mutantes sobreviventes ao teste (isto é, para o qual não há teste na suíte que
observe sua diferença de comportamento) indicam necessidade de novos
casos de teste na suíte.
* Caso os mutantes não sejam aprovados nos testes, significa que aquele
conjunto de testes é suficientemente bom para encontrar os tipos de
defeitos inseridos pelos operadores de mutação escolhidos.
* Os mutantes que não passaram nos testes podem ser considerados mutantes
mortos.

OBS: Quanto maior o conjunto de teste, maior o número de mutantes que ele consegue matar
e, consequentemente, maior o nível de confiabilidade desses casos de teste.

