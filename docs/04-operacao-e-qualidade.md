# Operação e qualidade

## Aplicação ao portfólio

Nesta fase, operação significa demonstração com dados fictícios. Não será necessário contratar fornecedores ou habilitar vendas reais. Os requisitos de lançamento comercial abaixo ficam como referência para uma eventual evolução; a entrega atual segue os critérios do documento 07.

A demonstração pública deve indicar que não realiza vendas, evitar coleta desnecessária de dados reais e impedir que visitantes alterem configurações ou dados compartilhados de forma permanente. Usar sessão isolada, acesso administrativo restrito ou restauração controlada dos dados de demonstração. Reembolsos, notificações e expedições serão simulados ou restritos a ambientes de teste.

## Responsabilidades a atribuir

Definir responsáveis por produto, desenvolvimento, catálogo, estoque, atendimento, expedição, financeiro e infraestrutura. Uma pessoa pode acumular funções; nenhuma função essencial deve ficar sem responsável antes do lançamento.

## Preparação operacional

- Definir cadastro e atualização de produtos, preços e disponibilidade.
- Documentar processamento diário de pedidos, exceções de pagamento e divergências de estoque.
- Definir como atender cancelamentos, devoluções, reembolsos e falhas de entrega.
- Definir a conciliação entre pedidos, cobranças e recebimentos.
- Revisar requisitos fiscais, de consumo, privacidade e políticas conforme país, produto e operação. Esta revisão está pendente; este documento não estabelece requisitos legais específicos.

## Segurança e dados

- Coletar apenas dados necessários e definir finalidade, acesso, retenção e exclusão.
- Manter segredos fora do repositório e utilizar configuração separada por ambiente.
- Restringir operações administrativas por permissão; definir proteção adicional para contas privilegiadas.
- Preferir fluxo de pagamento em que dados de cartão sejam tratados pelo provedor, sem armazenamento pela aplicação.
- Validar entradas e proteger consultas de pedidos contra acesso de terceiros.
- Registrar eventos operacionais sem expor credenciais, dados de pagamento ou informações pessoais desnecessárias.
- Planejar backups e validar restauração antes de depender deles em produção.

## Verificação antes de lançar

| Área | Evidência esperada |
| --- | --- |
| Compra | Jornada completa validada em ambiente de testes, incluindo pagamento recusado e nova tentativa. |
| Pagamento | Eventos duplicados, atrasados e fora de ordem não corrompem estados; conciliação verificada. |
| Estoque | Compras concorrentes, expiração e liberação de reservas testadas, se aplicáveis. |
| Permissões | Cliente não acessa pedido alheio e usuário sem permissão não executa ações administrativas. |
| Valores | Quantidades, descontos, entrega e arredondamento produzem total correto no servidor. |
| Experiência | Fluxos críticos revisados em celular, desktop e navegação por teclado. |
| Operação | Cancelamento, reembolso e atendimento executados em cenário de teste. |
| Recuperação | Procedimentos de restauração e reversão de implantação documentados e verificados. |

## Ambientes e lançamento

Separar desenvolvimento, homologação e produção conforme a plataforma escolhida. Usar dados fictícios e credenciais de teste fora de produção. Definir migrações, configuração, monitoramento e procedimento de reversão antes da primeira publicação.

Antes de abrir vendas, validar catálogo real, credenciais de produção, domínio, políticas, canais de atendimento e rotina operacional. Uma compra controlada em produção dependerá da autorização e das condições da operação.

## Acompanhamento

Monitorar falhas de checkout, processamento de pagamentos, notificações pendentes e divergências de pedidos. Definir quem recebe alertas e como responde. Ferramentas, limites de alerta e metas de recuperação ainda serão selecionados.
