# Relatório de Análise: Monitoramento de Autenticação

## 1. Objetivo
Analisar logs do sistema operacional Linux para identificar tentativas de acesso e garantir a integridade do ambiente.

## 2. Cenário de Logs
Filtro utilizado no Kibana: `event.dataset : "system.auth"`

## 3. Análise Observada
Durante o monitoramento, foram identificados logs de autenticação do usuário. 
- **Padrão detectado**: Registro contínuo de eventos de login no sistema.
- **Importância**: O monitoramento deste log é fundamental para detectar ataques de força bruta (brute-force) ou acessos não autorizados.

## 4. Próximos Passos (Hardening)
Para melhorar a segurança deste ambiente, as próximas ações recomendadas são:
- Implementar chaves SSH em vez de senhas.
- Configurar o Fail2Ban para bloquear IPs com excesso de tentativas de login.
