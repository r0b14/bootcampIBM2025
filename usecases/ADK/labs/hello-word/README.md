# 🤖✨ Watson Orchestrate — Tutorial "Hello World"

Bem-vindo ao seu primeiro tutorial com o **Watson Orchestrate**!  
Este README foi criado em estilo **colorido, educacional e interativo**, ideal para workshops, bootcamps e laboratórios práticos.

> 🔵 **Link oficial do tutorial (referência):**  
> https://developer.watson-orchestrate.ibm.com/tutorials/tutorial_1_hello_world

---

## 📚 Índice

- [📘 Visão Geral](#-visão-geral)
- [🎯 Objetivos](#-objetivos)
- [🧰 Pré-requisitos](#-pré-requisitos)
- [🚀 Passo 1 — Criar a Skill Hello World](#-passo-1--criar-a-skill-hello-world)
- [🔧 Passo 2 — Implementar a Lógica da Skill](#-passo-2--implementar-a-lógica-da-skill)
- [▶️ Passo 3 — Testar a Skill](#️-passo-3--testar-a-skill)
- [🤖 Passo 4 — Integrar com o Agente](#-passo-4--integrar-com-o-agente)
- [🧪 Exemplos de Uso](#-exemplos-de-uso)
- [🚀 Próximos Passos](#-próximos-passos)
- [📝 Créditos](#-créditos)

---

## 📘 Visão Geral

Este tutorial ensina como criar uma **skill personalizada** no Watson Orchestrate — a famosa **Hello World**.

Ao final, você será capaz de:

✨ Criar uma skill  
✨ Implementar lógica simples  
✨ Testar no ambiente do Orchestrate  
✨ Integrar ao agente e mandar ele executar sua automação  

---

## 🎯 Objetivos

- Aprender a criar uma skill do zero  
- Entender o fluxo básico de automação  
- Enviar e receber dados dentro da skill  
- Executar a skill via agente usando linguagem natural  
- Construir base para skills mais avançadas

---

## 🧰 Pré-requisitos

Antes de começar:

- Conta ativa no **Watson Orchestrate Developer**
- Navegador moderno
- Acesso ao painel de Skills
- Vontade de aprender 😄

---

## 🚀 Passo 1 — Criar a Skill Hello World

1. Acesse o painel do Watson Orchestrate.  
2. Clique em **Skills** → **Create New Skill**.  
3. Preencha as informações iniciais, como nome e descrição.  
4. Escolha entradas e saídas da skill.

Exemplo de configuração inicial:

```jsonc
{
  "skill": "hello_world",
  "description": "Minha primeira skill de teste",
  "inputs": [],
  "outputs": ["message"]
}
```

> 💡 **Dica:** Use descrições claras — elas ajudam o agente a entender quando usar sua skill.

---

## 🔧 Passo 2 — Implementar a Lógica da Skill

Agora, vamos adicionar o comportamento da skill.  
A lógica do “Hello World” é simples:

```python
def hello_world():
    return "Hello World! Sua automação está funcionando!"
```

Esta função será executada sempre que o agente chamar a skill.

---

## ▶️ Passo 3 — Testar a Skill

Abra o painel de testes e siga estes passos:

1. Clique em **Test**  
2. Execute a skill  
3. Veja o resultado no painel lateral  
4. Ajuste o código, se necessário  

Retorno esperado:

```json
{
  "message": "Hello World! Sua automação está funcionando!"
}
```

> 💡 **Se o retorno aparecer corretamente, sua skill está funcionando!**

---

## 🤖 Passo 4 — Integrar com o Agente

Agora que sua skill está criada e testada, vamos executá-la pelo agente:

1. Clique em **Deploy**  
2. Abra a interface do agente  
3. Envie comandos em linguagem natural

Exemplos:

```
Execute a skill Hello World.
```

```
Rodar minha skill Hello World.
```

O agente interpretará sua intenção e executará sua skill automaticamente.

---

## 🧪 Exemplos de Uso

Experimente os seguintes comandos no agente:

```
Execute a skill Hello World agora.
```

```
Qual é a mensagem da minha skill Hello World?
```

```
Rode minha automação Hello World.
```

---

## 🚀 Próximos Passos

Agora que você já domina o básico, continue sua jornada:

👉 Crie skills com parâmetros  
👉 Integre com APIs REST externas  
👉 Crie fluxos inteligentes  
👉 Automatize tarefas reais  
👉 Siga para o tutorial avançado de Workflows  

---

## 📝 Créditos

Este README segue a estrutura e conceitos do tutorial oficial:  
https://developer.watson-orchestrate.ibm.com/tutorials/tutorial_1_hello_world  

Conteúdo reescrito em formato educacional para uso em treinamentos e GitHub.
