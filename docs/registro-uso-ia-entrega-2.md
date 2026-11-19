# Registro de Uso de IA — Entrega 2 (Estilo e Responsividade)

Projeto Integrador — Interface Web com HTML e CSS
Tema 5: Catálogo de produtos ("Casa Viva", com dados fictícios)
Branch: `entrega-2`

## 1. Mapeamento de Uso

Ferramenta utilizada: Claude (Anthropic), modelo Claude Sonnet 5.5, por meio do Claude Code.

| Arquivo | Apoio de IA |
|---|---|
| `css/style.css` | IA ajudou em todos os commits e na escrita; variáveis em `:root`, Flexbox no cabeçalho, menu e formulário, Grid na listagem de produtos e no layout da página, e media queries mobile-first para 768px e 1200px. |
| `index.html`, `categoria.html`, `produto.html`, `contato.html` | IA ajudou em todos os commits e na escrita: `<meta name="viewport">`, `<link>` para o CSS, classe `skip-link` no skip link, classe `card` nos produtos, classe `formulario` no formulário e, em `categoria.html`, um `<div class="produtos">` envolvendo os cards. |

Todo o CSS desta entrega foi escrito com apoio de IA. O conteúdo do HTML, incluindo as alterações feitas foi mantido. A IA também executou os comandos de Git desta entrega: criação da branch `entrega-2`, commits e publicação.

## 2. Prompts Utilizados (na íntegra)

### Prompt 1



```text
Aplicar os estilos utilizando CSS: aplicar estilos utilizando CSS, aplicar responsividade (flexbox, grid, media queries). Formato de entrega: enviar o link do repositório GitHub; para esta entrega use o nome da branch como entrega-2.
Precisamos realizar as alterações de CSS conforme o enunciado do professor. Reveja o código que foi enviado e veja se está dentro dos parâmetros. Obrigado!
```

## 3. Revisão Técnica (mínimo de 3 alterações)

### Alteração 1

- **Arquivo:** css/style.css
- **O que a IA gerou:** --cor-primaria: #0b5394;
--cor-primaria-escura: #083a69;
- **O que foi alterado:** --cor-primaria: #1b6b3a;
--cor-primaria-escura: #0f4526;
- **Por que foi alterado:** O texto branco precisa de pelo menos 4,5:1 sobre a cor nova, que é o mínimo do PDF. Os valores estão numa variável só, então a troca vale para o cabeçalho, o rodapé, os títulos, os links e o botão de uma vez. Isso mostra o motivo de usar variáveis CSS.
### Alteração 2

- **Arquivo:** css/style.css
- **O que a IA gerou:** --largura-max: 75rem;
- **O que foi alterado:** --largura-max: 80rem;
- **Por que foi alterado:** 80rem equivale a 1280px, uma largura comum de notebook. Com 75rem sobravam faixas laterais nessa tela, e agora o site ocupa a largura inteira. Em telas maiores ele continua limitado e centralizado, o que evita linhas de texto muito longas.

### Alteração 3

- **Arquivo:** css/style.css
- **O que a IA gerou:** nav ul {
  display: flex;
  flex-direction: column;
  gap: var(--espaco-1);
  margin: 0;
  padding: 0;
  list-style: none;
}

- **O que foi alterado:** nav ul {
  display: flex;
  flex-wrap: wrap;
  gap: var(--espaco-1) var(--espaco-3);
  margin: 0;
  padding: 0;
  list-style: none;
}
- **Por que foi alterado:** Antes, os 4 links ocupavam uma coluna e o cabeçalho ficava com cerca de 260px de altura no celular. Agora os links ficam lado a lado e quebram só se faltar espaço, o que libera mais tela para o conteúdo. A altura de toque dos links não muda, porque o padding do nav a continua o mesmo.
