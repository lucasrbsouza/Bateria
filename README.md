# Bateria

## Tocador de Som

Este é um script JavaScript para um tocador de som. Ele permite que você toque sons específicos pressionando teclas no teclado ou clicando em botões na página. Além disso, você pode tocar uma composição inserindo uma sequência de teclas.

### Como usar

1. Primeiro, você precisa ter elementos de áudio em seu HTML com os ids correspondentes às teclas que você deseja usar (por exemplo, `#s_keya` para a tecla 'a'). Além disso, você precisa ter elementos div correspondentes com atributos `data-key` correspondentes (por exemplo, `div[data-key ="keya"]`).

2. Em seguida, inclua o script em seu arquivo HTML.

### Detalhes do Código

O código começa adicionando um ouvinte de evento 'keyup' ao `document.body`. Quando uma tecla é pressionada, ele chama a função `playsound` com o código da tecla.

A função `playsound` faz o seguinte:

- Seleciona o elemento de áudio e o elemento div correspondente à tecla pressionada.
- Se o elemento de áudio existir, ele reinicia o áudio e o toca.
- Se o elemento div existir, ele adiciona a classe 'active', fazendo com que o elemento pareça estar pressionado. Depois de 300 milissegundos, ele remove a classe 'active'.

Além disso, há um ouvinte de evento no botão do compositor. Quando clicado, ele obtém a composição do campo de entrada e a toca usando a função `playComposition`.

A função `playComposition` toca cada tecla na composição uma após a outra, com um atraso de 250 milissegundos entre cada uma.
