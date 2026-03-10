# 🔍 Bot de Discord CheckBan Free Fire
<p align="center">
  <img src="https://files.catbox.moe/egna6n.gif" width="100%">
</p>
![Status](https://img.shields.io/badge/status-ativo-brightgreen)

Um bot de Discord para verificar se uma conta de Free Fire está banida, utilizando o ID do usuário. Também inclui um servidor de status baseado em Flask.

- [Funcionalidades](#-funcionalidades)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Uso](#uso)
- [Como criar um Bot no Discord](#como-criar-um-bot-no-discord)
- [Como convidar o Bot](#-convidar-o-bot-para-seu-servidor)
- [Comandos do Bot](#-comandos-bot)
- [Tutorial em Vídeo](#-tutorial-em-vídeo-configuração-do-bot-checkban)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Licença](#licença)
- [Autor](#autor)

## 🚀 Funcionalidades

* Verifica se uma conta de Free Fire está banida usando o comando `!ID <user_id>`.
* Retorna o status do banimento e a duração (se disponível) em uma mensagem incorporada (embed) no Discord.
* Servidor web Flask em `http://localhost:10000` para indicar o status do bot.
* Credenciais seguras utilizando arquivo `.env`.

## Requisitos

* Python 3.8+
* Um token de bot do Discord
* Um arquivo `.env` contendo:
    ```ini
    TOKEN=seu_token_do_bot
    ```

## Instalação

1.  Clone este repositório:
    ```sh
    git clone [https://github.com/paulafredo/check-ban-and-info-discord](https://github.com/paulafredo/check-ban-and-info-discord)
    cd seu-repositorio
    ```
2.  Crie e ative um ambiente virtual:
    ```sh
    python -m venv .venv
    source .venv/bin/activate  # No Windows use: .venv\Scripts\activate
    ```
3.  Instale as dependências:
    ```sh
    pip install -r requirements.txt
    ```
4.  Crie um arquivo `.env` no diretório raiz e adicione suas credenciais:
    ```ini
    TOKEN=seu_token_do_bot
    ```
5.  Execute o bot:
    ```sh
    python main.py
    ```

## Uso

* Use `!ID <user_id>` em um servidor de Discord onde o bot esteja presente.
* O bot buscará informações de banimento da [api-check-ban-freefire](https://github.com/paulafredo/api-check-ban-freefire) e responderá com uma mensagem incorporada.
* O status do bot pode ser verificado através do servidor Flask rodando em `http://localhost:10000`.

## 🛠️ Como criar um Bot no Discord

1.  Vá para o [Portal de Desenvolvedores do Discord](https://discord.com/developers/applications).
2.  Clique em **"New Application"** (Nova Aplicação) e dê um nome ao seu bot.
3.  Na barra lateral esquerda, vá para a seção **"Bot"** e clique em **"Add Bot"** (Adicionar Bot), então confirme em **"Yes, do it!"**.
4.  Sob a seção **Token**, clique em **"Reset Token"** ou **"Copy"** para obter seu `TOKEN`.
5.  Vá em **"General Information"** (Informações Gerais) e copie o `APPLICATION_ID`.
6.  Cole ambos os valores no seu arquivo `.env`:
    ```ini
    APPLICATION_ID=seu_id_da_aplicacao
    TOKEN=seu_token_do_bot
    ```

## 🔗 Convidar o Bot para um servidor de Discord

1.  Vá em **OAuth2 > URL Generator** no Portal de Desenvolvedores.
2.  Em **Scopes** (Escopos), marque:
    * `bot`
    * `applications.commands`
3.  Em **Bot Permissions** (Permissões do Bot), marque pelo menos:
    * `Send Messages` (Enviar Mensagens)
    * `Embed Links` (Inserir Links)
4.  Copie a URL gerada e abra-a no seu navegador para convidar o bot para o seu servidor.

## 📚 Comandos do Bot

### `!ID <user_id>`
Verifica se uma conta de Free Fire está **banida** ou **não**.

* 📥 **Entrada:** um ID de usuário (UID).
* 📤 **Saída:** uma mensagem incorporada com o status da conta (banida ou não).
* ✅ **Exemplo:** `!ID 12345678`

### `!lang <language_code>`
Altera o **idioma de exibição** do bot para o usuário atual.

* 🌐 **Idiomas disponíveis:**
    * `en` – Inglês (padrão)
    * `fr` – Francês
* ✅ **Exemplos:**
    * `!lang en`
    * `!lang fr`

> ℹ️ Por padrão, o idioma é definido como **Inglês (`en`)** se nenhum outro idioma for selecionado.

## 🎥 Tutorial em Vídeo: Configuração do Bot CheckBan

Assista a este tutorial passo a passo para aprender como instalar e rodar o bot:

📺 [Assistir no YouTube]()

### 🤖 Convide o Bot para o seu Servidor

Clique no link abaixo para convidar o bot CheckBan para o seu servidor de Discord:

👉 [**Adicionar CheckBan ao seu Servidor**](https://discord.com/oauth2/authorize?client_id=1332414680928485457&permissions=274877975552&scope=bot+applications.commands)

## Tecnologias Utilizadas

* Python
* Discord.py
* Flask
* dotenv

## Licença

Este projeto está licenciado sob a Licença MIT. Sinta-se à vontade para usar e modificar.

## Autor

[ꅐꋊ꒯ꋪ 么](https://github.com/wndrgg)
