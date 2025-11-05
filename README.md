#  Projeto UNIP Face & Speech

Um assistente de voz com **rosto animado** e **inteligência de fala**, feito em Python.  
O projeto combina **reconhecimento de voz**, **síntese de fala** e **animações gráficas**, criando um robô que **ouve, fala e expressa emoções**.

---

##  Estrutura do Projeto

###  `unipface.py`
O **rosto do assistente**.

- Mostra um rosto animado (olhos, boca, expressões).
- Escuta o microfone esperando a palavra de ativação **“Unip”**.
- Quando ouve “Unip”, entende comandos simples como:
  - “pare”
  - “siga”
  - “quem é você”
  - “olá”
- Responde **falando com voz sintetizada** (Edge-TTS ou Pyttsx3).
- Muda as **expressões faciais** conforme o que está acontecendo (falando, bravo, neutro, etc.).

💡 **Em resumo:**  
> Um rosto digital que ouve, entende e responde com expressão facial.

---

###  `whisper_speech.py`
O **cérebro do assistente**.

- Espera a palavra de ativação **“Start”**.
- Usa **Whisper** (modelo da OpenAI) para transformar a fala do usuário em texto.
- Passa o texto para um modelo de **Pergunta e Resposta (Q&A)** offline.
- Encontra a melhor resposta e **fala com voz sintética** (Pyttsx3).
- Funciona até **6 perguntas** por sessão.

 **Em resumo:**  
> Um assistente de voz simples que entende perguntas e responde falando.

---

##  Requisitos

Antes de rodar, instale as dependências básicas:

```bash
pip install pygame pyttsx3 speechrecognition edge-tts transformers torch torchvision torchaudio
