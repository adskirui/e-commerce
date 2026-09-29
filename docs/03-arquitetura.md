# Arquitetura e estrutura propostas

## Escolha da abordagem

Nenhuma stack ou plataforma está selecionada. Avaliar primeiro plataforma pronta, solução extensível ou desenvolvimento próprio, considerando prazo, orçamento, experiência da equipe, personalização e custo de operação.

Com a finalidade de portfólio confirmada, desenvolvimento próprio é a proposta preferencial para tornar visíveis as competências técnicas. A escolha final depende das tecnologias que o autor domina ou deseja demonstrar.

Se houver desenvolvimento próprio, a proposta inicial é uma aplicação modular com implantação simples e banco transacional. A separação dos módulos não exige serviços independentes.

## Módulos de domínio

| Módulo | Responsabilidade |
| --- | --- |
| Catálogo | Produtos, variantes, categorias, imagens e publicação. |
| Preços | Preço vigente e regras comerciais aprovadas. |
| Carrinho e checkout | Intenção de compra, validações e cálculo do total. |
| Estoque | Saldo, reservas, baixas e devoluções, quando aplicável. |
| Pedidos | Registro da compra e transições de estado permitidas. |
| Pagamentos | Cobranças, eventos do provedor, conciliação e reembolsos. |
| Entrega | Cotação, expedição e rastreamento, quando aplicável. |
| Acesso e administração | Autenticação, permissões e auditoria. |
| Notificações | Comunicações transacionais e tratamento de falhas. |
| Fornecedores | Catálogo externo simulado, atualização de disponibilidade e encaminhamento de itens para atendimento. |

Para o portfólio, usar adaptadores substituíveis de pagamento, fornecedor e entrega. Fornecedores e transportadoras podem ser simulados de forma determinística; pagamento pode usar sandbox do provedor escolhido. A interface deve identificar o modo demonstrativo. Pedidos com itens de fornecedores diferentes podem gerar atendimentos e entregas separados, mantendo um único pedido do cliente.

## Dados conceituais

- Produto possui variantes vendáveis; cada variante tem identificador comercial e disponibilidade.
- Carrinho possui itens referenciando variantes. Seus valores devem ser revalidados no checkout.
- Pedido possui itens com cópia do nome, variante, quantidade e preço da compra. Alterar o catálogo não altera pedidos anteriores.
- Pedido pode ter várias tentativas de pagamento. Pagamento e reembolso possuem identificadores próprios e referências do provedor.
- Entrega e endereço são associados ao pedido quando necessários. Conta de cliente pode ser opcional, conforme a decisão sobre compra sem cadastro.
- Reserva de estoque registra quantidade, expiração e vínculo com a compra, se esse modelo for adotado.
- Valores monetários usam representação exata e moeda explícita, evitando ponto flutuante nos cálculos financeiros.

## Consistência e integrações

O servidor determina preços, totais e permissões. Retorno do navegador não comprova pagamento. Eventos do provedor precisam ter autenticidade verificada, processamento idempotente e tolerância a duplicação ou chegada fora de ordem.

Estado do pedido, estado do pagamento e estado da entrega devem ser tratados separadamente. As transições exatas serão documentadas após escolher os provedores. Reembolso solicitado não equivale a reembolso confirmado.

Definir a política de reserva e expiração antes de implementar estoque. Pagamentos confirmados após a expiração exigem tratamento explícito, como nova verificação de saldo e encaminhamento para atendimento ou reembolso.

Prever conciliação com o provedor para recuperar eventos perdidos. Credenciais e ambientes de teste e produção permanecem separados.

## Organização futura do código

Estrutura ilustrativa para desenvolvimento próprio; criar pastas de código somente após selecionar a stack:

```text
/
├── README.md
├── docs/                   # Produto, arquitetura, operação e decisões
├── src/
│   ├── storefront/         # Experiência de compra
│   ├── admin/              # Interface administrativa
│   ├── modules/            # Regras de negócio por domínio
│   └── integrations/       # Adaptadores de serviços externos
├── tests/                  # Testes de integração e jornadas críticas
├── scripts/                # Comandos de manutenção documentados
└── infra/                  # Configuração de implantação, se necessária
```

Frameworks e plataformas podem exigir outra organização. Evitar duplicar convenções nativas apenas para seguir este exemplo.

## Decisões técnicas pendentes

Plataforma, linguagem, framework, banco, hospedagem, armazenamento de imagens, autenticação, pagamento, entrega, notificações e observabilidade. Cada escolha deve considerar integração disponível, custo, manutenção e requisitos do negócio.
