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
Será realizada a otimização e atualização de uma função AWS Lambda existente. A otimização visa melhorar o desempenho e tornar o processamento mais rápido, enquanto a atualização contemplará a versão do Python e das layers utilizadas pela função.

⸻

2. Qual é o objetivo?
O objetivo é modernizar e otimizar a Lambda, garantindo maior eficiência, desempenho aprimorado e compatibilidade com versões atualizadas de Python e bibliotecas, assegurando a manutenção e evolução adequada do código em produção.

⸻

3. Tem algum risco?
Sim. Como a Lambda em questão já está em uso em um sistema produtivo, existe risco de impacto caso ocorram falhas na atualização ou incompatibilidades com a nova versão de Python e das layers. É necessário realizar testes prévios e validações antes da implantação em produção para mitigar esses riscos.

1. O que será realizado?
Será realizada a atualização de uma função AWS Lambda que consome mensagens de uma fila Amazon SQS e as publica em um tópico Kafka. A atualização contemplará a versão do Python e as layers utilizadas pela Lambda.

⸻

2. Qual é o objetivo?
O objetivo é manter a Lambda atualizada e compatível com versões mais recentes de Python e de suas dependências, garantindo maior estabilidade, suporte e segurança, além de manter a função alinhada com as boas práticas de manutenção de código.

⸻

3. Tem algum risco?
Sim. Como a Lambda já está em uso em ambiente produtivo, existe risco de impacto no funcionamento do sistema caso ocorram falhas durante a atualização ou incompatibilidades com as novas versões do Python e das layers. Para mitigar o risco, é importante realizar testes prévios em ambiente controlado antes da implantação em produção.

1. O que será realizado?
Será criada uma fila Amazon MQ para receber mensagens que serão disparadas para uma função Lambda. Além disso, será criada uma regra no Amazon EventBridge para redirecionar mensagens para uma fila Amazon SQS, que também será criada nesse processo.

⸻

2. Qual é o objetivo?
O objetivo é implementar um fluxo de mensageria que permita a recepção, roteamento e processamento de mensagens, integrando MQ, EventBridge, SQS e Lambda. Essa arquitetura garante maior flexibilidade no tratamento de eventos e prepara a base para integrações futuras dentro do ambiente AWS.

⸻

3. Tem algum risco?
Sim. Apesar de a fila MQ, a regra do EventBridge e o SQS serem novos recursos, a implantação será realizada dentro de uma pipeline que também provisiona peças já utilizadas em produção. Dessa forma, há risco de impacto caso ocorra alguma falha ou erro durante a execução da pipeline.
