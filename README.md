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
Será criada uma função AWS Lambda chamada envia-kafka, que receberá por payload os dados referentes ao Kafka (como o apontamento e o tópico) e a mensagem que deverá ser enviada. A Lambda será genérica, permitindo o envio de mensagens para qualquer instância de Kafka.

⸻

2. Qual é o objetivo?
O objetivo é disponibilizar uma Lambda genérica que facilite a integração com diferentes instâncias de Kafka, garantindo flexibilidade no envio de mensagens e padronização no processo de comunicação entre sistemas.

⸻

3. Tem algum risco?
Não. A Lambda será criada em um ambiente não produtivo e não possui dependências com recursos já existentes, portanto pode ser implementada sem risco de impacto no ambiente produtivo.

1. O que será realizado?
Será criada uma implantação para ajustar o apontamento do servidor Kafka configurado em uma AWS Step Function, garantindo que o fluxo utilize o destino correto.

⸻

2. Qual é o objetivo?
O objetivo é corrigir o apontamento do servidor Kafka dentro da Step Function, assegurando que as mensagens sejam direcionadas ao servidor apropriado, mantendo a integridade do fluxo de processamento.

⸻

3. Tem algum risco?
Não. O ajuste será realizado em ambiente não produtivo e não possui dependência com recursos já existentes, portanto pode ser implementado sem risco de impacto no ambiente produtivo.









1. O que será realizado?
Será criada uma regra no barramento “Liquidacao” do Amazon EventBridge, chamada regra_envia_kafka. Essa regra terá a função de receber mensagens de atualização de empréstimo de ativos e direcioná-las para a fila Amazon SQS envia-Kafka-dê-para, dentro do fluxo de disponibilização sistêmica das mensagens no tópico Kafka.

⸻

2. Qual é o objetivo?
O objetivo é implementar uma regra de roteamento no EventBridge para garantir que mensagens de atualização de empréstimo de ativos sejam devidamente enviadas para o SQS responsável por integrá-las ao fluxo sistêmico e, posteriormente, ao tópico Kafka.

⸻

3. Tem algum risco?
Não. A regra será criada em um ambiente não produtivo e não possui dependência com recursos já existentes, portanto pode ser implementada sem risco de impacto no ambiente produtivo.

1. O que será realizado?
Será ajustada a regra “regra_123” no barramento Liquidacao do Amazon EventBridge, adicionando um campo no payload que informará o nome da Step Function a ser chamada na sequência do fluxo da democratização.

⸻

2. Qual é o objetivo?
O objetivo é enriquecer o payload enviado pela regra, permitindo que a Step Function correta seja identificada e executada no fluxo da democratização. Esse ajuste garante maior clareza e controle sobre a orquestração das etapas do processo.

⸻

3. Tem algum risco?
Sim. A alteração será feita em ambiente produtivo, o que traz risco de impacto. No entanto, o fluxo da democratização ainda não é amplamente utilizado e o ajuste já foi previamente testado, o que reduz significativamente a probabilidade de problemas.

1. O que será realizado?
Será ajustada a função AWS Lambda envio-de-para para torná-la genérica, permitindo que possa chamar qualquer Step Function. O nome da Step Function será capturado dinamicamente a partir de um parâmetro recebido no payload.

⸻

2. Qual é o objetivo?
O objetivo é flexibilizar a Lambda envio-de-para, de forma que ela não fique vinculada a uma única Step Function, mas possa orquestrar diferentes fluxos conforme o parâmetro informado no payload. Isso aumenta a reutilização e reduz a necessidade de múltiplas funções para a mesma finalidade.

⸻

3. Tem algum risco?
Sim. A alteração será feita em ambiente produtivo, o que traz risco de impacto. No entanto, o ajuste já foi testado previamente, o que reduz significativamente a probabilidade de falhas na execução.
