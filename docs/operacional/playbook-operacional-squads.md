# Playbook Operacional para Squads

## 1. Objetivo do Playbook
Traduzir o framework SDLC + IA + GCP para rotina diaria dos squads.

Em linguagem simples:
Este documento explica o que cada time precisa fazer, em qual momento, com quais evidencias e quais ferramentas.

## 2. Estrutura de Trabalho da Squad
### Papeis minimos
- Product Owner: prioriza valor e backlog.
- Tech Lead: garante padrao tecnico e arquitetura.
- Devs: implementam funcionalidades e testes.
- QA/Engenharia de Qualidade: define estrategia de validacao.
- SRE/Operacao (dedicado ou compartilhado): confiabilidade e observabilidade.
- Ponto focal de seguranca (champion): controles de risco.

## 3. Fluxo Semanal da Squad
### Segunda
- Planejamento da semana.
- Revisao de prioridades e riscos.

### Diario
- Daily de 15 min com foco em bloqueios.

### Quarta/Quinta
- Refinamento tecnico + revisao de arquitetura (quando necessario).

### Sexta
- Demo interna, status dos KPIs e licoes aprendidas.

## 4. Checklist de Inicio de Sprint
- [ ] Objetivos de negocio claros para cada historia.
- [ ] Criterios de aceite definidos.
- [ ] Dependencias mapeadas.
- [ ] Riscos de seguranca e dados avaliados.
- [ ] Impacto em observabilidade mapeado.

## 5. Fluxo de Engenharia (Passo a Passo)
1. Criar branch de feature.
2. Implementar codigo com apoio de IA (quando fizer sentido).
3. Escrever testes unitarios e de integracao.
4. Abrir PR com template padrao.
5. Passar por review humano + quality gates.
6. Fazer merge e deploy em ambiente de homologacao.
7. Validar com produto/negocio.
8. Liberar para producao com janela definida.

## 6. Regras de Pull Request
Obrigatorio em toda PR:
- Contexto da mudanca.
- Evidencia de testes.
- Impacto em seguranca.
- Impacto em observabilidade.
- Plano de rollback.

## 7. Uso de IA no Dia a Dia
### Permitido
- Acelerar escrita de codigo e testes.
- Sugerir refatoracoes.
- Gerar documentacao tecnica inicial.
- Apoiar analise de incidentes.

### Nao permitido
- Subir codigo sem revisao humana.
- Enviar segredos ou dados sensiveis em prompts.
- Tomar decisao critica automatica sem aprovacao humana.

### Regra pratica
IA ajuda a produzir, humano aprova para publicar.

## 8. DevSecOps Operacional
### Pipeline minimo
- Build.
- Testes automatizados.
- SAST/analise estatica.
- Scan de vulnerabilidade de dependencias.
- Scan de imagem de container.
- Deploy com controle de aprovacao.

### Gate de bloqueio
Falha critica bloqueia merge/deploy.

## 9. Padrao de Observabilidade por Servico
Todo servico precisa de:
- Logs estruturados.
- Metricas de latencia/erro/throughput.
- Traces distribuidos.
- Alertas com dono definido.

Template de SLO basico:
- Disponibilidade mensal: 99.9%.
- Latencia p95: <= 300ms (ajustar por produto).
- Erro 5xx: <= 1%.

## 10. Runbook de Incidente (Resumo)
1. Detectar alerta.
2. Classificar severidade.
3. Comunicar canal oficial.
4. Mitigar impacto (rollback/fallback).
5. Resolver causa raiz.
6. Registrar postmortem sem culpabilizacao.
7. Criar acoes preventivas com prazo e dono.

## 11. Definicao de Pronto (DoR) da Squad
- Historia clara e priorizada.
- Dependencias mapeadas.
- Risco inicial avaliado.
- Criterios de aceite completos.

## 12. Definicao de Feito (DoD) da Squad
- Codigo revisado e aprovado.
- Testes e gates verdes.
- Logs/metricas/traces ativos.
- Documentacao atualizada.
- Plano de rollback validado.

## 13. Rituais de Melhoria Continua
- Retro quinzenal com foco em gargalos de fluxo.
- Revisao mensal de KPIs tecnicos e de negocio.
- Revisao trimestral de arquitetura e custo cloud.

## 14. KPIs Minimos da Squad
- Lead Time.
- Throughput.
- Taxa de retrabalho.
- Change Failure Rate.
- MTTR.
- Custo cloud por servico.

## 15. Checklist de Operacao em Producao
- [ ] Dashboard ativo.
- [ ] Alertas com destinatarios corretos.
- [ ] On-call definido.
- [ ] Runbook publicado.
- [ ] Objetivos de negocio monitorados.

## Navegacao

[← Voltar](../index.md)