## Guia de Javascript

### Assuntos:

* **[Array, métodos, length e spreed operator ;](#array-métodos-length-e-spreed-operator)**

* **[Objetos em Javascript ;](#Objetos-em-Javascript)**

* **[DOM Manipular HTML com Javascript ;](#DOM-manipular-html-com-javascript)**

* **[DOM Manipular CSS com Javascript ;](#DOM-manipular-css-com-javascript)**

* **[Funções em Javascript, e um extra: Arrow Function ;](#funções-em-javascript-e-um-extra-arrow-function)**

* **[Eventos no Javascript ;](#eventos-no-javascript)**

* **[Estruturas if else e switch case no Javascript ;](#estruturas-if-else-e-switch-case-no-javascript)**

* **[Estruturas for, forEach, while e do while no Javascript.](#estruturas-for-forEach-while-do-while-no-javascript)**

<br>

### Array, métodos, length e spreed operator

#### Declaração de Arrays:

* Forma padrão de declarar array:

* `let lista = []`

* Outra forma de declarar uma lista, é pelo método Array():

* `let lista2 = Array()`

#### Declaração de Arrays com Valores:

* `let produtos = ['Arroz', 'Feijão', 'Leite']`

* `var numeros = Array(10, 20, 30)`

* `let meses = ['Jan', 'Fev', 'Mar', 'Abr']`

#### Adicionar itens no final da lista, usando o método push():

* `produtos.push('Açúcar', 'Trigo')`

* Resultado: `['Arroz', 'Feijão', 'Leite', 'Açúcar', 'Trigo']`

* `numeros.push(40, 50, 60, 70)`

* Resultado: `[10, 20, 30, 40, 50, 60, 70]`

* `meses.push('Mai', 'Jun', 'Ago', '07')`

* Resultado: `['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Ago', '07']`

#### Remover itens no final da lista, usando o método pop():

* `produtos.pop()`

* Resultado: `['Arroz', 'Feijão', 'Leite', 'Açúcar']`

* `numeros.pop()`

* Resultado: `[10, 20, 30, 40, 50, 60]`

* `meses.pop()`

* Resultado: `['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Ago']`

#### Adicionar itens no início do array, usando o método unshift():

* `produtos.unshift('Uva', 'Maçã')`

* Resultado: `['Uva', 'Maçã', 'Arroz', 'Feijão', 'Leite', 'Açúcar']`

#### Remover itens no início do array, usando o método shift():

* `produtos.shift()`

* Resultado: `['Maçã', 'Arroz', 'Feijão', 'Leite', 'Açúcar']`

#### Remover itens de uma posição específica no array, com o método splice():

* `numeros.splice(1, 3)`

* splice(posição inicial, quantos remover)

* Resultado: `[10, 50, 60]`

#### Copiar itens de uma lista, usando o método slice():

* Copiando o array inteiro:

* `let meses1 = meses.slice()`

* Resultado: `['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Ago']`

* Copiar uma parte do array:

* `let meses2 = meses.slice(0, 3)`

* slice(posição inicial,  quantos copiar)

* Resultado: `['Jan', 'Fev', 'Mar']`

#### Ver o tamanho / comprimento do array, usando a propriedade length:

* `produtos.length`

* `meses.length`

* `numero.length`

* O resultado é quantidade total de elementos, dentro do array.

#### Copiar todos os itens da lista, usando o Spreed Operator ( ... ):

* `let teste = [...produtos, 'Ovo', 'Pera']`

* Resultado: `['Maçã', 'Arroz', 'Feijão', 'Leite', 'Açúcar', 'Ovo', 'Pera']`

#### Alterar itens do array pelo Índice:

* `let meses = ['Jan', 'Fev', 'Mar', 'Abr']`

* `meses[0] = 'Janeiro'`

* Resultado: `['Janeiro', 'Fev', 'Mar', 'Abr']`

* `meses[3] = 'Abril'`

* Resultado: `['Janeiro', 'Fev', 'Mar', 'Abril']`

<br>

### Objetos em Javascript

* Objetos são formados por: propriedade / chave : valor

#### Criar e declarar objetos:

* `let pessoa = {`

        nome   : "Luan",
        idade  : 20,
        peso   : 70.5,
        altura : 1.80,
        doador : false,
   `}`

* `let produtos = {`
    
        descricao : [],
        preco     : []
   `}`

* `const carros {`

        marca  : ['Ford', 'Fiat', 'GM'],
        modelo : ['Ka', 'Uno', 'Corsa'],
        ano    : [1999, 2005, 2010]
   `}`

#### Acessar propriedade usando ( . ):

* `pessoa.nome`

* Resultado: `'Luan'`

* `pessoa.idade`

* Resultado: `20`

* `pessoa.peso`

* Resultado: `70.5`

#### Acessar propriedade com [' ']:

* `pessoa['nome']`

* Resultado: `'Luan'`

* `pessoa['altura']`

* Resultado: `1.80`

#### Usando propriedade de objeto para cálculos, como a fórmula do IMC, por exemplo:

* `let imc = pessoa.peso / (pessoa.altura * pessoa.altura)`

#### Usando o método toFixed(), para limitar as casas decimais:

* `console.log("IMC " + imc.toFixed(2)`

#### Alterar valor de propriedade:

* `pessoa.nome = "João Matheus"`

* `produtos.descricao = ['Arroz']`

* `produtos.preco = [4.99]`

* Usando spreed operator, para não substituir o valor, mas sim, para adicionar uma cópia dos valores anteriores e colocar novos valores:

* `produtos.descricao = [...produtos.descricao, 'Feijão', 'Carne']`

* `produtos.preco = [...produtos.preco, 9.99, 4.79]`

#### Usando spreed operator em objetos declarados com constante ( const ):

* `carros.marca = [...carros.marca, 'VW']`

* `carros.modelo = [...carros.modelo, 'Fusca']`

* `carros.ano = [...carros.ano, 1979]`

<br>

### DOM Manipular HTML com Javascript
