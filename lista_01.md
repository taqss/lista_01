Faça uma cópia deste arquivo .md para um repositório próprio
Resolva as 8 questões objetivas assinalando a alternativa correta e justificando sua resposta.
Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
Lembre-se de utilizar as estruturas de código como esta aqui com `  ou
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
Resolva as questões com uso do Visual Studio Code ou ambiente similar.
Teste seus códigos antes de trazer a resposta para cá.
Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove.
Questões objetivas
1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.

```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
**a) A saída será undefined seguido de erro**
**Justificativa: Para o primeiro console.log(x) será undefined pois a variável foi atribuída, mesmo que depois do console.log(), e caso se a variavél x estivesse antes do cosole.log(), teria saído uma resposta. Agora para o consle.log(y), sua saída foi erro, pois a variável criada com let é limitada por ser apenas atribuída no seu escopo, resultando em uma variável sem atribuição numérica. **

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```
**a) Substituir if (a || b === 0) por if (a === 0 || b === 0)**
**Justificativa: Para o código anterior, há um erro, que se traduz quanto a estutura if para verificar se 'a' e 'b' são iguais a 0. A estrutura 'if (a || b === 0)' está incorreta pois apenas verifica o valor numérico de "b", enquanto 'a' seria sempre lido como 'true' para qualquer valor diferente de zero. Como solução, 'a' também deve ser especificada no código, ficando 'if (a === 0 || b === 0)' e tornando-o correto.**

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.

```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```
a) O código imprime 1000.

**b) O código imprime 200.**
**Justificativa: No código anterior, seu retorno seria 200 devido a dependência dele para com o termo 'break', que limita ele a parar de ler e retornar o 'preço' anteriormente atribuído. Logo, se houvesse um break depois da linha 6, o resultado seria 1000.**

c) O código imprime 50.

d) O código gera um erro.

4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.

```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

**d) 24**
**Justificativa: A lógica desse código se traduz da seguinte forma: dada uma lista que vai de 1 a 5, todos esses números serão multiplicados por 2 e em seguida haverá um filtro deles, que somente os que forem maiores que cinco serão selecionados e todos serão somados.**

5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```
a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

**c) ["banana", "abacaxi", "manga", "laranja"]**
**Justificativa: Para o código anterior, uma lista é apresentada, porém o termo 'splice' modifica o array original, sendo que, '1' indica qual termo é tomado como ponto de início para a remoção dos itens, '2' é o número de termos que serão retirados do array original, e logo em seguida vêm os termos que substituirão os que foram removidos. Portanto, serão removdos da lista 'maçã' e 'uva', e em seus lugares ficarão, respectivamente, 'abacaxi' e 'manga'.**

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.
II. Em JavaScript, a herança é implementada através da palavra-chave extends.

a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

**b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.**
**Justificativa: A segunda afrimação não justifca a primeira pois ela está apenas explicando como se aplica a herança, ao contrário de explicar o por quê de ela funcionar de tal forma.**

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```
I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.
II) O método apresentar() da classe Funcionario sobrepõe o método apresentar() da classe Pessoa, mas chama o método da classe pai usando super.
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

**a) I e II são verdadeiras.**
**Justificativa: A afirmção III está incorreta pois o código está correto, visto que a classe 'Funcionário' está herdando o método da classe 'Pessoa' através do termo "extends".**

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.

Asserção: O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.
Razão: Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

**b) A asserção é verdadeira e a razão é falsa.**
**Justificativa: Para JavaScript, quando é utilizado o método de sobrecarga, o último método a ser definido será válido, o que faz com que ele seja o substituto do método anterior**

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

Questões dissertativas
O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.
```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
```javascript
//criação das variáveis
var numeros = [1, 2, 3, 4];
var soma = 0;

//mudando numeros.seize para numeros.lenght, pois é a nomenclaura padrão para chamar um cumprimento de uma array
function somaArray(numeros) {
    for(i=0; i<numeros.lenght; i++) {
        //para que o loop seja criado, é necessário colocar o '+' antes do '='
        soma += 2*numeros[i];
    }
    return soma;
}
    console.log(somaArray(numeros));
```

Crie um exemplo prático no qual você tenha duas classes:
Uma classe Produto com atributos nome e preco, e um método calcularDesconto() que aplica um desconto fixo de 10% no preço do produto.
Uma classe Livro que herda de Produto e modifica o método calcularDesconto(), aplicando um desconto de 20% no preço dos livros.
Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe Livro.
```javascript
//criação da classe Produto
class Produto {
    constructor(nome, preco) {
    this.nome = nome;
    this.preco = preco;
    }

//criação do método calcularDesconto()
    calcularDesconto() {
        this.preco = this.preco * 0.9;
    }
}

//criação da classe que herda a classe Produto
class Livro extends Produto {
    calcularDesconto() {
        this.preco = this.preco * 0.8; //redefinição de 'calcularDesconto'
    }
}

    //criação das variáveis 'produto' e 'livro'
    produto = new Produto("Marca texto", 7.5)
    livro = new Livro("O Príncipe", 24.99)

    //criando a relação das variáveis com os métodos
    produto.calculasDesconto();
    livro.calcularDesconto

    console.log(produto)
    console.log(livro)
```
