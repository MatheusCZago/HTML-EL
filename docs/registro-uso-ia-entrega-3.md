# Registro de Uso de IA — Entrega 3 (Formulário e Refinamento)

Projeto Integrador — Interface Web com HTML e CSS
Tema 5: Catálogo de produtos ("Casa Viva", com dados fictícios)
Branch: `entrega-3`

## 1. Mapeamento de Uso

Ferramenta utilizada: Claude (Anthropic), modelo Claude Sonnet 5.5, por meio do Claude Code.

| Arquivo | Apoio de IA |
|---|---|
| `contato.html` | Validação nativa do formulário escrita pela IA: `required` em todos os campos, `type="email"`, `minlength` e `maxlength`, `pattern` no nome, opção vazia no `<select>` obrigatório, `method` e `action` no formulário e o aviso "Todos os campos são obrigatórios". Sem JavaScript. |
| `css/style.css` | Escrito pela IA nesta entrega: variável `--cor-erro`, estilo `:user-invalid` para campos inválidos e `resize: vertical` no `textarea`. |

A IA também revisou a acessibilidade (contraste de texto, navegação por teclado e foco) e a responsividade (ausência de rolagem horizontal entre 320px e 1440px). Não foi necessário alterar mais nada além do listado acima. O restante do código, incluindo as alterações feitas pelo estudante nas Entregas 1 e 2, foi mantido. A IA também executou os comandos de Git desta entrega: criação da branch `entrega-3`, commits e publicação.

## 2. Prompts Utilizados (na íntegra)

### Prompt 1

```text
Estamos na parte final. Vou precisar que você confira se os códigos estão corretos.
```

### Prompt 2

```text
Agora que a conferencia foi feita, podemos seguir para o GitHub Pages. Me dê um passo a passo breve para que eu publique corretamente e como devo entregar ao professor.
```

## 3. Revisão Técnica (mínimo de 3 alterações)

### Alteração 1

- **Arquivo:** contato.html
- **O que a IA gerou:** <textarea id="mensagem" name="mensagem" rows="5"
          required minlength="10" maxlength="500"></textarea>
- **O que foi alterado:** <textarea id="mensagem" name="mensagem" rows="5"
          required minlength="20" maxlength="500"></textarea>
- **Por que foi alterado:** Com 10 caracteres, "oi, tudo bem?" já passa e não diz nada sobre o produto. Com 20, a pessoa precisa escrever o suficiente para a loja conseguir responder.

### Alteração 2

- **Arquivo:** css/style.css
- **O que a IA gerou:** --cor-erro: #b42318;
- **O que foi alterado:** --cor-erro: #9b1c1c;
- **Por que foi alterado:** A variável controla a borda e a sombra de todos os campos inválidos de uma vez. Um vermelho mais escuro destaca melhor o campo errado do borda cinza normal (--cor-campo), o que ajuda quem tem baixa visão.

### Alteração 3

- **Arquivo:** contato.html
- **O que a IA gerou:** <p>Todos os campos são obrigatórios.</p>
- **O que foi alterado:** <p>Todos os campos são obrigatórios. Se algo estiver incorreto, o navegador indica qual campo corrigir.</p>
- **Por que foi alterado:** Quem usa leitor de tela escuta esse texto antes do formulário. Dizer o que acontece em caso de erro evita surpresa quando o envio é bloqueado e o foco volta para um campo.
