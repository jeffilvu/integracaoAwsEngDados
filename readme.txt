## Resumo do Projeto: Integração e Gerenciamento de Dados AWS

Este projeto demonstra a construção de um pipeline de ingestão e gerenciamento de dados utilizando serviços da Amazon Web Services (AWS) e Python, com foco em armazenamento de imagens e persistência de metadados em um banco de dados relacional. As principais etapas e tecnologias incluem:

*   **Configuração e Segurança**: Utilização de variáveis de ambiente e gerenciamento de segredos via `google.colab.userdata` para armazenar credenciais de forma segura (AWS Access Keys, credenciais de banco de dados).
*   **Banco de Dados na AWS (PostgreSQL)**: Conexão e manipulação de um banco de dados PostgreSQL (presumivelmente AWS RDS) para criar e gerenciar a estrutura de dados. Foi criada uma base de dados `inventario` e uma tabela `ARQUIVOS` para armazenar metadados de arquivos.
*   **Armazenamento de Objetos na AWS (S3)**: Interação com o Amazon S3 para listar e processar arquivos de imagem. A biblioteca `boto3` foi utilizada para conectar-se a um bucket S3 específico (`imagensengdados777`) e filtrar arquivos por prefixo e extensão (`.jpg`).
*   **Ingestão de Dados Inteligente**: Implementação de lógica para evitar duplicidade, verificando se os nomes dos arquivos já existiam no banco de dados antes de inseri-los. Um ID incremental foi atribuído a cada novo arquivo inserido.
*   **Verificação e Validação**: Após a ingestão, o projeto incluiu passos para consultar e exibir os dados inseridos no banco de dados, garantindo a integridade e sucesso da operação.

**Tecnologias Utilizadas**:
*   **Cloud**: AWS S3, AWS RDS (PostgreSQL)
*   **Linguagem de Programação**: Python
*   **Bibliotecas Python**: `boto3`, `psycopg2`
*   **Ambiente**: Google Colab para desenvolvimento e execução.
