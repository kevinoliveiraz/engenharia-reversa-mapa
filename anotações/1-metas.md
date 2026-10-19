# Configurações do <head>

- **charset="utf-8"**: define a codificação do texto, permitindo exibir acentos e cedilha corretamente. O arquivo também deve ser salvo em UTF-8.

- **viewport**: configura a área de exibição:
  - `width=device-width`: usa a largura do dispositivo.
  - `initial-scale=1`: inicia com escala de 100%.
  - `viewport-fit=cover`: permite ocupar toda a tela. O CSS precisa proteger os elementos próximos aos recortes do celular.

- **theme-color**: sugere uma cor para a interface dos navegadores compatíveis. O fundo da página é definido pelo CSS.

- **Script do tema**: recupera a preferência salva no localStorage e aplica o visual colorido antes da primeira exibição. O `try...catch` trata possíveis falhas nessa leitura.

- **description**: resume o conteúdo da página. Buscadores podem usar esse texto nos resultados.

- **title**: define o título exibido na aba do navegador.

## Ordem para estudar

Começar com `charset`, `viewport` básico e `title`.
Depois adicionar descrição, cor do navegador e recuperação do tema.

A adaptação do layout às telas depende também do CSS.