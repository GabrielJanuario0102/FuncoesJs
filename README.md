# FuncoesJs
Este é um projeto sobre Funções em Linguagens de Script cujo a linguagem utilizada é Javascript. Neste README.md haverá os tipos, definições e exemplos de funções em Js.
# Declaration Function
A Função <ins>**Declaração**</ins> define uma função com os específicos parâmetros.  
A sintaxe será da seguinte forma:
```javascript
function nome(parametro1,parametro2,parametro3) {
  //-> código a ser executado (statements);
};
```
- **_nome_**: nome da função;
- **_parametro_**: um argumento a ser passado para a função, sendo o limite, 255 argumentos;
- **_statements_**: as instruções que compoem o corpo da função.

Por padrão, funções retornam **UNDEFINED**. Para retornar outro valor, precisa-se ter uma instrução **RETURN** que especifíca o retorno da função chamada.

## Vantagens da Função Declaration
A função **Declaration** possui **_Hoisting_**, ou seja, é possível chamar a função antes dela ser declarada no código. Além disso, <ins>facilita a leitura em projetos grandes</ins>, pois as funções importantes ficam destacadas.

## Desvantagens da Função Declaration
Devido ao hoisting, declarar uma função com o mesmo nome em diferentes partes do código pode resultar na <ins>sobreescrita da função original</ins>. Além disso, possui menor controle de escopo, o que pode <ins>dificultar o encapsulamento e modularização do código</ins>.

## Exemplos de Função Declaration
```javascript
function soma(x,y) {
  let resultado = x + y;
  return resultado;
};
```
```javascript
function chamada(nome) {
  let frase = nome + ' está presente?';
  return frase;
};
```
```javascript
function quadrado(x) {
  return x*x;
};
```
# Expression Function
Uma Função <ins>**Expression**</ins> é muito similar, tem quase a mesma sintaxe de uma **Declaration**. A principal diferença entre uma <ins>expressão de função</ins> e a <ins>função de declaração</ins> é o nome da função, o qual pode ser emitido em expressões de funções para criar funções anônimas.
```javascript
var nome = function(parametro) {
  //-> código a ser executado(statements)
  }
```
- **_nome_**: nome da função;
- **_parametro_**: um argumento a ser passado para a função, sendo o limite, 255 argumentos;
- **_statements_**: as instruções que compoem o corpo da função.
## Vantagens da Função Expression
Oferece <ins>maior controle de escopo</ins>, podendo limitar a função a um bloco ou contexto específico, sendo ideal para funções que não precisam ser globais. Existe também  a <ins>possibilidade de criar funções sem nome</ins> e atribuí-las dinamicamente a  variáveis, objetos ou passar como argumento, além de ser boa para <ins>**Callbacks**</ins>.
## Desvantagens da Função Expression
<ins>**Não sofre hoisting**</ins> e possui menos clareza em funções grandes, também <ins>possui dependência do contexto da variável</ins>, dependendo de onde ela está armazenada.
## Exemplos de Função Expression
```javascript
let soma = function(x,y) {
  return x + y;
};
```

```javascript
var cumprimento = function(nome) {
  return nome + ', como está?';
};
```

```javascript
const metade = function(x) {
  return x/2;
};
```
# Arrow Function
Uma Função Arrow possui uma <ins>**sintaxe mais curta**</ins> quando comparada a uma função expression e não tem seu próprio **this**, **arguments**, **super** ou **new.target**. Estas expressões de funções <ins>são melhor aplicadas para funções que não sejam métodos</ins>, e elas <ins>não podem ser usadas como **constructors**</ins>.
```javascript
let nome = (parametro) => //-> código a ser executado (statements);
```
- **_nome_**: nome da função;
- **_parametro_**: um argumento a ser passado para a função, sendo o limite, 255 argumentos;
- **_statements_**: as instruções que compoem o corpo da função.
## Vantagens da Função Arrow
As Funções Arrow nos permite <ins>escrever funções de forma breve</ins>, sendo especialmente útil para funções simples. Além disso, <ins>funções arrow não possuem seu próprio **this**</ins>, adotando o valor do contexto onde foram definidas, evitando problemas comuns relacionadas ao this em funções tradicionais.
## Desvantagens da Função Arrow
<ins>São inadequadas para métodos de objetos devido a herança léxica do this</ins>. Arrow functions não são recomendadas para definir métodos dentro de objetos, pois o this não pode referenciar o objeto esperado. Também <ins>não pode ser usada como construtoras</ins> pois não podem utilizar o operador **New** e possuem a ausênsia de arguments.
## Exemplos de Função Arrow
```javascript
let oi = () => console.log('Oi chefe.');
```
```javascript
let chamada = (nome) => console.log(nome + ' está?');
```
```javascript
let dobro = (n) => n*2;
```
