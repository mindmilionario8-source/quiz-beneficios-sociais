# Quiz – Central de Informações sobre Benefícios Sociais

Site estático (HTML + JS), sem build. Funil: quiz → resultado → página de vendas → checkout.

## Rotas (hash)
- `/` quiz · `/#vendas` página de vendas

## Configuração
Edite `config.js`: link do checkout, preço, ID do Meta Pixel e ID do GA4. Cada commit publica na Vercel.

## Publicar na Vercel
1. Vercel → Add New → Project → importe este repositório.
2. Framework: Other. Sem comando de build. Diretório de saída: raiz.
3. Deploy. Depois, conecte seu domínio em Settings → Domains.

## Observações
- Eventos disparados: PageView, QuizStart, QuizQuestionAnswered, QuizComplete, SalesPageView, InitiateCheckout. Não há evento Purchase: configure-o apenas com confirmação real de compra pelo checkout.
- O painel administrativo do protótipo depende da plataforma Claude e não funciona fora dela. Aqui, a configuração é feita em `config.js` e as métricas ficam no Meta Pixel e no GA4.
- Textos e perguntas ficam no objeto `D` dentro do `index.html`.
- O site não coleta CPF, senha, dados bancários nem documentos. É um guia educacional independente, sem vínculo com órgãos governamentais.
