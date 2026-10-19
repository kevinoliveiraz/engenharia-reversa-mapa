# Tag <script defer src>

## Exemplo

```html
<script defer src="config.js"></script>
```

## Partes da tag

- `<script>`: indica código JavaScript.
- `src="config.js"`: informa o caminho do arquivo JavaScript.
- `defer`: adia a execução até o HTML terminar de ser interpretado.
- `</script>`: fecha a tag.

## Como funciona com defer

1. O navegador encontra a tag e começa a baixar o arquivo.
2. Continua interpretando o HTML durante o download.
3. Executa o JavaScript quando o HTML estiver interpretado e o arquivo estiver disponível.

## Por que usar neste projeto?

Permite que os botões, painéis e o espaço do mapa já existam
quando o JavaScript procurar esses elementos.

Vários scripts externos tradicionais com `defer` executam
na ordem em que aparecem no HTML.