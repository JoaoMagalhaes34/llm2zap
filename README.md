# llm2zap

O **llm2zap** é uma solução leve e estática desenvolvida para resolver conflitos de codificação de URL (URL encoding) em aplicações que bloqueiam redirecionamentos diretos, como o navegador embutido da aplicação Google ou Gemini.

Através de uma página intermédia, o script recebe os parâmetros de número e texto e converte-os instantaneamente numa ligação limpa, forçando a abertura do WhatsApp nativo sem erros de navegação ou pesquisas não intencionais.

## Destaques do Projeto

* **Zero Servidores (Client-side):** Funciona a 100% no navegador do utilizador, utilizando apenas HTML e JavaScript puro. Não requer base de dados nem processamento em backend (como Python ou Node.js).
* **Bypass de Dupla Codificação:** Evita que os navegadores internos transformem símbolos estruturais (`?`, `=`) em caracteres codificados (`%3F`, `%3D`), o que quebrava o redirecionamento.
* **Alojamento Gratuito:** Concebido para ser alojado diretamente no GitHub Pages sem custos ou configurações complexas.

## Como Funciona

A ferramenta atua como um intercetor dinâmico. O Modelo de Linguagem (LLM) gera uma ligação apontando para este repositório, passando os dados através da barra de endereços (utilizando o cardinal `#` para evitar bloqueios de rastreamento):

`https://o-seu-usuario.github.io/llm2zap/#num=5521999999999&msg=texto+a+enviar`

A página lê esses parâmetros, monta o endereço oficial da API do WhatsApp (`https://wa.me/...`) com a codificação correta e executa o salto imediato para a aplicação de mensagens.

## 🤖 Automatizar com Inteligência Artificial (Skills / Custom Instructions)

Para tirar o máximo partido do **llm2zap**, recomendamos que configure o seu assistente de IA (Gemini, ChatGPT, Claude) para utilizar este sistema de forma automática. Pode fazê-lo criando uma "Skill" (Habilidade), um "Gem" personalizado ou colando o texto abaixo nas suas "Instruções Personalizadas" (Custom Instructions).

Copie o seguinte comando de instrução, lembrando-se de substituir `SEU-USUARIO` pelo seu próprio nome de utilizador do GitHub:

> Sempre que eu pedir para preparar uma mensagem para o WhatsApp, siga este fluxo rigorosamente:
> 
> 1. Procure nos meus Contactos (se tiver acesso) o número de telefone da pessoa.
> 2. Escreva o rascunho da mensagem para a minha aprovação e confirme o número encontrado (com o código de país/DDI).
> 3. Após a minha aprovação, aplique a codificação de URL (URL encoding) no texto original, mantendo acentos e pontuações.
> 4. Gere a ligação de redirecionamento utilizando obrigatoriamente a seguinte estrutura com cardinal: 
>    `https://SEU-USUARIO.github.io/llm2zap/#num=[NÚMERO_COM_DDI]&msg=[MENSAGEM_CODIFICADA]`
> 5. Entregue o resultado final obrigatoriamente nestes dois formatos:
>    - **Para Celular:** Como uma hiperligação normal e clicável.
>    - **Para PC:** A mesma hiperligação dentro de um bloco de código puro (\`\`\`text), para que eu possa copiar e colar diretamente na barra de endereços do navegador.
