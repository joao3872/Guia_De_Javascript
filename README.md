## Guia de Javascript

### Assuntos:

* **[Array, métodos, length e spreed operator ;](#array-métodos-length-e-spreed-operator)**

* **[Objetos em Javascript ;](#Objetos-em-Javascript)**

* **[DOM Manipular HTML com Javascript ;](#DOM-manipular-html-com-javascript)**

* **[DOM Manipular CSS com Javascript ;](#DOM-manipular-css-com-javascript)**

* **[Funções em Javascript, e um extra, Arrow Function ;](#funções-em-javascript-e-um-extra-arrow-function)**

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

#### Método de Seleção:

* Seleção por Tag

* `document.querSelector('h1')`

* Seleção por Id

* `document.querySelector('#id_da_tag')`

* Seleção por Class

* `document.querSelector('.class_da_tag')`

#### Variáveis do Javascript:

* `var`

* var, serve para declarar uma variável.

* `let`

* let, declara variável e pode ter seu valor editado.

* `const`

* const declara variável, porém, não pode ter seu valor editado.

#### Capturar e armazenar valores em uma variável:

* `let titulo = document.querySelector(".titulo")`

* `var texto = document.querySelector('#texto')`

* `const dataNascimento = document.querySelector('.dataNascimento')`

* `var frase = 'Só sei, que nada sei !'`

* `let ano_nascimento = 1999`

* `const autor = "Fulano de Tal"`

#### Acessar valor / conteúdo de uma tag com a propriedade textContent:

* `let titulo = document.querySelector('.titulo')`

* `titulo.textContent`

#### Atribuir valor / conteúdo de uma tag com textContent:

* `titulo.textContent = "Título Novo..."`

#### Acessar valor de uma tag com innerHTML:

* `titulo.innerHTML`

#### Atribuir valor de uma tag com innerHTML:

* `titulo.innerHTML = 'Título Novo <span>OK</span>'`

#### Seleção de todas as Tags iguais, Class igual e Id igual:

* `const titulo = document.querySelectorAll('h2')`

* `let item = document.querySelectorAll('.item')`

* `var conteudo = document.querySelectorAll('#conteudo')`

* O .querySelectorAll(), armazena os valores / conteúdos de um container, em um Array interno, e separa por índices do Array.

<br>

* HTML para o exemplo abaixo:

`<div class="container">`

      <h3>Título 1</h3>
      <p>Texto 1</p>

`</div>`

`<div class="container">`

      <h3>Título 2</h3>
      <p>Texto 2</p>

`</div>`

`<div class="container">`

      <h3>Título 3</h3>
      <p>Texto 3</p>

`</div>`

#### Acessando e exibindo, os conteúdos do .querySelectorAll(), através do índice:

* `let testando = document.querySelectorAll('.container')`

* `document.write(testando[0].textContent)`

* Resultado:

      Título 1
      Texto 1

* `document.write(testando[1].textContent)`

* Resultado:

      Título 2
      Texto 2

* `document.write(testando[2].textContent)`

* Resultado:

      Título 3
      Texto 3

#### Para atribuir / editar valor dos itens do querySelectorAll():

* `testando[0].textContent = 'Novo Texto.'`

#### Seletores das versões anteriores, que ainda podem ser usadas:

* É recomendável o uso do querySelector() e do querySelectorAll(), porque são as duas seletores mais modernos.

* Seletor apenas para Tag:

* `let testeTag = document.getElementsByTagName('div')`

* Seletor apenas para Id:

* `let testeId = document.getElementById('titulo')`

* Seletor apenas para Class:

* `let testeClass = document.getElementsByClassName('box')`

### DOM Manipular CSS com Javascript

#### Inserir uma imagem com setAttribute():

* `let imagem = querySelector('#imagem')`

* .setAttribute(), serve para configurar um atributo. Basicamente este método possui dois parâmetros: nome do atributo a ser setado e o valor deste atributo.

* `imagem.setAttribute('src', 'image/img.png')`

* Pode ser usado para adicionar / modificar uma propriedade.

* `imagem.setAttribute('width', '230px')`

#### Manipulando CSS com DOM:

* `titulo.style.color = '#2194ff'`

* `titulo.style.background = '#000'`

* `titulo.style.borderBottom = '5px solid #2194ff'`

* `titulo.style.padding = '.625rem'`

* `titulo.style.borderRadius = '8px'`

#### Usando .setAttribute() para manipular CSS:

* `let box = document.querySelectorAll('.box')`

* `box[0].setAttribute('class', 'verde')`

* Com o  setAttribute('class', 'nomeClass'), você pode realizar todas as alterações no item do html, através do css usando a class específica, ao invés de utilizar o DOM para tudo.

#### Remover a class configurada pelo .setAttribute(), usando o removeAttribute():

* `box[0].removeAttribute('class')`

* O problema de usar o removeAttribute(), é que acaba removendo outras classes, além da class que é para remover.

* A solução para este problema, pode ser a classList.add() e classList.remove().

#### Escutador de Eventos, classList.add() e classList.remove():

* .addEventListener(), serve para escutar eventos, caso, esse método identifique o evento especificado em seu parâmetro, será executada uma ação.

* `btnDark.addEventListener('click', modoDark)`

* `function modoDark() {`

      tela.classList.add("dark")
      tela.classList.remove("light")
  `}`

* .classList.add("nomeDaClass"), adiciona uma class na lista de classes e aplica todas as alterações que a class CSS possui.

* .classList.remove("nomeDaClass"), remove a class da lista de classes e retira todas as alterações que a class CSS estava aplicando.

### Funções em Javascript, e uma extra, Arrow Function
