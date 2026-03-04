#  Automação de Alertas de Logs Críticos com n8n e Telegram

##  Visão Geral

Este projeto apresenta o desenvolvimento de um workflow de automação para monitoramento e notificação de logs críticos em tempo real utilizando a plataforma low-code **n8n**.

O objetivo foi reduzir a latência na identificação de falhas em ambientes DevOps, automatizando o envio de alertas instantâneos via Telegram e contribuindo diretamente para a redução do **MTTR (Mean Time To Recovery)**.

---

##  Arquitetura da Solução

A automação foi construída seguindo o modelo **Trigger → Process → Action**:

1. **Webhook (Trigger)**  
   Recebe um payload JSON contendo informações do log de erro.

2. **Edit Fields (Processamento)**  
   Formata os dados recebidos e gera uma mensagem de alerta estruturada.

3. **Telegram (Ação)**  
   Envia notificação instantânea para a equipe responsável.

O workflow opera com latência inferior a um segundo.

---

##  Tecnologias Utilizadas

- **n8n** (plataforma low-code)
- **Docker** (execução local)
- **Telegram Bot API**
- **Insomnia** (simulação de requisições HTTP)
- Webhooks e JSON

---

##  Funcionamento

Quando um erro crítico ocorre na aplicação:

- Um payload JSON é enviado para o Webhook
- O n8n processa e formata a mensagem
- O alerta é enviado automaticamente para o Telegram
- A equipe recebe a notificação em tempo real

Exemplo de informações enviadas:
- Nível do erro
- Nome da aplicação
- Mensagem detalhada

---

##  Resultados

- Redução significativa da latência de notificação
- Execução do workflow em menos de 1 segundo
- Eliminação do monitoramento manual de logs
- Melhoria direta no tempo de resposta a incidentes (MTTR)

---

##  Decisão Técnica

Inicialmente foi testada integração via SMTP (Gmail), porém a complexidade de autenticação OAuth2 não era adequada ao contexto low-code.

A integração com o **Telegram** foi escolhida por:

- Simplicidade de autenticação via Bot Token
- Facilidade de implementação
- Rapidez na entrega das notificações

---

##  Objetivo Acadêmico

Projeto desenvolvido como Trabalho de Conclusão da disciplina de **Interação Humano-Computador**, com foco em:

- Automação de processos
- DevOps e MTTR
- Monitoramento de logs
- Desenvolvimento Low-Code
- Integração com APIs externas

---

##  Documentação

O repositório contém o relatório completo em PDF com:

- Fundamentação teórica
- Arquitetura do workflow
- Configuração dos nós
- Resultados e validação
- Referências acadêmicas
