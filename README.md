# 📡 Ferramentas de Monitoramento (AZ-900)

**Resumo das capacidades do Assistente do Azure, Integridade do Serviço do Azure e Azure Monitor (Log Analytics, Alertas, Application Insights).**

---

## 🧭 Visão geral rápida
| Ferramenta | Finalidade | Quando usar |
|---|---|---|
| **Assistente do Azure (Azure Advisor)** | Recomendações proativas de **custo**, **segurança**, **confiabilidade**, **desempenho** e **excelência operacional** | Otimizar ambiente e reduzir desperdícios |
| **Integridade do Serviço do Azure (Service Health)** | Status e incidentes **do serviço da Microsoft** que impactam seus recursos | Entender interrupções regionais/serviço, RCA e alertas |
| **Azure Monitor** | Plataforma unificada para **métricas**, **logs**, **traces** e **alertas** | Observabilidade ponta a ponta de apps e infra |
| **Log Analytics (KQL)** | Consulta e análise de **logs** no **Workspace** | Investigar, correlacionar eventos e criar insights |
| **Alertas do Azure Monitor** | Regras sobre **métricas/logs/atividade** com ações automatizadas | Resposta rápida a desvios e SRE/operacional |
| **Application Insights** | APM: **telemetria de app**, **distribuição de traces**, **mapa de dependências**, **falhas** | Monitorar performance e experiência do usuário |

---

## 🧠 Assistente do Azure (Azure Advisor)
- Recomendações personalizadas por **assinatura** e **recurso**, categorizadas em:
  - **Custo** (direciona para reservas/savings plans, rightsizing de VMs).  
  - **Confiabilidade** (alta disponibilidade, Zonas/pares de região).  
  - **Segurança** (integração com Defender/segurança básica).  
  - **Desempenho** (SKUs, IOPS, consultas lentas).  
  - **Excelência Operacional** (práticas de governança).  
- Exportável e **integrável** a rotinas de governança/FinOps.

---

## 🩺 Integridade do Serviço do Azure (Service Health)
- **Service Issues**: incidentes em andamento;  
- **Planned Maintenance**: janelas de manutenção programada;  
- **Health Advisory**: comunicações importantes (mudanças, depreciações);  
- **Resource Health**: estado **específico do seu recurso** (disponível/degradado).  
- Configure **alertas** para ser notificado por e-mail/webhook/ITSM.

---

## 📊 Azure Monitor — plataforma de observabilidade
- **Fontes de dados**: métricas de plataforma, logs de atividade, **diagnósticos**, agentes em VM/Kubernetes, Application Insights.  
- **Armazenamento**: **Log Analytics Workspace** para logs; retenção e custo configuráveis.  
- **Visualização**: Dashboards, Workbooks, Métricas, Mapas de dependência.  
- **Automação**: Alertas + **Action Groups** (e-mail, SMS, webhook, ITSM, runbooks, Functions).

### 🔎 Log Analytics (KQL)
- Workspaces centralizam logs (ex.: `AzureDiagnostics`, `AppTraces`, `Heartbeat`).  
- **KQL** para consultas, correlação temporal e criação de **alertas** e **workbooks**.

### 🚨 Alertas do Azure Monitor
- Tipos: **métricas**, **logs (KQL)**, **atividade**, **service health**, **application insights**.  
- **Action Groups**: defina destinos e ações (notificação/automação).  
- **SLA operacional**: ajuste severidade, frequência e supressão.

### 🧩 Application Insights (APM)
- **Distribuição de traces**, **mapa de dependências**, **falhas e exceções**, **User/Session/Events**.  
- **Transações ponta a ponta** (correlação) e **amostragem** para controle de custo.  
- Indicadores: **Disponibilidade**, **Tempo de resposta**, **Taxa de erros**, **Satisfação**.

---

## 🔁 Boas práticas de monitoramento
- **Padronize** coleta (agent/diagnostics) por **Policy** e **templates** (Bicep/ARM).  
- **Separe** workspaces por ambiente (`dev/test/prod`) com **naming** e **tags** consistentes.  
- **Colete o necessário** (métricas essenciais, logs críticos) para **otimizar custos**.  
- **Crie alertas acionáveis** (runbooks/Functions) e evite **alert fatigue**.  
- **Dashboards/Workbooks** por público: SRE, Dev, Negócio.

---

## ✅ Recapitulando (o que você precisa saber)
- **Assistente do Azure**: recomendações práticas para melhorar custo, segurança e desempenho.  
- **Integridade do Serviço**: visibilidade de incidentes/saúde do **serviço** e do **seu recurso**.  
- **Azure Monitor**: telemetria unificada; use **Log Analytics** (KQL), **Alertas** e **Application Insights** para observabilidade completa.

