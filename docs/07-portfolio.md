# Entrega completa de portfólio

## Direção confirmada

Construir um e-commerce para portfólio, sem intenção de vender agora, representando uma loja própria com fornecedores ou dropshipping. A preferência é conceber uma experiência completa desde o início. Implementar por etapas permite validar essa experiência sem reduzir o objetivo final ao MVP.

## Escopo final proposto

| Frente | Funcionalidades |
| --- | --- |
| Loja | Home, categorias, busca, filtros, página de produto e variações, estados vazios e indisponibilidade. |
| Compra | Carrinho persistente, checkout, cotação de entrega simulada, cupom simples e pagamento de teste. |
| Cliente | Cadastro, login, recuperação de acesso em ambiente de teste, endereços, histórico e detalhes dos próprios pedidos. |
| Pós-venda | Solicitação de cancelamento ou devolução, acompanhamento e reembolso de teste com regras explícitas. |
| Administração | Gestão de produtos, categorias, variantes, preços, disponibilidade, pedidos, clientes e cupons. |
| Fornecedores | Cadastro fictício, vínculo de variantes, sincronização simulada de saldo e preço de custo, encaminhamento e falha de atendimento. |
| Logística | Entregas por fornecedor, rastreamento simulado e atualização dos estados de expedição. |
| Painel | Indicadores calculados a partir dos pedidos fictícios, com período e significado claros. |
| Engenharia | Permissões, validação no servidor, testes de fluxos críticos, logs úteis, configuração reproduzível e dados de demonstração. |
| Apresentação | Demo publicada, README com imagens, arquitetura, instruções locais, limitações conhecidas e roteiro de demonstração. |

Conta do cliente, busca e cupons integram esta proposta de entrega final, mesmo que não entrem no primeiro marco. Marketplace, assinaturas, aplicativo nativo e múltiplas moedas continuam fora do escopo por padrão.

## Cenários demonstráveis

1. Compra aprovada: navegar, selecionar variante, concluir pagamento de teste e acompanhar as entregas.
2. Pagamento recusado: apresentar erro útil e permitir nova tentativa sem duplicação indevida.
3. Disponibilidade alterada: simular falta de saldo do fornecedor e apresentar resolução antes da compra ou tratamento da exceção posterior.
4. Pedido com dois fornecedores: exibir atendimentos e rastreamentos separados, vinculados à mesma compra.
5. Pós-venda: solicitar cancelamento, processar decisão administrativa e acompanhar reembolso simulado.
6. Administração: cadastrar produto, publicar e confirmar sua exibição na loja.
7. Controle de acesso: impedir consulta de pedidos alheios e ações administrativas sem permissão.

## Artefatos esperados

- Briefing do nicho fictício e identidade visual.
- Mapa de páginas e protótipo responsivo.
- Diagrama de dados, estados e integrações após selecionar a stack.
- Backlog detalhado com critérios de aceite.
- Aplicação reproduzível com carga inicial de dados fictícios.
- Verificações automatizadas dos fluxos críticos e revisão visual.
- Demonstração publicada e roteiro curto para recrutadores ou clientes.
- Estudo de caso explicando problema, decisões, dificuldades e resultados técnicos efetivamente verificados.

## Critério de conclusão

O projeto estará pronto para apresentação quando os cenários acima forem reproduzíveis, a interface funcionar em celular e desktop, a documentação permitir executar o projeto e as simulações estiverem identificadas. Não apresentar métricas fictícias como vendas reais nem funcionalidades planejadas como implementadas.

## Próximas definições

Escolher nicho e linguagem visual; informar experiência atual e tecnologias que se deseja demonstrar; definir orçamento de hospedagem e disponibilidade semanal. Essas respostas permitem recomendar a stack e transformar o roadmap em tarefas estimadas.
