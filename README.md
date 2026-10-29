# 📊 🐍 Projetos em Python: Análise de Churn & Automação RPA

Este repositório reúne duas soluções em Python voltadas para a otimização de processos de negócios e análise de dados: uma **Análise Exploratória de Cancelamento de Clientes (Churn)** e uma **Automação de Leitura, Tratamento e Cadastro em Lote (RPA)**.

---

## 📌 Visão Geral do Repositório

1. **Análise de Churn**: Diagnóstico estatístico e comportamental dos fatores que causam a perda de clientes em uma base de mais de 800 mil usuários, visando propor ações de retenção.
2. **Automação RPA**: Solução de automação para leitura de ficheiros/planilhas, limpeza de dados com Pandas e inserção automática de produtos em sistemas corporativos utilizando PyAutoGUI.

---

## 📊 Projeto 1: Análise de Cancelamento de Clientes (Churn Analysis)

### 🎯 Problema e Objetivo
A empresa identificou uma taxa elevada de clientes inativos na sua base. Utilizando Pandas e Plotly, os dados foram tratados e analisados para identificar os gargalos operacionais e contratuais que impulsionam o cancelamento.

### 💡 Principais Insights Obtidos
* **Contratos Mensais**: Clientes no plano de assinatura mensal apresentaram taxa de cancelamento próxima de 100%. *Recomendação: incentivar a transição para planos anuais ou trimestrais via descontos.*
* **Atendimento ao Cliente (Call Center)**: Clientes que realizaram mais de 4 ligações para o suporte cancelaram o serviço. *Recomendação: criar alertas de atendimento prioritário para clientes que atingirem 3 chamados.*
* **Atraso no Pagamento**: Clientes com mais de 20 dias de atraso cancelaram invariavelmente. *Recomendação: estruturar réguas de cobrança preventiva e renegociação aos 10 dias de atraso.*

### 🔄 Etapas da Análise
1. **Importação**: Carregamento da base `cancelamentos.csv`.
2. **Limpeza de Dados**: Remoção do identificador único (`CustomerID`) e eliminação de valores nulos (`NaN`).
3. **Análise de Churn**: Cálculo da taxa percentual e absoluta de cancelamentos.
4. **Diagnóstico Visual**: Geração de histogramas interativos relacionando variáveis comportamentais ao status de cancelamento.

---

## 🤖 Projeto 2: Automação de Leitura, Tratamento e Cadastro (RPA)

### 🎯 Problema de Negócio e Impacto
A inserção manual de cadastros em sistemas legados é repetitiva, sujeita a erros operacionais e consome horas das equipes de operações. Esta solução resolve o problema garantindo:
* **Economia de tempo**: Processamento e registo em lote de centenas de itens por minuto de forma autónoma.
* **Redução de erros**: Validação prévia de tipos de dados, campos obrigatórios e formatos antes da inserção no sistema.

### 🔄 Fluxo de Funcionamento
1. **Leitura e Extração**: O script carrega a base de dados de entrada (`.xlsx` ou `.csv`).
2. **Tratamento (ETL)**: O Pandas limpa valores nulos, formata colunas de preços/códigos e valida a integridade dos registos.
3. **Execução em Lote**: O PyAutoGUI navega pelos campos da interface corporativa, preenche os dados automaticamente e confirma o registo de cada item.
4. **Registo de Logs**: Geração de relatórios do estado de execução para acompanhamento de sucessos ou falhas.

---

## 🛠️ Tecnologias Utilizadas

* **Python 3.x**: Linguagem base para desenvolvimento do script e notebook.
* **Pandas**: Leitura, limpeza, tratamento (ETL) e agregação de dados.
* **Plotly**: Geração de gráficos interativos para visualização da análise de churn.
* **PyAutoGUI / Keyboard**: Simulação de interação humana na interface gráfica (GUI).
* **OpenPyXL / CSV**: Suporte para manipulação de ficheiros Excel e CSV.
* **Jupyter Notebook / VS Code**: Ambientes de desenvolvimento executáveis.

---

## 🚀 Como Executar os Projetos

### Pré-requisitos
Certifique-se de ter o Python 3.8+ instalado na sua máquina.

### 1. Clonar o repositório
```bash
git clone [https://github.com/Caioh06/automacao-cadastro-produtos-python.git](https://github.com/Caioh06/automacao-cadastro-produtos-python.git)
cd automacao-cadastro-produtos-python
```

### 2. Criar e ativar um ambiente virtual
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux/macOS
python3 -m venv venv
source venv/bin/activate
```

### 3. Instalar as dependências
```bash
pip install pandas plotly pyautogui openpyxl ipykernel nbformat
```

### 4. Execução dos Módulos

* **Para a Análise de Churn**:
  1. Abra o ambiente Jupyter: `jupyter lab`
  2. Execute o arquivo `Analise_Churn/analise_cancelamentos.ipynb`.

* **Para a Automação de Cadastro (RPA)**:
  1. Certifique-se de que a interface do sistema de destino está aberta no ecrã.
  2. Execute o script principal:
     ```bash
     python Automacao_RPA/automacao_cadastro.py
     ```
``GLOBAL_FOOTER``
