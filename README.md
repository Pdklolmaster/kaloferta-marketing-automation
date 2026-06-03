# 🤖 Divulga-Kaloferta - Sistema  Completo

Este repositório funciona exclusivamente como um **Portfólio de Demonstração Visual e Arquitetural**. O código-fonte deste software é proprietário e protegido, sendo disponibilizado aqui apenas através de registros fotográficos do sistema em execução e da engenharia do seu código.

O sistema consiste num ecossistema completo de administração, com landing page responsiva, painel analítico de métricas em tempo real e uma robusta API REST para monitoramento de fluxos

<img width="571" height="1033" alt="serviço" src="https://github.com/user-attachments/assets/3b0ebebd-a886-4e01-ab6c-b3c0284f0a50" />
<img width="550" height="1080" alt="meee" src="https://github.com/user-attachments/assets/16e749f2-8d99-4bdc-b9c6-9a41df8f9bf6" />


## 🔐 Propriedade Intelectual e Licenciamento

O software contido e demonstrado neste repositório é protegido por leis de direitos autorais e propriedade intelectual:

- **Autoridade Exclusiva:** `kalofertapromo`
- **Regime de Licença:** Licença Administrativa (Uso, distribuição e reprodução estritamente restritos)
- **Criador Proprietário:** Pablo de Oliveira Silva
- **Contato Comercial / Suporte:** pablo_tecmastery@outlook.com

---

## 📸 Demonstração Visual (Galeria do Sistema)
<img width="1885" height="1015" alt="Captura de tela_2-6-2026_233952_www divulgakaloferta com br" src="https://github.com/user-attachments/assets/20fda9ca-3f57-470e-a4b4-06132ed0fc6c" />


### 🖥️ Interface do Utilizador e Painéis (UI/UX)
* **Landing Page Institucional:** 
  `<img width="1794" height="2490" alt="Captura de tela_2-6-2026_234122_www divulgakaloferta com br" src="https://github.com/user-attachments/assets/e9cdb4ef-ebe1-4d8a-b21a-258dfe782ec5" />

`
* **Dashboard de Métricas (Gráficos Interactivos estilo Grafana):** 
  `<img width="1794" height="2647" alt="Captura de tela_2-6-2026_234523_www divulgakaloferta com br" src="https://github.com/user-attachments/assets/8bc9358a-b9c3-4816-a54d-1727747c3e50" />

`

### 📂 Engenharia, Estrutura e Camada de Código
* **Arquitetura Geral do Diretório:** 
  `<img width="1534" height="1051" alt="pastas" src="https://github.com/user-attachments/assets/37f7ba5e-dba2-482f-a19d-7473d11988f5" />

`
* **Implementação de Rotas e Segurança (JWT):** 
 <img width="1526" height="1059" alt="jwt" src="https://github.com/user-attachments/assets/eeb569cc-1355-4b36-91f4-cebf823e2bdf" />

`

---

## 📋 Características e Engenharia do Software

A arquitetura lógica do sistema foi projetada sob uma estrutura escalável de microsserviços e consumo inteligente de dados

* **Visualização Avançada:** Gráficos interativos em tempo real gerados via `Chart.js`, cobrindo análise de uso diário, engajamento por plataforma, crescimento de utilizadores e receita mensal
* **Segurança de Borda:** Sistema de autenticação blindado utilizando tokens JWT (*JSON Web Tokens*) para controle estrito de acessos administrativos
* **Infraestrutura Automatizada:** Sincronização automatizada e *auto-refresh* global de dados estruturado a cada 5 minutos
* **Camada de Backend:** API REST nativa rodando em Node.js e Express, disponibilizando mais de 15 endpoints especializados mapeados para auditoria

---

## 🔗 Visão Geral da Arquitetura da API (Endpoints Mapeados)

A inteligência de back-end opera de forma isolada, separando requisições públicas de rotas administrativas que exigem credenciais

### Rotas de Acesso Público
- `GET /api/info` — Consulta de telemetria e status do bot
- `GET /api/stats/public` — Métricas de tração e estatísticas públicas

### Rotas Restritas (Requer Validação de Token Bearer JWT)
- **Painel Analítico:** `GET /api/stats` (Estatísticas gerais completas) e `GET /api/dashboard/summary`
- **Mapeamento de Tráfego:** `GET /api/usage/daily` (Volumetria de buscas diárias), `/by-platform` e `/by-hour`
- **Módulo Financeiro:** `GET /api/payments/stats` e `GET /api/payments/revenue` (Faturamento e histórico comercial)

---

## 🎨 Design do Sistema de Arquivos (Backbone)

<img width="1920" height="1080" alt="codigo" src="https://github.com/user-attachments/assets/0096fd6a-6fbd-40c6-8e93-613adf57618c" />
<img width="1920" height="1080" alt="pastas" src="https://github.com/user-attachments/assets/967a7f48-3f1c-42d1-a636-3cc27930dde0" />
<img width="1920" height="1080" alt="agent" src="https://github.com/user-attachments/assets/6332bc70-ab7a-4c24-829b-cf449c8018b2" />





O sistema foi estruturado sob o conceito de design de camadas para garantir modularidade e desacoplamento:

```text
┌─────────────────────────────────────────────────────────────┐
│                    CAMADA DE APRESENTAÇÃO                    │
├─────────────────────────────────────────────────────────────┤
│  • Dashboard Web (Next.js / React / TailwindCSS)             │
│  • Bot Telegram Autónomo (node-telegram-bot-api)             │
│  • Automação de WhatsApp (WhatsApp Web.js)                 │
└────────────────┬────────────────────────────────────────────┘
                 │
┌────────────────▼────────────────────────────────────────────┐
│                   CAMADA DE NEGÓCIO (CORE)                  │
├─────────────────────────────────────────────────────────────┤
│  • Affiliate Manager (Shopee, Mercado Livre, Amazon, etc.)  │
│  • Monitor Bot Engine (Telegram Userbot com GramJS)         │
│  • Conversor Dinâmico de Links (Detetor de Plataforma)      │
│  • Módulo de Gateways de Pagamento (Mercado Pago / PIX)     │
└────────────────┬────────────────────────────────────────────┘
                 │
┌────────────────▼────────────────────────────────────────────┐
│                   CAMADA DE INTEGRAÇÃO                      │
├─────────────────────────────────────────────────────────────┤
│  • LunaProxy Unlocker API (Anti-bot Web Scraping)           │
│  • Stealth Mode (Emulação de Headers Reais)                 │
│  • Camada de Cache (Memory Optimization / TTL)               │
└────────────────┬────────────────────────────────────────────┘
                 │
┌────────────────▼────────────────────────────────────────────┐
│                      CAMADA DE DADOS                        │
├─────────────────────────────────────────────────────────────┤
│  • SQLite Instance A (bot.db - Autenticação e Assinaturas)  │
│  • SQLite Instance B (monitor.db - Mapeamentos e Logs)      │
└─────────────────────────────────────────────────────────────┘


###🧠 Módulo: Agente de IA no Telegram (Autonomous AI Agent)

O ecossistema **Divulga Kaloferta** integra um Agente de IA autônomo focado em *Social Commerce* e curadoria automatizada de ofertas. Operando através de uma infraestrutura híbrida que combina o `node-telegram-bot-api` e o `gramjs` (Telegram Userbot), o agente atua como um tomador de decisões em tempo real dentro dos canais monitorados.

### ⚡ Capacidades e Engenharia do Agente

O comportamento do agente é guiado por pipelines de processamento e heurísticas de inteligência orçamentária e de vendas

* **Geração Inteligente de Copywriting (Prompt Engine):** O agente não apenas replica dados; ele processa os inputs brutos de produtos e gera dinamicamente textos persuasivos baseados em múltiplos modelos pré-definidos (Marketing, Minimalista e IA Cognitiva).
* **Análise Semântica e Filtro de Qualidade (Data Sanitization):** Antes de encaminhar qualquer oferta para os canais de destino, o agente realiza uma validação estrutural estrita[cite: 4]. Se identificar que os dados extraídos via APIs ou scraping possuem inconsistências (títulos incompletos, preços zerados ou imagens corrompidas), o agente bloqueia o envio autonomamente para proteger o engajamento do canal
* **Orquestração de Sessões e Fallbacks:** O agente gerencia sessões de usuário de forma independente (via QR Code ou Telefone), monitora fluxos de múltiplos grupos de origem simultaneamente e aciona rotinas de contingência (como rotação de cookies e chaves de scraping através do LunaProxy) sem necessidade de intervenção humana

### 📸 O Agente em Ação (Demonstração Visual)

* **Tomada de Decisão e Formatação de Oferta por IA:**  
  `![Agente de IA Processando Link](screenshots/ai_agent_action.png)`  
  *(Na imagem: O link bruto enviado pelo usuário é interceptado, enriquecido com inteligência de copywriting e formatado pelo agente em menos de 3 segundos)

<img width="1174" height="1036" alt="1" src="https://github.com/user-attachments/assets/b1f5a3f7-0f4c-4e06-8c13-efbb59f98229" />
<img width="1182" height="1028" alt="2" src="https://github.com/user-attachments/assets/51a99db0-863c-4211-bbc1-b48dcb6f4705" />
<img width="1174" height="1046" alt="3" src="https://github.com/user-attachments/assets/fc394c7b-a42d-455e-b447-17f103633a27" />
<img width="1179" height="1038" alt="Sem título" src="https://github.com/user-attachments/assets/adb5143a-5079-4c37-8735-864c7a95ebb9" />
