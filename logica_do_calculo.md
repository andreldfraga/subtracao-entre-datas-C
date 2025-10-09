🧮 Explicação Matemática do Cálculo de Diferença entre Datas

Este documento explica em detalhes a lógica matemática usada pelo programa para calcular a diferença entre duas datas em dias, meses e anos aproximados.

🗓️ 1. Representação das Datas

Cada data é convertida em um número total de dias desde o ano 1, seguindo a ideia de uma “linha do tempo contínua”.
Assim, podemos calcular a diferença entre duas datas apenas subtraindo esses totais.

A fórmula base é:

Total de dias
=
(
ano
−
1
)
×
365
+
soma dos dias dos meses anteriores
+
(
dia
−
1
)
+
bissextos anteriores
Total de dias=(ano−1)×365+soma dos dias dos meses anteriores+(dia−1)+bissextos anteriores
🔁 2. Cálculo dos Anos Bissextos

O calendário gregoriano define anos bissextos como aqueles:

divisíveis por 4,

exceto os divisíveis por 100,

a menos que também sejam divisíveis por 400.

A fórmula usada é:

bissextos at
e
ˊ
 o ano 
𝑋
=
⌊
𝑋
4
⌋
−
⌊
𝑋
100
⌋
+
⌊
𝑋
400
⌋
bissextos at
e
ˊ
 o ano X=⌊
4
X
	​

⌋−⌊
100
X
	​

⌋+⌊
400
X
	​

⌋

Essa conta garante que apenas os anos realmente bissextos sejam considerados no total de dias.

🧩 3. Conversão da Data em Dias

Para transformar uma data em número total de dias, o programa faz:

Multiplica o número de anos completos por 365.

Soma a quantidade de dias dos meses anteriores (usando o array meses[]).

Adiciona os dias do mês atual (menos 1).

Soma a quantidade de anos bissextos anteriores.

Se o ano atual for bissexto e o mês for posterior a fevereiro, adiciona +1 dia.

Isso gera um número absoluto que representa “quantos dias já se passaram desde o início do calendário”.

➗ 4. Diferença Entre as Datas

Com as duas datas convertidas em totais de dias:

Diferen
c
¸
a
=
∣
Total da Data A
−
Total da Data B
∣
Diferen
c
¸
	​

a=∣Total da Data A−Total da Data B∣

A diferença obtida é sempre positiva e representa o intervalo exato em dias entre as duas datas.

Depois, o programa converte essa diferença em valores aproximados:

Meses:

Meses
=
Diferen
c
¸
a
30
Meses=
30
Diferen
c
¸
	​

a
	​


Anos:

Anos
=
Diferen
c
¸
a
365
Anos=
365
Diferen
c
¸
	​

a
	​

🧠 5. Possíveis Melhorias

O cálculo atual usa aproximações (30 dias por mês e 365 por ano).
Algumas possíveis melhorias seriam:

Calcular anos, meses e dias exatos (ex: “2 anos, 3 meses e 12 dias”).

Considerar o número real de dias de cada mês no cálculo dos meses.

Permitir entrada e saída em formatos mais comuns, como dd/mm/aaaa.

Criar testes automáticos para validar diferentes combinações de datas.

✍️ Autor

André Fraga
Desenvolvido como exercício de raciocínio lógico e prática em C.