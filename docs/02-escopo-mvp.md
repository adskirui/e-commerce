# Escopo proposto do MVP

Proposta sujeita às respostas da descoberta. Prioridade inicial: permitir uma compra completa e uma operação administrável.

Após a definição de finalidade de portfólio, este MVP passa a representar um marco intermediário. A entrega final é a experiência completa do documento 07. Integrações externas usarão sandbox ou simulações identificadas; não haverá cobrança real.

## Jornadas principais

Cliente: encontrar produto → consultar detalhes e disponibilidade → adicionar ao carrinho → informar dados necessários → escolher entrega, quando aplicável → pagar → receber confirmação → acompanhar pedido e solicitar atendimento.

Operador: cadastrar produto → definir preço e disponibilidade → acompanhar pagamento → preparar e despachar pedido, quando aplicável → atualizar acompanhamento → tratar cancelamentos e reembolsos.

## Requisitos e critérios de aceite

| ID | Capacidade | Critério de aceite proposto |
| --- | --- | --- |
| MVP-01 | Catálogo | Exibir apenas produtos publicados, com nome, imagem, preço e disponibilidade; permitir navegação por categoria. |
| MVP-02 | Página de produto | Mostrar descrição, preço e variações aplicáveis; impedir inclusão de uma variação indisponível. |
| MVP-03 | Carrinho | Adicionar, alterar e remover itens; recalcular totais e informar mudanças de preço ou disponibilidade antes da compra. |
| MVP-04 | Checkout | Validar dados obrigatórios, apresentar itens, descontos, entrega e total antes da confirmação. Compra sem conta é uma proposta a validar. |
| MVP-05 | Pagamento | Criar cobrança via provedor; confirmar pagamento com informação validada no servidor; eventos repetidos não podem duplicar efeitos. |
| MVP-06 | Pedido | Gerar identificador único e preservar os dados comerciais da compra; permitir consulta somente por acesso autorizado. |
| MVP-07 | Administração | Restringir acesso; permitir gestão de catálogo e acompanhamento de pedidos com registro de ações sensíveis. |
| MVP-08 | Disponibilidade | Para estoque controlado, impedir venda acima do saldo conforme a política de reserva definida e testar compras concorrentes. |
| MVP-09 | Entrega | Para produtos físicos, informar preço e prazo antes do pagamento e permitir acompanhamento da expedição. |
| MVP-10 | Comunicação | Enviar confirmação após pagamento confirmado; falha de notificação não pode invalidar pedido pago. |
| MVP-11 | Pós-venda | Disponibilizar contato e fluxo operacional para cancelamento e reembolso, com estados e registros rastreáveis. |
| MVP-12 | Informações da loja | Disponibilizar identificação, atendimento e políticas revisadas para o mercado e a operação definidos. |

## Fora do MVP por padrão

Reavaliar apenas com justificativa de negócio: marketplace, programa de fidelidade, recomendações personalizadas, aplicativo nativo, múltiplas moedas, múltiplos estoques, assinaturas, avaliações e automações avançadas de marketing.

Busca textual, cupons e conta do cliente dependem do tamanho do catálogo e das necessidades da operação. Não são obrigatórios nesta proposta.

## Qualidade esperada

- Layout utilizável em celular e desktop, com atenção à navegação por teclado, rótulos e mensagens de erro.
- Dados comerciais e permissões validados no servidor.
- Erros de pagamento ou entrega devem permitir recuperação sem duplicar pedidos ou cobranças indevidamente.
- Segredos e dados sensíveis não devem aparecer no código cliente nem em logs.
- Metas de desempenho e disponibilidade serão definidas antes da implementação, conforme volume e orçamento.

## Regra para mudança de escopo

Para adicionar uma funcionalidade, registrar necessidade, prioridade, dependências, impacto estimado e responsável pela decisão. Se afetar a entrega acordada, revisar prazo ou retirar outro item explicitamente.
