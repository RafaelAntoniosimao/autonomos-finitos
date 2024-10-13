Simulador de autômatos finitos que processa palavras de entrada com base em um autômato definido em arquivo e gera os resultados, indicando se as palavras foram aceitas ou rejeitadas, além do tempo de processamento.

Como Usar
Formato dos Arquivos
Arquivo do Autômato: define o estado inicial, estados finais e transições no formato:

php

<estado_inicial>
<número_estados_finais>
<estados_finais>
<número_transições>
<estado_origem> <caractere> <estado_destino>
Arquivo de Testes: lista de palavras e resultados esperados no formato:

php

<palavra>; <resultado_esperado>
Compilação e Execução
Compile:

bash

gcc -o simulador simulador.c
Execute:

bash

./simulador arquivo_automato.txt arquivo_testes.txt arquivo_saida.txt
Exemplo de Arquivos
Automato:

css

0
2
4 7
5
0 a 1
2 a 3
3 b 2
Testes:


ababa;1
aabba;0
O arquivo de saída conterá:


ababa;1;1;0.0001
aabba;0;0;0.00005

