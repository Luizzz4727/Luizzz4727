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
Será realizada a criação de IAM Policies personalizadas na AWS, definindo permissões específicas para recursos como AWS Lambda, S3 Buckets, entre outros serviços. Em seguida, serão criadas IAM Roles com essas policies associadas, possibilitando que essas roles sejam atribuídas a serviços que necessitem de permissões controladas para executar suas funções.

⸻

2. Qual é o objetivo?
O objetivo é garantir que os serviços da AWS, como funções Lambda, buckets S3, entre outros, possuam as permissões adequadas e restritas conforme suas necessidades operacionais.

3. Tem algum risco?
Neste caso específico, não. As roles e policies criadas ainda não estão em uso e não serão vinculadas a nenhum recurso em produção neste momento. Portanto, não há risco de impacto no ambiente produtivo durante a criação ou modificação dessas permissões.


1. O que será realizado?
Será criada uma função AWS Lambda que atuará como destino de eventos gerados por alarmes do Amazon CloudWatch. Esses alarmes, ao serem disparados, enviarão eventos para o Amazon EventBridge, que, por sua vez, encaminhará essas mensagens para a função Lambda. A Lambda terá a responsabilidade de processar os eventos recebidos e repassar os alarmes para um sistema externo.

⸻

2. Qual é o objetivo?
O objetivo é implementar uma integração automatizada que permita que alarmes do CloudWatch sejam encaminhados de forma eficiente para outro sistema por meio de uma função Lambda. Essa solução facilita a comunicação entre os serviços da AWS e sistemas externos, possibilitando ações corretivas, notificações ou monitoramento avançado com base nos eventos gerados na nuvem.

⸻

3. Tem algum risco?
Neste caso, não. A função Lambda será nova, não estará vinculada a recursos existentes em produção e não impacta diretamente o ambiente produtivo. Portanto, sua criação e configuração podem ser realizadas sem risco de interferência em sistemas críticos ou em operação.


1. O que será realizado?
Serão criados monitores no Datadog para receber e processar os alarmes provenientes de serviços da AWS monitorados pelo Amazon CloudWatch. Os monitores serão configurados com diferentes níveis de severidade e, ao atenderem às condições definidas, irão gerar incidentes automaticamente dentro do Datadog para facilitar o acompanhamento e a resposta a falhas.

⸻

2. Qual é o objetivo?
O objetivo é centralizar e estruturar o monitoramento dos recursos da AWS no Datadog, categorizando os alertas por severidade e gerando incidentes automaticamente quando necessário. Isso melhora a visibilidade dos eventos críticos, agiliza o tempo de resposta e fortalece a observabilidade da infraestrutura de forma proativa.

⸻

3. Tem algum risco?
Não. A criação dos monitores é uma adição nova ao ambiente de monitoramento e não afeta sistemas ou componentes já existentes.
