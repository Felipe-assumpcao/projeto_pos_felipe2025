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

![Imagem do WhatsApp de 2025-10-24 à(s) 17 51 15_8aefa959](https://github.com/user-attachments/assets/261637d7-8db3-43b4-8118-116233b9b307)

Aqui estão exemplos dos retornos da API após a execução.

![Imagem do WhatsApp de 2025-10-24 à(s) 17 51 15_7ab9dbed](https://github.com/user-attachments/assets/01ad32be-ef6b-4f8c-a9dd-b55fc848a23c)

Documentação Interativa (/docs)

![Imagem do WhatsApp de 2025-10-24 à(s) 17 51 16_709ba894](https://github.com/user-attachments/assets/3d53f7db-8fd9-4b4e-95f4-42a957c59814)

Retorno do Endpoint (/stats)


![Imagem do WhatsApp de 2025-10-24 à(s) 17 51 16_266f54b9](https://github.com/user-attachments/assets/8c039809-9be3-45e4-9b4d-5211e65b51b2)



{
