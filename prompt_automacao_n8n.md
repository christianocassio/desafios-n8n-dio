Atue como um especialista em N8N.

Crie uma automação para triagem e direcionamento automático de tickets de atendimento recebidos via formulário.

Público:
Equipe de Suporte e Atendimento ao Cliente.

Ferramentas envolvidas:
Webhook (HTTP Trigger), OpenAI, Trello e Slack.

Fluxo:
1. Receber requisição HTTP via Webhook com dados do cliente (Nome, E-mail, Assunto, Mensagem).
2. Validar se o e-mail está preenchido.
3. Analisar o conteúdo da mensagem via OpenAI para identificar a categoria (Suporte, Dúvida Comercial, Reclamação) e a prioridade (Baixa, Média, Alta).
4. Criar um card no Trello no quadro de "Atendimento", na lista equivalente à categoria identificada.
5. Enviar uma mensagem formatada para o Slack com os detalhes do ticket.

Regras:
- Se o campo "E-mail" estiver vazio, interrompa a execução (Filter / Switch).
- Se a prioridade for "Alta", adicione a tag `@here` na notificação do Slack para alerta imediato.

Explique quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow.