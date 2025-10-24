# projeto_pos_felipe2025

Estrutura de Arquivos

projeto_pos_felipe/
├── data/
│   └── dados.csv          
├── src/
│   ├── core/
│   │   ├── _init_.py
│   │   ├── metrics.py      # Função 'analisar' (FP)
│   │   └── models.py       # Classes POO (DataLoader, StatsService)
│   ├── _init_.py
│   ├── app.py              # API FastAPI
│   └── make_stats.py       # Script para gerar stats.json
├── ui/
│   └── app.py              # App Streamlit (Opcional)
├── requirements.txt
├── stats.json              # Gerado pelo 'make_stats.py'
└── README.md


Siga os passos abaixo para configurar e rodar a aplicação.

1. Pré-requisitos

Python 3.8 ou superior

pip (gerenciador de pacotes do Python)

2. Instalação

Primeiro, clone o repositório e navegue para a pasta do projeto. Em seguida, crie um ambiente virtual e instale as dependências:


python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

pip install -r requirements.txt


3. Gerar as Estatísticas

Antes de iniciar a API, você precisa gerar o arquivo stats.json. Este arquivo contém os cálculos feitos a partir do dados.csv.

Execute o seguinte comando na raiz do projeto:

python src/make_stats.py


Isso irá criar (ou sobrescrever) o arquivo src/stats.json com as estatísticas atualizadas.

4. Iniciar a API FastAPI

Com as estatísticas geradas, você pode iniciar o servidor da API.


uvicorn src.app:app --reload


A API estará disponível em http://127.0.0.1:8000.

5. Iniciar a Interface Streamlit (Opcional)

Para visualizar os dados de forma interativa, abra um novo terminal (mantendo a API rodando no primeiro) e execute a aplicação Streamlit:

streamlit run ui/app.py


A interface do Streamlit estará disponível em http://localhost:8501.

Screenshots da API

Aqui estão exemplos dos retornos da API após a execução.

(Adicione aqui ps prints do dashboard)

Documentação Interativa (/docs)

(Adicione aqui um print da sua tela mostrando a página /docs)

Retorno do Endpoint (/stats)


(Adicione aqui um print da sua tela mostrando o JSON de retorno do /stats)
![01](https://github.com/user-attachments/assets/0ef7cdb6-175f-49ca-bd4e-a151e0cc684a)
![02](https://github.com/user-attachments/assets/8866876d-36b4-4835-80c6-e07b23250d58)
![03](https://github.com/user-attachments/assets/e241a4c7-1537-421a-93c6-337e44da7fc5)
![04](https://github.com/user-attachments/assets/782bdb1b-a89e-48d0-8d81-85520aae8175)

{
