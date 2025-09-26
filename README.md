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

1. O que será realizado?
Será criada uma fila Amazon SQS que receberá mensagens enviadas por um Amazon EventBridge e que serão consumidas por uma função AWS Lambda. Essa fila fará parte do fluxo de disponibilização sistêmica das mensagens de atualização de boletas de empréstimo de ativos no tópico Kafka.

⸻

2. Qual é o objetivo?
O objetivo é implementar uma fila intermediária para organizar e disponibilizar mensagens de atualização de boletas de empréstimo de ativos, garantindo que elas sejam processadas pela Lambda e posteriormente encaminhadas ao tópico Kafka. Isso promove maior confiabilidade e controle no fluxo de mensagens.

⸻

3. Tem algum risco?
Não. A fila será criada como uma nova peça no ambiente e não possui dependência com recursos já existentes, portanto não há risco de impacto em produção.


1. O que será realizado?
Será criada uma fila Amazon SQS que receberá mensagens enviadas por uma AWS Step Function e que serão consumidas por uma função AWS Lambda. Essa fila fará parte do fluxo de disponibilização sistêmica das mensagens de atualização de boletas de empréstimo de ativos no tópico Kafka.

⸻

2. Qual é o objetivo?
O objetivo é implementar uma fila intermediária para organizar e disponibilizar mensagens de atualização de boletas de empréstimo de ativos, garantindo que elas sejam processadas pela Lambda e posteriormente encaminhadas ao tópico Kafka. Isso aumenta a confiabilidade e a escalabilidade no tratamento das mensagens.

⸻

3. Tem algum risco?
Não. A fila será criada como uma nova peça no ambiente e não possui dependência com recursos já existentes, portanto não há risco de impacto em produção.

1. O que será realizado?
Será criada uma AWS Step Function que receberá mensagens de uma fila Amazon SQS no formato padrão INOA e as enviará, após formatação, para outra fila SQS. Esse processo faz parte do fluxo de disponibilização sistêmica das mensagens de atualização de boletas de empréstimo de ativos no tópico Kafka.

⸻

2. Qual é o objetivo?
O objetivo é orquestrar o tratamento e a transformação das mensagens recebidas no padrão INOA, garantindo que sejam encaminhadas para outra fila SQS no formato adequado. Dessa forma, assegura-se que as mensagens sigam corretamente o fluxo sistêmico até sua disponibilização no tópico Kafka.

⸻

3. Tem algum risco?
Não. A Step Function será criada como uma nova peça no ambiente, sem dependências com recursos existentes, portanto não há risco de impacto no ambiente produtivo.


1. O que será realizado?
Será criada uma função AWS Lambda que receberá mensagens de uma fila Amazon SQS e as enviará para um tópico Kafka, utilizando o schema Avro definido. A Lambda receberá como parâmetros o tópico, o schema e o apontamento do Kafka. Esse processo faz parte do fluxo de disponibilização sistêmica das mensagens de atualização de boletas de empréstimo de ativos no tópico Kafka.

⸻

2. Qual é o objetivo?
O objetivo é implementar uma Lambda capaz de consumir mensagens do SQS, adequá-las ao schema Avro definido e publicá-las em um tópico Kafka. Essa função garante a padronização dos dados e a correta disponibilização sistêmica das mensagens de atualização de boletas de empréstimo de ativos.

⸻

3. Tem algum risco?
Não. A Lambda será criada como uma nova peça no ambiente, sem dependências com recursos já existentes, portanto não há risco de impacto no ambiente produtivo.


1. O que será realizado?
Será realizado um ajuste em um valor armazenado em um AWS Secrets Manager. O secret guarda as credenciais do usuário produtor de um tópico Kafka, e a alteração consistirá em ajustar o valor do usuário de hx80001 para HX80001.

⸻

2. Qual é o objetivo?
O objetivo é corrigir a informação armazenada no secret, garantindo que o valor do usuário produtor do tópico Kafka esteja conforme o padrão esperado e devidamente padronizado.

⸻

3. Tem algum risco?
Não. O secret em questão não é utilizado atualmente por nenhum recurso, portanto a alteração pode ser feita sem risco de impacto no ambiente produtivo.
