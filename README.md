# 📊 Dashboard Gestão à Vista

Dashboard profissional de indicadores operacionais com atualização automática via GitHub + Vercel.

## 🌐 Acesso Online

> **Seu dashboard:** `https://SEU-PROJETO.vercel.app`

---

## 📁 Estrutura de Arquivos

```
📂 seu-repositorio/
├── index.html              ← Dashboard principal (abrir no navegador)
├── dashboard_data.json     ← Dados dos indicadores (ATUALIZAR ESTE!)
├── export_dashboard.py     ← Script Python para gerar o JSON da planilha
└── README.md               ← Este arquivo
```

---

## 🔄 Como Atualizar os Dados (Passo a Passo)

### Você vai precisar de:
- [Python 3](https://www.python.org/downloads/) instalado no computador
- [GitHub Desktop](https://desktop.github.com/) (versão gráfica, sem precisar de comandos)
- Sua planilha Excel (`Indicadores_Gestao_a_Vista_v11.xlsx`)

---

### Passo 1 — Preencha a planilha normalmente
Abra o Excel e adicione os novos lançamentos na aba `FATO_Lancamentos`.

---

### Passo 2 — Gere o arquivo JSON

Abra o **Terminal** (Windows: Prompt de Comando ou PowerShell) na pasta do projeto e execute:

```bash
python export_dashboard.py Indicadores_Gestao_a_Vista_v11.xlsx
```

Isso vai gerar/atualizar o arquivo `dashboard_data.json`.

---

### Passo 3 — Envie para o GitHub com o GitHub Desktop

1. Abra o **GitHub Desktop**
2. Você verá o arquivo `dashboard_data.json` como "modificado"
3. Escreva uma mensagem (ex: `Atualização março 2026`)
4. Clique em **"Commit to main"**
5. Clique em **"Push origin"**

---

### Passo 4 — Vercel atualiza automaticamente 🎉

O **Vercel** detecta o push e em ~30 segundos seu dashboard online já está atualizado!

---

## ⚡ Configuração Inicial no Vercel (só uma vez)

1. Acesse [vercel.com](https://vercel.com) e faça login com sua conta GitHub
2. Clique em **"Add New Project"**
3. Selecione este repositório
4. Clique em **"Deploy"** — pronto!
5. Copie a URL gerada (ex: `https://dashboard-gestao.vercel.app`)

---

## 🖥️ Para exibir nos monitores

1. Abra a URL do Vercel no navegador do monitor
2. Pressione **F11** para tela cheia
3. Clique em **▶ Auto-Rotação** para rotacionar automaticamente entre as visões

---

## 📋 Visões do Dashboard

| Aba | Responsável | Indicadores |
|-----|-------------|-------------|
| 🎯 Gerencial | Evelyn | KPIs estratégicos, CSAT, Custos |
| 🎧 Atendimento | Alan | SLAs, Tickets, Resolução 1º contato |
| ⚙️ Op. Serviços | Jonathan | SLA Diários, Novas Ações, Andamentos |
| 🏗️ Op. Meridio | Rodrigo | Implantações, Clientes, Cancelamentos |
| 📊 Tático | Múltiplos | Indicadores operacionais por sub-área |

---

## 🆘 Suporte

Em caso de dúvidas, verifique:
- Se o arquivo `dashboard_data.json` foi gerado corretamente (deve ter mais de 1KB)
- Se o Python está instalado: `python --version`
- Se o `openpyxl` está instalado: `pip install openpyxl`
