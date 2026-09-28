# llm2zap
O llm2zap é uma solução leve e estática desenvolvida para resolver conflitos de codificação de URL (URL encoding) em aplicações que bloqueiam redirecionamentos diretos, como o navegador embutido da aplicação Google ou Gemini.
Através de uma página intermédia, o script recebe os parâmetros de número e texto e converte-os instantaneamente numa ligação limpa, forçando a abertura do WhatsApp nativo sem erros de navegação ou pesquisas não intencionais.
Destaques do Projeto
 * Zero Servidores (Client-side): Funciona a 100% no navegador do utilizador, utilizando apenas HTML e JavaScript puro. Não requer base de dados nem processamento em backend (como Python ou Node.js).
 * Bypass de Dupla Codificação: Evita que os navegadores internos transformem símbolos estruturais (?, =) em caracteres codificados (%3F, %3D), o que quebrava o redirecionamento.
 * Alojamento Gratuito: Concebido para ser alojado diretamente no GitHub Pages sem custos ou configurações complexas.
Como Funciona
A ferramenta atua como um intercetor dinâmico. O Modelo de Linguagem (LLM) gera uma ligação apontando para este repositório, passando os dados através da barra de endereços:
[https://o-seu-usuario.github.io/llm2zap/?num=5521999999999&msg=texto+a+enviar](https://o-seu-usuario.github.io/llm2zap/?num=5521999999999&msg=texto+a+enviar)
A página lê esses parâmetros, monta o endereço oficial da API do WhatsApp ([https://wa.me/](https://wa.me/)...) com a codificação correta e executa o salto imediato para a aplicação de mensagens.


