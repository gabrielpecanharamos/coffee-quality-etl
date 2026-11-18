# coffee-quality-etl 

Este é um projeto de ETL completo, projetado para execução simples e direta, focado em transformar dados brutos em dados estruturados para análise.

O script `main.py` extrai e limpa os dados brutos em CSV, conecta-se ao **Microsoft SQL Server**, cria automaticamente a base de dados `dados_cafe` (caso ainda não exista) e estrutura as tabelas.

**Atenção:** Os ficheiros arabica_data.csv e robusta_data.csv devem estar guardados na mesma pasta dos scripts Python para que a execução funcione corretamente.

- **Consultas SQL (`queries.sql`):** Script contendo as queries de agregação, filtros de qualidade, comparações de altitude e rankings dos lotes (*Arábica* e *Robusta*).
- **Dashboard Interativo:** A camada de visualização deste projeto foi isolada em um repositório próprio, contendo o painel interativo e os prompts utilizados na sua construção:
- **[Repositório do Dashboard](https://github.com/gabrielpecanharamos/coffee-quality-dashboard)**

## Estrutura do Projeto

O repositório adota uma estrutura plana para garantir que pode abrir o VS Code e rodar os scripts imediatamente sem se preocupar com imports complexos de pastas:

```text
coffee-quality-etl/
├── arabica_data.csv        # Dados brutos de cafés Arábica
├── robusta_data.csv        # Dados brutos de cafés Robusta
├── main.py                 # Script ETL para carregar no SQL Server
├── queries.sql             # Queries SQL para análises e agregações
├── requirements.txt        # Bibliotecas necessárias
├── .gitattributes          # Configuração de linguagens no GitHub
└── README.md               # Documentação do projeto