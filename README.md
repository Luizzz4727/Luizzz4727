### Hi there 👋

<!--
**Luizzz4727/Luizzz4727** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

Tabela AWS Glue

1. O que será realizado?
Será criada e catalogada a tabela "NOME DA TABELA" no AWS Glue, registrada no banco de dados SOR da conta AWS. Essa tabela será utilizada para armazenar dados destinados ao data mesh, permitindo integração e consulta centralizada dos dados "DESCREVER fluxo" dentro do ecossistema da AWS.

2. Qual é o objetivo?
O objetivo é disponibilizar uma estrutura de armazenamento e catalogação de dados no AWS Glue que facilite a gestão, descoberta e integração dos dados no data mesh, garantindo organização e acessibilidade para consumo por diferentes áreas e serviços.

3. Tem algum risco?
Não. A criação e catalogação da tabela no AWS Glue é uma operação isolada, não afeta recursos existentes e não interfere em sistemas de produção. Trata-se de uma nova estrutura que será incorporada ao ambiente sem impacto operacional.

EventBridge e Step Function

1. O que será realizado?
Será criado um Amazon EventBridge e uma AWS Step Function. O EventBridge com o barramento "Liquidacao" receberá mensagens da Lambda "recebekafka", no padrão definido pelo "COLOCAR NOME DO SISTEMA", e atendendo os critérios da regra "NOME DA REGRA" criada neste barramento, encaminhará essas mensagens para uma fila SQS "democratizacao-de-para". A Step Function "NOME STEP" será executada pela Lambda "envio-de-para" que enviará um payload de entrada seguindo o mesmo padrão, e ela fará o tratamento necessário para ajustar a mensagem ao formato adequado para inserção no data mesh.

2. Qual é o objetivo?
O objetivo é implementar um fluxo de processamento que permita a integração de mensagens oriundas do "COLOCAR NOME DO SISTEMA", adaptando-as para o formato esperado pelo data mesh. Essa arquitetura facilita a ingestão de dados padronizados, assegurando compatibilidade e qualidade antes do armazenamento e uso no ambiente de dados.

3. Tem algum risco?
Não. Tanto o EventBridge quanto a Step Function serão criados em um ambiente não produtivo. Por serem peças novas, não há risco de impacto em sistemas em produção.

Lambda Democratização

1. O que será realizado?
Será criada uma função AWS Lambda "democratizacao" para consumir mensagens da fila Amazon SQS "democratizacao", converter o conteúdo dessas mensagens, que vem no formato JSON, para o formato Parquet e inserir os arquivos resultantes no bucket SOR. Esses dados inseridos poderão ser visualizados por meio da tabela "NOME DA TABELA" vinculada ao data mesh.

2. Qual é o objetivo?
O objetivo é automatizar o processo de ingestão e transformação de dados recebidos via SQS, garantindo que sejam armazenados no formato Parquet no bucket SOR, de forma que possam ser facilmente consultados e utilizados no data mesh. Isso otimiza o desempenho de consultas e mantém a padronização dos dados.

3. Tem algum risco?
Não. A Lambda será uma nova implementação, em um ambiente não produtivo. A operação será feita em ambiente controlado, sem risco de impacto no ambiente.
