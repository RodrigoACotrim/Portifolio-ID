 Projeto Final – Integração de Dados
Visão 360º do Cliente com Arquitetura Híbrida de Integração

Este repositório contém o desenvolvimento completo do Projeto Final de Avaliação da UC Integração de Dados (CTeSP TPSI).
O objetivo é implementar um sistema híbrido capaz de integrar informações de múltiplas fontes (batch, API e streaming) para construir uma Visão 360º do Cliente.

O projeto aborda todos os temas centrais da unidade curricular, passando por Fundamentos de Integração, Processos ETL, Qualidade de Dados, Seleção de Ferramentas e Integração Avançada.

 1. Cenário de Negócio

Uma empresa de serviços financeiros deseja modernizar o seu ecossistema de informação criando uma visão integrada do cliente. Para isso, três fontes de dados precisam de ser unificadas:

Sistema Legado (Batch) – Base de dados histórica e estruturada de clientes.

Sistema de Suporte (API/Web Service) – Contactos e moradas, dados semi-estruturados.

Sistema de Transações (Streaming) – Eventos financeiros em tempo real.

O foco está na criação de um Data Mart do Cliente permitindo análises consistentes, atualizadas e governadas.

 2. Estrutura do Repositório
/
│ README.md
│ Relatorio_Final.pdf
│
├── data/
│   ├── clientes_master_data.csv       # Base histórica de clientes  :contentReference[oaicite:3]{index=3}
│   ├── interacoes_web_stream.json     # Stream de interações  :contentReference[oaicite:4]{index=4}
│   └── mock_data_description.md       # Descrição dos erros intencionais nos dados  :contentReference[oaicite:5]{index=5}
│
├── etl/
│   ├── mapping_tables/
│   ├── pseudocode/
│   └── transformations/
│
└── diagrams/
    ├── arquitetura_conceptual.png
    ├── pipeline_streaming.png
    └── modelo_datamart.png

 3. Conteúdos Desenvolvidos (5 Fases do Projeto)
Fase 1 – Análise e Design Conceptual

Baseada nos requisitos do cenário e nos desafios de integração propostos no enunciado .

Inclui:
• Definição dos desafios de integração
• Arquitetura conceptual híbrida (Batch + API + Streaming)
• Glossário técnico com termos essenciais

Fase 2 – Mapeamento e Processo ETL (Sistema Legado)

Inclui:
• Seleção e mapeamento de 5 campos críticos
• Tabela de mapeamento para o Data Mart
• Pseudocódigo para transformação complexa
• Estratégia de carga (Full vs Incremental CDC)

Fase 3 – Qualidade e Consistência de Dados

Com base nos ficheiros fornecidos, que incluem erros intencionais .

Inclui:
• Data Profiling sobre moradas e contactos
• Regras de limpeza (ex.: uniformização de nomes)
• Tratamento de inconsistências como:
• NIF inválido do cliente 1009
• Sentiment score fora do domínio na interação I003
• Registo órfão (client_ref inexistente) na interação I005

Fase 4 – Seleção e Justificação de Ferramentas

Ferramentas escolhidas e justificadas com base em:
• Escalabilidade
• Custo
• Curva de aprendizagem
• Integração com o ecossistema

Inclui ferramentas ETL, Plataforma de Streaming e solução MDM.

Fase 5 – Integração em Contextos Avançados

Inclui:
• Design completo do pipeline de streaming
• Aplicação de CDC e Arquitetura Kappa/Lambda
• Parsing e normalização de XML
• Definição dos papéis de Data Owner e Data Steward
• Política de Governança com foco em RGPD (NIF, morada, dados sensíveis)

 4. Ficheiros de Dados (Mock Data)
Ficheiro	Descrição
clientes_master_data.csv	Base de clientes com falha intencional no NIF do cliente 1009
interacoes_web_stream.json	Stream com sentiment score inválido e registo órfão
mock_data_description.md	Explicação das falhas introduzidas para validação e cleansing
 5. Objetivo do Repositório

Este repositório serve como:
• Documentação do trabalho final
• Prova de competências em integração de dados
• Repositório técnico para ETL, Data Quality e Streaming
• Portfólio académico e profissional

 6. Como Executar ou Testar

Utilizar os ficheiros da pasta data/ como entradas.

Aplicar as transformações descritas nas fases 2 e 3.

Simular pipelines batch e streaming conforme a arquitetura proposta.

Validar regras de qualidade usando os erros intencionais.

 Autor

Projeto desenvolvido por Rodrigo Augusto Cotrim no âmbito da UC Integração de Dados.
