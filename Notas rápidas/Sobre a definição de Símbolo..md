---
tags:
  - rochol
  - teoria-da-informação
---
O primeiro capítulo desse livro emprega em diversos contextos diferentes o uso da palavra "Símbolo" sem especificar toda a vez o nível de abstração a qual ele está se referindo. Claro que é em parte defeito do eu-leitor não me atendar a esse detalhe, mas não estar atento aos diferentes níveis de abstração em que esse símbolo pode ser utilizado dificulta o entendimento de algumas coisas. Aqui vai a maneira como eu entendi:

Existem três "Símbolos" a saber:

O "símbolo lógico", ou "símbolo da fonte" é a ideia abstrata que carrega consigo um significado que não importa muito para o estudo da teoria da informação. No nosso alfabeto, um símbolo lógico é cada uma das letras que o compõe. Símbolos lógicos são representados, ou melhor, codificados, por símbolos do alfabeto de elementos.

O "símbolo do alfabeto de elementos" estão um nível abaixo na pilha de abstração. Esses são os símbolos utilizados para representar um símbolo lógico. Na comunicação de dados digitais, esse símbolos são os bits, 0 e 1, que podem ser utilizados para representar um símbolo lógico do nosso alfabeto de símbolos lógicos. Da tabela ASCII, o caractere A é um símbolo lógico, representado em um conjunto de bits pela sequência `01000001`.

> Tanto os Símbolos Lógicos quanto os Símbolos do alfabeto de elementos são parte da camada da Fonte de Informação; eles existem em um nível de abstração mais alto que os símbolos de modulação, que por sua vez, pertencem à camada do Canal de Transmissão.

Símbolos de modulação são a representação física de um símbolo lógico codificado, e descrevem o estado de um sinal durante a transmissão de um símbolo lógico.  Podem ser uma voltagem, uma fase de onda - qualquer forma de representação física de um símbolo lógico.

A hierarquia então é essa: Um **símbolo lógico** é codificado em **símbolos do alfabeto de elementos** e transmitido através do canal de comunicação na forma de um **símbolo de modulação**.

Para facilitar a minha vida, vou sempre me referir aos símbolos do alfabeto de elementos como bits. Acho que o próprio Shannon fazia isso. Sei lá, não entrei em contato direto com a fonte primária ainda. Num futuro próximo...

---
## Referências:
[[Informação]]

