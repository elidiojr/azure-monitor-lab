# Guia Prático: Monitoramento de Máquinas Virtuais no Microsoft Azure 📊

## 📌 Descrição

Este repositório faz parte do desafio da DIO: **"Monitoramento de Máquinas Virtuais no Azure"**.

Aqui estão documentadas as principais práticas de **monitoramento**, **alertas**, **logs** e **diagnósticos** aplicados a VMs no ambiente Azure.

---

## 🎯 Objetivos do Projeto

- Aplicar os conceitos de monitoramento aprendidos nas aulas.
- Configurar alertas para eventos críticos (exemplo: exclusão de uma VM).
- Documentar as etapas para facilitar futuras implementações.
- Compartilhar o conteúdo com outros profissionais e estudantes.

---

## 🧱 Conteúdo

### 1. Introdução ao Monitoramento no Azure

- O que é o **Azure Monitor**
- Diferença entre **Logs**, **Métricas** e **Alertas**
- Importância do monitoramento proativo de recursos

### 2. Principais Recursos Utilizados

- **Azure Monitor**
- **Log Analytics Workspace**
- **Alertas de Métricas**
- **Alertas de Atividade (Activity Log Alerts)**
- **Action Groups (Grupos de Ação)**

---

## 🚀 Etapas Práticas Realizadas

### ✅ Configuração de Diagnóstico da VM

- Habilitação de diagnósticos na VM
- Envio de logs e métricas para o **Log Analytics Workspace**

### ✅ Criação de um Log Analytics Workspace

- Nome do workspace
- Região
- Associação com as VMs

### ✅ Configuração de Alertas para Eventos Críticos

Exemplo: **Alerta para detectar exclusão de VM**

- **Fonte:** Azure Activity Log
- **Condição:** Evento "Delete Virtual Machine"
- **Ação:** Envio de e-mail através de um Action Group

**Detalhes do Alerta Criado:**

- **Nome:** `Alert_VM_Deletion`
- **Condição:** Quando uma VM for excluída
- **Ação:** Envio de notificação por e-mail ao administrador

### ✅ Teste dos Alertas

- Exclusão de uma VM de teste
- Verificação do recebimento de alerta por e-mail

### ✅ Visualização de Logs e Métricas

- Acesso ao **Log Analytics**
- Execução de consultas utilizando **KQL (Kusto Query Language)**

## 💡 Dicas Importantes

- Sempre validar os **Action Groups** antes de criar os alertas, garantindo que os destinatários estão corretos.
- Usar **tags** nas VMs para facilitar a organização e o monitoramento por ambiente (ex: produção, desenvolvimento).
- Criar um **Resource Group dedicado** apenas para serviços de monitoramento, seguindo boas práticas de governança no Azure.
- Aproveitar os **Dashboards do Azure Monitor** para obter uma visão consolidada da saúde dos recursos.
- Utilizar **filtros personalizados** ao criar os alertas para evitar falsos positivos.
- Realizar **testes de alerta periodicamente** para garantir que as configurações continuam válidas.
- Monitorar o consumo de recursos das VMs para evitar custos desnecessários.
- Aproveitar o recurso de **Autoscale** (quando aplicável) para ajustar o tamanho das VMs automaticamente com base nas métricas de uso.
- Configurar **retenção de logs** adequada ao seu cenário, evitando acúmulo de dados desnecessários.
- Integrar o Azure Monitor com ferramentas externas (como **Microsoft Teams**, **Slack** ou **ITSM**) usando Webhooks ou Logic Apps.

## 🔗 Links Úteis

- [Azure Monitor Overview](https://learn.microsoft.com/azure/azure-monitor/overview)
- [Activity Log Alerts](https://learn.microsoft.com/azure/azure-monitor/alerts/activity-log-alerts)
- [Log Analytics](https://learn.microsoft.com/azure/azure-monitor/logs/log-analytics-overview)
- [Kusto Query Language (KQL)](https://learn.microsoft.com/azure/data-explorer/kusto/query/)
- [Documentação Azure CLI](https://learn.microsoft.com/cli/azure/monitor)
- [Azure Resource Manager (ARM) Templates](https://learn.microsoft.com/azure/azure-resource-manager/templates/overview)
- [Azure Pricing Calculator](https://azure.microsoft.com/pricing/calculator/)

## ✅ Status do Projeto

| Item                           | Status      |
|--------------------------------|-------------|
| Curso assistido                | ✅ Concluído |
| Laboratório executado          | ✅ Concluído |
| Configuração de monitoramento  | ✅ Concluída |
| Testes de alertas              | ✅ Realizados |
| Documentação criada            | ✅ Concluída |
| Repositório público no GitHub | ✅ Concluído |
