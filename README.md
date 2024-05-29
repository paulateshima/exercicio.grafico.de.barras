# Exercício Gráfico de Barras (Lógica de Programação)

Através de gráficos podemos expressar visualmente dados ou valores numéricos, e assim facilitar a nossa compreensão. Gráficos ajudam a entender o relacionamento entre valores e nos ajudam a analisar dados para chegarmos em determinadas conclusões.

Existem vários tipos de gráficos, um bastante famoso é o gráfico de barras, que é o objeto de estudo desse exercício.

Para alimentarmos nosso infográfico, procuramos em alguns relatórios da Alura quais navegadores os nossos alunos mais utilizavam em 2015 e 2016, e separamos os dados:

Em 2015: 50% usava Chrome, 25% Firefox, 20% Safari, 5% Outros (Opera, IE, etc).
Em 2016: 65% usava Chrome, 20% Firefox, 13% Safari, 2% Outros (Opera, IE, Edge, etc).
Ou seja, no ano de 2015, 50% dos nossos alunos usaram o navegador Chrome, 25% Firefox** e assim em diante. Já em 2016, 65% usavam Chrome e apenas 20% Firefox.

Um gráfico de barras nada mais é do que um monte de retângulos representando os valores, algo assim:

![image](https://github.com/paulateshima/exercicio.grafico.de.barras/assets/170154538/dcc7bfd6-4f86-4149-886c-90a1deee2d7b)

Esse gráfico ainda está incompleto, pois falta uma legenda que mostraria que a cor azul representa Chrome, verde é Firefox, amarelo Safari e vermelho Outros. Mesmo assim, já é algo interessante para praticar.

Você já aprendeu a desenhar um retângulo e até criamos uma função com esse propósito. Desenhar um texto também já sabemos, mas vamos relembrar com o código abaixo:

```
<canvas width="600" height="400"></canvas>

<script>

    function desenhaRetangulo(x, y, largura, altura, cor) {
        var tela = document.querySelector('canvas');
        var pincel = tela.getContext('2d');

        pincel.fillStyle=cor;
        pincel.fillRect(x,y, largura, altura);
        pincel.strokeStyle='black';
        pincel.strokeRect(x,y, largura, altura);
    }

    function desenhaTexto(x, y, texto) {
        var tela = document.querySelector('canvas');
        var pincel = tela.getContext('2d');

        pincel.font='15px Georgia';
        pincel.fillStyle='black';
        pincel.fillText(texto, x, y);    
    }

    // aqui vem mais

</script>
```
Também já vimos como representar vários valores dentro de um Array. Assim podemos guardar o percentual que corresponde a cada ano. No mundo de gráficos, os valores são chamados de série:

```
var serie2015 = [50, 25, 20, 5];
var serie2016 = [65, 20, 13, 2];
```

Cada valor no array representa ao percentual ( %). No ano 2016 (ou melhor, na série 2016), 65% dos alunos usavam Chrome, 20% Firefox etc.

Dessa maneira, assim como podemos representar o percentual de cada ano, também podemos apresentar todas as cores utilizadas no gráfico de barras. Repare que o nosso gráfico possui 4 cores, que são “azul”, “verde”, “amarelo” e “vermelho”. Nesse sentido, é possível criar uma lista com as respectivas cores:

```
var cores = ['blue', 'green', 'yellow', 'red'];
```

Tendo isso em mãos vem agora a sua tarefa:** Escreva uma função** desenhaBarra que cria uma barra com as seguintes especificações: 4 retângulos - o primeiro azul, o segundo verde, etc., como apresentado na imagem acima.

A chamada da função deve ser:

```
desenhaBarra(50, 50, serie2015, cores, '2015');
desenhaBarra(150, 50, serie2016, cores, '2016');
```

A primeira barra começa com x=50 e y=50, recebe a série de 2015, as cores e o texto '2015'. Baseado nisso já podemos escrever a função:

```
function desenhaBarra(x, y, serie, cores, texto) {
    // aqui precisamos desenhar vários retângulos!
}
```
Dentro da função você precisa implementar um laço e nele precisa recuperar o valor da série, que nada mais é do que a altura do retângulo:

![image](https://github.com/paulateshima/exercicio.grafico.de.barras/assets/170154538/780e16ae-59c8-4efc-9877-22e5b90b17c1)

Agora é com você!

Implemente a função desenhaBarra e chame-a para desenhar duas barras.

O desenho deverá ficar dessa maneira:

![image](https://github.com/paulateshima/exercicio.grafico.de.barras/assets/170154538/6ac64641-644b-4466-ac54-5c8c2305a684)

O código completo é?

