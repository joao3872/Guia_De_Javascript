## Guia de Javascript

### Assuntos:

* **[Array, métodos, length e spreed operator ;](#array-métodos-length-e-spreed-operator)**

* **[Objetos em Javascript ;](#Objetos-em-Javascript)**

* **[DOM Manipular HTML com Javascript ;](#DOM-manipular-html-com-javascript)**

* **[DOM Manipular CSS com Javascript ;](#DOM-manipular-css-com-javascript)**

* **[Funções em Javascript, e Arrow Function ;](#Funções-em-Javascript-e-Arrow-Function)**

* **[Eventos no Javascript ;](#eventos-no-javascript)**

* **[Estruturas if else e switch case no Javascript ;](#estruturas-if-else-e-switch-case-no-javascript)**

* **[Estruturas for, forEach, while e do while no Javascript.](#estruturas-for-forEach-while-e-do-while-no-javascript)**

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

* ``titulo.innerHTML = `Título Novo <span>OK</span>` ``

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

<br>

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

<br>

### Funções em Javascript, e Arrow Function

#### Função sem parâmetros e sem retorno (procedure), é um procedimento:

* `function olaMundo() {`

      document.write('Olá Mundo sem retorno.')
  `}`

#### Função sem parâmetros e com retorno (function), é uma função:

* `function olaMundo2() {`

      return 'Olá Mundo com retorno.'
  `}`

#### Fazer a chamada da função, para executá-la:

* `olaMundo()`

* No caso da função olaMundo2(), é preciso utilizar document.write() para chamar a função, porque o return da mesma, está retornando apenas uma string.

* `document.write(olaMundo2())`

* #### Observação:
    Caso, dentro da função esteja assim: return document.write('Um texto aqui...'), a função poderá ser chamada assim: olaMundo2()

#### Funções com Parâmetros e sem retorno (procedure):

* `let x = 2`
* `let y = 1`
* `let frase = "Só sei, que nada sei..."`

<br>

* `function somar(num1, num2) {`

      document.write(num1 + num2)
  `}`

#### Funções com Parâmetros e com retorno (function):

* `function somar2(n1, n2) {`

      return n1 + n2
  `}`

#### Chamada das funções:

* `somar(x, y)`

* `document.write(somar2(17, 5))`

* ``document.write(`<p>somar2(3, 5)</p>`)``

#### Função dentro de outra:

* Uma função dentro da outra, pode ser colocada com nome, apenas o nome da função ou pode adicionar uma função anônima.

* `function exibirSoma() {`

      somar(x, y)
  `}`

* `exibirSoma()`

* Função Anônima: não possui nome, pode ter parâmetros se precisar, e pode ter retorno, caso necessário.

* `titulo.addEventListener('click', function () {`

      alert("Clicou no Título.")
  `})`

#### Arrow Function:

* Arrow Functions é uma técnica que surgiu em 2015, a partir do ES6 (EcmaScript 6).

* `const fraseArrow = () => document.write("Essa é uma frase de exemplo, com Arrow Function.")`

* #### Observações:
    Não precisa usar as palavras: function e return.

    Não se usa nome nesta função, porém, precisa usar variável.

    Não precisa usar {} ( chaves ), caso, a Arrow Function seja usada para executar uma única instrução.

    Se for usada duas instruções ou mais para ser executada pela arrow function, é obrigatório o uso de chaves.

    E também, é considerada uma Função Anônima.

* ``const frase2Arrow = () => `<p>Frase secundária de exemplo, com Arrow Function...</p>` ``

#### Chamada da Arrow Function:

* `fraseArrow()`

* Quando dentro da função não é usado um método de saída, a chamada da função é declarada assim:

* `document.write(frase2Arrow())`

<br>

### Eventos no Javascript

#### Evento onLoad:

* Serve para executar uma função, quando a página é carregada e também, toda vez que a página é recarregada.

* `onLoad="carregou()"`

#### Evento onScroll:

* Serve para executar uma função, quando a barra de rolagem ( scroll ) rolar / quando for movimentada.

* `onScroll="rolandoScroll()"`

#### Evento onClick:

* Serve para executar uma função, quando um item é clicado.

* `onClick="clicou()"`

#### Evento onMouseOver:

* Executa uma função, quando o cursor do Mouse estiver sob / em cima de um item.

* `onMouseOver="itemFocado()"`

#### Evento onFocus:

* Executa uma função, quando o item é focado. Exemplo: quando o onFocus é usado em uma tag input, o foco é  ativado quando o usuário, clica dentro do input.

* `<input type="text" placeholder="Digite aqui..." onFocus="focoNoInput()" />`

#### Evento onFocusOut:

* Executa uma função, quando o item perde o foco. Exemplo: quando o onFocusOut é utilizado em uma tag input e mesmo está focado, o foco é perdido quando o usuário clica fora do input.

* `onFocusOut="semFocoNoInput()"`

#### Evento onKeyPress:

* Executa uma função, quando qualquer tecla do teclado é apertada / pressionada e em seguida é solta.

* `onKeyPress="avisarQueTeclou()"`

* #### Observação:
    Quando os eventos são utilizados no HTML, devem possuir a palavra on na frente do evento. E além disso, quando um evento é usado no HTML, o mesmo é executado de forma Imperativa / forçada.

#### Usando eventos no Javascript:

* Eventos no JS, são utilizados através do método, .addEventListener(), com este não pode colocar a palavra on na frente do evento.

* `let button1 = document.querySelector('#btn1')`

* `let button2 = document.querySelector('#btn2')`

* `let botaoEnviar = document.querySelector('#btn3')`

* `button1.addEventListener('mouseover', function () {`

      console.log('Foco no botão 1.')
  `}`

* `button2.addEventListener('blur', function () {`

      console.log('Botão 2 perdeu o foco.')
  `})`

* HTML para o exemplo abaixo:

`<form action="">`

    <input type="email" placeholder="E-mail..." class="input_email" />`

    <input type="password" placeholder="Senha..." class="input_senha" />

    <button type="submit" id="btn3" class="btn_enviar">Enviar</button>

`</form>`

* #### Observação:
    Dentro da tag form, possui um botão do tipo submit, é justamente o submit, que faz o envio dos dados preenchidos nos itens dentro da tag form.
    Quando as informações são submetidas, a página recarrega. Então para evitar isso, é necessário usar o método: .preventDefault(), para não fazer o envio com recarregamento da página.

* `botaoEnviar.addEventListener('click', function (event) {`

      event.preventDefault()
      console.log('Clicou no Botão Enviar.')
  `})`

<br>

### Estruturas if else e switch case no Javascript

* `let sit1 = document.querySelector('.sit1')`

* `let sit2 = document.querySelector('#sit2')`

* `let sit3 = document.querySelector('.sit3')`

* `let escolha = document.querySelector('#escolha')`

* `let notaFinal1 = 3`

* `let notaFinal2 = 8`

* `let notaFinal3 = 5`

#### Estruturas Condicionais:

* IF ( se )

* Neste caso, se a condição for complida a ação entre { }, será realizada. Agora, se a condição não for satisfeita, com apenas o if, não vai realizar nenhuma ação.

* `if (notaFinal1 >= 7) {`

      sit1.textContent = 'Aprovado !'
  `}`

* Usar apenas o if, é bom quando você quer executar um único tipo de ação, somente naquela vez.

#### IF ( se ) e ELSE ( senão ):

* Essa é uma Condicional Composta. Serve para verificar uma condição e fazer o seguinte: se a condição for satisfeita, será executado a ação dentro do bloco do IF, caso a condição não seja satisfeita vai executar outra ação.

* `if (notaFinal1 >= 7) {`

      sit1.textContent = 'Aprovado(a)'
  `} else {`

      sit1.textContent = 'Reprovado(a)'
  `}`

#### IF Ternário:

* O que vem antes do ponto de interrogação, é a condição.
* O ponto de interrogação ( ? ) significa: então.
* Dois pontos ( : ) significa: senão.

* `notaFinal2 >= 7 ? sit2.textContent = 'Passou' : sit2.textContent = 'Ficou'`

* Se no IF Ternário, a condição for satisfeita será executada a ação que está entre ( ? ) e ( : ), se não for satisfeita vai executar o que vem depois de ( : ).

#### IF Encadeado ou Aninhado:

* Neste caso, podem ser feitas muitas verificações.

* `if (notaFinal3 >= 7) {`

      sit3.textContent = 'Aprovado'
  `} else if (notaFinal3 <= 3) {`

      sit3.textContent = 'Reprovado'
  `} else {`

      sit3.textContent = 'Recuperação'
  `}`

* Se a condição não for satisfeita no if, a condição passa a ser verificada no else if.
* Se no else if, a condição não for satisfeita, executa o que está no else.
* A condição que for satisfeita, irá executar a sua respectiva ação.

#### Switch Case:

* #### Observações:
  * switch case é uma estrutura de Decisão.

  * switch significa: escolha e o case significa: caso.

  * Executa uma ação de acordo com o valor da variável.

  * Verifica se o valor desta variável, é igual ao valor especificado no case, se essa verificação for verdadeira, vai executar uma ação.

  * É usado o break para parar, depois de um case ser executado, se não utilizar o break, todos os casos serão executados de uma vez.

  * E por fim, se nenhum caso for satisfeito, será executado o que estiver no default.


* Executa o default:

* `let situacao = ''`

* `let situacao = 'Aprovado'`

* Executa case 'Aprovado'.

* `let situacao = 'Reprovado'`

* Executa case 'Reprovado'.

* `let situacao = 'Recuperação'`

* Executa case 'Recuperação'.

* `switch (situacao) {`

      case 'Aprovado':
          escolha.textContent = 'Passou de ano !'
          break
      case 'Reprovado':
          escolha.textContent = 'Não passou de ano.'
          break
      case 'Recuperação':
          escolha.textContent = 'Ainda tem uma chance.'
          break
      default:
          escolha.textContent = 'Estude.'
  `}`

<br>

### Estruturas for, forEach, while e do while no Javascript

* `let carros = ['Camaro', 'Onix', 'S10']`

#### Estrutura de Repetição For ( para ):

* Normalmente a variável usada no for, é a letra ( i ), que significa: interador, interação ou index.

* O for é formado por: Variável de interação, Condição e Incremento ou Decremento.

* O incremento, faz a contagem dos itens de 1 em 1 em ordem crescente.

* E o decremento, faz a contagem em ordem decrescente.

* `for (let i = 1; i <= 5; i++) {`

      document.write(i + " ")
  `}`

* For com decremento:

* `for (let i = 5; i >= 0; i--) {`

      document.write(i + " ")
  `}`

#### Varrendo um array com FOR:

* Enquanto a variável de interação for menor ou igual ao tamanho da lista, conte mais um.

* `for (let i = 0; i <= carros.length; i++) {`

      document.write(`<li>${carros[i]}</li>`)
  `}`

#### forEach ( para cada ):

* forEach é um método / função de array.

* `let frutas = ['Pera', 'Uva', 'Maçã', 'Banana', 'Melancia']`

* Os parâmetros do forEach: elementos do array e índice.

* `frutas.forEach(function (fruta, i) {`

      document.write(`${i} ${fruta} <br>`)
  `})`

* Não é obrigatório o uso de dois parâmetros, você pode usar só um também.

* `carros.forEach(function (carro) {`

      document.write(`${carro} <br>`)
  `})`

#### Estrutura de Repetição WHILE ( enquanto ):

* É necessário criar variável de contador fora do laço.

* `let contador = 0`

* `while (contador < frutas.length) {`

      document.write(`${frutas[contador]} <br>`)
      contador++   // contador + 1
  `}`

#### Estrutura DO WHILE ( faça enquanto ):

* do while, executa a ação pelo menos uma vez, mesmo antes da verificação do while ser feita.

* `let iterador = 0   // variável de contador.`

* `do {`

      document.write(`${carros[iterador]} <br>`)
      iterador++   // iterador + 1
  `} while (iterador < carros.length)`

<br>

### Créditos:

* #### Este conteúdo, foi baseado nas aulas do curso de Javascript do <a href="https://m.youtube.com/c/ProfessorEdsonMaia" target="_blank">Professor Edson Maia</a>, no YouTube.

* #### <a href="https://youtube.com/playlist?list=PLnex8IkmReXxZEXje06kW1uCwm5iC8M_Z" target="_blank">Link do Curso</a>
