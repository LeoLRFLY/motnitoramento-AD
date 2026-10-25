# Sistema de Monitoramento de Diretrizes de Aeronavegabilidade

Protótipo de interface web para acompanhar diretrizes de aeronavegabilidade (ADs) publicadas por ANAC (Brasil), FAA (EUA), EASA (Europa) e TCCA (Canadá) em um só lugar.

## O que o projeto faz

É um site estático (HTML + JavaScript no navegador, estilizado com Tailwind CSS via CDN), sem back-end e sem build. Páginas:

- `index.html`: página inicial com busca (texto + autoridade), diretrizes recentes e resumo dos recursos. Ao buscar, redireciona para `diretrizes.html?q=...&authority=...`.
- `diretrizes.html`: lista de diretrizes com filtros e botão "Mais detalhes".
- `estatisticas.html`: painéis de estatísticas (total, por autoridade, por mês, mais recentes).
- `configuracoes.html`: preferências de notificação por e-mail e informações do sistema.

**Importante:** os dados são fictícios/fixos no HTML. Carregamento, busca e salvamento de configurações são simulados com `setTimeout` e `Math.random()`. Não há integração real com APIs das autoridades, nem envio real de e-mails.

## Como rodar

Não há dependências para instalar. Requer internet para carregar o Tailwind pelo CDN.

1. Clone o repositório.
2. Abra `index.html` no navegador (duplo clique), **ou** sirva a pasta localmente:

   ```bash
   python3 -m http.server 8000
   # depois acesse http://localhost:8000
   ```

Para publicar, basta hospedar os arquivos em qualquer serviço de site estático (por exemplo, GitHub Pages).
