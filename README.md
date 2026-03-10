# 🔍 Bot de Discord CheckBan Free Fire

<p align="center">

![Status](https://img.shields.io/badge/status-ativo-brightgreen)
![Python](https://img.shields.io/badge/python-3.8+-blue)
![License](https://img.shields.io/badge/license-MIT-green)

</p>

Um bot de Discord para verificar se uma conta de Free Fire está banida utilizando o **UID do jogador**.
O bot consulta uma API externa e retorna o status diretamente no Discord usando **mensagens embed**.

<p align="center">
<img src="https://files.catbox.moe/egna6n.gif" width="750">
</p>

---

* [Funcionalidades](#-funcionalidades)
* [Requisitos](#requisitos)
* [Instalação](#instalação)
* [Uso](#uso)
* [Como criar um Bot no Discord](#-como-criar-um-bot-no-discord)
* [Como convidar o Bot](#-convidar-o-bot-para-seu-servidor)
* [Comandos do Bot](#-comandos-do-bot)
* [Tutorial em Vídeo](#-tutorial-em-vídeo-configuração-do-bot-checkban)
* [Tecnologias Utilizadas](#tecnologias-utilizadas)
* [Licença](#licença)
* [Autor](#autor)

---

## 🚀 Funcionalidades

* Verifica se uma conta de Free Fire está banida usando o comando `!ID <user_id>`.
* Retorna o status do banimento e a duração (se disponível) em uma **mensagem incorporada (embed)** no Discord.
* Servidor web Flask em `http://localhost:10000` para indicar o **status do bot**.
* Credenciais seguras utilizando arquivo `.env`.

---

## Requisitos

* Python 3.8+
* Um token de bot do Discord
* Um arquivo `.env` contendo:

```
TOKEN=seu_token_do_bot
```

---

## Instalação

1. Clone este repositório:

```
git clone https://github.com/wndrgg/checkban-discord-bot
cd checkban-discord-bot
```

2. Crie e ative um ambiente virtual:

```
python -m venv .venv
```

Windows

```
.venv\Scripts\activate
```

Linux / Mac

```
source .venv/bin/activate
```

3. Instale as dependências:

```
pip install -r requirements.txt
```

4. Crie um arquivo `.env` no diretório raiz e adicione suas credenciais:

```
TOKEN=seu_token_do_bot
```

5. Execute o bot:

```
python main.py
```

---

## Uso

Use o comando abaixo em um servidor de Discord onde o bot esteja presente.

```
!ID <user_id>
```

Exemplo:

```
!ID 12345678
```

O bot buscará informações de banimento da API:

https://github.com/paulafredo/api-check-ban-freefire

O status do bot também pode ser verificado através do servidor Flask:

```
http://localhost:10000
```

---

## 🛠️ Como criar um Bot no Discord

1. Vá para o Portal de Desenvolvedores do Discord

https://discord.com/developers/applications

2. Clique em **New Application**.

3. Na barra lateral esquerda vá em **Bot**.

4. Clique em **Add Bot**.

5. Copie o **TOKEN**.

6. Cole no arquivo `.env`:

```
TOKEN=seu_token_do_bot
```

---

## 🔗 Convidar o Bot para um servidor de Discord

1. Vá em **OAuth2 → URL Generator**.

2. Em **Scopes**, marque:

```
bot
applications.commands
```

3. Em **Bot Permissions**, marque pelo menos:

```
Send Messages
Embed Links
```

4. Copie a URL gerada e abra no navegador para convidar o bot.

---

## 📚 Comandos do Bot

### `!ID <user_id>`

Verifica se uma conta de Free Fire está **banida** ou **não**.

📥 Entrada: UID do jogador
📤 Saída: mensagem embed com o status da conta

Exemplo:

```
!ID 12345678
```

---

### `!lang <language_code>`

Altera o idioma de exibição do bot.

Idiomas disponíveis:

```
en – Inglês (padrão)
fr – Francês
```

Exemplos:

```
!lang en
!lang fr
```

---

## 🎥 Tutorial em Vídeo: Configuração do Bot CheckBan

Assista ao tutorial completo no YouTube.

📺 [Assistir no YouTube]()

---

## 🤖 Convide o Bot para o seu Servidor

👉 https://discord.com/oauth2/authorize?client_id=1332414680928485457&permissions=274877975552&scope=bot+applications.commands

---

## Tecnologias Utilizadas

* Python
* Discord.py
* Flask
* dotenv

---

## Licença

Este projeto está licenciado sob a **Licença MIT**.

---

## Autor

[ꅐꋊ꒯ꋪ 么](https://github.com/wndrgg)
