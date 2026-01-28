---
tags:
  - conceito
  - teoria-da-informação
  - entropia
  - rochol
  - shannon
---
Claude E. Shannon foi o primeiro a propor uma maneira quantitativa de estudar Informação, partindo do princípio de que Informação é uma função da probabilidade, uma medida associada ao processo de seleção de símbolos em um alfabeto.

Se um símbolo tem 100% de chance de ocorrer em um alfabeto, não há o quê comunicar, a parte receptora sabe exatamente o que será enviado através do canal. A Quantidade de Informação que um símbolo comunica tem a ver com a incerteza que o receptor tem sobre a sua ocorrência no evento da seleção, portanto, quanto menor a probabilidade, maior é a quantidade de informação que um símbolo carrega.

De forma analítica, a representação da Informação deve seguir os seguintes comportamentos:
- Se um símbolo tem alta probabilidade de ocorrer, a quantidade de informação que ele carrega é baixa. 
- Se um símbolo tem baixa probabilidade de ocorrer, a quantidade de informação que ele carrega é baixa.
- A quantidade de informação deve ser monotonicamente decrescente com a probabilidade de ocorrência de um símbolo.

A função matemática que descreve esse comportamento é, tomando um alfabeto X{x<sub>1</sub>, x<sub>2</sub>, x<sub>3</sub>, ... x<sub>n</sub>}:

$I(x_{i}) = -\log_{2}p_{i} = \log_{2}\frac{1}{p_{i}}$

Onde x<sub>i</sub> é um elemento qualquer do alfabeto X, e p<sub>i</sub> é a probabilidade da seleção desse elemento no processo elemento.

>**Informação é uma grandeza associada a um símbolo de um alfabeto**

A quantidade de informação contida em uma mensagem *M* de *k* caracteres pode ser expressada simplesmente pela soma da quantidade de informação associada a cada caractere da mensagem:

$Q(M) = \sum_{i=1}^{k} -\log_{2}p_{i}$

Aqui cabe comentar também que a probabilidade de ocorrência de um símbolo não tem nenhuma relação direta com o alfabeto, mas sim com o que está sendo comunicado com aquele alfabeto.
Os caracteres da tabela ASCII, por exemplo, não carregam em si nenhuma probabilidade, eles são apenas um padrão de codificação. A probabilidade de seleção de cada caractere desse alfabeto, depende diretamente do idioma utilizado!
### Referências:
ROCHOL, Juergen. Comunicação de dados. Porto Alegre: Bookman, 2012. ([amazon](https://www.amazon.com.br/Comunica%C3%A7%C3%A3o-Dados-22-Juergen-Rochol/dp/8540700379))
