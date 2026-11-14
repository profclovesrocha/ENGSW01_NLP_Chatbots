# DAY 1:
- Entrega do Desafio · Bloco 2
  
# DAY 2:
- PROJETO COM TInject: https://github.com/mikelustosa/Projeto-TInject
- Chat App: https://github.com/profclovesrocha/ideias/blob/main/Projects/3-Advanced/Chat-App.md

# Decrição do Projeto Final 
- Este é a proposta de Projeto Técnico como Desafio Final em Equipe (Valendo de 0,0 a 10,0 pontos), aplicando os conceitos de Processamento de Linguagem Natural (NLP) e Chatbots desenvolvidos na disciplina ao domínio operacional de Rotas Especiais de Helicóptero (REH)
.
🚁 PROJETO TÉCNICO: DESAFIO FINAL (EM EQUIPE)
Tema: Assistente Conversacional Inteligente para Consulta Operacional e Planejamento de Rotas Especiais de Helicóptero (REH)
Modalidade: Equipes de 3 a 5 discentes
Avaliação: 0,0 a 10,0 pontos
🎯 1. OBJETIVO DO DESAFIO
Desenvolver um protótipo funcional de assistente conversacional (Chatbot com RAG e saída estruturada) capaz de auxiliar pilotos e operadores aéreos no planejamento e consulta de Rotas Especiais de Helicóptero (REH) em Regiões Terminal (TMA). O sistema deve responder a dúvidas sobre corredores visuais, altitudes de tráfego, pontos de notificação compulsória e restrições operacionais, garantindo zero alucinação e validação estrita de esquemas.
📋 2. ESTRUTURA DOS ENTREGÁVEIS (4 MÓDULOS)
Módulo 1: Especificação e Prompt de Sistema (Peso: 2,5 pontos)
Prompt de Sistema Decomposto (5 Partes Canônicas): Definição clara de ROLE_AND_IDENTITY, CONTEXT_AND_GOALS, CONSTRAINTS_AND_SAFETY (impedir alucinação de coordenadas aéreas), INPUT_OUTPUT_SCHEMA e FALLBACK_AND_HANDOFF.
Árvore de Decisão Conversacional: Mapeamento do caminho feliz (ex: consulta de corredor visual), variações de intenção (condições meteorológicas de rota) e cenários de estresse (solicitação de pouso fora de rota).
Matriz de Fallback Detalhada (L1 a L3):
L1 (Clarificação): Ambiguidade de nome de rota ou waypoint.
L2 (Menu Guiado): Opções fechadas de corredores aéreos disponíveis na TMA.
L3 (Handoff): Transferência imediata da sessão para o Controle de Tráfego Aéreo (Operador Humano).
Módulo 2: Ingestão de Dados & Arquitetura de NLP / RAG (Peso: 2,5 pontos)
Base de Conhecimento REH: Ingestão de cartografia e regulamentação de tráfego aéreo (corredores visuais, altitudes mínimas/máximas em pés, pontos de reporte).
Pipeline de Busca Semântica: Indexação de documentos e aplicação de estratégia de recuperação para garantir respostas fundamentadas nas publicações aeronáuticas.
Módulo 3: Execução Interativa & Validação Estrita (Peso: 3,0 pontos)
Interface Executável: Aplicação interativa em Streamlit, Chainlit ou Gradio.
Validação de Esquema com Pydantic V2: O chatbot deve responder obrigatoriamente em formato JSON estruturado contendo:
{
  "corredor_reh": "string",
  "altitude_autorizada_ft": "integer",
  "pontos_notificacao": ["list"],
  "restricoes_meteorologicas": "string",
  "nivel_confianca": "float",
  "requires_handoff": "boolean",
  "resposta_usuario": "string"
}
Gestão de Contexto e Tokens: Mecanismo de Janela Deslizante (Sliding Window) mantendo o Prompt de Sistema fixo e podando o histórico recente sob limites de tokens da API.
Módulo 4: Repositório GitHub e Apresentação (Peso: 2,0 pontos)
Repositório Organizado: Estrutura limpa contendo README.md detalhado, requirements.txt e scripts modularizados.
Pitch & Demonstração (10 min): Apresentação da equipe demonstrando o fluxo em tempo real, testes de segurança/jailbreak e a ativação da matriz de fallback/handoff.
📊 3. RUBRICA DE AVALIAÇÃO (0,0 a 10,0)
Critério
Descrição
Pontuação
Especificação & Prompt de Sistema
Clareza no System Prompt de 5 partes, matriz de fallback de 3 níveis e robustez contra injection.
0,0 – 2,5
Arquitetura NLP & RAG
Qualidade da recuperação de informações regulatórias de REH e fidelidade sem alucinações.
0,0 – 2,5
Protótipo Funcional & Pydantic
Estabilidade da interface, validação JSON estrita via Pydantic e gestão eficiente de tokens.
0,0 – 3,0
Documentação & Apresentação
Qualidade do repositório no GitHub, clareza do código e desempenho da equipe na demonstração.
0,0 – 2,0
NOTA FINAL
10,0 pontos
Nota: O repositório da disciplina no GitHub traz a estrutura central de NLP e Chatbots da turma ENGSW01
, fornecendo a base técnica para a aplicação deste desafio no domínio aeronáutico de REH.
