![Curso - JavaScript Super Saiyajin](http://i.imgur.com/jGXoRO6.png)

# Aula 01 - Conhecendo funções

## O que é uma função?

<br>

> **f( x ) = y**

<br>

> Uma função ou aplicação é uma relação de um conjunto `A` com um conjunto `B`.

*fonte: [Função (matemática) - Wikipedia](https://pt.wikipedia.org/wiki/Fun%C3%A7%C3%A3o_(matem%C3%A1tica))*

<br>

![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/Venn_diagram_of_a_function.svg/450px-Venn_diagram_of_a_function.svg.png)

<br>

Podemos imaginar que o conjunto `A` é o conjunto dos valores dos nossos <br>
parâmetros e o conjunto `B` é o conjunto dos valores dos resultados.

Logo essa relação entre esses dois conjuntos pode também ser<br> 
uma transformação, filtragem, etc. Por exemplo:


![](http://clubes.obmep.org.br/blog/wp-content/uploads/2015/11/separado.png)

Nesse caso temos duas funções:

- uma filtra os números pares;
- a outra filtra os números ímpares;

Essas duas funções utilizam o mesmo conjunto de entrada, o conjunto dos números Naturais e suas respostas são **sub-conjuntos** dos números Naturais.

> Você sabe que temos outros conjuntos numéricos também né?!


- Conjunto dos Naturais;
- Conjunto dos Inteiros;
- Conjunto dos Racionais;
- Conjunto dos Irracionais;
- Conjunto dos Reais ;



## Entendendo as operações matemáticas básicas

- soma: 
  - ( x, y ) => x + y 
  - ( y ) => ( x ) => x + y 
- subtração:
  - ( x, y ) => soma( x, -y ) 
  - ( y ) => ( x ) => soma( x )( -y ) 
  + invertendo essa operação
- multiplicação: ( utilizando apenas a soma )
  - ( x, y ) => x * y 
  - ( y ) => ( x ) => ...
  + invertendo essa operação
- divisão: ( utilizando apenas a soma )
  - ( x, y ) => x / y 
  - ( y ) => ( x ) => ...
  + invertendo essa operação

> Na lógica matemática e na ciência da computação, lambda cálculo , também escrito como cálculo-λ é um sistema formal que estuda funções recursivas computáveis, no que se refere a teoria da computabilidade, e fenômenos relacionados, como variáveis ligadas e substituição. Sua principal característica são as entidades que podem ser utilizadas como argumentos e retornadas como valores de outras funções.
> 
> A parte relevante de lambda cálculo para computação ficou conhecida como lambda cálculo não-tipado. O lambda cálculo tipado e o não-tipado tem suas ideias aplicadas nos campos da lógica, teoria da recursão (computabilidade) e linguística, e tem tido um grande papel no desenvolvimento da teoria de linguagens de programação (com a versão não-tipada sendo a inspiração original para programação funcional, em particular Lisp...
> 
> ...
> 
> Como os nomes de funções são uma mera conveniência, o lambda cálculo não tem interesse em nomear uma função. Já que todas as funções esperando mais de um argumento podem ser transformadas em funções equivalentes recebendo uma única entrada (via Currying), o lambda cálculo não tem interesse em criar funções que aceitam mais de um argumento. 

*fonte: [Cálculo lambda - Wikipedia](https://pt.wikipedia.org/wiki/C%C3%A1lculo_lambda)*

<br>

> **Entendeu  o porquê estou mostrando como criar essas operações<br>
básicas onde recebo apenas um parâmetro por vez?**

<br>

Caso você ainda não tenha entendido irei demonstrar praticamente.

Imagine que você quer ter uma função que sempre multiple por `2` algum valor.

```js

const double = ( x ) => x * 2

```

Podemos facilmente criar uma função para reaproveitar isso, dessa forma:


```js

const times = ( y ) => ( x ) => x * y
const double = times( 2 )
const triple = times( 3 )
const tenTimes = times( 10 )

```

<br>


> Agora vamos fazer uma que multiplique por 3 e outra por 10.

```js

const times = ( y ) => ( x ) => x * y
const double = times( 2 )
const triple = times( 3 )
const tenTimes = times( 10 )

```


<br>

> **Muito simples né?**

Perceba que quebramos uma função que possuía dois parâmetros<br>
em outras duas funções que recebem apenas um parâmetro cada.



> Então agora vamos escrever essa mesma função usando apenas a soma!


```js

const sum = ( y ) => ( x ) => x + y

const times = ( y ) => ( x ) => ...


```

### Lembrete 1

> Percebeu que não criamos **funções** porém não criamos nenhuma constante <br>
> para os valores que passaremos como parâmetro?

Isso se deve graças a dois conceitos que são obrigatórios para uma linguagem <br> estar contida no Paradigma Funcional:

- [First-class Function]()
- [High-Order Function]()

## Desafio

Criar a função de divisão utilizando apenas a função de soma, <br>
onde ela receba 2 valores inteiros e consiga retornar um <br>
valor decimal. Por exemplo: `5 / 2 = 2.5`

Além disso explique como dois valores do conjunto dos Números Naturais<br>
transformou-se em um valor que não está contido nesse grupo e qual o grupo que ele pertence.

> **Lembrando que a ÚNICA função aceita dentro da divisão será a da soma!**




###### Oozaru

![](http://i.imgur.com/kPZOvNa.png)

Como demonstrei anterioremente, utilizamos funções<br>
anônimas, que definimos em constantes, pois isso nos remetei ao [Cálculo lambda](https://pt.wikipedia.org/wiki/C%C3%A1lculo_lambda) que é a base da <br>
Programação Funcional.

Logo preciso também lhe mostrar do outro jeito, usando `function`.

> Por isso a `function` está na seção ***Oozaru***! Pois você pode<br>
> usar mas **EU** não lhe aconselho.
> 


<br>
<hr>
<br>