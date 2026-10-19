# Links do <head>

A tag <link> conecta a página a um recurso.

- `rel`: informa a função do recurso.
- `href`: informa o endereço ou caminho do arquivo.
- `type`: informa o formato do recurso, quando necessário.

## Função de cada link

| Recurso | Para que serve |
| --- | --- |
| `rel="icon"` | Define o ícone exibido na aba do navegador. |
| `rel="preconnect"` | Antecipa a conexão com o servidor dos dados do mapa. É uma otimização opcional. |
| `crossorigin` | Prepara essa conexão para solicitações entre origens no modo CORS. |
| `maplibre-gl.css` | Estiliza marcadores, cards flutuantes e controles do MapLibre. |
| `styles.css` | Define os estilos básicos e responsivos da aplicação. |
| `theme-city.css` | Complementa o layout e define a aparência clara da interface. |
| `theme-blue.css` | Aplica a aparência azul quando o HTML tem `data-map-theme="blue"`. |

## Formato do favicon

O tipo deve corresponder ao formato real da imagem:

- PNG: `href="assets/favicon.png"` e `type="image/png"`.
- SVG: `href="assets/favicon.svg"` e `type="image/svg+xml"`.

## Ordem dos estilos

Ordem utilizada:

1. CSS do MapLibre.
2. styles.css.
3. theme-city.css.
4. theme-blue.css.

Quando regras aplicáveis têm a mesma prioridade e especificidade,
a que aparece depois prevalece.

## Observações

- `unpkg.com` distribui o arquivo da biblioteca pela internet.
- `@5.6.2` fixa a versão utilizada do MapLibre.
- Os três CSS próprios foram separados para organizar o código.
- Os prédios 3D são configurados pelo JavaScript.
- No HTML, o `href` recebe apenas o caminho ou URL, sem a sintaxe de links do Markdown.