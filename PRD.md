# PRD - Plataforma de Treinamento Gamificada

## 1. Visao Geral

### 1.1 Nome do Produto
Plataforma de Treinamento Gamificada.

### 1.2 Contexto
Este produto oferece uma experiencia de aprendizado online com trilha sequencial de disciplinas, quizzes, gamificacao por badges, forum colaborativo e suporte via monitoria e IA.

### 1.3 Problema
Alunos de treinamentos internos/academicos costumam ter:
- baixa continuidade de estudo;
- pouca visibilidade de progresso;
- dificuldade para tirar duvidas rapidamente;
- baixa interacao com comunidade.

### 1.4 Proposta de Valor
Entregar uma jornada guiada e motivadora, com progresso claro, recompensas por desempenho e suporte multiponto (monitor + IA + forum).

## 2. Objetivos de Produto

## 2.1 Objetivos Primarios
- Aumentar taxa de conclusao de disciplinas.
- Reduzir tempo medio de resolucao de duvidas.
- Melhorar engajamento semanal dos alunos.
- Dar visibilidade operacional para monitores e administradores.

## 2.2 Metas de Sucesso (KPIs)
- Conclusao por disciplina >= 70% dos alunos ativos.
- WAU/MAU >= 60%.
- Tempo medio para primeira resposta em duvidas <= 24h.
- Taxa de aprovacao no quiz final >= 75% apos 2 tentativas.
- Participacao no forum (posts + respostas) >= 30% dos alunos ativos/mensal.

## 3. Perfis de Usuario

### 3.1 Aluno
Responsavel por consumir conteudo, concluir aulas, realizar quizzes, abrir duvidas, interagir no forum e acompanhar conquistas.

### 3.2 Monitor
Responsavel por acompanhar alunos vinculados, analisar progresso e responder duvidas.

### 3.3 Administrador
Responsavel por configurar disciplinas/conteudos, gerenciar monitores, acompanhar relatorios e governanca da plataforma.

## 4. Escopo do Produto

### 4.1 Escopo In-Scope (MVP Atual + Consolidacao)
- Autenticacao com login, cadastro e recuperacao de senha.
- Controle de papeis (admin, monitor, user).
- Trilhas de disciplinas em ordem sequencial.
- Aulas com conteudo em video/material complementar.
- Quiz por aula e quiz final por disciplina.
- Gamificacao com badges por desempenho.
- Dashboard do aluno com estatisticas e progresso.
- Forum com criacao de post e filtros.
- Fluxo de duvidas com monitoria.
- Painel de monitor com alunos e duvidas.
- Painel administrativo para disciplinas, monitores e relatorios.
- Chat com IA para apoio ao estudo.

### 4.2 Out of Scope (nesta versao)
- Aplicativo mobile nativo.
- Certificacao oficial com assinatura digital.
- Integracoes com LMS externo (Moodle, Canvas etc).
- Notificacoes push em app.

## 5. Requisitos Funcionais

### 5.1 Autenticacao e Conta
- RF-001: Usuario deve poder criar conta com nome, email e senha.
- RF-002: Usuario deve poder entrar com email e senha.
- RF-003: Usuario deve poder solicitar reset de senha por email.
- RF-004: Sistema deve suportar fluxo de redefinicao de senha no primeiro acesso (quando aplicavel).
- RF-005: Sistema deve identificar role do usuario (admin, monitor, user) e aplicar rotas protegidas.

### 5.2 Jornada de Aprendizado (Aluno)
- RF-006: Sistema deve listar disciplinas ordenadas por ordem definida.
- RF-007: Disciplina N so deve ser desbloqueada quando disciplina N-1 estiver concluida.
- RF-008: Usuario deve poder abrir detalhes da disciplina com aulas, materiais e progresso.
- RF-009: Sistema deve controlar progresso por aula concluida.
- RF-010: Usuario deve poder realizar quiz por aula quando disponivel.
- RF-011: Sistema deve registrar resultado do quiz por aula (pontuacao, acertos e status).
- RF-012: Quiz final deve ser desbloqueado somente apos concluir todas as aulas da disciplina.
- RF-013: Sistema deve considerar aprovacao no quiz final com nota minima de 70%.
- RF-014: Sistema deve permitir refazer quiz final.

### 5.3 Gamificacao e Conquistas
- RF-015: Sistema deve calcular badges por disciplina conforme desempenho em quizzes e progresso.
- RF-016: Sistema deve exibir badges em dashboard e pagina de conquistas.
- RF-017: Sistema deve sinalizar novo badge desbloqueado apos evento elegivel.
- RF-018: Sistema deve manter ranking por disciplina baseado em regras de badges.

### 5.4 Forum
- RF-019: Usuario autenticado deve poder criar post no forum.
- RF-020: Post deve aceitar categoria, titulo, conteudo e contexto opcional (disciplina/aula).
- RF-021: Sistema deve listar posts com filtros por categoria, disciplina e busca textual.
- RF-022: Sistema deve exibir contagem de curtidas e respostas por post.

### 5.5 Duvidas e Monitoria
- RF-023: Aluno com monitor vinculado deve poder abrir duvida em disciplina/aula.
- RF-024: Sistema deve permitir status da duvida: open, answered, resolved.
- RF-025: Aluno deve visualizar suas duvidas com filtros por status.
- RF-026: Monitor deve visualizar duvidas dos alunos vinculados.
- RF-027: Monitor deve responder duvidas e acompanhar historico.

### 5.6 Painel do Monitor
- RF-028: Monitor deve acessar dashboard com total de alunos vinculados.
- RF-029: Monitor deve ver metricas de progresso e media de desempenho dos alunos.
- RF-030: Monitor deve navegar para detalhe de aluno e suas duvidas.

### 5.7 Painel Administrativo
- RF-031: Admin deve criar, editar e remover disciplinas.
- RF-032: Admin deve configurar ordem das disciplinas.
- RF-033: Admin deve gerenciar conteudos da disciplina (aulas, materiais, quizzes).
- RF-034: Admin deve promover usuario para monitor e remover papel de monitor.
- RF-035: Admin deve vincular e desvincular alunos de monitores.
- RF-036: Admin deve acessar relatorios gerais e relatorios de monitoria.

### 5.8 IA Educacional
- RF-037: Aluno deve poder usar chat com IA dentro do contexto da disciplina.
- RF-038: IA deve atuar como suporte pedagogico e nao como substituicao de avaliacao.

## 6. Regras de Negocio

- RN-001: A progressao de disciplinas e sequencial.
- RN-002: Aprovacao no quiz final requer nota >= 70.
- RN-003: Quiz de aula pode exigir minimo de 66% para concluir aula quando aplicavel.
- RN-004: Badges sao calculados com base em resultados de quizzes e conclusoes.
- RN-005: Aluno sem monitor vinculado nao abre nova duvida de monitoria.
- RN-006: Permissoes de rota devem respeitar role do usuario.
- RN-007: Exclusao de disciplina pode impactar aulas, materiais e quizzes vinculados.

## 7. Requisitos Nao Funcionais

### 7.1 Performance
- RNF-001: Carregamento inicial das paginas principais em ate 3s (rede padrao banda larga).
- RNF-002: Consultas criticas devem priorizar paralelizacao e pagina relevante.

### 7.2 Seguranca
- RNF-003: Todas as rotas sensiveis devem estar protegidas por autenticacao e role.
- RNF-004: Dados devem ser protegidos por regras de acesso no backend (RLS no Supabase).
- RNF-005: Chaves de integracao (Supabase/Gemini) devem ser injetadas por variaveis de ambiente.

### 7.3 Confiabilidade
- RNF-006: Operacoes de gravacao devem retornar feedback claro de sucesso/erro.
- RNF-007: Erros de rede devem ter fallback de UI (loading/empty/error states).

### 7.4 Usabilidade
- RNF-008: Fluxos principais devem ser responsivos para desktop e mobile web.
- RNF-009: Interfaces devem exibir estado de progresso e proximos passos do aluno.

### 7.5 Observabilidade
- RNF-010: Eventos de produto devem ser mensuraveis para funil de aprendizado e suporte.

## 8. Jornada do Usuario (Resumo)

### 8.1 Aluno
Cadastro/Login -> Dashboard -> Disciplina desbloqueada -> Aulas + Quiz por aula -> Quiz final -> Badge/Conquista -> Proxima disciplina.

### 8.2 Aluno com Duvida
Tela da disciplina ou Minhas Duvidas -> Abrir duvida -> Monitor responde -> Aluno marca como resolvida.

### 8.3 Monitor
Login -> Dashboard monitor -> Lista de alunos -> Analise de progresso -> Resposta de duvidas.

### 8.4 Admin
Login -> Gestao de disciplinas -> Gestao de monitores -> Vinculos aluno-monitor -> Relatorios.

## 9. Dependencias Tecnicas

- Frontend: React + Vite + React Router.
- Backend e dados: Supabase (Auth, PostgreSQL, RPC, Storage).
- IA: Google Gemini API.
- Design/icone: React Icons + CSS modular por pagina/componente.

## 10. Instrumentacao e Metricas

### 10.1 Eventos Minimos Recomendados
- EVT-001: login_sucesso
- EVT-002: disciplina_aberta
- EVT-003: aula_concluida
- EVT-004: quiz_aula_enviado
- EVT-005: quiz_final_enviado
- EVT-006: badge_desbloqueado
- EVT-007: duvida_criada
- EVT-008: duvida_respondida
- EVT-009: post_forum_criado

### 10.2 Dashboards Operacionais
- Funil: visita dashboard -> abre disciplina -> conclui aulas -> envia quiz final -> aprovado.
- Qualidade pedagogica: media por quiz, taxa de reprovacao por disciplina.
- Suporte: volume de duvidas por status e tempo de resposta.

## 11. Roadmap Proposto

### Fase 1 - Estabilizacao
- Revisar permissoes de dados por role e cobertura de regras de acesso.
- Padronizar tratamento de erro e mensagens para usuario.
- Completar instrumentacao de eventos de produto.

### Fase 2 - Escala de Aprendizado
- Melhorar ranking e comparativos por turma/disciplina.
- Adicionar trilhas personalizadas por desempenho.
- Notificacoes in-app para pendencias e conquistas.

### Fase 3 - Eficiencia Operacional
- Relatorios executivos com coortes e retencao.
- Automacao de atribuicao de monitor por capacidade.
- Base de conhecimento para respostas assistidas por IA.

## 12. Criterios de Aceite (Nivel Produto)

- CA-001: Usuario acessa somente rotas permitidas para seu role.
- CA-002: Disciplina bloqueada nao pode ser acessada antes da conclusao da anterior.
- CA-003: Quiz final so libera apos concluir todas as aulas da disciplina.
- CA-004: Resultado de quiz e progresso persistem corretamente apos refresh/sessao.
- CA-005: Badge desbloqueado aparece no fluxo e nas telas de conquistas.
- CA-006: Duvida criada por aluno aparece no painel do monitor vinculado.
- CA-007: Admin consegue promover/remover monitor e gerenciar vinculos com alunos.
- CA-008: Forum aceita criacao e listagem com filtros sem quebra de navegacao.

## 13. Riscos e Mitigacoes

- R-001: Complexidade de regras de permissao por role.
  - Mitigacao: matriz de acesso por tabela + testes de politica RLS.
- R-002: Queda de engajamento apos primeiras disciplinas.
  - Mitigacao: reforco de gamificacao, lembretes e trilhas guiadas.
- R-003: Dependencia de servico externo de IA.
  - Mitigacao: fallback de interface e mensagens claras em indisponibilidade.

## 14. Premissas

- Ha equipe para manutencao de conteudo (disciplinas, aulas, quizzes).
- Monitores serao cadastrados e vinculados ativamente pelo admin.
- Ambiente Supabase esta com schema/migracoes atualizados.

## 15. Anexos

- Documento tecnico de arquitetura (a criar/atualizar).
- Matriz de permissoes por perfil (a criar/atualizar).
- Plano de testes E2E dos fluxos criticos (a criar/atualizar).
