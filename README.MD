🗓️ Calculadora de Diferença entre Datas

Um pequeno programa em C que calcula a diferença entre duas datas, mostrando o resultado em dias, meses e anos.
Feito com o objetivo de praticar manipulação de estruturas, funções e controle de fluxo em C.

💡 Sobre o projeto

O programa solicita duas datas ao usuário (Data A e Data B) e calcula a diferença entre elas considerando anos bissextos.
O resultado é exibido em:

Total de dias

Total aproximado de meses

Total aproximado de anos

⚙️ Funcionalidades

Validação de datas (dia, mês e ano)

Verificação de ano bissexto

Cálculo preciso de diferença entre datas

Interface simples via console

🧩 Estrutura do código

O código utiliza:

struct para armazenar as datas

Funções auxiliares como:

ehBissexto() → verifica se o ano é bissexto

contaBissextos() → conta os anos bissextos até o ano anterior

calcula_total_de_dias() → converte a data em número total de dias

diferenca_de_dias() → retorna a diferença em dias entre duas datas

🚀 Como executar

Compile o programa:

gcc datas.c -o datas


Execute:

./datas

🧠 Exemplo de uso
****** Calculadora de diferença entre datas ******

*** Dados da data A ***
Digite o ano da data A: 2020
Digite o mês da data A (1-12): 1
Digite o dia da data A: 1

*** Dados da data B ***
Digite o ano da data B: 2025
Digite o mês da data B (1-12): 10
Digite o dia da data B: 9

A diferença entre as duas datas é de:
- 2108 dias,
- ou 70 meses,
- ou 5 anos.