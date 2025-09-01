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

Envio da mensagem da Step Function para uma nova fila SQS

Eu como analista desejo adicionar um bloco de configuração na Step Function "sf-democratizacao" para que a mesma mensagem processada também seja enviada para uma nova fila SQS.


Criação da fila SQS envia-kafka

Eu como analista desejo criar uma fila SQS chamada "envia-kafka" que receberá mensagens da Step Function "sf-democratizacao" e enviará para a Lambda "envia-kafka"


Criação da Lambda envia-kafka

Eu como analista desejo criar uma Lambda chamada "envia-kafka" que receba mensagens da fila SQS "envia-kafka" e envie essas mensagens para um tópico Kafka.


Criação do tópico Kafka Avro

Eu como analista desejo criar um tópico Kafka em formato Avro chamado "custodia-de-mercado-de-capitais-avro-atualizacao-emprestimo-ativos-local" para armazenar as mensagens de atualização de boletas de empréstimo de ativos, tornando-as disponíveis para futuros consumidores.

