# santanderbootcamp2025
Projeto desenvolvido durante a Santander BootCamp 2025, focado na criação de um pipeline ETL (Extract, Transform, Load) para geração de mensagens personalizadas de Pipeline ETL com IA.

Projeto desenvolvido durante a Santander BootCamp 2025, focado na criação de um pipeline ETL (Extract, Transform, Load) para geração de mensagens personalizadas de marketing bancário utilizando Inteligência Artificial.

## Objetivo

Criar mensagens de marketing personalizadas para clientes do Santander, enfatizando a importância dos investimentos, através de um processo automatizado de ETL integrado com IA Generativa.

## Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** - Manipulação e análise de dados
- **Google Generative AI (Gemini)** - Geração de conteúdo com IA
- **CSV** - Formato de entrada e saída de dados

## Estrutura do Projeto

### 1. Extract (Extração)
- Leitura de arquivo CSV contendo IDs e informações dos usuários
- Conversão dos dados para estrutura manipulável (lista de dicionários)
- Preparação da estrutura para receber as mensagens geradas

### 2. Transform (Transformação)
- Integração com API do Google Gemini (IA Generativa)
- Geração de mensagens personalizadas para cada cliente
- Validação e tratamento de erros nas requisições
- Limitação de caracteres conforme requisitos (máximo 100 caracteres)

### 3. Load (Carregamento)
- Consolidação dos dados processados
- Exportação para arquivo CSV com mensagens personalizadas
- Visualização dos resultados finais

## Como Executar

### Pré-requisitos
```bash
pip install pandas google-generativeai
```

### Configuração

1. Obtenha sua API Key do Google AI Studio: [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)

2. Configure a chave no código:
```python
genai.configure(api_key="SUA_CHAVE_AQUI")
```

3. Prepare o arquivo `SDW2025.csv` com a estrutura:
```csv
UserID,Name,Account
1,João Silva,12345
2,Maria Santos,67890
```

### Execução
```[python](https://colab.research.google.com/)
SantanderDevWeek2026.ipynb
```

## Resultados

O projeto gera um arquivo `campanha_marketing_santander.csv` contendo:
- ID do usuário
- Nome
- Conta
- Mensagem personalizada de marketing

## Observações Importantes

- A API original do projeto (`sdw-2023-prd.up.railway.app`) foi descontinuada e por esse motivo avançamos sem ela
- O foco do projeto é demonstrar o fluxo completo de ETL
- A geração de mensagens pode ser substituída por templates caso a API não esteja disponível
- Rate limiting implementado (1.5s entre requisições) para respeitar limites da API gratuita

## Estrutura de Arquivos
```
santanderbootcamp2025/
│
├── SDW2025.csv                           # Arquivo de entrada
├── SantanderDevWeek2026.ipynb            # Arquivo principal
├── campanha_marketing_santander.csv      # Arquivo de saída
└── README.md                             # Documentação
```

## Aprendizados

- Implementação de pipeline ETL completo
- Integração com APIs de IA Generativa
- Manipulação de dados com Pandas
- Tratamento de erros e validações
- Boas práticas em automação de processos

## Autor

**Bruno Pereira**

LinkedIn: [https://www.linkedin.com/in/brunocdpereira/](https://www.linkedin.com/in/brunocdpereira/)

## Agradecimentos

Agradeço à Digital Innovation One (DIO) e ao Santander pela oportunidade de participar deste desafio e aprimorar conhecimentos em Ciência de Dados, Python, API e Inteligência Artificial.

## Licença

Este projeto foi desenvolvido para fins educacionais durante a Santander BootCamp 2025.
