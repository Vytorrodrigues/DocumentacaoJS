# DocumentaçãoJS

- Documentação de todo conteúdo de Javascript que estudei até agora
- Está documentação é para organizar o conteúdo e facilitar nos estudos e revisões futuras
- Vocês podem adicionar as anotações de vocês, o objetivo é deixar essa documentação robusta e de fácil entendimento para todos
- Javascript é uma linguagem dinâmica, possuindo alterar variáveis e até mesmo o tipo das variáveis
- **LEMBREM DE FAZER OS COMMITS REGISTRANDO AS MUDANÇAS PFV**


# Ecmascript:

- Ecmascript é diferente do javascript, ele especifica como o JS funciona

# Strict mode:

- "use strict";
- Serve para definir correções no código, evita erros silenciosos. Podendo inibir algumas funcionalidades também

# Declaração de variáveis:

- Variáveis (tipo primitivo) são armazenadas na memória, diferentes de objetos que tem seu valor atribuido a ele (tipo referencial)
- **Const, let e var**: 
- **Const** possui escopo/alcance global e não pode ser alterado
- **Var** também possui escopo global, mas ela pode ser mudada facilmente, por isso não é muito bom usa-lá
- **Let** possui escopo global e local, a depender de onde for inserida
- Atualmente o recomendado é usar o let e const para evitar sobreposição de variáveis. Deve-se ficar de olho sempre no escopo
- Escopo é onde e como determinado elemento são acessíveis
- Variáveis em JS são case sensitive, ou seja: diferenciam letras maíusculas de minúsculas 
ex: let nome = "Pedro"; é diferente de let Nome = "Pedro";
- No js vc pode declarar tanto em camel case: nomeObjeto, como em snake case: nome_objeto DAR PREFRÊNCIA AO CAMELCASE 
- Não pode usar espaço para declarar uma variável

# Hoisting:
- Usar variáveis ou funções antes mesmo de ser executada, o elemento é movido para o topo do bloco
- Variáveis são movidas para o topo do seu escopo, mas precisam ser declaradas antes
- Funções também vão para o topo do escopo 

# Operadores: 

* = em JS significa recebe determinado valor
- Números flutuantes em JS usam o . 
ex: 1.2, 4.56 etc
- + (Soma), - (Subtração), / (Divisão inteira), * (Multiplicação) , ** (Potência), % (Mod/ Módulo/ Resto)
- ++ (Incremento), -- (Decremento): Aritméticos
- += (a = a + 1), -=, *=, /=, **=, %=, : Atribuição
- == (Igual), === (Igual ao tipo de elemento, string, número, booleano etc), != (Diferente), !== (Dieferente do tipo), >(Maior), <(Menor), <= (Menor igual), >= (Maior igual), ??= (igual a null ou undefined): *Comparadores*
- && (*and*), || (*or*), !() (*not*): Operadores lógicos dão respostas binárias, True(1) ou False(0)
- *Ordem de procedência*: (), **, *  /  %, +  -
- *Ordem de procedência dos operadores lógicos*: !, &&, ||

# Ternário:

- Teste lógico atribuido á uma variável
- ? :  -> ->  Teste? True: False;

# Functions:

- Conjunto de instruções dentro de um determinado escopo, que pode ser ativado ao digitar seu nome
ex: function falar(){};
falar(); Aqui eu estou chamando a função para ativala
- Dentro dos parenteses vão seus argumentos ex: event
- Dentro da função temos os parãmetros
- Return dentro da função permite que usemos o valor fora da função
- Arrow function ou FUNÇÃO ANÔNIMA é a forma simplificada de escrever uma função ex: **() => {};**
- Muito utilizada em Programação Orientada a Objetos (POO), permite agrupamento e reuso do código, sequência lógica, além de permitir um código escalável, de fácil entendimento, boa manuntenção, prolongando a vida do script

# JSdoc: 
- Documentar no próprio código o funcionamento das funções, seus argumentos e parâmetros
- /**
  *@param {*}email user email
  *@param {*}password more than 6 characters
  *@returns //o que a função retorna
  */

# Formatador:
- Permite a interpolação
- Ao usar crase pode passar o formatador dentro  ex: `${variável}`
- Formatadores ajudam a evitar muitas concatenações, a depender do caso

# Document Object Notation (DOM):

- window, document, body, html etc. São elementos da árvore DOM, eles seguem a linha de como o código HTML é montado, como raízes de uma árvore, aqueles acima são pais dos elementos abaixo
ex: window -> location
    document -> head/body 
- **.querySelector("id/class e nome da tagdentro do elemento")**: nome da tag, com #id ou .classe que vc deseja selecionar no document
- **.querySelectorAll("")**: seleciona  todos os elementos de mesmo nome, cria uma lista
- O querySelector não é suportado por versões antigas dos navegadores(antes de 2008/9)/ por isso usa-se transpiladores ex: babeljs.io
- **.getElementById("")**: pega o elemento HTML baseado em seu ID
- **.getElementByTagName("")**: pega o elemento pelo nome da tag
- **.getElementByName("")[]**: não entendi como funciona esse direito *TODO: PESQUISAR*
- **.getElementByclassName("")**: pega o elemento pelo nome da classe
- **.innerText = ""**: usado para inserir texto no código HTML, apenas o texto visível, considera o estilo css
- **.textContent = ""**: pega todo texto incluindo o oculto e script, sendo mais rápido
- **.innerHTML = ""**: pega a formatação em código e passa direto para o código, mas deve ter cuidado para não inserir códigos sensiveis pois pode exibir brechas e permitir invasões no sistema. Permite consturir elementos html e inserir com JS
- **.value = ""** pega as informações nos campos selecionados
- **.target = ""** exibe quando um elemento é  clicado
- **.item()**: seleciona o elemento pela posição dele
- **.classList()**: acessa classe do elemento
- **.add()**: adiciona uma classe, atribuido ao classList
- **.remove()**: remove uma elemento
- **.toggle()**: se tiver classe remove, se não tiver adiciona, atribuido ao ClassList
- - **typeof()**: verifica o tipo do elemento, string, object, number
- **Number()**: transforma elemento em número, usado quando não precisa definir se é inteiro ou decimal
- **.Number.isInteger()**: verifica se o numero é int e retorna: true para int e false para float
- **parseInt()**: para transformar em inteiro 
- **parseFloat()**: para um flutuante
- **string()**: ou toString() muda para uma string ou só colocar dentro de aspas ""
- **toUpperCase()**: deixa maíusculo
- **toLowerCase()**: deixa minúsculo
- **toFixed()**: permite selecionar quantas casas decimais queremos que o número apresente
- **replace(elemento que quero substituir, elemento que quero adicionar)**: permite alterar uma sequencia de carcateres iu uma string
- **toLocaleString("pt-br", {style: "currency", currency: "BRL"})**: exibição de valor monetário, euro, dolar, yen, etc
- **.createElement()**: cria um elemento tag HTML
- **.setAttribute("atributo, nome")**: coloca um atributo em um elemento HTML, id, class, src etc. Se for uma função tem que colocar os parenteses 
- **.removeAttribute()**: remove o atributo
- **.createTextNode()**: cria texto
- **appendChild()**: adiciona o elemento como filho, mas só um por vez
- **append()**: acrescenta um elemento após o último filho, pode adicionar mais de um elemento por vez
- **prepend()**: adiciona um elemento antes do último filho
- **.charAT()**: seleciona um caractere do string
- **.localeCompare()**: compara os strings de acordo com a localidade, incluindo acentuação etc
- **.style.color = "nome da cor"**: muda a cor do parametro
- **.style** : usado para mudar elementos css
  
# DOM Events:

- **onclick**: ao clicar com o mouse no elemento
- **ondblclick**: dois clicks no elemento
- **onmouseover**: passar mouse em cima do elemento
- **onmouseout**:  dispara quando o mouse sai do elemento
- **onmousemove**: mouse movido dentro do elemento
- **onmousedown**: clique do scroll do mouse precionado
- **onmouseup**: quando o clique do botão do mouse que estava pressionado é solto
- **onfocus**:  dispara quando elemeno recebe foco
- **onchange**: dispara ao mudar o conteúdo
- **onblur**: quando o elemento perde o foco
- **onkeydown**: quando uma tecla é pressionada
- **onkeypress**: quando tecla pressionada é solta
- **onkeyup**: quando a tecla é solta sobre um elemento
- **onload**: dispara ao carregar página
- **onresize**: dispara ao redimensionar tela
- **focus**: focar campo

- Os eventos podem ser chamados de duas formas: variável.evento(função que quero chamar); ou variável.addEventListenner("evento", função sem parenteses);

# Objetos:

- Instância de uma classe
- Métodos: são instruções, comportamentos desse objeto, funções
- Propriedade: característica ou atributo de um objeto
- Objeto dentro de outro é um aninhamento de objetos
- Declarar com snake_case
- Objetos são elementos declarados com {} onde recebem uma propriedade e um valor
ex: const localizacao = {
        cidade: "João Pessoa",
        cep: 679802,
        rua: "Antonio Valdenor Labamda"
        pais: function localidade(){}; -Isso é um método

}
- Objetos literais são objetos simples com propriedades (atributo, valor) e métodos
- **Desestruturação de Objeto**: criamos uma variavel com o nome da propriedade dentro de chaves{}, para alterar o valor dessa propriedade usamos : (dois pontos)
ex:
    let user {
        name: "Fulano",
        pass: "1234"
    }

    const {name} = usuario;
    const {name:Beltrano} = usuario; //Aqui mudamos o valor da propiedade
    console.log(user.name) - acessando objeto
    //desestruturando obj com um método
    const {user, pass} =  user;
- Podemos desestruturar os objetos com métodos também
- É MUITO IMPORTANTE SEGUIR A ORDEM DOS NATRIBUTOS NA DESESTRUTURAÇÃO
    function newUser({user, pass}){
      //código
    };

    newUser({
      name: novo valor
      pass: novo valor
    });
  
- Se dermos um console aqui, conseguiriamos ver o valor da propiedade, no caso "Fulano"
- Para acessar objeto(atributos e métodos) chamamos assim: objeto.atributo ou objeto["atirbuto"] / objeto.metodo()
- Podemos usar o this para acessalos também
- **new**: Instancia de um objeto, usado para instanciar novos objetos
ex:
 function constructor(parametro){
     const obj = {};
     obj.parametro = parametro;

     return obj;
}

# Opitional Chaining(?):
- ? antes do . para acessar objetos
- Encadeamento opcional
- Permite acessar valores sem saber o conteúdo do objeto e retorna null, nulish, undefined
ex: objeto?.atributo -> retorna o valor

# Coalescência Nula(??):

- Verifica se é null ou undefined
- Se dor nulo retorna o valor da direita, se não seu conteúdo
ex: const nulo = null;
    const coalescencia = nulo ?? "Confirmado nulidade";
    console.log(coalescencia);
- Nesse caso o valor retornado seria "Confirmado nulidade", pois eu define uma váriavel do tipo nula

# Array/Matrizes:

- Usada para armazenar valores, objetos, variáveis etc. Ela é armazenada em uma variável
- Array vazio: let arr = [];
- As posições do array são contadas a partir do 0, ou seja: let arr = [1, 2, 3, 4]; equivale a 0, 1, 2, 3 em relação as posições
- **Desestruturação de array**: para desestruturar um array atribuimos um array de variáveis ao array antigo, estabelecendo váriaveis aos conteúdos do índice
- _ ou , ignora elementos do array. Para selecionar a posição do elemento que você quer
ex: const arr = [a, b];
    const newArr [variavelA, variavelB] = arr

- **Array.isarray()**: é usado para descobrir se tal elemento é um array
- **.join()**: troca separador dos itens do meu array / une textos
- **.pop()**: remove o último elemento do array
- **.shift()**: remove o primeiro elemento 
- **.lenght()**: mostra quantos elementos/comprimento do array/Strings
- **array[array.length - 1(aqui eu passo o valor de quantos elementos quero verificar)]**: verifica o elemento do array e me retorna seu valor, de trás para frente
- **unshift()**: adiciona um item a primeira posição
- **.push()**: adiciona elementos no final
- **.splice( posição do elemento, quantidade de itens que quero remover, qual item quero adicionar)**
- **split()**: separa baseado em um intervalo e transforma em um novo array
- **.from()**: separa cada letra e elemento do array, incluindo espaços
- **.concat()**: soma arrays
- **.slice(a,b)**: fatia o array a: baseado na posição dos elementos citados, e b: ultima posição especificada não é contada
- **.sort()**: deixa em ordem alfabética 
- **.sort((a,b) => a - b)**: usado para ordenar de forma crescente ou .sort(function(a,b) => { return a - b})
- **indexOf()**: busca posição no array
- **.forEach()**: faz uma iteração pelo array, função para cada elemento do array
- **.map()**: cria um novo array após mapear o antigo baseado em uma callback
- **.filter()**: filtra o array antigo, criando um novo array
- **.find()**: faz uma busca no array baseado em uma condição e retorna seu conteúdo
- **reduce((accumulator, currentValue, index) => {}, value)**: executa uma função retornando um único valor(value): soma, conta, concatenação etc
- **.findIndex()**: retorna o indice do array do primeiro elemento que satisfaça a condição. Caso contrário retorna -1 (Se tiver o use strict ativo no código ele da erro)
- **.include()**: verifica se tem algo incluso, busca strings
- **.starsWith()**: verifica se a string começa com o valor passado
- **endsWith()**: verifica se a string termina com o valor passado 

# Imutabilidade

- Impede que o elemento principal seja alterado
- Cria-se um cópia e a modifica, mantendo o original
- Podemos fazer uam referência, assim permitindo alterar os dois objetos
ex:    const objA = {
        atributoA:  valorA,
        atributo: valoB
  };
const objB = objA; //referência
- Para poder fazer as alterações só em um, devemos criar um novo objeto. Pra isso usamos o spread
ex: const objA = {atributos}
    const objB = {...objA}
- Assim temos um novo objeto na memória e o outro permanece imutável
- Devemos respeitar a ordem dos elementos e colocar o spread sempre primeiro, se não os valores passados pelo spread irão substituir os anteriores
- O mesmo vale para arrays também
- **Detectar mudanças** de objetos mutados é difícil, pois são mudados diretamente. Isso requer um objeto mutado p/ ser comparado as cópias de suas própria versões anteriores e uma árvore inteira de objetos p/ ser cruzada.
- **Objetos imutáveis** é mais fácil, se for referente ao anterior, concluimos que teve mudança

# Deep copy

- Valores referenciados
- Pesquisa mais profunda
- Pega itens aninhados (objetos e arrays)
- Utilização de spreads
ex: const objA = { atributoA: valorA, atributoB: [ { atributoC: valoC } ] };
    const objB = { ...objA, atributoB: [ ...objA.atributoB ] };
- Ao fazer as modificações, será possível acessar o objeto/array aninhado aninhado

# Shalow copy

- Valores primitivos
- Copia superficial, não pega os itens aninhados
- O que altera em A, altera em B também.
- É um elemento referenciado
ex: const objA = { atributoA: valorA, atributoB: valorB };
    const objB = { ...objA, atributoB: valorC };

# Shalow Freeze

- Impede modificações de objetos
- Não é uma modificação profunda (não funciona em objetos aninhados)
- Js em si não impede a modificação de objetos
ex: Object.freeze(nome do objeto);

# Deep freeze

- Imutabilidade total de um objeto, incluindo aninhados
- Para isso aplicamos uma função
ex: function deepFreeze(object){
     //pega as propriedades do objeto
    const props Reflect.ownKeys(object);
    //iteração nas propriedades do objeto
    for (let prop of props) {
      const value = object[prop]; //valor da propriedade
  };

  //verificação p/ aplicar deepFreeze no objeto
  if (value && typeof === "object" || typeof === "function") {
     deepFreeze(value);
  };
  return Object.freeze(object);
};

# Laços de repetição:

- **For, While**;
- **For**: usamos quando temos uma quantidade definida de loops, *for(inicialização, enquanto/teste lógico, /o que o código deve fazer){}*;
ex: um incremento -> -> *for(let i = 0; i < array.length; i++){console.log(array[i])};* esse código faz uma iteração passando por todos os elementos de um array (iterar: executar repetidamente)
- **for in**: *for (var in array)* interação em objetos e arrays
- **for of**: *for (var array of array)* interação pelas propriedades do objeto, só intera objeto se o obj estiver dentro do array
- **While:** usamos quando não sabemos a quantidades de loops a serem definidos, a variável de iteração é declarada fora do loop
- *while(condição){ código, incremento};*
- *do {código, incremento} while(condição);*
ex: 
    let array = [1, 2, 3, 4, 5, 6, 7];
    var i = 0;
    while(i < array.length){
        console.log(array[i]);
        i++
    };
- Nesse exemplo, assim como o do for, eu estou passando por cada elemento do array e imprimindo ele para ver seu elementos, se eu quisesse saber as posições bastava imprimir somente a váriavel de iteração i
- **continue**: pula a execução e vai para próxima

# Condições:

- **If, Else, Else if, Switch**
- *if(condição){ true }* condição simples
- *if (condição){ true }else{ false };* condição composta
- *if(condição){ true }else if(condição2){ true }else{ false }* condição aninhada
- É possível colocar outros if e else if dentro de um if etc.
- *Switch()*{ 
    case1: 
        resultado que eu quero
        break
    case2:
        resultado que eu quero
        break //quebra o loop 
    default:  
        break
};
- No *case* colocamos os casos e suas respectivas condições, no *Default* colocamos um erro, caso as condições não sejam cumpridas
- O switch funciona de forma literal, igual ao tipo ===
- É possível colocar um case dentro de outro, resultando em um mesmo valor


# Eventos de tempo:

- Execução de código em intervalo de tempo
- **setTimeout(função, tempo em milisegundos)**: executado somente uma vez
- **setInterval(função, tempo em milisegundos)**: executa repetidamente em 
determinado intervalo
- **clearTimeout(), clearInterval()**: usado para parar esse evento de tempo, definimos eles a uma váriavel e colocamos essa váriavel dentro do clear
- 1000 milisegundos = 1 segundo

# Classes:

- **Class**
- Herança baseada em protótipos
- Fábrica de objetos
- *constructor()* método para criação de objetos, baseado nos valores dentro dos parenteses
- É possível criar classes somente com métodos
- *this* é usado para criar os atributos das classes, chama os parametros e atribui a um objeto, faz referencia ao contexto
- Usar PascalCase para nomear classes
- Para instanciar um objeto é só fazer o seguinte: new nomeClasse() dentro do parentese passo o atributo que quero adicionar entre aspas ""
ex:
    class User(){
        constructor(email, password){
            this.email = email;
            this.password = password;
        }
    }
    const fulano = new User("fulano@email.com", "123345");
- Atributo privado em uma classe: *#nome_do_atributo*, são usados para não deixar atributos ou métodos acessiveis fora dessa classe. É usado quando precisamos que nenhuma outra classe interfira em um bloco
- Para desbloquear o atributo, pelo constructor: 
ex:    
    constructor(){ 
        this.#nome_do_atributo = valor que desejo atribuir;
    }
- Isso feito antes do constructor
- Posso usar get e set com atributos privados, deixandos privados
ex:
    get #nome_do_atributo(){
        return this.#nome_do_atributo;
    }
    set #nome_do_atributo(atributo){
        this.#nome_do_atributo = atributo;
    }
- Podemos deixar métodos privados tbm:
ex:
    #metodo(){}
- **static(){}**: Usado para chamadas diretas, sem necessidade de criação de objeto, deixa o método estático. Perite passar valores pelo método sem instanciar uma classe
- **get valorDaPropriedade(){}**: acessa a propriedade, se comporta como ela, mas executa uma função quando chamada
- **set valorDaPropriedade(novoValor){ this.modeloatributo = novoModelo}**: usado para atribuir um valor a propriedade, também se comporta como propriedade, mas executa uma função ao receber o valor/ validar valor antes de atribuílo a um atributo
- **extends**: herança de classe por prototipagem, quer dizer que uma função herda as propriedades e métodos de outra 
ex: class A extends B {};
- O método herdado pode ser reescrito com uma nova função (Só static metodos)


# Prototype chain:

- Cada objeto, array, método tem um link para outro objeto chamado prototype, fazendo uma cadeia até chegar em null onde encerra a cadeia
- O objeto prototype tem atributo prototype
ex: ["A", "B", "C"] -> array.prototypr -> objeto.prototype -> null (fim da cadeia)
- O prototype é o mecanismo pelo qual os objetos em JS herdam recursos uns dos outros
- O objeto prototype herda do seu prototype ascendente, as propriedades não são do objeto em si, mas sim ao prototype do objeto
- Um objeto pode usar qualquer propriedade dentro desse encadeiamento

# DATAS e Manipulações:

- **new Date()**: pega a hora e data atual do pc
- O new Date() leva em consideração o mês padrão de 0 á 12 se passado com aspas
- Existem 2 formas de definir data, seguindo o padrão americano (ano, mês, dia):
ex: new Date(2025, 08, 13, 09, 25, 00) / new Date("2025-08-13T09:25:00") / new Date("August 13, 2023, 09:25:00")
- **.getDay()**: pega o dia e começa contar do domingo, por ser um array vai de 0 á 6
- **.getFullyear()**: pega o ano atual
- **.getMonth()**: pega o mês atual, array que vai de 0 á 11 - janeiro á dezembro
- **.getDate()**: pega os dias do mês, 1 á 31
- **.getHours()**: horas de 0 á 23
- **.getMinutes()**: minutos de 0 até 59
- **.getSeconds()**: 0 até 59
- **.getMilliseconds()**: 0 até 999
- **setDate, Hours etc(atributo, valor que deseja acrescentar)**: usado para acrescentar dias, horas, minutos, segundos etc
- **.toLocaleString()**: data do país
.toLocaleString("pt-br", {
    dateStyle: "short/long/medium/full"
    timeStyle - estiliza hora
    day: "2-digit"
    month: -- configura os digitos da impressão
    hour: -- configura os digitos da impressão
    minute: -- configura os digitos da impressão
})
- Ainda posso usar o toLocaleString() para moedas locais
ex: .toLocaleString(valor, {
    style: "currency"
    currency: "tipo da moeda"
})
- **.toTimeString() / .toLocaleTimeString()**: um passa a data sem o padrão de brasilia e o outro passa com
- Date.parse(data) converte para milisegundos *TODO: pesquisar, não entendi com funciona*
- JavaScript conta a data a partir de 00:00h de 01/01/1970 UTC(Coordinated Universal Time)
- O Fuso horário local é baseado no ambiente executado
- **Intl API - Internacionalizção:** API para datas locais
ex:
const date = Intl.DateTimeFormat().resolvedOption(); - Vemos os objetos da chamada da Api e seus atributos
const dateIntl = Intl.DateFormat("padrãoLocal").format(new Date()); - pega  a hora local
- **.getTimeZoneOffset():** diferença de fuso em minutos (dividiu por 60 resulta em horas)
- **.toISOString():** Retorna padrão de timezone - diferença de fuso
  
# Math:

- Usado para fazer cálculos matemáticos
- **.ceil()**: arredonda sempre pra cima
- **round()**: aredonda para baixo se o valor for menor que 5 e para cima se for maior que 5
- **sqrt()**: raiz quadrada
- **random()**: valor aleatório entre 0 e 1, ex: 0.3455
- **floor()**: retorna a parte inteira
- **pow(a, b)**: base A elevada ao expoente B

# Regex:

- Expressões regulares
- utilizado para fazer verificações de dados
- /\D+/g -> regex para captar strings
- /\s/g -> regex para captar espaços
- O g permite acessar globalmente
- // Servem para delimitar o começo e fim do regex
- \ Indica o regex e a letra indica o tipo
- **+** Indica que esse regex pode pegar elementos consecutivos
- **.match()**: verifica se bate a informação
- **.test()**: testa se atende o padrão
- **.replace(a, b)**: permite trocar valores, a: valor que deseja trocar / b: o valor que vai substituir


# JAVASCRIPT OBJET NOTATION ou JSON:

- Converte objeto em texto ou texto em objeto
- JSON é estático, pois é texto
- Usado para transmitir dados entre sistemas, por exemplo: dados de uma API
- **JSONparse()**: transforma um texto JSON em objeto
- **JSONstringify()**: Transforma um objeto em JSON

# Funções assíncronas

- O JS por natureza funciona de forma single thread, executa uma coisa por vez
- As funções assíncronas são resolvidas enquanto o Js executa outra função
- Retornam uma promise (promeça/resultado) podendo ser um sucesso ou não
- **async**: usado para dizer que uma função é asssíncrona 
- **await**: pausa a função e espera a resolução da promise
- async e await devem ser usados juntos
ex: function asyncFunction(){
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        const inSucess = true;
        if (inSucess){
          resolve("Conection is ok!");
        } else {
          reject("Conection is not stated!")
       };
    }, 3000);
  });
};
//tratamento de erro
asyncFunction().then((response) => {
   console.log(`Sucesso ${response}`);
}).catch((error) => {
   console.log(`Error: ${error}`)
}).finally(() => {
   console.log("Execution ended");
});
- **then()**: é usado para capturar a resposta da promise
- **catch()**: usado para capturar o erro
- **finally()**: executado independente de dar certo ou errado, é o final da execução do código
//Definindo asíncronismo com async e await para tratamento
async function fetch(){
  try{
   const response = await asyncFunction();
   console.log(response);
  }catch(error){
    console.log(`Error: ${error}`);
  }finally{
    console.log("Execution ended");
  };
};
fetch();
- O assync tbm pode ser usado de outra forma: const fecth = async () => {}; / o await segue da mesma forma de antes
- Promise.resolve(true/false).then().catch().finally(); seria outra forma de fazer promise com tratamento de erro


# Event Loop e execução de código

- Js single thread: executa uma linha por vez (procedural, sincronismo, o código é executado de cima para baixo, empilhando e desempilhando funções quando necessário)
- Js no blocking: não trava o contexto da execução, por isso usamos assíncronismo nas funções, para lidar com a execução
- Concurrent: tarefas assíncronas concorrem umas com as outras. O modelo de concorrência do JS é em event loop
- **Event loop**: gerencia a execução do código assíncrono e eventos em um único thread
- Execução dos códigos:
- **Callstack** Armazena as chamadas de função em execução, quando a função é chamada ela empillha em pilha, tudo passa pela callstack podendo nela ser executado nela. O que não for passa p/ WEB API
- **WEB API**: utiliza outros recursos (DOM, setTimeout, fetch)
- **Callbackqueue**: fila que armazena callback e eventos que aguardam ser chamados p/ execução
- **EVENT LOOP**: verifica a pilha de callstack e callback, se houver um espaço na calltscak ele move da fila de callback para pilha de chamadas. Antes de verificar a fila de callbacks, o eventloop executa todas as microtasks pendentes
- A pilha de chamadas é constituida de **Microtask** e **Macrotask**
- **Microtask**: tarefas de alta prioridade para serem executadas, executada antes da macrotask(temporizadores e promises)
- **Macrotask**: tarefas de menor prioridade, callback de eventos, setTimeout, setInterval
- **queueMicrotask()** usado para criar microtask e adiciona-lá a fila de execução
- Ordem de execução: código síncrono, microtask, promise e temporizadores
ex:
   console.log(1);
  queueMicrotask(() => {
    console.log(2);
  });
  setTimeout(() => {
    console.log(3);
  });
  console.log(4);
  Promise.resolve(true).then(() => {
    console.log(5);
  });
- Qual seria o resultado desse código?

# Requisições HTTP:

- Requisições em APIS
- **fetch("link")**: passamos o link que estamos requisitando
- O fetch possui um promise, que significa que; tratamento para dar certo ou errado. O site pode cair, a API pode não funcionar mais etc
- **.then()**: usado quando a nossa requisição da certo
- **catch(erro)**: usado quando a requisição da errado
- **.then((response) => reponse.json())**: estamos transformando a requição em um arquivo de JSON
- **json()** retorna a resposta da requisição em formato JSON
- **clone()**: cria um clone da resposta da requisição
- **redirect()**: cria uma nova resposta com uma URL diferente
- **formData()**: retorna o resultado da requisição como um objeto do tipo FormData
- **arrayBuffer()**: retorna a resposta da requisição como um ArrayBuffer
- **blob()**: retorna a resposta da requisição como um Blob/ blob(Binary Large Object: é um objeto com dados binários brutos e imutáveis ex: arquivo de imagem, video, audio e outros dados não textuais)
 -**text()**: retorna a resposta da requisição como uma string

# PROGRAMAÇÃO ORIENTADA A OBJETO OU POO:

- Diferente da abordagem procedural(o código é gerado de cima pra baixo), permite códigos escaláveis e com uma boa qualidade de vida, permitindo manutenção e aplicabilidade
- Usamos métodos para atribuir responsabilidades
- Generalizar com intuito de reuso


# **MODULARIZAÇÃO DO CÓDIGO**: 

- Encapsulamento do código, é onde atribuímos responsabilidades
-Fazer um arquivo com classes e métodos e fazer os imports dessas classes
- Antes de fazer as importações, colocar dentro da tag script no código HTML o atributo: type="module"
- **Export**: usado para exportar as modularizações
- **Import**: usado para importar as modularizações
ex: 
    export default function;
    import function from ./'nome do arquivo';
- Podemos fazer o export de objetos se forem muitas funções, **ENCAPSULANDO** elas, JS não permitir exportar mais de um método de uma vez se não for assim/ tomar cuidado para não confundir os nomes
ex:
    export default {
        nomeDoQueVouexportar: método1,
        nomeDoQueVouexportar: método2,
    }

  import nome do arquivo from "./nomedoArquivo.js";

- **as**: permite mudar o nome das importações ou exportações ex: functionA as functionB
- Devemos sempre respeitar os nomes das funções nas exportações/ importações
- Export default - define um padrão / uma responsabilidade / objeto de funções
- named - função exportada pelo nome
- Podemos exportar todo conteúdo usando *
- Usamos {} para importar funções específicas
- É possível exportar a função diretamente ex:  export function(){};
- Ao exportar classes devemos instanciar o metódo em um objeto  ex:  import classA from "./arquivo.js";   const a = new classA();

# SPREADS, RESTS:

- **Spreads**: ... permite que objetos iteraveis (expressões de arrays ou strings) seja expandido p/ ser usdao como arguento. Separa os elementos
- ex: (...elemento/nome do objeto, array)
- **Rest**: ...rest (vai como parâmetro dentro da função)
- Recebe vários informações de uma vez
- Conhecido como args
- ex: ...args / ...rest

# EXCEÇÕES:
- Condições de imprevisto do código, interrompe o fluxo da operação, pode incluir erro.
- try - tentativa
- catch - captura de erro da tentativa
- finally - condição que vai rodar independente da tentativa ou erro
- ex: try {
  //tentativa
  } catch (error) {
      //captura do erro
  } finally {
      //aqui encerramos as conexões
      //executa mesmo dando certo ou errado
  }

# Error:
- Tratamentos de erros são usado para caso ocorra algum erro na aplicação
- **instanceof**: verifica se a instancia é de tal tipo, usado em erros
- **TypeError**: tipo de erro
- -**RangeError**: erro fora do intervalo
- -**throw**: Usado no try catch para lançar erros, ele pula direto qualquer verificação e vai direto pro catch
ex: class MyCustomError{
    constructor(message){
      this.message = message;
  }
};
try{
  throw new MyCustomError(`CLASSE DE ERRO CUSTOMIZADA: ${this.message}`);
} catch(error) {
    if(error instanceof MyCustomError){
     console.log(error.message);
    }else {
      console.log("Não foi possível executar") 
    }
};

# CALLBACKS:
- Função como argumento de outra
- Funções com um tempo para ativar
  ex: function execute(taskName, callback){
      console.log("Executado tarefa");
      callback();
  };
  function callback(){
      console.log("Tarefa finalizada");
  };

  execute("Download do arquivo...", () => {
    console.log("Tarefa finalizada.");
  });


# OBS:

- **SINTAXE REDUZIDA:** usado quando quero acessar itens ou definir condições simples, as {} você usa quando quer fazer blocos de código
- **.padStart/End(a, b)**: preenche String a partir do inicio ou do final. a: numero de elementos / b: valor que quero trocar
-**.trim()**: Remove espaços em banco do inicio e final da string
- **.value**: é usado para obter o valor de um input
- Declarar um input.value = ""; quer dizer que estou declarando para o input ser limpo
- Usar src dentro de aspas duplas necessita aspas simples
ex: "src = '' "
- A tag script vai no final do código HTML para indicar que o script pegue os respectivos elementos que o antecedem
- Comentários no JS são feitos com // para comentar linha e /**/ para comentar mais de uma linha
- \n usado para quebra de linha no JS
-  JS é fracamente tipado, então se vc somar "5" + 5 ele faz a correção e devolve 10, mas não é bom usar esse método pois pode conter erros de resultados
- JavaScript lê linha por linha durante a execução do código 
- **Null:** ausência de valor
- **NaN**: não é um número
- **Undefined**: variável com valor não definido
- **console.table()**; imprimi em um formato de tabela
- 0, -1, "", null, undefined, NaN, -> são valores **false**
- {} (objeto vazio), [] (array vazio), número INT, floats, "Oi" (String com valor dentro), " " (espaço em branco / caractere) -> são valores **true**
- Ao usar comandos para mudar atributos e criar elementos, adicionar etc. Prestar atenção na ordem do código, pois a posição das declarações muda no HTML
- A criar uma function em um formulário, devemos usar um event dentro dos parametros da function e chamar um prevent default para evitar que o formulário resete
ex: function(event){
    event.preventDefault();
};
