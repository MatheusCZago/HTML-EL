# Registro de Uso de IA — Entrega 1 (Esqueleto Semântico)

Projeto Integrador — Interface Web com HTML e CSS
Tema 5: Catálogo de produtos ("Casa Viva", com dados fictícios)
Branch: `entrega-1`

## 1. Mapeamento de Uso

Ferramenta utilizada: Claude (Anthropic), modelo Claude Sonnet 5.5, por meio do Claude Code.

| Arquivo | Apoio de IA |
|---|---|
| `index.html` | IA ajudou em todos os commits e na escrita (home com categoria e produto em destaque). |
| `categoria.html` | IA ajudou em todos os commits e na escrita (listagem de produtos da categoria Cozinha). |
| `produto.html` | IA ajudou em todos os commits e na escrita (página de detalhe da Cafeteira Elétrica Aurora). |
| `contato.html` | IA ajudou em todos os commits e na escrita (formulário de contato/interesse, apenas a estrutura). Depois da primeira versão, a IA incluiu o `<article>` que faltava, para que as quatro páginas tenham todos os landmarks exigidos. |
| `img/cafeteira-aurora.svg`, `img/facas-chef-lume.svg`, `img/panela-brasa.svg` | Imagens substitutas (placeholders) geradas pela IA. |

Nenhum arquivo desta entrega foi escrito sem apoio de IA. Os dados do catálogo (nome da loja, produtos, preços e especificações) são fictícios e foram inventados pela IA. A IA também executou os comandos de Git: limpeza do repositório, commits e publicação da branch `entrega-1`.

## 2. Prompts Utilizados (na íntegra)

### Prompt 1

```text
Preciso que entenda o projeto em andamento da faculdade na matéria de HTML. Dados anexados nos arquivos da conversa.
Escolha do tema: 5. Catálogo de produto
Dados fictícios
Nada muito detalhado, preciso apenas que funcione.
Preciso que seja simples, pois é apenas a primeira entrega.
No github, apague tudo que estiver no repositório: [MatheusCZago](https://github.com/MatheusCZago) / [HTML-EL](https://github.com/MatheusCZago/HTML-EL) ; e comece do zero, EU estou permitindo e quero dessa forma, apague tudo e refaça.
Quero algo simples e que contenha apenas o pedido para a primeira entrega.
```

### Prompt 2

```text
Agora que o GitHub está feito e preparado para receber os códigos, avalie os seguintes códigos que vou enviar, faça as alterações necessárias para rodar, faça o commit de tudo e me diga tudo que fez logo em seguida.
```

### Prompt 3

```text
Beleza. Agora preciso que você confira se está tudo pronto para o envio, caso não esteja, me informe sobre o que está faltando.
```

## 3. Revisão Técnica (mínimo de 3 alterações)

### Alteração 1

- **Arquivo:** _(index.html , categoria.html e produto.html)_
- **O que a IA gerou:** _(alt="Cafeteira Elétrica Aurora com jarra de vidro e base preta")_
- **O que foi alterado:** _(alt="Imagem ilustrativa da Cafeteira Elétrica Aurora")_
- **Por que foi alterado:** _(o alt deve transmitir o conteúdo real da imagem para quem usa leitor de tela.)_

### Alteração 2

- **Arquivo:** _(contato.html)_
- **O que a IA gerou:** _(<option>Cafeteira Elétrica Aurora</option>)_
- **O que foi alterado:** _(<option value="cafeteira-aurora">Cafeteira Elétrica Aurora</option>)_
- **Por que foi alterado:** _(o valor enviado pelo formulário fica estável e independente do texto exibido.)_

### Alteração 3

- **Arquivo:** _(contato.html)_
- **O que a IA gerou:** _(<textarea ... rows="5" cols="40">)_
- **O que foi alterado:** _(Remoção do cols="40")_
- **Por que foi alterado:** _(cols define a largura, que é apresentação. O projeto separa estrutura (Entrega 1) de estilo (Entrega 2, com CSS), então a largura deve ser decidida no CSS.)_
