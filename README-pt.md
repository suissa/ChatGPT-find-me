# ChatGPT-find-me

## Visão Geral

O **ChatGPT-find-me** é uma skill/framework projetada para otimizar sites e aplicações web, garantindo que sejam facilmente descobertos, rastreados, compreendidos e citados por LLMs (Large Language Models), agentes de IA, mecanismos de busca semântica (AI Search) e crawlers. 

O objetivo não é utilizar truques de "SEO tradicional", mas focar na clareza estrutural, densidade factual e acessibilidade técnica (Agentic UX/Agent-Readable Sites).

## Base de Estudo e Inspiração

Esta skill foi fundamentada e inspirada nos insights detalhados do estudo:
🔗 **[How ChatGPT Picks Sources](https://suganthan.com/blog/how-chatgpt-picks-sources/)** por Suganthan.

O estudo analisa o comportamento de seleção de fontes pelo ChatGPT, destacando que a IA prioriza:
- **Autoridade e Confiança:** Sites com forte reputação e citações externas.
- **Rastreabilidade Técnica:** HTML limpo, texto acessível sem a necessidade de renderização complexa de JavaScript (SSR/SSG recomendados).
- **Frescor (Recency) e Atualização:** Conteúdos atualizados frequentemente e com datas claras.
- **Estruturação Semântica:** Respostas diretas e factuais (Claims) suportadas por estruturas lógicas legíveis (dados estruturados, headings claros).

A skill adapta essas descobertas para um checklist prático de desenvolvimento e auditoria.

## Princípios Centrais (AEO - Answer Engine Optimization)

1. **Factual e Verificável:** A IA precisa conseguir validar a informação através de texto simples, não escondido em PDFs, vídeos ou imagens.
2. **Crawlability Primária:** Agentes de IA, como o `OAI-SearchBot` e `GPTBot`, devem ser capazes de navegar no seu `robots.txt` e ler o HTML inicial perfeitamente.
3. **Páginas de Claim (Afirmação):** Estruturar informações críticas (preço, funcionalidades, contatos, localidade) em URLs independentes ou âncoras semanticamente ricas.
4. **Isolamento de UI/UX:** A experiência bonita para o usuário não pode ofuscar os dados brutos necessários para a máquina.

## Como Aplicar

1. **Auditoria de Rastreabilidade:** Verifique status codes, excesso de JS, `robots.txt` e renderização em modo texto puro.
2. **Mapeamento de Claims:** Defina exatamente o que a IA *precisa* saber sobre o seu negócio (ex: "Entregamos na cidade X", "A assinatura custa Y").
3. **Ajuste Estrutural:** Implemente Schema JSON-LD, arquivos de contexto para LLMs (`llms.txt`), tags canônicas e garanta que conteúdo vital está no DOM inicial.
4. **Publicação e Teste:** Utilize bots textuais ou simuladores de scraper para validar se o agente "enxerga" o que você espera.

---
*Construído para a era dos Agentes Web e LLM Search.*
