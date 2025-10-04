
# 🧑‍💼 AskHR: Automatize tarefas de RH com a IA da Agentic

## Índice

- [Descrição do caso de uso](#use-case-description)
- [Arquitetura](#Arquitetura)
- [Pre-requisitos](#pre-requisitos)
- [Instruções](#Instruções)
  - [Abrir Agent Builder](#abrir-agent-builder)
  - [Ciar Agente de RH](#criar-agente-de-rh)
  - [Teste o Agenre de RH em Preview](#teste-o-agente-de-rh-em-preview)
  - [Testar o Agente de RH no Chat](#testar-o-agente-de-rh-no-chat)
    
## Descrição do caso de uso
Este caso de uso visa desenvolver e implementar um agente AskHR utilizando o IBM Watsonx Orchestrate, conforme ilustrado no diagrama de arquitetura fornecido. Este agente capacitará os funcionários a interagir com os sistemas de RH e acessar informações de forma eficiente por meio de IA conversacional.

Neste laboratório, construiremos um agente de RH no Watsonx Orchestrate, utilizando ferramentas e conhecimento externo para se conectar a um Sistema de Gestão de Capital Humano simulado. Este agente recupera informações relevantes de documentos para responder às consultas dos usuários e permite que eles visualizem e gerenciem seus perfis.

## Arquitetura

<img width="1000" alt="image" src="arch_diagm.png">

## Pre-requisitos

- Verifique com seu instrutor se **todos os sistemas** estão funcionando antes de continuar.
- Confirme se você tem acesso ao ambiente techzone correto para este laboratório.
- Confirme que você fez o dowload do arquivo LABS.zip 


## Instruções:
### Abrir Agent Builder

- Faça login na IBM Cloud (cloud.ibm.com). Navegue até o menu hambúrguer no canto superior esquerdo, depois até Lista de Recursos. Abra a seção de IA/Machine Learning. Você deve ver um serviço **watsonx Orchestrate**, clique para abrir.

  <img width="1000" alt="image" src="../../../environment-setup/assets/cloud-resource-list.png">

- Clique no botão "Launch watsonx Orchestrate".

   <img width="1000" alt="image" src="../../../environment-setup/assets/cloud-wxo.png">

- Bem-vindo ao watsonx Orchestrate. Abra o menu hambúrguer, clique na seta para baixo ao lado de **Build**. Em seguida, clique em **Agent Builder**:

   <img width="1000" alt="image" src="hands-on-lab-assets/step_1_v2.png">

### Ciar Agente de RH
1. Clique em **Create agent +**:

<img width="1000" alt="image" src="hands-on-lab-assets/step_2_v2.png">

2. Selecione **Create from scratch**, de o nome ao seu agente, por exemplo, `Agente de RH`, e preencha o campo **Description** conforme mostrado abaixo:﻿

```
Você é um agente que lida com as dúvidas dos funcionários sobre RH. Você fornece respostas curtas e diretas, com no máximo 200 palavras ou menos. Você pode ajudar os usuários a verificar os seus dados do perfil, recuperar o saldo de folgas mais recente, atualizar cargo ou endereço e solicitar folgas. Você também pode responder a perguntas gerais sobre os benefícios da empresa.
```  
Clique em **Create**:

   <img width="1000" alt="image" src="hands-on-lab-assets/step_3_v2.png">


3. Selecione **Default** na seção **Agent style**.

   <img width="1000" alt="image" src="hands-on-lab-assets/step_5_v3.png">

4. Role a tela para baixo até a seção **Knowledge**. Clique em **Choose knowledge**.

<img width="1000" alt="image" src="hands-on-lab-assets/step_6_v3.png">

5. Clique em  **Upload files** e depois **Next**

<img width="1000" alt="image" src="hands-on-lab-assets/step_7_v3.png">

6. Clique e arraste o arquivo de Benefícios para funcionários (Arquivo "Employee-Benefits_ptbr.pdf" dentro da pasta "1. AskRH" gerada após descompactar o LABS.zip) e clique em **Next**:

<img width="1000" alt="image" src="hands-on-lab-assets/step_8_v3.png">  

7. Copie a seguinte descrição na seção **Description** e clique em **Save**:

```
Esta base de conhecimento aborda os benefícios dos funcionários da empresa, incluindo licenças-maternidade, política de animais de estimação, acordos de trabalho flexíveis e pagamento de empréstimos estudantis.
``` 

8. Role para baixo até a seção **Toolset**. Clique em **Add tool +**:

<img width="1000" alt="image" src="hands-on-lab-assets/step_9_v3.png">

9. Selecione **Add from file or MCP server**:

   <img width="1000" alt="image" src="hands-on-lab-assets/step_10_v4.png">

10. Selecione **Import from file**:

<img width="1000" alt="image" src="hands-on-lab-assets/step_11_v3.png">

11. Arraste e solte ou clique para carregar o arquivo **hr.yaml** (Arquivo "hr.yaml" dentro da pasta "1. AskRH" gerada após descompactar o LABS.zip) , então clique em **Next**:

   <img width="1000" alt="image" src="hands-on-lab-assets/step_12_v3.png">  

12. Selecione todas as operações e clique em **Done**:

   <img width="1000" alt="image" src="hands-on-lab-assets/step_13_v3.png">

13. Role para baixo até a seção **Behavior**. Insira as instruções abaixo no campo **Instructions**:

```
Use sua base de conhecimento para responder a perguntas gerais sobre benefícios para funcionários.

Use as ferramentas para obter ou atualizar informações específicas do usuário.

Quando o usuário solicitar a exibição de dados de perfil, a verificação do saldo de folgas, a atualização do cargo/endereço ou a solicitação de folga pela primeira vez, primeiro pergunte o nome do usuário, depois invoque a ferramenta e use o mesmo nome em toda a sessão, sem solicitá-lo novamente.

Quando o usuário solicitar folga, converta as datas para o formato AAAA-MM-DD. Por exemplo, 22/05/2025 deve ser convertido para 2025-05-22 antes de passar a data para a ferramenta post_request_time_off.
 ```

 <img width="1000" alt="image" src="hands-on-lab-assets/hr_step12.png">

14. Ative o botão de alternância para **Chat with documents**. Selecione **None** em **Citations show in webchat**. Ative o botão de **Show agent**. Clique em **Deploy** no canto superior direito para implantar seu agente:
   <img width="1000" alt="image" src="hands-on-lab-assets/step_14_v3.png">

### Teste o Agenre de RH em Preview
Teste seu agente no chat de pré-visualização à direita, fazendo as seguintes perguntas e validando as respostas. Elas devem ser semelhantes às mostradas nas capturas de tela abaixo:

> IMPORTANTE: Quando o agente perguntar seu nome você deve perguntar ao Agente de Suporte lá na página do git.

```
Qual é a política para animais de estimação? 
```
<img width="1000" alt="image" src="hands-on-lab-assets/hr_step13.png">

```
Mostrar os dados do meu perfil.
Gostaria de atualizar meu título. 
```
<img width="1000" alt="image" src="hands-on-lab-assets/hr_step13_2.png">

```
Atualize meu endereço.
Qual é o meu saldo de folgas?
```
<img width="1000" alt="image" src="hands-on-lab-assets/hr_step13_3.png">

```
Solicitar folgas.
Mostrar os dados do meu perfil.
```
<img width="1000" alt="image" src="hands-on-lab-assets/hr_step13_4.png">

#### Testar o Agente de RH no Chat
- Clique no menu de hambúrguer no canto superior esquerdo e depois clique em **Chat**:

<img width="1000" alt="image" src="hands-on-lab-assets/hr_step15.png">

- Certificar-se que o **HR Agent** está selecionado. Agora você pode testar seu agente (Pode repetir as mesmas perguntas do teste anterior)

<img width="1000" alt="image" src="hands-on-lab-assets/hr_step16.png">
