# 🎙️ IANA — Assistente de Voz com IA

> Um assistente de voz simples, rápido e direto ao ponto.
> Sem enrolação, sem firula — só pergunta e resposta.

---

## 👨‍💻 Autor

**Leonardo S Melo**

> Engenheiro de Machine Learning que resolveu brincar de criar uma “Alexa caseira” … e acabou criando algo bem sólido.

---

## 🧠 Sobre o Projeto

O **IANA** é um assistente de voz baseado em navegador que:

* 🎤 escuta sua voz (Speech-to-Text)
* 🤖 envia a pergunta para um LLM (via backend seguro)
* 🔊 responde com voz sintetizada (Text-to-Speech)

Tudo isso rodando com:

* Frontend puro (HTML + JS)
* Backend Node.js
* Integração com LLM (Groq / Llama) <--- **Vai precisar de um cadastro no site do Groq e criar um API (grátis porém limitado/Otimo lilmite para laboratorios para varios projetos)**

---

## ⚙️ Arquitetura

```text
🎤 Microfone (Browser)
   ↓
SpeechRecognition API
   ↓
Frontend (JavaScript)
   ↓
Backend (Node.js / Express)
   ↓
LLM (Groq API)
   ↓
Resposta
   ↓
SpeechSynthesis API 🔊
```

---

## 🚀 Tecnologias utilizadas

### Frontend

* Web Speech API (STT + TTS)
* JavaScript puro
* HTML5

### Backend

* Node.js
* Express
* node-fetch
* CORS

### IA

LLM: Llama 3 (via Groq) **<--- Versão **lLama-3.3-70b-versatile** limitada treinada até ano 2023**

---

## 🔥 Features

* ✅ Assistente por voz em tempo real
* ✅ Respostas curtas e diretas
* ✅ Voz feminina (quando disponível no sistema)
* ✅ Auto-restart do reconhecimento (não trava)
* ✅ Backend seguro (API key protegida)
* ✅ Código enxuto e organizado

---

## 🧩 Problemas resolvidos (os famosos bugs “invisíveis”)

* ❌ Microfone parando sozinho
* ❌ Voz sendo cortada no meio
* ❌ Loop infinito de respostas
* ❌ Conflito entre escutar e falar
* ❌ Exposição de API key no frontend

Se você já tentou fazer isso antes… sabe o inferno que é 😄

---

## 🛠️ Como rodar o projeto

### 📁 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/iana-assistente.git
cd iana-assistente
```

---

### ⚙️ 2. Backend

```bash
cd assistente-backend
npm install
node server.js
```

Servidor rodando em:

```
http://localhost:3000
```

---

### 🌐 3. Frontend

```bash
cd assistente-frontend
python -m http.server 8000
```

Abra no navegador:

```
http://localhost:8000/assistente.html
```

---

## 🔐 Segurança

A API key **não fica no frontend**.

```text
Frontend → Backend → API
```

Se você colocar chave no JS… alguém vai pegar. Simples assim.

---

## 🎤 Como usar

1. Clique em **🎤 Iniciar**
2. Fale sua pergunta
3. Espere a resposta
4. Repita

---

## ⚠️ Limitações

* Depende do navegador (Chrome funciona melhor)
* Web Speech API não é 100% estável
* Voz feminina depende do sistema operacional

---

## 💡 Insights técnicos

### 🧠 1. O problema nunca foi IA

O maior desafio aqui não foi o modelo, mas sim:

```text
Concorrência entre:
- entrada de áudio (mic)
- saída de áudio (TTS)
```

---

### 🔄 2. Controle de estado é tudo

Sem isso:

```text
💥 caos total
```

Com isso:

```text
✨ assistente funcional
```

---

### ⚡ 3. Latência importa

* menos tokens = respostas mais rápidas
* menos chamadas = mais fluidez

---

## 🚀 Próximos passos

* 🧠 memória de conversa
* 🎯 wake word (“IANA”)
* 🌐 deploy online
* 🎨 interface moderna
* ⚙️ automações reais

---

## 🤝 Contribuição

Pull requests são bem-vindos.
Mas se quebrar o microfone… você conserta 😄

---

## 📄 Licença

MIT

---

## 🧠 Nota final

Esse projeto parece simples…

até você tentar fazer funcionar sem travar 😄

---

> “Software não quebra por falta de IA.
> Quebra por falta de controle de estado.”
> — provavelmente você depois desse projeto

