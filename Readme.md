 # Curso de JavaScript

## Variáveis

A variavel é utilizada para receber um valor e este valor vai ser utilizado em algum lugar do seu programa.
Para declarar uma variavel no javascript utilizamos o *let* que é o tipo da variavel tambem existe a *var* que pertence a uma linguagem mais antiga, *=* que é a atribuição da varial, *idade* que é o nome da variavel `Para nomear uma variavel não pode começar com numero, ter espaço ou ter caracteres especiais a forma recomendada para escrever o nome da variavel é camelCase primeira letra minuscula e as maiusculas ficam para diferenciar as palavras`, *5* que é o valor da variavel e temos que finalizar a sentença com *;*
````
let idade = 5;
idade = 10;
console.log(idade)

Na saida irá imprimir 10, pois é uma variavel que pode mudar ao longo do programa.
````
`console.log("");` Utilizado para printar na tela como printf(C) ou print(Python)

`//` Utilizado para deixar mensagens ao longo do codigo

## Constantes
 As constantes como propriamente dito é uma variavel que não pode mudar.
````
const idade = 5;
console.log(idade)
Na saida ira imprimir 5;
````

## Tipos primitivos

### Tipos de valores

let nome = "Nicole"; `String - é quando se junta varios caracteres em uma variavel`
let numero = 21; `Number - Qualquer valor numerico`
let aprovado = true; `Boolean - Booleano`
let sobrenome = undefined; `Undefined - Não está definido`
let cor = null; `Object - Casos que vc queira resetar o valor`

### Tipagem dinâmica

`typeof` Verifica o tipo das variáveis

## Tipos de referência

### Objetos
O objeto vai juntar as informações em um lugar só.

let pessoa = {}; `Objeto vazio`

let nome = {
    chave1: 'Valor1',
    chave2: 'Valor2',
    chave3: 'Valor3',
    chave4: 'Valor4',
    chave5: 'Valor5'
};

Exemplo:

````
let pessoa = {
    nome: "Nicole",
    idade: 21,
    aprovado: true
};

console.log(pessoa);
````

### Arrays

Arrays são um conjunto de dados que pode ser acessado por um indice.
Os indices sempre começam com o 0.
Exemplo:
````
let familia = [31,41,51,61];
console.log(familia);
saida:
0: 31
1: 41
2: 51
3: 61
length: 4
````
Para acessar um indice especial temos que acessar como se fosse um vetor.
````
let familia = [31, 41, 51, 61];
console.log(familia[1]);
saida:
41
````

### Functions

As funções controlam o fluxo de execução do programa, para nomear uma função vc deve nome um verbo mais um substantivo.

Exemplo:
````
let corSite = "Azul"
function resetaCor (cor,tonalidade){
    corSite = cor + " " + tonalidade;
};
console.log(corSite);
resetaCor("azul","escuro");
console.log(corSite);
````
### Tipos de funções

Realiza uma tarefa, mas nao devolve nada.
````
function dizerNome(){
    console.log('Jonathan')
};
dizerNome();
````
Faz um calculo ou operação e retorna a tarefa.
````
function soma(valor) {
    return valor + 2;
};
//console.log(soma(7))
let resultado = soma(5)
console.log(resultado)
````
## Operadores

### Operadores Aritiméticos
````
let numero = 5;
console.log(numero + numero); //soma
console.log(numero - numero); //subtração
console.log(numero * numero); //multiplicação
console.log(numero / numero); //divisão
console.log(numero % numero); //resto da divisão
console.log(numero ** numero); //exponencial
console.log(++numero); //incremento
console.log(--numero); //decremento
````
### Operadores
'>' // maior    '>=' // maior ou igual  '===' // igual
'<' // menor    '<=' // menor ou igual  '!==' // diferente
### Operadores Atribuição
````
let numero = 5; //Atribuição
console.log(numero);

let numero = 5;
numero += numero; //numero = numero + numero
console.log(numero); 

let numero = 5;
numero -= numero; //numero = numero - numero
console.log(numero); 

Pode ser feito com todos operadores matemáticos.
````
### Operadores de Igualdade

Igualdade estrita (Compara o typo e o valor)

````
console.log(1 === 1); // retorna true
console.log('1' === 1); // retorna false
````

Igualdade solta (Compara o valor)

````
console.log(1 == 1); // retorna true
console.log('1' == 1); // retorna true
````
### Operador Ternário
````
let pontos = 9;
// se pontos for maior ou igual a 10 responda premiado se não responda não premiado.
let tipo = pontos >= 10 ? 'premiado' : 'não premiado';
console.log(tipo);
````
### Operadores Lógicos
Os operadores lógicos são usados para tomar decisões baseados em condições multiplas.

1 - E (&&) retorna true se todos os operandos for true.
````
console.log(true && true);
````
2 - OU (||) retorna true se um dos operandos for true.
````
console.log(false || true);
````
3 - NOT (!) vai fazer uma negação.
````
pessoa = false;
idade = false;
let afirmativo = pessoa || idade;
console.log(afirmativo);

let negativo = !afirmativo;
console.log(negativo);
````
### Comparações não booleanas
Valores falsy: undefined, null, '', 0, false, NaN - not a number (se o resultado de uma operação for diferente do que deveria ser)
Valores truthy: É tudo que não contem no falsy.
### Operadores Bitwise

# MINI-PROJETO 1 
## TROCANDO VALOR DE UMA VARIÁVEL
````
let a = 'Vermelho';
let b = 'Azul';
let c = a;
a = b;
b = c;
console.log(a);
console.log(b);
````
## IF... ELSE
````
if (Condição) {
    //codigo
}
else if (Outra condição) {
    //codigo
}
else {
    //codigo
}
````

## Switch... Case
````
let permissao; // comum, gerente, diretor

permissao = 'diretor';

switch (permissao) {
    case 'comum':
        console.log("usuario comum");
        break;
    case 'gerente':
        console.log("usuario gerente");
        break;
    case 'diretor':
        console.log("usuario diretor");
        break;
    default:
        console.log("usuario incorreto");
}
````
## Laço/Loop

### FOR
O laço for precisa de uma condição de entrada e saida.
````
for (let i = 0; i < 5; i++) {
    console.log('estou aprendendo', i);
}
````
### WHILE
O laço while precisa de uma condição de saida;
````
let i = 5;
while (i >= 1) {
    if (i % 2 !== 0) {
        console.log(i);
    }
    i--;
}
````
### DO... WHILE
O laço do while executa primeiro depois vê a condição do loop.
````
let i = 0;

do {
    console.log('digitando', i);
    i++;
}
while (i < 10)
````
### FOR... IN
Loop para interação de propriedades de objetos ou elementos de um array.
````
const pessoa = {
    // key: 'value',
    nome: 'Nicole',
    idade: '21'
};
// key - value (chave - valor)
for (let chave in pessoa) {
    console.log(chave, pessoa['nome'], pessoa.nome);
}
Saida:
/*  nome Nicole Nicole
    idade Nicole Nicole */

const cores = ['vermelho', 'azul', 'rosa'];

for (let indice in cores) {
    console.log(indice, cores[indice]);
}
Saida:
/*  0 vermelho
    1 azul
    2 rosa      */
````
### FOR... OF
Loop para uma interação mais simples de arrays.
````
const pessoa = [{
    // key: 'value',
    nome: 'Nicole',
    idade: '21'
}]
const cores = ['vermelho', 'azul', 'rosa'];

for (let cor of cores) {
    console.log(cor);
}
/*      vermelho
        azul
        rosa        */

for (let chave of pessoa) {
    console.log(chave.nome);
    console.log(chave.idade);
}
/*    Nicole
      21           */

````
# Mini-Projeto 2 (Escreva uma função que usa 2 numeros e retorna o maior entre eles)
````
max(-1, 1);
function max(num1, num2) {
    let maior = num1 > num2 ? num1 : num2;
    console.log(maior);
}
````
# Mini-Projeto 3 (FIZZBUZZ)
````
// Divisil por 3 retorna FIZZ
// Divisil por 5 retorna BUZZ
// Divisil por 3,5 retorna FIZZBUZZ
// Não é divisil por 3 e por 5 retona o numero
// não é um numero retorna não é um numero

const resultado = FIZZBUZZ(15);
console.log(resultado);

function FIZZBUZZ(entrada) {
    if (typeof entrada !== 'number')
        return 'Não é um número';
    if (entrada % 3 === 0 && entrada % 5 === 0)
        return 'FIZZBUZZ';
    if (entrada % 3 === 0)
        return 'FIZZ';
    if (entrada % 5 === 0)
        return 'BUZZ';
    return entrada;

}
````

# Mini-Projeto 6 (ENCONTRE A STRING)
````
const pessoa = {
    nome: 'Nicole',
    idade: 21,
    sexo: 'feminino',
    curso: 'engenharia química'
}

for (let chave in pessoa) {
    if (typeof pessoa[chave] === 'string') {
        console.log(chave, pessoa[chave]);
    }
}
````


# Mini-Projeto * (Asteriscos)

````
exibirAsteriscos(5);
function exibirAsteriscos(quantidade) {
    algumaCoisa = '';
    for (let i = 0; i <= quantidade; i++) {
        algumaCoisa += '*'
        console.log(algumaCoisa);
    }
}
````
## Factory Functions (função de fabrica)
Aqui retorna um objeto novo na hora de instaciar

function criarCelular(marcaCelular, tamanhoTela, capacidadeBateria) {
    return {
        marcaCelular,
        tamanhoTela,
        capacidadeBateria,
        ligar() {
            console.log('Fazendo ligação...')
        }
    }
}

const celular = criarCelular('samsung', 5.2, 5000);
console.log(celular);

Saida:
/* {marcaCelular: 'samsung', tamanhoTela: 5.2, capacidadeBateria: 5000, ligar: ƒ} */

## Constructor Function (função de construtor)
Aqui cria-se um objeto novo na hora de instaciar

//Pascal Case - A primeira letra vem em maiuscula por exemplo UmDoisTresQuatro

function celular(marcaCelular, tamanhoTela, capacidadeBateria) {
    this.marcaCelular = marcaCelular, //this serve para referenciar a forma do objeto atual que voce esta manipulando
        this.tamanhoTela = tamanhoTela,
        this.capacidadeBateria = capacidadeBateria,
        this.ligar = function () {
            console.log('Fazendo ligação...')
        }
}
const celular1 = new celular('samsung', 5.2, 5000);
console.log(celular1);

## Natureza dinâmica de objetos

Um objeto é dinâmico sendo possivel adicionar ou retirar propriedades de dentro dele

const meuAmor = {
    Nome: 'Isaac Miranda',
    Idade: 21,
    eleMeAma: 'sim'
}
//Adicionando
meuAmor.nomeDaAmada = 'Nicole';
meuAmor.meses = function () {
    console.log('OOOI TE AMOOOO')
}
//Deletando
delete meuAmor.Nome;
delete meuAmor.eleMeAma;
console.log(meuAmor);

## Clonando Objetos

### Object.assign(p/ onde que vai este objeto copiado ,  Aonde este objeto esta sendo copiado)

const pessoa = {
    nome: 'Nicole',
    idade: 21,
    sexo: 'feminino',
    curso: 'engenharia química'
}

const objeto = Object.assign({
    ama: 'Isaac' //pode adicionar propriedades aqui
}, pessoa);
console.log(objeto);

### Três pontos

const pessoa = {
    nome: 'Nicole',
    idade: 21,
    sexo: 'feminino',
    curso: 'engenharia química'
}

const objeto2 = { ...pessoa };
console.log(objeto2);


## MATH
https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Math

Math é um objeto embutido que tem propriedades e métodos para constantes e funções matemáticas. Não é um objeto de função.

Propriedades:

Math.E
Constante de Euler e base dos logaritmos naturais, aproximadamente 2.718.
Math.LN2
Logaritmo natural de 2, aproximadamente 0.693.
Math.LN10
Logaritmo natural de 10, aproximadamente 2.303.
Math.LOG2E
Logaritmo de E na base 2, aproximadamente 1.443.
Math.LOG10E
Logaritmo de E na base 10, aproximadamente 0.434.
Math.PI
Relação entre a circunferência de um círculo e o seu diâmetro, aproximadamente 3.14159.
Math.SQRT1_2
Raiz quadrada de 1/2; Equivale a 1 dividido pela raiz quadrada de 2, aproximadamente 0.707.
Math.SQRT2
Raiz quadrada de 2, aproximadamente 1.414.

Métodos:

Math.abs(x)
Retorna o módulo, ou valor absoluto, de um número (|x|).
Math.acos(x)
Retorna o arco-coseno de um número (arccosx).
Math.acosh(x) 
Retorna o arco-coseno hiperbólico de um número.
Math.asin(x)
Retorna o arco-seno de um número (arcsinx).
Math.asinh(x) 
Retorna o arco-seno hiperbólico de um número.
Math.atan(x)
Retorna o arco-tangente de um número (arctanx).
Math.atanh(x) 
Retorna o arco-tangente hiperbólico de um número (arctanx).
Math.atan2(x, y)
Retorna o arco-tangente do quociente de seus argumentos.
Math.cbrt(x) 
Retorna a raiz cúbica de um número.
Math.ceil(x)
Retorna o menor inteiro que é maior ou igual a um número.
Math.cos(x)
Retorna o coseno de um número (cosx).
Math.cosh(x) 
Retorna o coseno hiperbólico de um número .
Math.exp(x)
Retorna ex, onde x é o argumento, e e é a constante de Euler (2.718...), a base do logaritmo natural.
Math.expm1(x) 
Retorna ex-1.
Math.floor(x)
Retorna o maior inteiro que é menor ou igual a um número.
Math.fround(x) (en-US) 
Retorna a mais próxima representação de ponto flutuante de precisão-única de um número.
Math.hypot([x[,y[,…]]]) 
Retorna a raiz quadrada da soma dos quadrados dos argumentos (
x2+y2+…
).
Math.imul(x) (en-US) 
Retorna o resultado de uma multiplicação de inteiro de 32-bit.
Math.log(x)
Retorna o logaritmo natural (logex ou lnx) de um número.
Math.log1p(x) 
Retorna o logaritmo natural de 1 + x (loge(1+x) ou ln(1+x)) de um número.
Math.log10(x) 
Retorna o logaritmo de x na base 10 (log10x).
Math.log2(x) 
Retorna o logaritmo de x na base 2 (log2x).
Math.max([x[,y[,…]]])
Retorna o maior dentre os parâmetros recebidos.
Math.min([x[,y[,…]]])
Retorna o menor dentre os parâmetros recebidos.
Math.pow(x,y)
Retorna a base x elevada à potência y do expoente, ou seja, xy.
Math.random()
Retorna um número pseudo-aleatório entre 0 e 1.
Math.round(x)
Retorna o valor arrendodado de x, para o valor inteiro mais próximo.
Math.sign(x) 
Retorna o sinal de x, indicando se é positivo, negativo ou zero.
Math.sin(x)
Retorna o seno de um número (sinx).
Math.sinh(x) 
Retorna o seno hiperbólico de um número (sinhx).
Math.sqrt(x)
Retorna a raiz quadrada positiva de um número.
Math.tan(x)
Retorna a tangente de um número (tanx).
Math.tanh(x) 
Retorna a tangente hiperbólica de um número (tanhx).
Math.toSource() 
Retorna a string "Math".
Math.trunc(x) 
Retorna a parte inteira de x, removendo quaisquer dígitos fracionários.

## STRING
https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/String

// Tipo primitivo typeof igual string
const mensagem = 'Hello, i love you';

//Tipo Objeto typeof igual objeto
const outraMensagem = new String('Hi');

outraMensagem.length //tamanho da mensagem
mensagem.includes('hello') // Pesquisa para ver se existe hello dentro da variavel mensagem
mensagem.startsWith('') //Se inicia com... verifica se inicia com oque vc deseja pesquisar
mensagem.endsWith('')//Termina com... Verifica se termina com oque vc deseja pesquisar
mensagem.indexOf('')//Determina o indice aonde se inicia com oque vc deseja pesquisar
mensagem.replace('hello', 'hi') // troca hello por hi
mensagem.trim() // Retira os espaços excedentes do inicio e do final de uma frase
mensagem.split(' ') // separa por espaços e transforma em um array

## Template Literal

Template literal é composto por ` ` que mantem toda formatação da string, como por exemplo:

````
const mensagem = `Oi esta eh 
minha primeira 
mensagem`

console.log(mensagem);

SAIDA:
Oi esta eh 
minha primeira 
mensagem
````
Podemos tambem trabalhar com qualquer tipo de método, avaliação ou expressão para o codigo ficar dinâmico, como funções, variáveis ou metodos aritméticos
````
const chamada = 'segunda';

const mensagem = `Oi esta eh 
minha ${chamada} mensagem`

console.log(mensagem);

SAIDA:
Oi esta eh 
minha segunda mensagem

````

## DATE
Date é uma forma de utilizar a data e horario no javascript tendo muito jeitos de se utlizar o mesmo.

````
const data = new Date(); // Aqui ele puxa a data e horario atual e no restante mostra a data que foi imposta.
const data1 = new Date('march 06 2019 09:30');
const data2 = new Date(2019, 02, 06, 9, 30);
console.log(data);
console.log(data1);
console.log(data2);

SAIDA:
Mon Jan 24 2022 12:23:16 GMT-0300 (Horário Padrão de Brasília)
Wed Mar 06 2019 09:30:00 GMT-0300 (Horário Padrão de Brasília)
Wed Mar 06 2019 09:30:00 GMT-0300 (Horário Padrão de Brasília)
````

## Metodos GET e SET:
Métodos GET é aonde vc o utiliza para extrair informações de um objeto.
Métodos SET é aonde vc pode alterar o valor.

## Exercicio exibir endereço
````
let endereco = {
    rua: '1',
    numero: '2',
    bairro: '3'
}

function mostrarEndereco(endereco) {
    for (let chave in endereco)
        console.log(chave, endereco[chave]);
}
mostrarEndereco(endereco);

SAIDA:
rua 1
numero 2
bairro 3
````
## ARRAYS

### ADICIONANDO ELEMENTOS
````
const numero = [1, 2, 3];

//Inicio                  ADICIONA UM NUMERO NO INICIO
numero.unshift(0);
console.log(numero);

//Meio                     ADICIONA UM NUMERO NO MEIO
numero.splice(1, 0, 'n');
//Remove elementos de um array e, se necessário, insere novos elementos em seu lugar, retornando os elementos deletados.
console.log(numero);

//Final                    ADICIONA UM NUMERO NO FINAL
numero.push(4);
console.log(numero);

SAIDA:
[0, 1, 2, 3]
[0, 'n', 1, 2, 3]
[0, 'n', 1, 2, 3, 4]
````
### Encontrando elementos (TIPO PRIMITIVO)
````
const numero = [1, 2, 3, 2];

console.log(numero.indexOf(2)); //Retorna o indice em que esse numero se encontra e se nn encontrar retorna -1
console.log(numero.lastIndexOf(2)); //Retorna a ultima ocorrência do numero indicado e nos mostra o indice
console.log(numero.includes(4));//Retorna true se existir ou false se não existir
````

### Encontrando elementos (Tipo de Referência)
 find = Retorna o valor do primeiro elemento na matriz em que o predicado é verdadeiro e indefinido caso contrário.
````
const marca = [
    { id: 1, nome: 'a' },
    { id: 2, nome: 'b' },
]

const marcas = marca.find(function (marca) {
    return marca.id == 1;
});
console.log(marcas);
````

## ARROW FUNCTIONS
Esta função faz a mesma coisa da tipo de referência e a unica diferença é que não precisamos escrever a function ficando mas legivel o nosso codigo.
````
const marca = [
    { id: 1, nome: 'a' },
    { id: 2, nome: 'b' },
]
console.log(marca.find((marca) => marca.nome === 'a'));
console.log(marca.find(() => marca.nome === 'a')); // se nn tivesse uma constante
````
## Removendo Elementos

const numeros = [1, 2, 3, 4, 5];

//REMOVE UM NUMERO NO FINAL:
numeros.pop();
console.log(numeros);

//REMOVE UM NUMERO NO INICIO:
numeros.shift();
console.log(numeros);

//REMOVE UM NUMERO NO MEIO:
numeros.splice(1/*REMOVE POR INDICE DO ARRAY */, 1 /*QUANTOS INDICES A SER REMOVIDOS */);
console.log(numeros);

## ESVAZIAR UM ARRAY
let numeros = [1, 2, 3, 4, 5, 6];
let outros = numeros;

//Solução 01 (Nesta solução o array numeros fica vazio mas o outros não fica pois pegou a atribuição de numeros)
/*numeros = [];
console.log(numeros);
console.log(outros);*/

//Solução 02 (Nesta solução o array numeros e o outros fica vazio)
//SAIDA: []
//       []
/*numeros.length = 0;
console.log(numeros);
console.log(outros);*/

//Solução 03 (Nesta solução o array e o outros fica vazio como na solução numero 2 porém está é um pouco mais trabalhosa.)
/*numeros.splice(0, numeros.length);
console.log(numeros);
console.log(outros);*/

//Solução 04 (Neste caso, se for utilizado para um array muito grande a uma chance de dar um bug no sistema então este não é muito utilizado)
/*while (numeros.length > 0)
    numeros.pop()
console.log(numeros);
console.log(outros);*/

## Combinando e dividindo ARRAYS:

const primeiro = [1, 2, 3];
const segundo = [4, 5, 6, 7];

//Combinado
const combinado = primeiro.concat(segundo); // SAIDA [1, 2, 3, 4, 5, 6, 7]
console.log(combinado);

//Dividir
//const cortado = combinado.slice(0, 4); // SAIDA [1, 2, 3, 4]
//const cortado = combinado.slice(1); // SAIDA [2, 3, 4, 5, 6, 7] 
const cortado = combinado.slice(); // SAIDA [1, 2, 3, 4, 5, 6, 7] 
console.log(cortado);

## Operador SPREAD

const primeiro = [1, 2, 3];
const segundo = [4, 5, 6, 7];

//Combinado
//const combinado = [...primeiro, ...segundo]; //SAIDA: [1, 2, 3, 4, 5, 6, 7]
const combinado = [...primeiro, 56, ...segundo, 'a']; //SAIDA: [1, 2, 3, 56, 4, 5, 6, 7, 'a']
console.log(combinado);

//Clonando
const clonado = [...combinado]; //SAIDA: [1, 2, 3, 56, 4, 5, 6, 7, 'a']
console.log(clonado);

## Metodo ForEach
Semelhante ao for of temos o forEach:

const numeros = [1, 2, 3, 4, 5];

numeros.forEach(function (numero) {
    console.log(numero);
})

SEGUNDO METODO UTILIZANDO O METODO DA FLECHA:
Deixa o codigo cada vez mais limpo.

numeros.forEach((numero) => console.log(numero))

SAIDA: (Percorre cada indice do array numeros)
1
2
3
4
5

numeros.forEach((numero, indice) => console.log(numero, indice))

SAIDA (Percorre cada indice do array numeros e nos mostra o indice também):

1 0
2 1
3 2
4 3
5 4

## Metodo JOIN e SPLIT
const numeros = [1, 2, 3, 4, 5];
const frase = 'Ola meu nome eh nicole maia';

//Adiciona todos os elementos de um array em uma string, separados pela string separadora especificada.
const resultado = numeros.join('.')
console.log(resultado);
//SAIDA: 1.2.3.4.5

//Divida uma string em substrings usando o separador especificado e retorne-as como uma matriz.
const quebrando = frase.split(' ')
console.log(quebrando);
//SAIDA: ['Ola', 'meu', 'nome', 'eh', 'nicole', 'maia']

## Recebendo dados (input)
let nome = prompt('qual o seu nome');
console.log(nome);

if (nome === 'nicole') {
    alert('é isso ai garotinha');
}

## Manipulação do DOM

document = estamos falando da página inteira do site.
.getElementById = queremos obter o elemento usando a propriedade id.
.innerText = que é o texto que esta dentro do elemento.
.getElementsByClassName = queremos obter o elemento usando a propriedade class.
.value = é o valor que está dentro do input.

exemplo:
document.getElementsByClassName('text')[0].innerText = 'outrotext'
usasse [] pois esta no plural elements

document.getElementById('text').innerText = 'outrotext'


### document.getElementById()
Retorna a referência do elemento através do seu ID.

var elemento = document.getElementById(id);

````
<!DOCTYPE html>
<html>
<head>
  <title>Exemplo getElementById</title>
  <script>
  function mudarCor(novaCor) {
    var elemento = document.getElementById("para1");
    elemento.style.color = novaCor;
  }
  </script>
</head>
<body>
  <p id="para1">Algum texto de exemplo</p>
  <button onclick="mudarCor('blue');">Azul</button>
  <button onclick="mudarCor('red');">Vermelho</button>
</body>
</html>
````


















































































































