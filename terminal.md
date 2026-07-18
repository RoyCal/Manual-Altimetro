# Instalação do Programa de Recuperação de Dados

Esta seção descreve os passos necessários para instalar e configurar o aplicativo de terminal responsável pela comunicação com o altímetro.

## Pré-requisitos

Antes de prosseguir, certifique-se de que todos os requisitos descritos na página **[Requisitos](requisitos.md)** foram atendidos.

## 1. Obter o aplicativo

O código-fonte do aplicativo de terminal está disponível no seguinte repositório do GitHub:

**https://github.com/RoyCal/Altimetro-TCC**

Caso o Git esteja instalado em seu computador, clone o repositório executando o comando abaixo:

```bash
git clone https://github.com/RoyCal/Altimetro-TCC.git
```

Como alternativa, é possível fazer o download do código-fonte diretamente pelo GitHub utilizando a opção **Code → Download ZIP** e, em seguida, extrair o conteúdo em uma pasta de sua preferência.

> **Observação:** também está disponível nesse repositório o firmware do altímetro, no arquivo entitulado **firmware.ASM**.

## 2. Instalar as dependências do Python

Abra um terminal na pasta do aplicativo e execute o comando abaixo para instalar todas as dependências necessárias:

```bash
pip install -r requirements.txt
```

Aguarde até que a instalação seja concluída sem erros.

## 3. Configurar o banco de dados

Na pasta raiz do projeto, crie manualmente um arquivo chamado `db_config.py`.

Em seguida, insira o seguinte conteúdo, substituindo os valores conforme a configuração do seu banco de dados:

```python
HOST = "localhost"
USER = "root"
PASSWORD = "senha_do_mysql"
DATABASE = "nome_do_banco_de_dados"
```

> **Observação:** o banco de dados não precisa existir previamente no servidor MySQL. Caso ele ainda não exista, o aplicativo realizará sua criação automaticamente na primeira execução.

## 4. Instalar o driver USB (se necessário)

Caso o computador não reconheça o módulo USB-TTL utilizado pelo altímetro, instale o driver **PL2303**.

O instalador já está incluído no repositório com o nome:

```text
PL2303_Prolific_DriverInstaller_v1.5.0.exe
```

No gerenciador de dispositivos, localize o módulo não reconhecido na aba **Portas (COM e LPT)** e o desinstale removendo seu driver atual. Após isso, execute o instalador e siga as instruções exibidas na tela. Após a instalação, recomenda-se desconectar e reconectar o módulo USB-TTL ao computador.

## Conclusão

Após concluir as etapas acima, o Programa de Recuperação de Dados estará devidamente instalado e configurado, estando pronto para ser executado conforme as instruções de utilização.

---

← [Voltar ao menu principal](/README.md)
