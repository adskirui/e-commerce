# Roadmap e backlog inicial

Sem datas comprometidas. Estimativas dependem de escopo, plataforma, equipe, orçamento e integrações.

Destino confirmado: portfólio completo. Neste roadmap, lançamento significa publicação de uma demonstração, sem vendas reais. O MVP é intermediário e a etapa final inclui o escopo do documento 07. A evolução será orientada por feedback sobre o projeto, não por receita.

| Etapa | Entrega | Dependência | Critério de conclusão |
| --- | --- | --- | --- |
| 1. Descoberta | Briefing e objetivo do negócio | Respostas do responsável pelo projeto | Público, oferta, região, operação e limites definidos. |
| 2. Escopo | MVP revisado e backlog priorizado | Descoberta | Jornadas e critérios de aceite acordados. |
| 3. Solução | Plataforma, integrações e arquitetura | Escopo | Decisões registradas e viabilidade das integrações críticas verificada. |
| 4. Experiência | Mapa de páginas e protótipo do fluxo de compra | Escopo e identidade inicial | Catálogo, produto, carrinho, checkout e acompanhamento revisados. |
| 5. Fundação | Projeto executável, configuração e ambientes | Solução | Execução local e implantação de homologação reproduzíveis. |
| 6. Compra completa | Catálogo, carrinho, checkout e pagamento | Fundação e provedores de teste | Pedido pago criado de ponta a ponta em homologação. |
| 7. Operação | Administração, entrega e pós-venda | Compra completa | Operador consegue processar pedidos e tratar exceções. |
| 8. Lançamento | Verificações e preparação operacional | Etapas anteriores | Critérios de qualidade cumpridos e responsáveis prontos para operar. |
| 9. Evolução | Melhorias orientadas por uso | Operação ativa | Prioridades revisadas com dados e feedback. |

## Primeiras tarefas

- PLAN-01: responder às perguntas essenciais do briefing. Responsável: a definir. Status: pendente.
- PLAN-02: validar a hipótese de loja de um único vendedor. Status: concluído; usuário definiu loja própria com fornecedores ou dropshipping.
- PLAN-03: revisar itens obrigatórios e exclusões do MVP. Depende de PLAN-01 e PLAN-02.
- PLAN-04: comparar abordagens de plataforma com custos e limitações atuais. Depende de PLAN-03.
- PLAN-05: escolher pagamento e entrega conforme o mercado. Depende de PLAN-01 e PLAN-04.
- PLAN-06: detalhar mapa de páginas e fluxo operacional. Depende de PLAN-03.
- PLAN-07: estimar implementação e custos recorrentes. Depende de PLAN-04, PLAN-05 e PLAN-06.

## Modelo de tarefa de implementação

Cada tarefa deve conter objetivo do usuário, escopo, critérios verificáveis de aceite, dependências, responsável e status. Acrescentar riscos e estratégia de validação quando relevantes.

Uma tarefa estará concluída quando cumprir seus critérios, passar pelas verificações pertinentes e tiver documentação atualizada quando o comportamento mudar.

## Riscos iniciais

| Risco | Como reduzir |
| --- | --- |
| Desenvolver antes de entender a operação | Fechar descoberta e revisar MVP antes de implementar. |
| Escopo crescer sem revisão de recursos | Registrar impacto e repriorizar a cada inclusão. |
| Integração essencial inviável ou cara | Verificar disponibilidade e custo antes de selecionar a solução. |
| Cobrança e pedido divergirem | Projetar idempotência, conciliação e tratamento de exceções. |
| Loja vender sem capacidade de atender | Validar estoque, entrega, suporte e pós-venda antes do lançamento. |
