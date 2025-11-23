# 🧑‍💼 AskHR

<img alt="AskHR" src="assets/hr_landscape.jpg">

Um dos grandes desafios para qualquer organização é gerenciar as operações de RH. Conforme a empresa cresce, fica cada vez mais difícil acessar informações rapidamente e executar tarefas com facilidade.

Com a chegada dos sistemas baseados em agentes e o poder dos modelos de raciocínio, isso muda: <b>Agora é possível ter um único ponto de acesso para realizar praticamente todas as operações de RH de forma simples e integrada. </b>

## 🤔 O Problema

A <b>TechCorp Inc.</b>, líder global em tecnologia com mais de 100 mil colaboradores, enfrentava um grande desafio na gestão das operações de RH. Com o crescimento acelerado, ficou cada vez mais difícil lidar com dados de perfil, solicitações de férias e gestão da força de trabalho de forma eficiente. 

Os sistemas tradicionais já não davam conta da escala e da complexidade. Além disso, diferentes ferramentas de fornecedores eram usadas para tarefas específicas, tornando a integração complicada e prejudicando a experiência do usuário.

## 🎯 Objetivo

Com este caso de uso, vamos enfrentar o desafio adotando uma plataforma empresarial: <b>watsonx Orchestrate</b>, com recursos de agentes inteligentes e ferrammentas e integrações pdoerosas.

Neste laboratório, você vai ver como as ferramentas pré construídas do <b>watsonx Orchestrate</b> podem se integrar a sistemas de gestão de RH¹ podem permitir a criação de ferramentas personalizadas para conectar facilmente esses sistemas.

Com insights orientados por agentes, vamos ajudar a TechCorp a acelerar a busca por informações, reduzir tarefas administrativas e tornar a gestão da força de trabalho muito mais eficiente.

¹ O Watsonx Orchestrate é compatível com sistemas externos como Workday e SuccessFactors, Service Now, SalesForce. [Clique aqui](https://www.ibm.com/br-pt/products/watsonx-orchestrate/integrations) para saber mais

## 📈 Valor de Negócio

Usar um sistema com suporte de IA para otimizar processos de RH pode gerar impactos em várias frentes: redução do tempo de resposta, maior satisfação dos usuários, aumento da produtividade e até diminuição da sobrecarga dos colaboradores. Tudo isso contribui para agregar valor ao negócio.

Além disso, aproveitar as capacidades de agentes traz benefícios adicionais, como mais segurança nos dados e respostas mais precisas, sem riscos de alucinação, garantindo uma experiência confiável e fortalecendo a imagem da marca.

## Arquitetura

Para simplificar a interação dos colaboradores com os sistemas de RH, criamos o AskHR, um agente inteligente desenvolvido com o IBM watsonx. Essa solução utiliza um modelo de orquestração multiagente, garantindo raciocínio avançado, execução fluida de ações e uma experiência ágil para os usuários.

A arquitetura é baseada no <b>watsonx Orchestrate</b>, permitindo que o agente gerencie uma ampla variedade de consultas e solicitações de RH de forma eficiente e integrada.

#### Capacidades principais do agente AskHR:

1. Automatizar tarefas rotineiras de RH, como consultar saldo de férias, solicitar folgas e atualizar dados dos colaboradores.

2. Oferecer uma experiência simples e intuitiva, permitindo que os funcionários interajam com os sistemas de RH por meio de uma interface amigável.

3. Garantir segurança e precisão, usando raciocínio avançado e ferramentas para buscar ou atualizar informações de forma confiável.

4. Integra-se facilmente aos sistemas internos, utilizando conectores OpenAPI para uma conexão sem complicações.

5. Aproveitar o poder do watsonx Orchestrate, coordenando fluxos, raciocínio inteligente e tarefas web para oferecer uma experiência completa de RH com IA.

<img alt="AskHR" src="assets/arch_diagm.png">

### Componentes da Arquitetura

- **Agente de RH e Aplicativo (IBM watsonx Orchestrate)**: O agente de RH atua como o orquestrador central, gerenciando as interações com o usuário e delegando tarefas para as ferramentas apropriadas no aplicativo de RH.

Ele possui uma coleção de ferramentas reutilizáveis, um agente RAG alimentado por OpenAPI e descrições de metadados. Cada ferramenta é projetada para executar uma tarefa específica relacionada a RH, como:  
Verificação de saldos de folgas  
Envio de solicitações de folga  
Atualização de dados pessoais (cargo, endereço residencial)

O agente RAG recupera informações relevantes de documentos para responder às consultas dos usuários.

- **Sistema de Gestão de Capital Humano (HCM)**: O aplicativo de RH se comunica com o sistema HCM subjacente para buscar ou atualizar dados dos funcionários, garantindo sincronização e precisão em tempo real.

## 🎥 Demonstração
[▶️ Assistir à demonstração do Ask HR](https://bucket-wxo.s3.us-south.cloud-object-storage.appdomain.cloud/ashHR_demo_new_version.mp4)

> [!IMPORTANTE]  
> Este laboratório usa um simulador para um sistema de Gestão de Capital Humano. No entanto, isso pode ser facilmente substituído por qualquer sistema real em produção, como Workday ou outros.

## 📄 Laboratório prático passo a passo

Por favor, veja as instruções passo a passo [aqui](assets/hands-on-lab-askHR.md) sobre como você pode implementar este caso de uso.
