# Biblioteca de ícones SVG

Esse bloco funciona como um catálogo: cada desenho é definido uma vez
e pode ser usado em vários botões ou partes da interface.

SVG é um formato vetorial: descreve desenhos por formas e coordenadas.

## Partes do código

| Parte | Função |
| --- | --- |
| `<svg>` | Abre o conjunto de desenhos vetoriais. |
| `class="icon-defs"` | Permite que o CSS esconda a caixa dessa biblioteca. |
| `aria-hidden="true"` | Retira a biblioteca da árvore de acessibilidade, evitando anúncios desnecessários. |
| `xmlns="http://www.w3.org/2000/svg"` | Identifica o padrão SVG; esse endereço funciona como identificador. |
| `<defs>` | Agrupa definições que serão utilizadas em outros lugares. |
| `<symbol>` | Define um modelo reutilizável de desenho. |
| `id="i-plus"` | Dá um identificador único ao modelo. |
| `viewBox="0 0 24 24"` | Define uma área interna de coordenadas com origem em 0,0 e tamanho 24 × 24. |
| `<path d="...">` | Desenha um caminho seguindo comandos e coordenadas. |
| `<circle>` | Desenha um círculo. |
| `<rect>` | Desenha um retângulo. |

O viewBox define as coordenadas internas. O tamanho exibido na tela
pode ser controlado pelo CSS.

## Exemplo: cadastrar o ícone de adicionar

```html
<svg class="icon-defs"
     aria-hidden="true"
     xmlns="http://www.w3.org/2000/svg">
  <defs>
    <symbol id="i-plus" viewBox="0 0 24 24">
      <path d="M12 5v14M5 12h14"/>
    </symbol>
  </defs>
</svg>
```

### Como o desenho do sinal de mais funciona

- `M12 5`: move o início do traço para a posição 12,5.
- `v14`: desenha uma linha vertical descendo 14 unidades.
- `M5 12`: move para outro início, na posição 5,12.
- `h14`: desenha uma linha horizontal avançando 14 unidades.

As duas linhas formam o sinal de mais.

## Como mostrar o ícone em um botão

```html
<button aria-label="Adicionar aviso">
  <svg class="icon" aria-hidden="true">
    <use href="#i-plus"></use>
  </svg>
</button>
```

- `<use>` reutiliza o desenho cadastrado.
- `href="#i-plus"` procura o símbolo com `id="i-plus"`.
- O `aria-label` informa a função do botão aos leitores de tela.

Para trocar o desenho, basta apontar para outro símbolo existente,
como `#i-search`, `#i-map` ou `#i-close`.

## CSS para esse exemplo

```css
/* Esconde a caixa da biblioteca de definições. */
.icon-defs {
  position: absolute;
  width: 0;
  height: 0;
  overflow: hidden;
}

/* Define a aparência das cópias exibidas na interface. */
.icon {
  width: 24px;
  height: 24px;
  fill: none;
  stroke: currentColor;
  stroke-width: 2;
}
```

- `fill: none`: deixa as formas sem preenchimento.
- `stroke: currentColor`: usa a cor do texto para desenhar os traços.
- `stroke-width: 2`: define a espessura dos traços.

## Atenção aos fechamentos

O trecho enviado termina antes de `</defs>` e `</svg>`.
Esses fechamentos precisam aparecer depois do último símbolo.

`aria-hidden` cuida da acessibilidade; a ocultação visual da caixa
é feita pelo CSS.

## Para estudar

Comece cadastrando e exibindo apenas o ícone de adicionar.
Depois reutilize o mesmo padrão para entender os outros.